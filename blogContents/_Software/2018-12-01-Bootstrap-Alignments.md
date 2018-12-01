---
title: Bootstrap Alignments
layout: post
categories: Blogging
---

Alginment are very much required for a web developer to tell how the elements are arranged in a webpage !

<br>

lets have a detailed look at it !

<br>
<br>
END Alignment !
<div class="container bg-warning" style="margin-top:30px">
    <section class="row bg-warning align-items-end" style="height:200px">
    <div class="col bg-secondary"> column1 </div>
    <div class="col bg-success"> column2 </div>
    <div class="col bg-info"> column3 </div>
    </section>
</div>


<br>
<br>
 Alignment start !
<div class="container bg-warning" style="margin-top:30px">
    <section class="row bg-warning align-items-start" style="height:200px">
    <div class="col bg-secondary"> column1 </div>
    <div class="col bg-success"> column2 </div>
    <div class="col bg-info"> column3 </div>
    </section>
</div>


<br>
<br>
Alignment Center !
<div class="container bg-warning" style="margin-top:30px">
    <section class="row bg-warning align-items-center" style="height:200px">
    <div class="col bg-secondary"> column1 </div>
    <div class="col bg-success"> column2 </div>
    <div class="col bg-info"> column3 </div>
    </section>
</div>

<br>
<br>
Alignment Center with self align for item !
<div class="container bg-warning" style="margin-top:30px">
    <section class="row bg-warning align-items-center" style="height:200px">
    <div class="col bg-secondary align-self-start"> column1 </div>
    <div class="col bg-success align-self-center"> column2 </div>
    <div class="col bg-info align-self-end"> column3 </div>
    </section>
</div>


<br>
<br>
Alignment Center with Justify start !
<div class="container bg-warning justify-content-start" style="margin-top:30px">
    <section class="row" style="height:200px">
    <div class="col-4 bg-secondary "> column1 </div>
    <div class="col-4 bg-success "> column2 </div>
    </section>
</div>



<br>
<br>
Alignment Center with Justify Center !
<div class="container bg-warning justify-content-center" style="margin-top:30px">
    <section class="row" style="height:200px">
    <div class="col-4 bg-secondary "> column1 </div>
    <div class="col-4 bg-success "> column2 </div>
    </section>
</div>


<br>
<br>
Alignment Center with Justify Between !
<div class="container bg-warning justify-content-between" style="margin-top:30px">
    <section class="row" style="height:200px">
    <div class="col-4 bg-secondary "> column1 </div>
    <div class="col-4 bg-success "> column2 </div>
    </section>
</div>


<br>
<br>
Working with Offsets !
<div class="container bg-warning " style="margin-top:30px">
    <section class="row" style="height:200px">
    <div class="col-4 bg-secondary offset-md-1"> column1 </div>
    <div class="col-4 bg-success offset-md-3"> column2 </div>
    </section>
</div>


<br>
<br>
Margin Alignements 
<div class="container bg-warning " style="margin-top:30px">
    <section class="row" style="height:200px">
    <div class="col-4 bg-secondary margin-auto"> column1 </div>
    <div class="col-4 bg-success "> column2 </div>
    </section>
</div>

Need to learn about padding display and margines.

margin - m
it has following variants

l -left
r- right
t-top
b-bottom
x- left or right
y- top or bottom - y -axis
blank all way around. 

example mt-1, means margin top -1

here 0, 1, 2, 3, 4, 5 has relativd margins respect to font size. 

0 - 0
1 - 0.25
2 - 0.5
3 - 1
4 - 1.5
5 - 3
$spacer variable will note this. 


<br>
<br>
Margin example - my own 
<div class="container bg-warning ">
    <section class="row" style="height:200px">
    <div class="col bg-danger text-light text-justify m-5"> This is going to be big text with the option to justify the content in the column box. m5 </div>
    <div class="col bg-success text-light text-justify mt-5"> Another text with some option to have margins with just - mt-5 </div>
    </section>
</div>


<br>
<br>
Padding example - my own 
<div class="container bg-warning ">
    <section class="row" style="height:200px">
    <div class="col bg-danger text-light text-justify p-5"> This is going to be big text with the option to justify the content in the column box. padding p5 </div>
    <div class="col bg-success text-light text-justify pt-0"> Another text with some option to have padding with just - pt-0 </div>
    </section>
</div>


<br>
<br>
Span Elements 
<div class="container bg-warning ">
    <section class="column">
    <span class="px-2 bg-primary"> Span inline element 1 </span>
    <span class="px-3 bg-info"> Span inline element 2 </span>
    <div class="d-inline bg-success"> Span inline element  3</div>
    </section>
</div>



<br>
<br>
Flexible Boxes :
Aside  HTML tags are used for side content apart from main article eg:logins, comment form etc. 
<aside class="container">
    <section class="d-flex flex-row-reverse">
        <div class="p-1 text-light bg-primary"> one </div>
        <div class="p-2 text-light bg-secondary"> two </div>
        <div class="p-3 text-light bg-info"> three </div>
    </section>
</aside>

<br>
<br>
Flexible Boxes : row : Justify Start 
<aside class="container">
    <section class="d-flex flex-row flex-justify-start">
        <div class="p-4 text-light bg-primary"> one </div>
        <div class="p-4 text-light bg-secondary"> two </div>
        <div class="p-4 text-light bg-info"> three </div>
    </section>
</aside>


<br>
<br>
Flexible Boxes : row : Justify Center 
<aside class="container">
    <section class="d-flex flex-row flex-justify-center">
        <div class="p-4 text-light bg-primary"> one </div>
        <div class="p-4 text-light bg-secondary"> two </div>
        <div class="p-4 text-light bg-info"> three </div>
    </section>
</aside>


<br>
<br>
Flexible Boxes : column : Justify Center 
<aside class="container">
    <section class="d-flex flex-column align-items-center">
        <div class="p-4 text-light bg-primary"> one </div>
        <div class="p-4 text-light bg-secondary"> two </div>
        <div class="p-4 text-light bg-info"> three </div>
    </section>
</aside>


<br>
<br>
Flexible Boxes : column : Justify Baseline based on typography like h1,h2 
<aside class="container">
    <section class="d-flex flex-column align-items-baseline">
        <div class="p-4 h1 text-light bg-primary"> one </div>
        <div class="p-4 h2 text-light bg-secondary"> two </div>
        <div class="p-4 h3 text-light bg-info"> three </div>
    </section>
</aside>


<br>
<br>
Flexible Boxes : column : Justify Baseline based on typography 
also for certain devices can be given in the order. 
<aside class="container">
    <section class="d-flex flex-row align-items-baseline">
        <div class="p-4 align-self-md-start text-light bg-primary"> one </div>
        <div class="p-4 align-self-center text-light bg-secondary"> two </div>
        <div class="p-4 align-self-end text-light bg-info"> three </div>
        <div class="p-4 align-self-baseline text-light bg-danger"> four </div>
        <div class="p-4 align-self-strectc text-light bg-success"> five </div>
    </section>
</aside>