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
        
          <div style="background:#000;height:200px;width=$contentwidth">
            {% if category == "videos" %}
              <div style="float:left;width:50%">
                <a href="{{ post.url | prepend: site.baseurl }}">
                  <img src="/videos/thumbnails/{{ post.title }}.jpg" style="height:200px">
                </a>
              </div>
              <div style="float:right;height:100%;width:50%">
                <div style="padding:20px">
                  <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }} (video)</span>
                  <h2>
                    <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
                  </h2>
                  <p style="font-size:12px">{{ post.excerpt }}</p>
                </div>
              </div>
              <br style="clear:both;"/>
              <hr>
            {% else %}
              <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
              <h2>
                <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
              </h2>
              <p style="font-size:12px">{{ post.excerpt }}</p>
            {% endif %}
          </div>
        </li>
      {% endfor %}
    {% endfor %}
  </ul>