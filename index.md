---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
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
