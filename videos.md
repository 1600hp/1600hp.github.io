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
              <div style="background:#000;height:200px;width=$content-width">
                <div style="float:left;width:50%;overflow:hidden">
                  <a href="{{ post.url | prepend: site.baseurl }}">
                    <img src="/videos/thumbnails/{{ post.title }}.jpg" style="height:200px">
                  </a>
                </div>
                <div style="float:right;height:100%;width:50%">
                  <div style="padding:20px">
                    <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
                    <h2>
                      <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
                    </h2>
                    <p style="font-size:12px">{{ post.excerpt }}</p>
                  </div>
                </div>
                <br style="clear:both;"/>
                <hr>
                </div>
          </li>
        {% endif %}
      {% endfor %}
    {% endfor %}
  </ul>