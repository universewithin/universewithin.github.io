---
layout: default
title: Tetrahedron
permalink: /tetra/
---

<div id="sketch-holder"></div>

Use mouse or trackpad to rotate object, and count the number of:   

- faces? 
- vertices?  
- edges?  

In the language of math, this object is called a __tetrahedron__.  
The name offers a clue to the number of faces it has.

---

<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.8.0/p5.min.js"></script>
<script>

function setup() {
	createCanvas(648, 400, WEBGL);  
}

let s = 64;
//let r = s/2;
let c = 255;

function draw() {
	background(153);
	angleMode(DEGREES);

	//drag to move the world.
	orbitControl(5,5);

	normalMaterial();
	rotateX(-60);
	rotateY(72);

    stroke('#222222');
	strokeWeight(2);
	//lights();

	//(s,s,s) (s,-s,-s) (-s,-s,s) (-s,s,-s)

	push();

	fill(color(c,0,0));
	beginShape();
	vertex(s,s,s);
	vertex(s,-s,-s);
	vertex(-s,-s,s);
	endShape(CLOSE);

	fill(color(c,c,0));
	beginShape();
	vertex(s,s,s);
	vertex(s,-s,-s);
	vertex(-s,s,-s);
	endShape(CLOSE);

	fill(color(0,c,0));
	beginShape();
	vertex(s,s,s);
	vertex(-s,-s,s);
	vertex(-s,s,-s);
	endShape(CLOSE);

	fill(color(0,0,c));
	beginShape();
	vertex(s,-s,-s);
	vertex(-s,-s,s);
	vertex(-s,s,-s);
	endShape(CLOSE);

	pop();

	// line(s,s,s,s,-s,-s);
	// line(s,s,s,-s,-s,s);
	// line(s,s,s,-s,s,-s);

	// line(s,-s,-s,-s,-s,s);
	// line(s,-s,-s,-s,s,-s);
	// line(-s,-s,s,-s,s,-s);
}

</script>

<div>
	<a href="/cube/" class="previous">&laquo; previous</a>
	<a href="/octa/" class="next">Next &raquo;</a>
</div>

