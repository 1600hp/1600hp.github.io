---
layout: page
title: Videos
permalink: /videos/
---

  <ul class="post-list">
    <p> In which you can watch me make a fool of myself instead of just imagining it. </p>
	<!--more-->
    {% for post in site.posts %}
	  {% for category in post.categories %}
	    {% if category == "videos" %}
          <li>
            <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
  
            <h2>
              <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
            </h2>
          </li>
		{% endif %}
      {% endfor %}
    {% endfor %}
  </ul>