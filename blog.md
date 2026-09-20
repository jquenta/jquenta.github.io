---
layout: default
title: Blog
---

# My Blog

Each post here is written in the style of a short personal note on some topic I found interesting or useful during my research. Don't hesitate to point out any mistakes or typos!

## Posts

{% for post in site.posts %}
### [{{ post.title }}]({{ post.url | relative_url }})
<small>{{ post.date | date: "%d %B %Y" }}</small>

{% endfor %}

