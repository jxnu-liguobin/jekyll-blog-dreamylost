---
layout: page
title: 梦境亦是美，醒来亦是空
---
## 近期

{% for post in site.posts limit:5 %}

- [{{ post.title }}]({{ post.url }}), <small>{{ post.date | date_to_string }}</small>
{% if post.description %}
    - <small>{{ post.description }}</small>
{% endif %}

{% endfor %}

- [更多…](/archive.html)

{% for tag in site.index.showtag %}

## {{ tag }}

{% for post in site.tags[tag] %}

- [{{ post.title }}]({{ post.url }})
{% if post.description %}
    - <small>{{ post.description }}</small>
{% endif %}

{% endfor %}

{% endfor %}
