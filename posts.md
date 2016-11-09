---
layout: page
title: Posts
permalink: /posts/
---

  <ul class="post-list">
    {% for post in site.posts %}
      {% for category in post.categories %}
        {% if category == "updates" %}
          <li>
            <div style="background:#000;height:200px">
              <div style="padding:20px">
                <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
                    <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
                      <p style="font-size:16px"><b>{{ post.title }}</b></p>
                    </a>
                <hr>
                <p style="font-size:12px;margin-top:10px">{{ post.excerpt }}</p>
              </div>
            </div>
          </li>
        {% endif %}
      {% endfor %}
    {% endfor %}
  </ul>