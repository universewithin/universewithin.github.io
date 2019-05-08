---
layout: default
title: Octahedron
permalink: /octa/
---

<div id="sketch-holder"></div>

Use mouse or trackpad to rotate object, and count the number of:   

- faces? 
- vertices? 
- edges?   

In the language of math, this object is called an __octahedron__.  
The name offers a clue to the number of faces it has.

---

<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.8.0/p5.min.js"></script>
<script>

function setup() {
	createCanvas(648, 400, WEBGL); 
}

let s = 96;

let c = 255;
let a = 0.81; // alpha level

function draw() {
	background(222);
	angleMode(DEGREES);

	//drag to move the world.
	orbitControl(7,7);

	normalMaterial();
	rotateX(-60);
	rotateY(72);

	stroke('#222222');
	strokeWeight(4);
	//lights();

	// ( 0, s, 0) 
	// (s,0,0) (-s,0,0) (0,0,s) (0,0,-s)
	// ( 0,-s, 0)

	push();

	fill(color('rgba(c,0,170,a)'));
	beginShape();
	vertex( 0, s, 0);
	vertex(-s, 0, 0);
	vertex( 0, 0,-s);
	endShape(CLOSE);

    fill(color('rgba(c,0,85,a)'));
	beginShape();
    vertex( 0, s, 0);
    vertex( 0, 0,-s);
    vertex( s, 0, 0);
	endShape(CLOSE);

    fill(color('rgba(c,0,0,a)'));
	beginShape();
    vertex( 0, s, 0);
    vertex( s, 0, 0);
    vertex( 0, 0, s);
	endShape(CLOSE);

    fill(color('rgba(c,85,0,a)'));
	beginShape();
    vertex( 0, s, 0);
    vertex( 0, 0, s);
    vertex(-s, 0, 0);
	endShape(CLOSE);

    //

    fill(color('rgba(0,c,c,a)'));
	beginShape();
    vertex( 0,-s, 0);
    vertex(-s, 0, 0);
    vertex( 0, 0,-s);
	endShape(CLOSE);

    fill(color('rgba(0,170,c,a)'));
	beginShape();
    vertex( 0,-s, 0);
    vertex( 0, 0,-s);
    vertex( s, 0, 0);
	endShape(CLOSE);

    fill(color('rgba(0,85,c,a)'));
	beginShape();
    vertex( 0,-s, 0);
    vertex( s, 0, 0);
    vertex( 0, 0, s);
	endShape(CLOSE);

    fill(color('rgba(0,0,c,a)'));
	beginShape();
    vertex( 0,-s, 0);
    vertex( 0, 0, s);
    vertex(-s, 0, 0);
	endShape(CLOSE);

	pop();

 //    line(0,s,0,s,0,0);
 //    line(0,s,0,-s,0,0);
 //    line(0,s,0,0,0,s);
 //    line(0,s,0,0,0,-s);

 //    line(0,-s,0,s,0,0);
 //    line(0,-s,0,-s,0,0);
 //    line(0,-s,0,0,0,s);
 //    line(0,-s,0,0,0,-s);

 //    line(-s,0,0,0,0,-s);
 //    line(0,0,-s,s,0,0);
 //    line(s,0,0,0,0,s);
 //    line(0,0,s,-s,0,0);
}

</script>

<div>
	<a href="/tetra/" class="previous">&laquo; previous</a>
	<!-- a href="" class="next">Next &raquo;</a -->
</div>

