---
layout: page
permalink: /archives/
title: Archives
description: An archive of all my writings.
nav: true
nav_order: 2
---

### Writings by Category
<ul>
{% assign sorted_categories = site.categories | sort %}
{% for category in sorted_categories %}
  <li><a href="{{ site.baseurl }}/blog/category/{{ category | first | slugify }}/">{{ category | first }}</a></li>
{% endfor %}
</ul>


### Writings by Year
<ul>
{% assign posts_by_year = site.posts | group_by_exp:"post", "post.date | date: '%Y'" %}
{% assign sorted_posts_by_year = posts_by_year | sort: 'name' | reverse %}
{% for year in sorted_posts_by_year %}
  <li><a href="{{ site.baseurl }}/blog/{{ year.name }}/">{{ year.name }}</a></li>
{% endfor %}
</ul>