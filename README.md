# grid-path-finder
NPM module for path-finding on a grid.


An NPM module that finds the shortest path between two nodes on a grid.
Accepts two positions and a grid. The positions are objects with x and y properties. The grid is a 2d array with values of 0 (vacant node) or 1 (wall node).
Created by [Ruaidhri MacKenzie](https://github.com/fankadore).


```sh
npm install grid-path-finder
```

## Example

```js
const pathFinder = require('grid-path-finder');

const startPos = {x: 0, y: 0};
const endPos = {x: 5, y: 0};
const grid = [
  [0, 0, 0, 1, 0, 1, 0, 0, 0, 0, 0, 0],
  [1, 1, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0],
  [0, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0],
  [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
  [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
  [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
  [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
  [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
  [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
  [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
  [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
  [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
];
const path = pathFinder(startPos, endPos, grid);
```

## API

```js
const pathFinder = require('grid-path-finder');
```

Function | return | Params | Description
--- | --- | --- | ---
`pathFinder` | array `path` | (object `startPosition`, <br>[object `endPosition`, <br>[array `grid`]) | Accepts a 2d array and two position objects with x and y properties. Returns an array of position objects or null if no route is found
