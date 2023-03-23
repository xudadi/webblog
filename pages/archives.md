---
layout: post
title: 归档
permalink: /archives.html
---
{% for post in site.posts %}
    {% assign year = post.date | date: '%Y' %}
    {% assign nyear = post.next.date | date: '%Y' %}
    {% if year != nyear %}
## {{ post.date | date: '%Y' }}
{:.archive-title}
    {% endif %}
* {{ post.date | date: '%m-%d' }} &raquo; [{{ post.title }}]({{ post.url }} "{{ post.title }}"){:.archive-item-link}
{% endfor %}
