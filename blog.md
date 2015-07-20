---
layout: page
status: publish
published: true
top_level_menu_weight: 30
title: Blog
permalink: /blog/

author:
  display_name: admin
  login: admin
  email: alskor@gmail.com
  url: ''
author_login: admin
author_email: alskor@gmail.com
wordpress_id: 23
wordpress_url: http://www.taskadapter.com/wp/?page_id=23
date: '2012-05-24 05:27:53 -0700'
date_gmt: '2012-05-24 05:27:53 -0700'
categories: []
tags: []
comments: []
---
<p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>

