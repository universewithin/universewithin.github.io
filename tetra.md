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

---

<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.8.0/p5.min.js"></script>
<script>

function setup() {
	//createCanvas(710, 400, WEBGL);
	//createCanvas(600, 600, WEBGL);
	createCanvas(648, 400, WEBGL);
	//cvs.style('display', 'block');    
}

let s = 64;
//let rad60 = 60*PI/180;
let rad60 = radians(60);

function draw() {
	background(250);

	//drag to move the world.
	orbitControl(6,6);

	normalMaterial();
	rotateX(-s/13);
	rotateY(-s/13);
	rotateZ(-s/13);

	//fill(255);
    stroke('#222222');
	strokeWeight(2);

	//(s,s,s) (s,-s,-s) (-s,-s,s) (-s,s,-s)

	push();

	beginShape();
	vertex(s,s,s);
	vertex(s,-s,-s);
	vertex(-s,-s,s);
	endShape(CLOSE);

	beginShape();
	vertex(s,s,s);
	vertex(s,-s,-s);
	vertex(-s,s,-s);
	endShape(CLOSE);

	beginShape();
	vertex(s,s,s);
	vertex(-s,-s,s);
	vertex(-s,s,-s);
	endShape(CLOSE);

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

<center>
	<a href="/cube/" class="previous">&laquo; previous</a>
	<a href="/octa/" class="next">Next &raquo;</a>
</center>

