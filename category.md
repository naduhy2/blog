---
layout: page
title: Category
permalink: /category
---
<h2>Categories</h2>

{% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  <p>
    {% for post in category[1] %}
      <!-- <li><a href="{{ post.url }}">{{ post.title }}</a></li> -->
    {% endfor %}
  </p>
{% endfor %}
