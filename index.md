---
layout: page
title: Coding Genetic Codes
---
{% include JB/setup %}

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

<ul class="nav">
<h3 style="color:red;background:#F8F8F8;text-align:center;>
  
  <li>
  <a href="http://yangjl.com/en/">English</a> | 
  <a href="http://yangjl.com/">Home</a> | 
  <a href="http://yangjl.com/cn/">中文</a> | 
  <a href="http://yangjl.com/about/">About</a> | 
  <a href="http://yangjl.com/vitae/">VITAE</a>
  
  </li>
</h3>
</ul>