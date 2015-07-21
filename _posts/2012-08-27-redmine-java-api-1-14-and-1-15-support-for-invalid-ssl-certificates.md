---
layout: post
title: 'Redmine Java API 1.14 and 1.15: support for invalid SSL certificates'
author:
  display_name: admin
  login: admin
  email: alskor@gmail.com
  url: ''
author_login: admin
author_email: alskor@gmail.com
wordpress_id: 375
wordpress_url: http://www.taskadapter.com/?p=375
date: '2012-08-27 02:29:01 -0700'
date_gmt: '2012-08-27 02:29:01 -0700'
categories:
- redmine java api
tags: []
comments: []
---
<p>Redmine Java API 1.14 brings support for invalid SSL certificates. Before this, the API would refuse to work with servers using self-signed certificates (which seems to be the absolute majority of all the SSL certificates in the world).</p>
<p>Details:&nbsp;<a href="https://github.com/taskadapter/redmine-java-api/issues?milestone=5&amp;state=closed">https://github.com/taskadapter/redmine-java-api/issues?milestone=5</a></p>
<p>Version 1.15 does not have any new functionality, but supports a newer JSon library. See&nbsp;<a href="https://github.com/taskadapter/redmine-java-api/issues/47">https://github.com/taskadapter/redmine-java-api/issues/47</a>&nbsp;for details.</p>
<p>The next Task Adapter version (2.1) will use the latest Redmine Java API 1.15.</p>
