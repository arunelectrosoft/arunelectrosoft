---
layout: post
title:  "Web Animations"
date:   2019-09-18
categories: Blogging
---

Web Animations as spice to web page.

Refer to <b> <a href="https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API/Tutorial/Getting_started_with_WebGL" > Getting Started with WebGL </a> </b>

WebGL is a good option to render the webpage with animations. 

Let us start our exploration based on above 
getting started page !!
<br>
<!---Defining the drwaing canvas -->
<canvas id="sampleCanvas1" width="400" height="200"></canvas>
<script>
//
// start here
//
function main() {
    const canvas = document.querySelector("#sampleCanvas1");
    // Initialize the GL context
    const gl = canvas.getContext("webgl");
    // Only continue if WebGL is available and working
    if (gl === null) {
      alert("Unable to initialize WebGL. Your browser or machine may not support it.");
      return;
    }
    // Set clear color to black, fully opaque
    gl.clearColor(0.0, 0.0, 0.0, 1.0);
    // Clear the color buffer with specified clear color
    gl.clear(gl.COLOR_BUFFER_BIT);
  }
  window.onload = main;
</script>
<br>
Note:
Detailed WebGL and other graphics for webpage is given in below link, 
<b> <a href="https://docs.google.com/document/d/1-lAvR9GXaNJiqUIpm3N2XuGUWv_JrkpGizDN0bNq7wY/edit#" >WebGL Next Design Doc </a> </b>
