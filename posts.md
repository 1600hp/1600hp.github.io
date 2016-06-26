---
layout: page
title: Posts
permalink: /posts/
excerpt: Basically all the boring parts that are mostly words.  Beats me why anyone would read these.
---

  <ul class="post-list">
    {% for post in site.posts %}
      {% for category in post.categories %}
        {% if category == "updates" %}
          <li>
            <div style="background:#000;height:200px;width=$contentwidth">
              <div style="padding:20px">
                <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
                <h2>
                  <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
                </h2>
                <hr>
                <p style="font-size:12px">{{ post.excerpt }}</p>
              </div>
            </div>
          </li>
        {% endif %}
      {% endfor %}
    {% endfor %}
  </ul>