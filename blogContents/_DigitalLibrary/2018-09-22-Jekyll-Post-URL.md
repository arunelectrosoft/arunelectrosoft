---
title: Jekyll-PostURL-permalink
layout: post
categories: LearningSeries
permalink: /simpleSet/
---

Jekyll Permalink keyword in front yaml section decides the URL of the posts.

If no Permalink is being set, then
/year/month/day/title.html is used as default Permalink


Permalink are the way to organise the output URL style.
/:categories/:year/:month/:day/:title:output_ext

<b> Note: Note the URL of this post. </b>


The Following keywords can be used in permalink url construction

1. Hour
2. Minutes
3. second
4. title
5. categories

Following are built-in Jekyll permalink formats,

date :- /:categories/:year/:month/:day/:title:output_ext

pretty :- /:categories/:year/:month/:day/:title/

ordinal :- /:categories/:year/:y_day/:title:output_ext

none :- /:categories/:title:output_ext
