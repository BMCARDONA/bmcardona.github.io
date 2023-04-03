---
layout: page
title: Reading List
permalink: /reading-list/
---

{% raw %}
## Reading List

Here are some books I've read recently, sorted by publication date:

{% bibliography --query @*[type=book] --sort-by=issued:date --reverse --csl=chicago-fullnote-bibliography.csl %}
{% endraw %}