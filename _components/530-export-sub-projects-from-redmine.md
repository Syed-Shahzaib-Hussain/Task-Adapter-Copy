---
layout: docs
title: Exporting sub-projects from Redmine
permalink: /docs/redmine/export-sub-projects-from-redmine/
---

## {{ page.title }}

Redmine subprojects are not directly supported by Task Adapter.

Here's what you can do if you need to export data from several related Redmine projects.
Suppose, you have a top-level project "top1" and two subprojects "sub1", "sub2".

In Task Adapter's "Edit config" dialog: set the project name to the top-project.

If you do not set anything in "Query ID" field then all issues will be loaded from the given project.
Otherwise Task Adapter will use the issues returned by the saved query.

Set this in your Redmine (menu Administration -> Settings) (this is the default setting in Redmine 1.2+).

<img src="{{ site.baseurl }}/images/uploads/redmine_admin_show_issues_subprojects.png"/>

Then you can load all the issues from the Redmine project and its subprojects in TA. Here's how these issues are shown in Redmine web UI:

<img src="{{ site.baseurl }}/images/uploads/redmine_webui_issues_in_subprojects.png" />
