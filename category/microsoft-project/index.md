---
layout: post
title: Microsoft Project
---

<p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

  <ul class="post-list">
    {% for post in site.categories.microsoft-project %}
      *
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>

    {% endfor %}
  </ul>

