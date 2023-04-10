---
layout: page
permalink: /blog/archives/
title: Archives
description: An archive of all my writings.
nav: true
nav_order: 3
---

### Writings by Category
<!-- <ul>
{% for category in site.categories %}
  <li><a href="{{ site.baseurl }}/blog/category/{{ category | first | slugify }}/">{{ category | first }}</a></li>
{% endfor %}
</ul> -->

<ul>
{% assign sorted_categories = site.categories | sort %}
{% for category in sorted_categories %}
  <li><a href="{{ site.baseurl }}/category/{{ category | first | slugify }}/">{{ category | first }}</a></li>
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

### Writings by Year
- [2023](https://bmcardona.github.io/blog/2023/)



