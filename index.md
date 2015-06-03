---
layout: page
title: Coding Genetic Codes
---
{% include JB/setup %}

<div class="hm">
	<h2 style="color:red;background:#eedfcc;">
    	<a href="http://yangjl.com">HOME</a>
    </h2>

   	<style type="text/css">
	.hm {
    	text-align: center;
    	background: $secondary-color;
    	color: $light-color;
    	padding: 8px 15px;
    	border-radius: 5px;
    	margin: 1.5 * $spacing-unit 0;

    	a {
        	font-weight: 700;
        	color: #fff;
        	margin-left: 10px;

        	&:hover {
            	border-bottom: 1px dashed #fff;
        	}
    	}
	}
	</style>
</div>


<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
