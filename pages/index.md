---
layout: home
title: 主页
permalink: /
nav_order: 1
---

<link rel="stylesheet" href="{{ site.baseurl }}/assets/css/custom.css">

<ul>
{% for post in site.posts %}
  <li>
    <h3>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </h3>
    {{ post.excerpt }}
  </li>
{% endfor %}
</ul>
