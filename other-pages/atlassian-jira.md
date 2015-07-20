---
layout: page
status: publish
published: true
title: Atlassian Jira
author:
  display_name: admin
  login: admin
  email: alskor@gmail.com
  url: ''
author_login: admin
author_email: alskor@gmail.com
wordpress_id: 331
wordpress_url: http://www.taskadapter.com/?page_id=331
date: '2012-06-22 03:27:30 -0700'
date_gmt: '2012-06-22 03:27:30 -0700'
categories: []
tags: []
comments:
- id: 9
  author: Synchronize Issues in Mantis and in JIRA - DexPage
  author_email: ''
  author_url: http://dexpage.com/synchronize-issues-in-mantis-and-in-jira/
  date: '2015-06-27 15:53:42 -0700'
  date_gmt: '2015-06-27 15:53:42 -0700'
  content: "[&#8230;] you can implement your own sync using Jira&#8217;s REST API
    as @Daria replied above, or you can use Task Adapter for manual data synchronization
    between Jira and Mantis. [&#8230;]"
---
<p>Atlassian Jira is a powerful bug tracking / task management tool. Unfortunately, it does not show a good overview like "when will this project complete". Microsoft Project, on the other hand, is a powerful project management tool, but the project plan created by it is almost impossible to keep up-to-date. Many managers use Microsoft Project to create a plan in the beginning of a project to roughly estimate required resources and completion date, but when the project actually starts, the plan quickly becomes out of date and useless.</p>
<p>To solve this, you can generate a Microsoft Project plan using the tasks you exported from your Jira project.<br />
This way your project plan is always up-to-date and accurate. You can open it in Microsoft Project, update there, and then re-export back to your Jira server.</p>
<p>Integration works both ways: you can export tasks from Microsoft Project to Atlassian Jira and vice versa.</p>
<h2>Jira server requirements.</h2><br />
Task Adapter requires "Remote API Access" enabled in your Jira instance.&nbsp;Use the following menu in Jira web interface: <strong>Administration</strong> >> <strong>General Configuration</strong> >> <strong>Accept remote API calls</strong>.</p>
<h2>Supported Jira versions.</h2><br />
<strong>Task Adapter 2.1+ supports Atlassian Jira 5.0 or higher (or any current Jira OnDemand instances). </strong>Previous&nbsp;Jira versions do not have remote interfaces required for the data transfer. The last Task Adapter version still compatible with Jira 4 was 2.0.2, you can get it here:&nbsp;<a href="http://www.taskadapter.com/releases/taskadapter-2.0.2.zip">download the old Task Adapter 2.0.2</a>.</p>
<p><a href="/user-guide/atlassian-jira">How to configure Task Adapter for Atlassian Jira usage</a></p>
