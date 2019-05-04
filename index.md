---
title: Polytopes
layout: home
#thumbnail: /examples/p5js/images/fireworks-2.png
#tagline: Ooh! Aah!
#sort-key: 100
meta-title: P5.js Polytopes Example
meta-description: Use P5.js to explore some basic polytopes (3D objects with "flat" faces)!
#meta-image: /examples/p5js/images/fireworks-1.png
tags: [example, p5.js]

---

<div id="sketch-holder"></div>

Use touchscreen to rotate object, and count the number of:

faces?
edges?
vertices?

---

<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.6.1/p5.min.js"></script>
<script>
function setup() {
createCanvas(710, 400, WEBGL);
}

let s = 128;

function draw() {
background(250);
let radius = width * 1.5;

//drag to move the world.
orbitControl(5,5);

normalMaterial();
rotateX(-s/13);
rotateY(s);


push();
box(s, s, s);
pop();

}

</script>

---
