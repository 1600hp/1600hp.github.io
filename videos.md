---
layout: page
title: Videos
permalink: /videos/
---

  <ul class="post-list">
    {% for post in site.posts %}
      {% for category in post.categories %}
        {% if category == "videos" %}
          <li>
              <div style="background:#000;height:200px">
                <div style="float:left;width:50%">
                  <a href="{{ post.url | prepend: site.baseurl }}">
                    <img src="/videos/thumbnails/{{ post.title }}.jpg" style="height:200px">
                  </a>
                </div>
                <div style="float:right;height:100%;width:50%">
                  <div style="padding:20px">
                    <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
                    <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
                      <p style="font-size:16px"><b>{{ post.title }}</b></p>
                    </a>
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