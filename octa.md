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

---

<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.8.0/p5.min.js"></script>
<script>

function setup() {
	//createCanvas(710, 400, WEBGL);
	//createCanvas(600, 600, WEBGL);
	createCanvas(648, 400, WEBGL);
	//cvs.style('display', 'block');    
}

let s = 128;

function draw() {
	background(250);
	let radius = width * 1.5;

	//drag to move the world.
	orbitControl(6,6);

	normalMaterial();
	//rotateX(-s/13);
	//rotateY(s);

	stroke('#222222');
	strokeWeight(4);

    line(0,s,0,s,0,0);
    line(0,s,0,-s,0,0);
    line(0,s,0,0,0,s);
    line(0,s,0,0,0,-s);

	line(0,-s,0,s,0,0);
    line(0,-s,0,-s,0,0);
    line(0,-s,0,0,0,s);
    line(0,-s,0,0,0,-s);

    line(-s,0,0,0,0,-s);
    line(0,0,-s,s,0,0);
    line(s,0,0,0,0,s);
    line(0,0,s,-s,0,0);

    // line(s,0,0,s,s,0);
    // line(s,s,0,0,s,0);
    // line(0,s,0,0,0,0);
    // line(0,0,0,s/2,s/2,s);
    // line(s,0,0,s/2,s/2,s);
    // line(s,s,0,s/2,s/2,s);
    // line(0,s,0,s/2,s/2,s);

}

</script>

<center>
	<a href="/tetra/" class="previous">&laquo; previous</a>
	<!-- a href="" class="next">Next &raquo;</a -->
</center>

