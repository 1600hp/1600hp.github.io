---
layout: page
title: Tags
permalink: /tags/
excerpt: Want to find something?  Let me make that less unlikely.
---
{% for tag in site.tags %}

  <a class="page-link" href="{{ site.baseurl }}{{ tag | first }}">{{ tag | first }}</a>
{% endfor %}
