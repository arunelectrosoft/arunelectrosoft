---
layout: post
title:  "WebPage using Jekyll & GithubPages"
date:   2018-09-22
categories: Blogging
---

Jekyll Installation is simple.

Refer to
<b> <a href="https://jekyllrb.com/docs/" > JEKYLL DOCUMENTATION </a> </b>


1. Install Ruby
2. $sudo gem install jekyll bundle
3. $sudo jekyll new website_name
4. $sudo jekyll serve

5. Working with Blog for GitHub Pages
   $ bundle update
   $ sudo bundle exec jekyll clean && sudo bundle exec jekyll server --baseurl ""

Above command will host the static site in local host http://127.0.0.1:4000

what is Jekyll ?
It is a static website ( website using plain html) generator.

What are the default folders ?

1. config.yml (yaml format - improved version of json)
2. _layouts folder can be created
3. _posts - contain the writing content or pages of the website.
4. _data can be used for overall variables used in site.
5. _sass is for the sass based css generator
6. assets and images are folders used to have extra content related resources


What is Bootstrap ?
Why so much craze on this new topic called bootstrap, to understand this
we need to know what is responsive pages.



What is Responsive Pages ?
The site will change its content size based on the device screen size.

What i understood from BootStrap,
BootStrap is a collection of opensource java scripts,
which will generate css, along with html for creating responsive pages.

Responsive pages helps to view content on mobile/desktop seamlessly.

<a href="http://jekyllbootstrap.com/"> Jekyll Bootstrap </a>

A blogger with same idea as mine, posted how to use the
bootstrap with jekyll on github pages.

<a href="http://veithen.github.io/2015/03/26/jekyll-bootstrap.html" >
Using Bootstrap with CSS. </a>

First Success with :
https://stackoverflow.com/questions/28733425/adding-bootstrap-to-jekyll

But Better to integrate Jekyll with Bootstrap 4, or latest version as per link
below.
https://experimentingwithcode.com/creating-a-jekyll-blog-with-bootstrap-4-and-sass-part-1/
above link needs some understanding of jekyll and how it works, so it may not work in first shot. !!

Common Erros and Resolution:
1. https://stackoverflow.com/questions/45205310/bootstrap-css-not-working-on-github-pages
2. https://stackoverflow.com/questions/48778736/github-pages-failing-to-properly-link-to-my-assets-and-relative-urls
3. https://stackoverflow.com/questions/16316311/github-pages-and-relative-paths
4.  One Guys has done extensive liquid markup coding
in link https://github.com/plusjade/jekyll-bootstrap/tree/master/_includes/JB

