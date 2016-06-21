---
layout: page
title: Everything
permalink: /everything/
excerpt: All the content in one place.  I went to a lot of trouble to sort it, but whatever, I guess you can ignore that.
---

  <ul class="post-list">
    {% for post in site.posts %}
	  {% for category in post.categories %}
        <li>
          <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
  
          <h2>
            <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
          </h2>
        </li>
      {% endfor %}
    {% endfor %}
  </ul>