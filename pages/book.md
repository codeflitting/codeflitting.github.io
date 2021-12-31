---
layout: page
title: 读书
permalink: /book/
nav_order: 2
---

<link rel="stylesheet" href="{{ site.baseurl }}/assets/css/custom.css">

<div class="post">
  <ul id="container" class="post-list">
  {% for category in site.categories %}
  {% if category[0] == "book" %}
  
    <li class="item">
      {% for post in category[1] %}
      <span class="post-tag">
      {{ post.date | date_to_string: "ordinal", "US" }}</span>
      <div class="post-body">
        <a href="{{ post.url }}">{{ post.title }}</a>
        <p>
          {{ post.excerpt }}
        </p>
      </div>
      <a class="post-readmore" href="{{ post.url }}">Read more</a>
      {% endfor %}
    </li>
  
  {% endif %}
  {% endfor %}
  </ul>
</div>
