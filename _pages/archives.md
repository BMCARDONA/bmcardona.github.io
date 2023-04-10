---
layout: page
permalink: /blog/archives/
title: Archives
description: An archive of my writings.
nav: true
nav_order: 3
---

## By Category
<ul>
{% for category in site.categories %}
  <li><a href="{{ site.baseurl }}/blog/category/{{ category | first | slugify }}/">{{ category | first }}</a></li>
{% endfor %}
</ul>

<!-- <ul>
{% for category in site.categories %}
  <li><a href="{{ site.baseurl }}/blog/category/{{ category | first | slugify }}/">{{ category | first }}</a></li>
{% endfor %}
</ul> -->

<!-- <ul>
{% for category in site.categories %}
  <li><a href="/blog/category/{{ category | first | slugify }}/">{{ category | first }}</a></li>
{% endfor %}
</ul> -->

## By Year
- [2023](https://bmcardona.github.io/blog/2023/)



