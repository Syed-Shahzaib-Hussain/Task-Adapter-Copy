---
layout: post
title: Redmine Java API 2.1.0 is released
author:
  display_name: admin
date: '2015-01-26 09:50:51 -0800'
categories:
- redmine java api
---

We just released a new version of Redmine Java API: 2.1.0.

Main changes:

* Feature #120. Support "on behalf of user" operations
* Feature #124. Allow lock user (support user status field)
* Feature #165. Implement retrieving custom field definitions
* Feature #169. added new method: create issues using project database ID
* Issue #174. Workaround for bug in Redmine 2.6.0 (it returns invalid structure for empty custom field)
* Bug #164. Fix setting project on existing issue
* Plus some minor bugfixes.

The library is tested with Redmine 2.6.0.

The <a href="http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22com.taskadapter%22%20AND%20a%3A%22redmine-java-api%22">library is available in Maven Central repository</a>.
