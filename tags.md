---
layout: page
title: Tags
permalink: /tags/
excerpt: Want to find something?  Let me make that less unlikely.
---
{% for tag in site.tags %}
  "{{ tag | first }}"{% unless forloop.last %},{% endunless %}
{% endfor %}
