---
layout: default
title: Cube (Hexahedron)	
---

<div id="sketch-holder"></div>

Use mouse or trackpad to rotate object, and count the number of:   

- faces? 
- vertices?
- edges?    

In the language of math, a cube is also known as a __hexahedron__.  
This name offers a clue to the number of faces it has.

---

<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.8.0/p5.min.js"></script>
<script>

function setup() {
	createCanvas(648, 400, WEBGL);
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
	box(s, s, s);
	pop();
}



</script>

<div>
	<!-- a href="" class="previous">&laquo; previous</a -->
	<a href="/tetra/" class="next">Next &raquo;</a>
</div>

