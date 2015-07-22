---
layout: post
title: 'Task Adapter 2.6: Basecamp and Microsoft Project improvements'
author:
  display_name: admin
wordpress_id: 592
wordpress_url: http://www.taskadapter.com/?p=592
date: '2013-08-07 07:11:49 -0700'
date_gmt: '2013-08-07 07:11:49 -0700'
categories:
- release
- microsoft project
- basecamp classic
---
<p>Task Adapter 2.6 release changelog:</p>

## Basecamp Classic:

<ul>
<li>support "completed at" field (save it to "actual finish" field in MSP if the Basecamp task is marked as "Completed").

Actual finish is set for tasks which have "completed_at" field set. So if this field set and "Completed" is not, actual finish will still be set.</li></p>
<li>minor bugfixing in the Editor.</li>

</ul></p>

## Microsoft Project:

<ul>
<li>set Done ratio even when estimated time is not set.

Microsoft Project only accepts and shows "Done ratio" tasks which have either time or duration set.

What happens when you load tasks from a bug tracker, which does not support estimated time, but does support some notion of "Done ratio"? Task Adapter will now set the estimated time for  those tasks as "8h" when saving to Microsoft Project.  This is a little trick which forces MSP to show the "Done Ratio" correctly on the Gantt Diagram.</li>

</ul></p>
