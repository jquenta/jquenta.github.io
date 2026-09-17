---
layout: default
title: Blog
---

# About this blog

Each post here serves as a personal note where I discuss a certain topic I found interesting or useful during my research work. Don't hesitate to point out any mistakes or typos!

## Posts

{% for post in site.posts %}
## [{{ post.title }}]({{ post.url | relative_url }})

<small>{{ post.date | date: "%d %B %Y" }}</small>

{% endfor %}

