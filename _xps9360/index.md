---
layout: post 
title: XPS 9360 
permalink: /xps9360/index.html
---

These are my notes about my Dell XPS 9360. It runs [Manjaro](http://www.manjaro.org) Linux. It runs quite well, but I've made some improvements and adjustments along the way.

{% assign collection = site.xps9360 | sort: 'sequence' %}

| Note | Description |
|---:|---|
{% for note in collection -%}
  {% if note.title != 'XPS 9360' -%}
  | [{{ note.subject }}]({{ note.url }}) | {{ note.summary }} |
  {% endif %}
{%- endfor -%}
