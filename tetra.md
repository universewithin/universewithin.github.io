---
layout: default
title: Tetrahedron
permalink: /tetra/
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
	//createCanvas(710, 400, WEBGL);
	createCanvas(600, 600, WEBGL);
	//cvs.style('display', 'block');    
}

let s = 128;
//let rad60 = 60*PI/180;
let rad60 = radians(60);

function draw() {
	background(250);

	//drag to move the world.
	orbitControl(6,6);

	normalMaterial();
	//rotateX(-s/13);
	//rotateY(s);

	//fill(255);
    stroke('#222222');
	strokeWeight(4);
    line(0,0,0,s,0,0);
    line(s,0,0,s,s,0);
    line(s,s,0,0,s,0);
    line(0,s,0,0,0,0);
    line(0,0,0,s/2,s/2,s);
    line(s,0,0,s/2,s/2,s);
    line(s,s,0,s/2,s/2,s);
    line(0,s,0,s/2,s/2,s);

 //    push();

//    drawtetrahedron();
 //    pop();

}

function drawtetrahedron() {
   beginShape(TRIANGLES);
   vertex(-s/2,0,0);
   vertex(0,sin(rad60)*(-s),0);
   vertex(s/2,0,0);    
  endShape();
  beginShape(TRIANGLES);
   vertex(-s/2,0,0);
   vertex(0,sin(rad60)*(-s)*.5,sin(rad60)*(s));
   vertex(s/2,0,0);    
  endShape();
   beginShape(TRIANGLES);
   vertex(-s/2,0,0);
   vertex(0,sin(rad60)*(-s)*.5,sin(rad60)*(s));
   vertex(0,sin(rad60)*(-s),0);    
  endShape();
    beginShape(TRIANGLES);
     vertex(0,sin(rad60)*(-s),0);
     vertex(0,sin(rad60)*(-s)*.5,sin(rad60)*(s));
       vertex(s/2,0,0);
  endShape();
  
}


// function draw() {
// 	background(250);

// 	//drag to move the world.
// 	orbitControl(6,6);

// 	push();
	
// 	fill(255);

//   	beginShape();
//   	vertex(s, s, s);
//   	vertex(-s, -s, s);
//   	vertex(-s, s, -s);
//   	vertex(s, -s, -s);
//   	endShape(CLOSE);

// 	pop();

// 	normalMaterial();
// 	rotateX(-s/13);
// 	rotateY(s);
// }

</script>

<center>
	<a href="/index/" class="previous">&laquo; previous</a>
	<a href="/octa/" class="next">Next &raquo;</a>
</center>

