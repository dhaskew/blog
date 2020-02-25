---
layout: post 
title: Cheatsheets 
permalink: /cheatsheets/index.html
---

A collection of various lists about technology with useful commands and links.

{% assign collection = site.cheatsheets | sort: 'sequence' %}

| Note | Description |
|---:|---|
{% for note in collection -%}
  {% if note.title != 'Cheatsheets' -%}
  | [{{ note.subject }}]({{ note.url }}) | {{ note.summary }} |
  {% endif %}
{%- endfor -%}
