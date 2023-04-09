---
layout: page
permalink: /archive/
title: Archive
description: An archive of my writings.
nav: true
nav_order: 4
---

<div class="post">
  <ul class="post-list">
    {% for post in paginator.posts %}

    {% if post.external_source == blank %}
      {% assign read_time = post.content | number_of_words | divided_by: 180 | plus: 1 %}
    {% else %}
      {% assign read_time = post.feed_content | strip_html | number_of_words | divided_by: 180 | plus: 1 %}
    {% endif %}
    {% assign year = post.date | date: "%Y" %}
    {% assign tags = post.tags | join: "" %}
    {% assign categories = post.categories | join: "" %}

    <li>
      <p class="post-tags">
          {% if categories != "" %}
          &nbsp; &middot; &nbsp;
            {% for category in post.categories %}
            <a href="{{ category | slugify | prepend: '/blog/category/' | prepend: site.baseurl}}">
              <i class="fas fa-tag fa-sm"></i> {{ category }}</a> &nbsp;
              {% endfor %}
          {% endif %}
      </p>
    </li>

    {% endfor %}
  </ul>
  {% include pagination.html %}

</div>