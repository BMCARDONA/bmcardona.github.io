---
layout: page
permalink: /archives/
title: Archives
description: An archive of all my writings.
nav: true
nav_order: 3
---

### Writings by Category
<ul>
{% assign sorted_categories = site.categories | sort %}
{% for category in sorted_categories %}
  <li><a href="{{ site.baseurl }}/blog/category/{{ category | first | slugify }}/">{{ category | first }}</a></li>
{% endfor %}
</ul>


### Writings by Year

- [2023](https://bmcardona.github.io/blog/2023/)

{% assign posts_by_year = site.posts | group_by_exp:"post", "post.date | date: '%Y'" %}
{% assign sorted_posts_by_year = posts_by_year | sort: 'name' | reverse %}

{% for year in sorted_posts_by_year %}
  <li><a href="#">{{ year.name }}</a></li>
  <ul>
    {% for post in year.items %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}



