---
layout: post
title: 'Task Adapter 2.9.0: support for default values.'
author: admin
date: '2015-01-28 05:33:41 -0800'
categories:
- redmine
- atlassian jira
- release
- microsoft project
---

Main improvements are:

* support default values for empty fields.
You can now provide default values to set in target system when there is no corresponding value in the source system.
E.g. your source Redmine does not contain "environment" field, but JIRA has "Environment" configured as "required".
You can provide "environment 1" as the default value and it will be set to all new JIRA issues in this sync configuration.

![Default values](/images/uploads/default_values1.png)

* Redmine, MSP: support "target version" field
* JIRA, MSP: support "Environment" field
* localize Login and Export pages
* Minor GUI bugfixes
