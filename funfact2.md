---
layout: default
title: Fun fact 2...
permalink: /funfact__2/
---

<div id="sketch-holder"></div>

---

<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.8.0/p5.min.js"></script>
<script>

function setup() {
	createCanvas(648, 400, WEBGL);  
}

let s = 64;
let v = s*2*sqrt(2);
let w = s*4*sqrt(2);
let c = 255;

function draw() {
	background(222);
	angleMode(DEGREES);

	//drag to move the world.
	orbitControl(5,5);

	normalMaterial();
	rotateX(-60);
	rotateY(72);

    stroke('#222222');
	strokeWeight(2);

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

	noFill();

	stroke('#222222');
	strokeWeight(3);

	// medium tetrahedron
	line( v, v, v, v,-v,-v);
	line( v, v, v,-v,-v, v);
	line( v, v, v,-v, v,-v);
	line( v,-v,-v,-v,-v, v);
	line( v,-v,-v,-v, v,-v);
	line(-v,-v, v,-v, v,-v);

	stroke('#444444');
	strokeWeight(3);

	// large tetrahedron
	line( w, w, w, w,-w,-w);
	line( w, w, w,-w,-w, w);
	line( w, w, w,-w, w,-w);
	line( w,-w,-w,-w,-w, w);
	line( w,-w,-w,-w, w,-w);
	line(-w,-w, w,-w, w,-w);

	pop();
}

</script>


