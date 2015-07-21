---
layout: docs
title: Export sub-projects from Redmine
permalink: /docs/redmine/export-sub-projects-from-redmine/
author:
  display_name: admin
  login: admin
wordpress_id: 90
wordpress_url: http://www.taskadapter.com/wp/?page_id=90
date: '2012-05-25 00:45:20 -0700'
date_gmt: '2012-05-25 00:45:20 -0700'
categories: []
---

Redmine Subprojects are not directly supported by Task Adapter.

<p>Here's what you can do if you need to export data from several related Redmine projects. Suppose, you have a top-level project "top1" and two subprojects "sub1", "sub2".</p>
<p>In Task Adapter's "Edit config" dialog: set the project name to the top-project.</p>
<div>If you do not set anything in "Query ID" field then all issues will be loaded from the given project. Otherwise Task Adapter will use the issues returned by the saved query.</div>
<p>Set this in your Redmine (menu Administration : Settings) (this is the default setting in Redmine 1.2+)</p>
<div><img src="http://www.taskadapter.com/wp-content/uploads/2012/05/redmine_admin_show_issues_subprojects.png" alt="" /></div>

<div>Then you can load all the issues from the Redmine project and its subprojects in TA.</div>
<p>Here's how these issues are shown in Redmine web UI:</p>
<p><img src="http://www.taskadapter.com/wp-content/uploads/2012/05/redmine_webui_issues_in_subprojects.png" alt=""/></p>
