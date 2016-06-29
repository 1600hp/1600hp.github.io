---
layout: page
title: Tags
permalink: /tags/
excerpt: Want to find something?  Let me make that less unlikely.
---

{% for tag in site.tags %}
  <hr>
    {% for page in site.tags.tag %}
      {% assign count = forloop.length %}
    {% endfor %}
  <div>
    <a class="page-link" href="{{ tag | prepend: site.baseurl }}">{{ tag }} ({{ count }})</a>
  </div>
{% endfor %}