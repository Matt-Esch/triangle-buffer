# triangle-buffer [![Build Status][1]][2]

A DOM based 3D triangle renderer

## Example


```js
// Create a viewport with fovy PI/2
// and update body on window resize

var Viewport = require('css-viewport'),
    createBuffer = require('triangle-buffer');


var v = new Viewport(Math.PI/2);

window.onresize = updatePerspective;
updatePerspective();

function updatePerspective() {
    v.update(document.body);
};

// Create a triangle buffer using body and viewport v
triangleBuffer = createBuffer(document.body, v);

// And render some triangles
triangleBuffer.begin();
triangleBuffer.drawTriangle([
    [0,0,0],
    [0,50,50],
    [50,50,0]
]);
triangleBuffer.end();
```

## Installation

`npm install triangle-buffer`

## Contributors

 - Matt-Esch

## MIT Licenced


  [1]: https://secure.travis-ci.org/Matt-Esch/triangle-buffer.png
  [2]: http://travis-ci.org/Matt-Esch/triangle-buffer
