---
layout: docs
title: Atlassian JIRA
permalink: /docs/atlassian-jira/
---

* This text will be replaced with table of contents
{:toc}

## General info

Atlassian JIRA is a powerful bug tracking / task management tool. Unfortunately, it does not show a good overview like
"when will this project complete".
Microsoft Project, on the other hand, is a powerful project management tool, but the project plan created by it is
almost impossible to keep up-to-date.
Many managers use Microsoft Project to create a plan in the beginning of a project to roughly estimate required
resources and completion date, but when the project actually starts, the plan quickly becomes out of date and useless.

You can generate a Microsoft Project plan using the tasks you exported from your JIRA project.

This way your project plan is always up-to-date and accurate. You can open it in Microsoft Project, update there,
 and then re-export back to your JIRA server.

Integration works both ways: you can export tasks from Microsoft Project to Atlassian JIRA and vice versa.

## JIRA server requirements.

Task Adapter requires "Remote API Access" enabled in your JIRA instance. Use the following menu in JIRA web interface:
 **Administration** >> **General Configuration** >> **Accept remote API calls**

## Supported JIRA versions.

**Task Adapter 2.1+ supports Atlassian JIRA 5.0 or higher (or any current JIRA OnDemand instances).**
Previous JIRA versions do not have remote interfaces required for the proper data transfer.
The last Task Adapter version still compatible with JIRA 4 was 2.0.2, you can get it here:
[download Task Adapter 2.0.2 - only use this legacy version for JIRA 4](https://bitbucket.org/taskadapter/releases/downloads/taskadapter-2.0.2.zip)

<a href="/docs/atlassian-jira-configuration">How to configure Task Adapter for Atlassian JIRA usage</a>
