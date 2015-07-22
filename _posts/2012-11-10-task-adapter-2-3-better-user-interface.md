---
layout: post
title: 'Task Adapter 2.3: better User Interface'
author:
  display_name: admin
wordpress_id: 434
wordpress_url: http://www.taskadapter.com/?p=434
date: '2012-11-10 04:20:53 -0800'
date_gmt: '2012-11-10 04:20:53 -0800'
categories:
- atlassian jira
- release
- microsoft project
- mantisbt
- github
---
<p>Task Adapter 2.3 brings important changes in the User Interface.</p>
<p>First of all, we **combined two task fields mapping panels into one** as promised in the previous blog post. This is a big change and we ask you to try this out and let us know what you think of it.</p>
<p>Second, we redesigned most of the editors to make them more consistent and usable. We know we still have a long way to go in terms of usability and design, but we hope the new version is easier to use than the old one.</p>
<p>Other important changes:</p>
<p>**User Interface.**</p>
<ul>
* New start page design.
* New "Check for update" feature (manual check for now).
* Config filter on the start page to make it easier to find a config there.
* A lot of new validations and bugfixes in the UI.
* License info panel is moved from "Configure" to "Support" page.

</ul>

**Microsoft Project.**</p>
<ul>
* (!) **Changed** **default** Microsoft Project setting for "Start date" from **"no constraint" to "Must Start On"**.
* Added validation that Microsoft Project text fields are only used once in one config. This means that you can't mistakenly map JIRA's "Task Type" and "Task Status" fields to the same "TEXT20" field in Microsoft Project.

</ul>

**Github**.</p>
<ul>
* Bug fixed: all the task fields were transferred even if they were un-selected in "fields mapping" dialog.

</ul>

**MantisBT.**</p>
<ul>
* GUI: Removed some fields from the editor, which are not supported by MantisBT connector yet.

</ul>

 </p>
