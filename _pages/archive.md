---
layout: page
permalink: /archive/
title: Archive
description: An archive of my writings.
nav: true
nav_order: 4
---

<div>
    <h2>Categories</h2>
    <ul>
        {% for category in site.categories %}
            <li><a href="/categories/{{ category | slugify }}/">{{ category | capitalize }}</a></li>
        {% endfor %}
    </ul>
</div>