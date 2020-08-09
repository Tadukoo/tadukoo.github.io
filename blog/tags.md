---
layout: default
title: Tags
---
# Tags

{% assign tags = site.tags | sort %}

#### Table of Contents
{% for tag in tags %}* [{{tag[0]}}](#{{tag[0] | slugify}}) - {{tag[1].size}} posts
{% endfor %}

{% for tag in tags %}## {{tag[0]}}
{% for post in tag[1] 
  %}* [{{post.title}}]({{post.url}}) by {{post.author}} - {{post.date | date_to_string}}
{% endfor %}
{% endfor %}