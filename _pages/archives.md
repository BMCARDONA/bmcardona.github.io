---
layout: page
permalink: /blog/archives/
title: Archives
description: An archive of my writings.
nav: true
nav_order: 3
---

## By Category
- [Books](https://bmcardona.github.io/blog/category/books/)
- [Productivity](https://bmcardona.github.io/blog/category/productivity/)

## By Year
- [2023](https://bmcardona.github.io/blog/2023/)

<!-- <div class="my-class">
    <p>This is some HTML code.</p>
    <ul>
        <li>List item 1</li>
        <li>List item 2</li>
        <li>List item 3</li>
    </ul>
    {% for post in page.posts %}
    <tr>
        <th scope="row">{{ post.date | date: "%b %-d, %Y" }}</th>
        <td>
            <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </td>
    </tr>
    {% endfor %}
</div> -->

<ul>
{% for category in site.categories %}
  <li><a href="/categories/{{ category | first | slugify }}/">{{ category | first }}</a></li>
{% endfor %}
</ul>

<ul>
{% for category in site.categories %}
  <li><a href="{{ site.baseurl }}/category/{{ category | first | slugify }}/">{{ category | first }}</a></li>
{% endfor %}
</ul>

<ul>
{% for category in site.categories %}
  <li><a href="/category/{{ category | first | slugify }}/">{{ category | first }}</a></li>
{% endfor %}
</ul>


