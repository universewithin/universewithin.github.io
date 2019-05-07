---
layout: default
title: Tetrahedron
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

	//drag to move the world.
	orbitControl(6,6);

	push();
	
	fill(255);

  	beginShape();
  	vertex(s, s, s);
  	vertex(-s, -s, s);
  	vertex(-s, s, -s);
  	vertex(s, -s, -s);
  	endShape(CLOSE);

	pop();

	normalMaterial();
	rotateX(-s/13);
	rotateY(s);
}

</script>

<center>
	<a href="universewithin.github.io/index.md" class="previous">&laquo; previous</a>
	<a href="universewithin.github.io/octa.md" class="next">Next &raquo;</a>
</center>

