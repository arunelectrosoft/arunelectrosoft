---
title: Jekyll Collections Exploration
layout: post
categories: LearningSeries
---


Lets Explore the concept of Collections:

Collections are like categories
- used to group by directory structure.
- defined in _config.yml file
- the folder name follows the _"nameOfCollection" in _config.yml file.
- under the folder the different posts can present.

example:

in _config.yml

{%- highlight markdown -%}
collections:
  postByTopics:
    output: true
{%- endhighlight -%}


Later it can be accessed using liquid Tags.

{% for post in site.postByTopics %}
  <div class="post">
     <h2> <a href="{{post.url}}"> {{post.title}} </a> </h2>
   </div>
{% endfor %}


The collections and layout concepts are needed for better blogging.
