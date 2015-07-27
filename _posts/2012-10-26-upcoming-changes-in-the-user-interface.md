---
layout: post
title: Upcoming changes in the User Interface
author: admin
date: '2012-10-26 23:39:05 -0700'
categories:
- development
---

We admit that the current User Interface is pretty kludgy and inconsistent and we promise to make it better soon!
The main usability problem affecting everyone is that the fields mapping panel is pretty illogical and you need
 to read documentation to figure out what "Remote ID" means on Microsoft Project tab and what exactly checkboxes
 affect on the fields mapping panels - loading the data from this connector or saving to it?

So the next version (2.3) will have a single page for mapping fields between data connectors instead of two separate tabs.

Preview of the new interface:

![TaskAdapter new mapping]({{ site.baseurl }}/images/uploads/2012/10/ta_new_mapping1.png)

<p>And here is the current User Interface (version 2.2) for your comparison.
 As you see, fields mappings are stored separately for Redmine and for Microsoft Project here:

![Task Adapter 2.2 Editor Redmine]({{ site.baseurl }}/images/uploads/2012/10/old_ta_ui.png)

![Task Adapter 2.2 Editor Microsoft Project]({{ site.baseurl }}/images/uploads/2012/10/old_ta_ui_msp.png)

This old interface makes you wonder what happens when you select "Assignee" field in Redmine editor
and un-select it in Microsoft Project, right? Well, not anymore after we release version 2.3.

Another thing is that you can now start export right from the Config Details page.

Stay tuned for more changes!
