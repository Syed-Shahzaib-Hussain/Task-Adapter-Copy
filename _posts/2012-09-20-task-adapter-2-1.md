---
layout: post
title: Task Adapter 2.1.
author:
  display_name: admin
wordpress_id: 390
wordpress_url: http://www.taskadapter.com/?p=390
date: '2012-09-20 01:13:33 -0700'
date_gmt: '2012-09-20 01:13:33 -0700'
categories:
- redmine
- atlassian jira
- release
- microsoft project
- github
---
<p>Task Adapter 2.1 looks and behaves similarly to version 2.0, but its internals were significantly redesigned for better maintainability and testability.</p>
<p>The main user-facing changes in 2.1 release are:</p>
<h4>User Interface</h4></p>
<ul>
* Many small bugfixes. A major interface improvement is planned for the next version (2.2).

</ul></p>
<h4>Atlassian JIRA:</h4></p>
<ul>
* Support for Estimated Time field.
* Support for "precedes / follows" relations, commonly used by Microsoft Project to track dependencies between tasks.
* A lot of minor bugfixes.
* **Note: the oldest supported Atlassian JIRA version is now 5.0. **Unfortunately, the older JIRA versions don't have the remote interfaces Task Adapter needs.

</ul></p>
<h4>Microsoft Project:</h4></p>
<ul>
* Bug fixed: "Can't create Tasks Relations" message after saving to an MSP file with "mpp" extension.
* Bug fixed: Exception when import from MSP file which was deleted.

</ul></p>
<h4>Github</h4></p>
<ul>
* Support for free-form Queries.
* Minor bugfixing.

</ul></p>
<h4>Redmine</h4></p>
<ul>
* Use the latest Redmine Java API v. 1.15.
* Better support for Redmine 2.0.2 or newer.
* Minor bugfixing.

</ul></p>
