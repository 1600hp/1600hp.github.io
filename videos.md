---
layout: page
title: Videos
permalink: /videos/
excerpt: In which you can watch me make a fool of myself instead of just imagining it.
---

  <ul class="post-list">
    {% for post in site.posts %}
	  {% for category in post.categories %}
	    {% if category == "videos" %}
          <li>
		      <div style="height:200">
			    <div style="float:left"><a href="{{ post.url | prepend: site.baseurl }}"><img src="/videos/thumbnails/{{ post.title }}.jpg" style="width:400px;height:200px"></a></div>
				<div style="padding:20px;background:#000;height:100%">
			      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
			      <h2>
			        <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
			      </h2>
				</div>
	  	      </div>
          </li>
		{% endif %}
      {% endfor %}
    {% endfor %}
  </ul>