---
layout: page
title: videos
permalink: /videos/
---

  <h1 class="page-heading">videos</h1>

  <ul class="video-list">
    {% for video in site.videos %}
      <li>
        <span class="video-meta">{{ video.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="video-link" href="{{ video.url | prepend: site.baseurl }}">{{ video.title }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>