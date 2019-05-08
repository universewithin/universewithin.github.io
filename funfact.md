---
layout: default
title: Fun fact...	
permalink: /funfact/
---
<div id="sketch-holder"></div>
A cube fits perfectly within a larger octahedron, which fits perfectly within an even larger cube, and so on and so on!  
  
In the model below, the smaller cube's __eight__ _vertices_ match up to the centers of the octahedron's __eight__ _faces_.  
And _that_ octahedron's __six__ _vertices_ match up to the centers of the larger cube's __six__ _faces_!  
  
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

    stroke('#444444');
	strokeWeight(3);

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


