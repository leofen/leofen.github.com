---
layout: page
title: 主页
tagline: Supporting tagline
---
{% include JB/setup %}

##文章列表

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
    <p> {{post.content | split:'<!--more-->' |first}} </p>
    <a href="{{ post.url }}">Read more...</a><br><br>
  {% endfor %}
</ul>



