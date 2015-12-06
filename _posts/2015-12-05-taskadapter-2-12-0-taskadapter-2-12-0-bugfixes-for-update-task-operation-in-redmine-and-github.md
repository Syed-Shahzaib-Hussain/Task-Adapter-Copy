---
layout: post
title: 'TaskAdapter 2.12.0: bugfixes for “update task” operation in Redmine and Github'
date: '2015-12-05 16:35:00 -0700'
categories:
- release
- microsoft project
- redmine
- github
---

Good news, everyone!

TaskAdapter 2.12.0 has some important bugfixes:

* bug fixed: “update task” operation in Redmine and Github was failing to find tasks
* bug fixed: tasks loaded from MantisBT with “assignee” mapping selected cannot be saved to MSP
* bug fixed: task cannot be updated in GitHub when login name (assignee name) is empty

Other changes in this version:
* switched from Java 6 to Java 8. This means from now on Java 8 (Java Runtime Environment 8) is required to run the application.
* switched from Jetty 8 to Jetty 9 (embedded web-server used to run the web application).
