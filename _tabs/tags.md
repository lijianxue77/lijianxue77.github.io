---
layout: page
title: Tags
permalink: /tags/
---
{% for tag in site.tags %}
<span style="font-size: 30px"><span class="fa-layers fa-fw">
<i class="fas fa-tag"></i>
<span class="fa-layers-counter">{{ tag[1].size }}</span>
</span>
{{ tag[0] }}</span>
{% for post in tag[1] %}
- {{post.date | date_to_string}}  [{{post.title}}]({{post.url | absolute_url}})
{% endfor %}
{% endfor %}
