---
layout: post
title: Task Adapter 2.1.
author:
  display_name: admin
  login: admin
  email: alskor@gmail.com
  url: ''
author_login: admin
author_email: alskor@gmail.com
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
<li>Many small bugfixes. A major interface improvement is planned for the next version (2.2).</li><br />
</ul></p>
<h4>Atlassian Jira:</h4></p>
<ul>
<li>Support for Estimated Time field.</li>
<li>Support for "precedes / follows" relations, commonly used by Microsoft Project to track dependencies between tasks.</li>
<li>A lot of minor bugfixes.</li>
<li><strong>Note: the oldest supported Atlassian Jira version is now 5.0. </strong>Unfortunately, the older Jira versions don't have the remote interfaces Task Adapter needs.</li><br />
</ul></p>
<h4>Microsoft Project:</h4></p>
<ul>
<li>Bug fixed:&nbsp;"Can't create Tasks Relations" message after saving to an MSP file with "mpp" extension.</li>
<li>Bug fixed:&nbsp;Exception when import from MSP file which was deleted.</li><br />
</ul></p>
<h4>Github</h4></p>
<ul>
<li>Support for free-form Queries.</li>
<li>Minor bugfixing.</li><br />
</ul></p>
<h4>Redmine</h4></p>
<ul>
<li>Use the latest Redmine Java API v. 1.15.</li>
<li>Better support for Redmine 2.0.2 or newer.</li>
<li>Minor bugfixing.</li><br />
</ul></p>
