---
layout: page
title: Archives
permalink: /archives/
---
{% for post in site.posts %}
{% assign year=post.date | date: "%Y" %}
{% assign nyear=post.next.date | date: "%Y" %}
{% if year != nyear %}
<span style="font-size:30px">
<span class="fa-layers fa-fw"><i class="fa fa-calendar"></i></span>
{{year}}</span>
{% endif %}
- {{post.date | date_to_string}}  [{{post.title}}]({{post.url | absolute_url}})
{% endfor %}
