---
layout: page
title: videos
permalink: /videos/
---

  <ul class="post-list">
    {% for post in site.posts %}
	  {% if 'video' in post.categories %}
        <li>
          <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
  
          <h2>
            <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
          </h2>
        </li>
      {% endif %}
    {% endfor %}
  </ul>