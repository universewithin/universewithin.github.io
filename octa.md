---
layout: default
title: Octahedron
permalink: /octa/
---

<div id="sketch-holder"></div>

Use mouse or trackpad to rotate object, and count the number of:   

- faces? 
- edges?  
- vertices?  

---

<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.8.0/p5.min.js"></script>
<script>

function setup() {
	createCanvas(710, 400, WEBGL);
	//cvs.style('display', 'block');    
}

let s = 128;

function draw() {
	background(250);
	let radius = width * 1.5;

	//drag to move the world.
	orbitControl(6,6);

	normalMaterial();
	rotateX(-s/13);
	rotateY(s);

	push();
	//box(s, s, s);
	pop();
}

</script>

<center>
	<a href="/tetra/" class="previous">&laquo; previous</a>
	<!-- a href="" class="next">Next &raquo;</a -->
</center>
