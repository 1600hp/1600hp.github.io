---
layout: page
title: Tags
permalink: /tags/
excerpt: Want to find something?  Let me make that less unlikely.
---

{% for tag in site.tags %}
  <p>{{ tag }}</p>
  <hr>
{% endfor %}