---
title: Bootstrap Grid System
layout: post
categories: Blogging
---

Understanding Bootstrap grid system !

It is following the newspaper 12 column layout style.


<section class="container">
    <section class="row">
        <div class="col"> Equal </div>
        <div class="col"> Equal </div>
        <div class="col"> Equal </div>
        <div class="col"> Equal </div>
        <div class="col"> Equal </div>
        <div class="col"> Equal </div>
        <div class="col"> Equal </div>
        <div class="col"> Equal </div>
        <div class="col"> Equal </div>
        <div class="col"> Equal </div>
        <div class="col"> Equal </div>
        <div class="col"> Equal </div>
    </section>
</section>


<br>
<br>
Choosing the Column in the layout by specifying the coloum
<section class="container">
    <section class="row">
        <div class="col"> Auto </div>
        <div class="col-8"> Auto </div>
        <div class="col-2"> Auto </div>
    </section>
</section>

<br>
<br>

For Mobile screen automatic size change and stack into row wise, one below one. 
Re-size the browser to undersand this behaviour. 
<section class="container">
    <section class="row">
        <div class="col-sm"> Mobile </div>
        <div class="col-sm"> Mobile </div>
        <div class="col-sm"> Mobile </div>
    </section>
</section>

<br>
<br>

Ordering the column :
<section class="container">
    <section class="row">
        <div class="col-sm order-3"> Third in display </div>
        <div class="col-sm order-2"> First </div>
        <div class="col-sm order-1"> Second - dont go by name </div>
    </section>
</section>

<br>
<br>

Nesting the columns using nested section tag !!
Important concept - to layout the blog or webpage. 
Hint: Check where the fist div tag is getting closed !

<section class="container">
    <section class="row">
        <div class="col bg-warning"> First
        <section class="row">
            <div class="col bg-secondary"> Second </div>
            <div class="col bg-success"> Third </div>
        </section>
        </div>
    </section>
</section>


Adoptive Sizing for the container !!
Based on device width !!

<section class="container">
    <section class="row">
    <div class="col-sm-6 col-md-10 col-lg-4 bg-success">
     This is a Sample text ! This will align based on the device width, to make this as a really long sentence ! I am typing simply without any new line !
    </div>
    </section>
</section>