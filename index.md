---
layout: default
title: Polytopes
---

<div id="sketch-holder"></div>

Use touchscreen to rotate object, and count the number of:   

- faces? 
- edges?  
- vertices ?  

---

<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.8.0/p5.min.js"></script>
<script>

// // lock scroll position, but retain settings for later
// var scrollPosition = [
//   self.pageXOffset || document.documentElement.scrollLeft || document.body.scrollLeft,
//   self.pageYOffset || document.documentElement.scrollTop  || document.body.scrollTop
// ];
// var html = jQuery('html'); // it would make more sense to apply this to body, but IE7 won't have that
// html.data('scroll-position', scrollPosition);
// html.data('previous-overflow', html.css('overflow'));
// html.css('overflow', 'hidden');
// window.scrollTo(scrollPosition[0], scrollPosition[1]);


// document.body.ontouchmove = (e) => { e.preventDefault; return false; }; 

function setup() {
	createCanvas(710, 400, WEBGL);
	//cvs.style('display', 'block');    
}

let s = 128;

function draw() {
	background(250);
	let radius = width * 1.5;

	//drag to move the world.
	orbitControl(8,8);

	normalMaterial();
	rotateX(-s/13);
	rotateY(s);

	push();
	box(s, s, s);
	pop();
}

$('#recover').trigger({
    type: 'mousedown',
    which: 3
});

// .trigger({
//     type: 'mousedown',
//     which: 1
// });

</script>
