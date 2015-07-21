---
layout: docs
title: Github integration
permalink: /docs/github/
---

## Github

Github is a popular web-site for hosting Git repositories. It  also offers Issues management,
similar to bug trackers like MantisBT and JIRA. Although Github's issues management is quite simple
(it lacks time estimates and many other features), it is actually very convenient, fast and user friendly.

Sometimes you need to export your tasks from Microsoft Project, Atlassian JIRA or other systems to Github.
This is when Task Adapter comes in handy. It saves the time you would spend manually coping/pasting tasks from the other systems.

### Github configuration dialog

<a href="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_github1.png"><img src="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_github1.png" alt=""/></a>

* **Description**  Any label you want to help you identify this Github config.
* **Server URL**  Github server URL. While most people will use github.com, there is also a downloadable version of the
 same service called Github Enterprise, which can be installed locally. This is the case when you would want to change
 the default "github.com" address to the server name where you install your local Github Enterprise.
* **Login**  Your Github login
* **Password** Your Github password
* **Repository ID**  Your Github repository ID
* **Query**  Any text query allowed by Github. Task Adapter does not interpret this query, but rather just sends it
 to Github to retrieve data. Sample value: "milestone=7&state=closed"
