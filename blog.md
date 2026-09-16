---
layout: default
title: Blog
---

# Blog

Here you can find my notes and articles about ...

{% for post in site.posts %}
## [{{ post.title }}]({{ post.url | relative_url }})

<small>{{ post.date | date: "%d %B %Y" }}</small>

{% endfor %}

