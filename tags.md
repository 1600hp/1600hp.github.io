---
layout: page
title: Tags
permalink: /tags/
excerpt: Want to find something?  Let me make that less unlikely.
---
{% for tag in site.tags %}
  {% for page in site.tags.tag %}
    {% assign count = forloop.length %}
  {% endfor %}
  {{ count }}
  {{ tag | first }}
{% endfor %}
