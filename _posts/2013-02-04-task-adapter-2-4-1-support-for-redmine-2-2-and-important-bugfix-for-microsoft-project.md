---
layout: post
title: 'Task Adapter 2.4.1: support for Redmine 2.2+ and important bugfix for Microsoft
  Project'
author: admin
date: '2013-02-04 21:56:00 -0800'
categories:
- redmine
- release
- microsoft-project
- mantisbt
---

Task Adapter 2.4.1 brings several bugfixes and one minor feature in MantisBT editor.

### Microsoft Project.

* bug fixed: creating tasks in Redmine fails with "parent task is invalid" error in some cases.


### MantisBT (Bug Tracker).

* Support "show saved queries"
* exported tasks/issues are not related to selected Project/Query ID
* exceptions when Project Key is not provided

### Redmine.

* "404 not found" error is shown when trying to create an Issue in Redmine without setting a project key
* change the default "transfer priority" value to "unselected" for Redmine
* verify that we properly support Redmine 2.2.0+
* use Redmine Java API 1.18 with the authentication bugfix

### User Interface.

* fields are in a different order in "new config" and "edit config" pages

### Other.

* Updated Jetty version to 8.1.8 (this is the embedded webserver used by Task Adapter internally).
* Updated Vaadin version (web-framework).
