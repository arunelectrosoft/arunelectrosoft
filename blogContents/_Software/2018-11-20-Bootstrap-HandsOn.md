---
title: Bootstrap Learnings
layout: post
categories: Blogging
imageused1 : farm-image-1
output: false
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
 <img src= "{{ site.baseurl }}{{ site.data.images[page.imageused1].url }}" class="img-fluid" alt="farm image icon alternative text"  style="height:auto; width:auto; display:block; max-width:800px; max-height:800px; ">

<a href="https://getbootstrap.com/docs/4.1/content/images/"> Bootstrap Image tutorials </a>


Media Breakpoints in Bootstrap:

<style>
@media(min-width:576px) { body {background:lightblue;}  }
@media(min-width:768px) { body {background:cyan;}  }
@media(min-width:992px) { body {background:lightgreen;}  }
@media(min-width:1200px) { body {background:yellow;}  }
@media(max-width:500px) { body {background:gray;}  }


</style>


<br>
<br>

For Bootstrap Navigation Bars !

Lets learn about Nav bar from Bootstrap and how it is helpful to design navigatable webpages !

Try to re-use the navbars from Bootstrap Navbar sample code itself. its better. 


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

<br>
<br>
Bootstrap also has h1 to h5 level heading classes. 
<div class="container"> 
    <h1 class="h1 text-capitalize text-italic">
    Need to write in proper fonts and using proper typography to make readers read!
    </h1>
</div>

<br>
<br>
Heading with a small sideline 
<div class="container"> 
    <h1 class="h1 text-capitalize text-italic">
    This is Typed Text
    <small class="text-muted"> Without much thoughts! </small>
    </h1>
</div>


<br>
<br>
Display Headline Tag ! 
<div class="container"> 
    <h1 class="display-1">
    BIG Display tag
    </h1>
</div>


<br>
<br>
Text rowours - with option to override !
<br>
"!important" tag in code is necessary to override the default bootstrap rowor!

<div class="container"> 
    <h3 class=" text-primary">  Text - primary  </h3>
    <h3 class=" text-secondary">  Text - secondary  </h3>
    <h3 class=" text-danger">  Text - danger  </h3>
    <h3 class=" text-success">  Text - success  </h3>
    <h3 class=" text-info">  Text - info  </h3>
    <h3 class=" text-warning">  Text - warning  </h3>
    <h3 class=" text-dark">  Text - dark  </h3>
    <h3 class=" text-body">  Text - body  </h3>
    <h3 class=" text-black">  Text - black  </h3>
    <h3 class=" text-light">  Text - light  </h3>
</div>
<style>
    .text-light {
        rowor: #ff00ff !important;
    }
</style>

<br>
<br>
 Learning About paragraphs in bootstrap !
<div class="container"> 
    <h1> Learning about paragraph tags !</h1>
    <p class="lead"> This is my lead paragaraph with good spacing between lines. </p>
    <blockquote class="blockquote text-center text-muted p-3"> Quoted text with gray light fonts !
    <footer class="blockquote-footer">
     from author 
     <cite title="Life of Gypsy Guys"> Nomad like Gypsy Guy ! </cite>
    </footer>
     </blockquote>
</div>

<br>
<br>
Some Tags in Bootstrap !
<div class="container"> 
   <ul>
    <li>  <mark> Farmer </mark></li>
    <li> <del> Agriculture </del> </li>
    <li> <s> Land </s></li>
    <li> <ins> What else to do ??</ins></li>
    <li> <u> Have to think this !!</u></li>
    <li> <small> think about world level </small></li>
    <li>  <strong> who is the reason ? </strong></li>
    <li> <em>  We all are, lets run away from city and use our time , not fall into the trap of 9-5 job and sit back ! a farmer is a person living, working as per natural clock, not like 9-5. and be idle and wait for society to change. </em></li>
   </ul>
</div>


<br>
<br>
Bootsrap Lists
<div class="container"> 
    <ul class="list-group"> 
    <li class="list-group-item list-group-item-primary"> Primary item <span class="small aligh-right"> inline text </span></li>
    <li class="list-group-item list-group-item-secondary"> Secondary item </li>
    <li class="list-group-item list-group-item-success"> Success item </li>
    <li class="list-group-item list-group-item-info"> Info item </li>
    <li class="list-group-item list-group-item-warning"> Warning item </li>
    <li class="list-group-item list-group-item-danger"> Danger item </li>
    <li class="list-group-item list-group-item-light"> Light item </li>
    <li class="list-group-item list-group-item-dark"> dark item </li>
    </ul>
</div>

<br>
<br> 

list items may contain other span elements. 
dl - refers to description list. 

<dl> 
    <dt> Memory</dt>
    <dd> Boon or curse - no idea</dd>
    <dt> Good thoughts </dt>
    <dd> Good for oneself - gives good sleep most times !</dd>
</dl>

<br>
<br> 
With Bootstrap !

<dl class="row"> 
    <dt class="col-sm-3"> Memory</dt>
    <dd class="col-sm-9"> Boon or curse - no idea</dd>
    <dt class="col-sm-3"> Good thoughts </dt>
    <dd class="col-sm-9"> Good for oneself - gives good sleep most times !</dd>
</dl>


<br>
<br> 
Bootstarp has cool, javascript based list, with information for the selected tag. 

<dl class="row"> 
    <dt class="col-sm-3"> Memory</dt>
    <dd class="col-sm-9"> Boon or curse - no idea</dd>
    <dt class="col-sm-3"> Good thoughts </dt>
    <dd class="col-sm-9"> Good for oneself - gives good sleep most times !</dd>
</dl>


<br>
<br> 
Fixed Top Title and wondering about sticky-top and fixed-top tags !
<h1 class="h2 sticky-top" > Learning Typgropahy </h1>
<br>
<br> 
<br>
<br> 
<br>
some text
<br> 
<br>
<br> 
<br>
<br> 
<br>
<br> 
<br>
some text
<br> 
<br>
<br> 