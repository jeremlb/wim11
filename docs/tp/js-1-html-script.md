Créer un fichier `index.html` et `script.js` à partir des contenus suivants

### index.html

```html
<!DOCTYPE html>
<html lang="fr">

<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <style>
    .menu {
      text-align: center;
    }

    .row {
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .cell {
      width: 10px;
      height: 10px;
      font-size: 10px;
      border: 1px solid black;
      display: inline-flex;
      justify-content: center;
      align-items: center;
      font-weight: bold;
    }
  </style>
</head>

<body>
  <menu class="menu">
    <button id="next-gen">Prochaine Génération</button>
    <button id="autoplay">Auto Play</button>
    <br><br>
    Génération numéro: <span id="generation-value"></span> | Taille de la grille: <span id="grid-size-value"></span>
  </menu>

  <div id="container"></div>
  <script src="script.js"></script>
</body>

</html>
```

### script.js
```js
// -----------------------------------------------------------------------------------------------------------------
/**
 * Cette partie du code, vous n'avez pas besoin d'y toucher. Elle permet de gérer la grille et l'affichage des cellules
 */

class GridManager {
  ACTIVE_COLOR = 'black';
  INACTIVE_COLOR = 'grey';

  gridContainerId;
  gridSize;
  grid = [];

  constructor(gridSize, gridContainerId) {
    if (!gridSize || gridSize < 30) {
      throw new Error('The grid size must be at least 30');
    }

    if (!gridContainerId) {
      throw new Error('gridContainerId must be set');
    }

    this.gridSize = gridSize;
    this.gridContainerId = gridContainerId;
    this.createGrid();
  }

  createGrid() {
    const container = document.getElementById(this.gridContainerId);
  
    for (let i = 0; i < this.gridSize; i++) {
      const row = document.createElement('div');
      row.className = 'row';
  
      const gridRow = [];
  
      for (let j = 0; j < this.gridSize; j++) {
        const cell = document.createElement('div');
        cell.className = 'cell';
        cell.style.backgroundColor = this.INACTIVE_COLOR;
        row.appendChild(cell);
  
        gridRow.push(cell);
      }
  
      container.appendChild(row);
      this.grid.push(gridRow);
    }
  }

  destroyGrid() {
    for (let x = 0; x < this.gridSize; x++) {
      for (let y = 0; y < this.gridSize; y++) {
        const node = this.grid[y][x];
        node.parentNode.removeChild(node);
      }
    }

    const container = document.getElementById(this.gridContainerId);
    while (container.firstChild) {
      container.removeChild(container.lastChild);
    }

    this.grid = [];
  }

  setInitialState(initialState) {
    const coords = initialState.split(';').map(coord => coord.split(','));
    coords.forEach((coord) => this.activeCell(+coord[0], +coord[1]));
  }

  isInGridRange(x, y) {
    return x >= 0 && x < this.gridSize && y >= 0 && y < this.gridSize;
  }

  isActiveCell(x, y) {
    return this.isInGridRange(x, y) && this.grid[y][x].style.backgroundColor === this.ACTIVE_COLOR;
  }

  activeCell(x, y) {
    if (!this.isInGridRange(x, y)) {
      return;
    }

    this.grid[y][x].style.backgroundColor = this.ACTIVE_COLOR;
  }
  
  deactiveCell(x, y) {
    if (!this.isInGridRange(x, y)) {
      return;
    }
    
    this.grid[y][x].style.backgroundColor = this.INACTIVE_COLOR;
  }
  
  getNumberActiveNeighbourCells(x, y) {
    const neighbours = [
      [x-1, y-1], [x, y-1], [x+1, y-1],
      [x-1, y],             [x+1, y],
      [x-1, y+1], [x, y+1], [x+1, y+1],
    ];
  
    return neighbours.map(cell => this.isActiveCell(cell[0], cell[1])).filter(cell => cell === true).length; 
  }

  logCurrentGridState() {
    const activeCells = [];
  
    for (let x = 0; x < this.gridSize; x++) {
      for (let y = 0; y < this.gridSize; y++) {
        if (this.isActiveCell(x, y)) {
          activeCells.push(`${x},${y}`);
        }
      }
    }
  
    console.log(activeCells.join(';'));
  }
}
// -----------------------------------------------------------------------------------------------------------------


const INITIAL_STATE = '11,1;12,1;10,2;9,3;9,4;9,5;10,6;11,7;12,7;2,4;1,5;2,5;18,28;17,28;19,27;20,26;20,25;20,24;19,23;18,22;17,22;27,25;28,24;27,24;11,28;12,28;10,27;9,26;9,25;9,24;10,23;11,22;12,22;2,25;1,24;2,24;18,1;17,1;19,2;20,3;20,4;20,5;19,6;18,7;17,7;27,4;28,5;27,5';
const GENERATION_INTERVAL = 1000; // 1 seconde
const DIV_CONTAINER_ID = 'container'; 
const BTN_AUTOPLAY_ID = 'autoplay';
const BTN_NEXT_GEN_ID = 'next-gen';
const GENERATION_VAL_ID = 'generation-value';
const GRID_SIZE_VAL_ID = 'grid-size-value';

function computeNextGeneration(gridManager, generation) {
  // incrémenter la valeur de la génération et l'afficher à côté de 'Génération numéro:'

  const nextGrid = [];

  for (let x = 0; x < gridManager.gridSize; x++) {
    const row = [];
    for (let y = 0; y < gridManager.gridSize; y++) {
      const isActive = gridManager.isActiveCell(x, y);
      const numberActiveNeighbourCells = gridManager.getNumberActiveNeighbourCells(x, y);

      if (!isActive) {
        row.push(numberActiveNeighbourCells === 3 ? true : false);
      } else {
        row.push(numberActiveNeighbourCells === 2 || numberActiveNeighbourCells === 3 ? true : false);
      }
    }

    nextGrid.push(row);
  }

  for (let x = 0; x < nextGrid.length; x++) {
    for (let y = 0; y < nextGrid[x].length; y++) {
      nextGrid[x][y] ? gridManager.activeCell(x,y) : gridManager.deactiveCell(x,y);
    }
  }

  gridManager.logCurrentGridState();
  return generation;
}

// Fonction principale du jeu
function main() {
  let autoplayInterval;
  let gridSize = 60;
  let generation = 0;

  let gridManager = new GridManager(gridSize, DIV_CONTAINER_ID);
  gridManager.setInitialState(INITIAL_STATE);
  
  // Lorsqu'un utilisateur clique sur 'Auto Play'
  document.getElementById(BTN_AUTOPLAY_ID).addEventListener('click', () => {
    if (autoplayInterval) {
      return;
    }
  
    autoplayInterval = setInterval(() => {
      generation = computeNextGeneration(gridManager);
    }, GENERATION_INTERVAL);
  });

  // Lorsqu'un utilisateur clique sur 'Prochaine Génération'
  document.getElementById(BTN_NEXT_GEN_ID).addEventListener('click', () => {
    if (autoplayInterval) {
      clearInterval(autoplayInterval);
      autoplayInterval = null;
    }
  
    computeNextGeneration(gridManager);
  });
}


// Le jeu est démarré ici
main();
```