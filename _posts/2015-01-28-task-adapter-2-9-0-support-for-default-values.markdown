---
layout: post
status: publish
published: true
title: 'Task Adapter 2.9.0: support for default values.'
author:
  display_name: admin
  login: admin
  email: alskor@gmail.com
  url: ''
author_login: admin
author_email: alskor@gmail.com
wordpress_id: 731
wordpress_url: http://www.taskadapter.com/?p=731
date: '2015-01-28 05:33:41 -0800'
date_gmt: '2015-01-28 05:33:41 -0800'
categories:
- Uncategorized
- redmine
- atlassian jira
- release
- microsoft project
tags: []
comments: []
---
<p>Main improvements are:</p>
<p>* support default values for empty fields.</p>
<p>You can now provide default values to set in target system when there is no corresponding value in the source system. E.g. your source Redmine does not contain "environment" field, but JIRA has "Environment" configured as "required". You can provide "environment 1" as the default value and it will be set to all new JIRA issues in this sync configuration.</p>
<p><a href="http://www.taskadapter.com/wp-content/uploads/2015/01/default_values1.png"><img class="alignnone size-full wp-image-736" alt="default_values" src="http://www.taskadapter.com/wp-content/uploads/2015/01/default_values1.png" width="741" height="390" /></a></p>
<p>* Redmine, MSP:&nbsp;support "target version" field</p>
<p>* JIRA, MSP: support "Environment" field</p>
<p>* localize Login and Export pages.</p>
<p>* Minor GUI bugfixes.</p>
