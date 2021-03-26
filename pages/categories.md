---
layout: page
permalink: /categories/
title: Categories
---





<div id="archives">

{% for post in site.categories.misc %}
 <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
  
</div>



