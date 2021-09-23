---
layout: default
title: Features
---

{% assign features = site.features | sort: 'order'%}
{% for feature in features %}

## {{ feature.title }}

{{ feature.content }}

***

{% endfor %}
