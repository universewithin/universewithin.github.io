---
layout: default
title: Fun fact...	
permalink: /funfact/
---

<div id="sketch-holder"></div>

Use mouse or trackpad to rotate object... 

---

<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.8.0/p5.min.js"></script>
<script>

function setup() {
	createCanvas(648, 400, WEBGL); 
}

let s = 64;
let v = s*3/2;
let w = v;

function draw() {
	background(222);
	let radius = width * 1.5;

	//drag to move the world.
	orbitControl(6,6);

	normalMaterial();
	rotateX(-s/13);
	rotateY(s);

	push();
	box(s, s, s);

	stroke('#222222');
	strokeWeight(3);

	// octahedron wireframe
    line( 0, v, 0, v, 0, 0);
    line( 0, v, 0,-v, 0, 0);
    line( 0, v, 0, 0, 0, v);
    line( 0, v, 0, 0, 0,-v);

    line( 0,-v, 0, v, 0, 0);
    line( 0,-v, 0,-v, 0, 0);
    line( 0,-v, 0, 0, 0, v);
    line( 0,-v, 0, 0, 0,-v);

    line(-v, 0, 0, 0, 0,-v);
    line( 0, 0,-v, v, 0, 0);
    line( v, 0, 0, 0, 0, v);
    line( 0, 0, v,-v, 0, 0);

    stroke('#333333');
	strokeWeight(4);

    // large cube wireframe
    line( w, w, w, w,-w, w);
    line( w,-w, w,-w,-w, w);
    line(-w,-w, w,-w, w, w);
    line(-w, w, w, w, w, w);

    line( w, w, w, w, w,-w);
    line( w,-w, w, w,-w,-w);
    line(-w,-w, w,-w,-w,-w);
    line(-w, w, w,-w, w,-w);

    line( w, w,-w, w,-w,-w);
    line( w,-w,-w,-w,-w,-w);
    line(-w,-w,-w,-w, w,-w);
    line(-w, w,-w, w, w,-w);


	pop();
}

</script>


