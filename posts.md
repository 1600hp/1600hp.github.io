---
layout: page
title: Posts
permalink: /posts/
---

  <ul class="post-list">
    <p> Basically all the boring parts that are mostly words.  Beats me why anyone would read these. </p>
	<!--more-->
    {% for post in site.posts %}
	  {% for category in post.categories %}
	    {% if category == "updates" %}
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