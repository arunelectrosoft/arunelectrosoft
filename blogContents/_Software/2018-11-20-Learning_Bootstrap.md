---
title: Learning Bootstrap Part 1
layout: post
categories: Blogging
imageused1 : farm-image-1
---



<br>
Bootstrap Topic -  Container with Colours
<br>
<div class="container bg-primary">  Primary ! </div>
<div class="container bg-secondary">  Secondary! </div>
<div class="container bg-danger">  Danger ! </div>
<div class="container bg-warning">  Warning ! </div>
<div class="container bg-info">  Information ! </div>
<div class="container bg-dark">  Dark ! </div>
<div class="container bg-white">  White ! </div>

<br>

Working with Images and Container !!

<br>

Image Properties :
Title: {{ site.data.images[page.imageused1].title}}
Url:  {{ site.data.images[page.imageused1].url}}

<br>

Somehow using the imagedata set directly doesnot work. 
following lines dont work !
no idea why !!
Title: {{ site.data.images[farm-image-1].title}}
Url:  {{ site.data.images[farm-image-1].url}}

<br>

Image with Bootstrap Fluid Image class :
 <img src= "{{ site.data.images[page.imageused1].url }}" class="img-fluid" alt="farm image icon alternative text"  style="height:auto; width:auto; display:block; max-width:800px; max-height:800px; ">

<a href="https://getbootstrap.com/docs/4.1/content/images/"> Bootstrap Image tutorials </a>


Media Breakpoints in Bootstrap:

<style>
@media(min-width:576px) { body {background:lightblue;}  }
@media(min-width:768px) { body {background:cyan;}  }
@media(min-width:992px) { body {background:lightgreen;}  }
@media(min-width:1200px) { body {background:yellow;}  }
@media(max-width:500px) { body {background:gray;}  }


</style>