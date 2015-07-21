---
layout: docs
title: Microsoft Project
permalink: /docs/microsoft-project/
---

## Microsoft Project integration

Task Adapter supports Microsoft Project XML files (also known as "MSPDI" - Microsoft's XML file format for storing project data).
The following applications can load and save data from/to MSPDI format:

* Microsoft Project 2002-2013
* Merlin Project Management (Mac OS)
* Serena OpenProj
* many others.

Task Adapter supports unlimited nesting for tasks in the project plan.
Microsoft Project configuration dialog (Task Adapter is running locally on your machine, so-called "Local mode"):

<a href="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_msp_local.png"><img class="alignnone size-full wp-image-471" title="edit_msp_local" alt="" src="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_msp_local.png" width="458" height="374" /></a></p>
<p>Microsoft Project configuration dialog (Task Adapter is running on some remote server - "Server mode"):

<a href="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_msp_server.png"><img class="alignnone size-full wp-image-472" title="edit_msp_server" alt="" src="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_msp_server.png" width="460" height="400" /></a></p>

* **Description** Any text to help you identify this MSP file later.
* **File name** Full or relative path to the MSP XML file. If the file does not exist, it will be created when
 exporting data from Task Adapter. If a relative path is provided, it will be created in the folder
 where you unpacked Task Adapter to.

Note that Task Adapter cannot create Microsoft Project files in MPP format, so there are two separate fields -
 for "Input file" and "Output file". You should normally provide the same name in both fields if you're using
 Microsoft Project's XML file format.

Otherwise, you can provide an "MPP" file path in "Input file" and an XML file name in "Output file".

* **MSP Text Fields to use for some internal stuff** This section shows in READ-ONLY mode the MSP fields used
 by Task Adapter to store some internal flags.

Some task fields from Redmine or JIRA can be saved to more than one field in Microsoft Project.
For example, JIRA's "Due Date" can be saved into "Finish" or "Deadline" in Microsoft Project.
The project file will behave differently in Microsoft Project, depending on these settings,
so you need to analyse the fields mappings and select what's best for you. It all depends on your needs.

<a href="http://www.taskadapter.com/wp-content/uploads/2012/05/redmine_msp_fields_mapping.png"><img src="http://www.taskadapter.com/wp-content/uploads/2012/05/redmine_msp_fields_mapping.png"/></a>

<a name="fields_mapping"></a>Only the selected fields will be exported when saving data into this MS Project file. <a href="#fields_mapping">Link</a>

* <a name="save_remote_ids"></a> **Id** <a href="#save_remote_ids">Link</a>&nbsp;When you load a Microsoft Project file into Task Adapter and then export tasks into Redmine / Atlassian JIRA / Chiliproject/etc.. , Task Adapter can remember the IDs of the created tasks. These "remote IDs" are stored in the Microsoft Project file itself (assuming that the option is&nbsp;<em>selected</em>).

This way you can later edit the project file (using Microsoft&nbsp;Project), load it to Task Adapter again and re-export tasks to the same Redmine/JIRA/..., so that the tasks without "remote IDs" will be&nbsp;**created**&nbsp;and the old ones (which have been previously created in Redmine/jira/...) will be&nbsp;**updated**. This is convenient if you want to export data from the same Microsoft Project file several times and don't want to create duplicate tasks in your Redmine/JIRA/...

At the same time, it can be confusing if you export data into Redmine/JIRA,
then delete the new tasks on the server and try exporting data from the same MSP file again.
Task Adapter will report that it can't update non-existing tasks. This is because it assumes that MSP tasks with
saved "Remote IDs" should already exist in the export destination point.
**Unselect** this option if you want Task Adapter to always create NEW tasks from the same MSP file.
If selected, you need to configure which text field to use in a Microsoft Project file to store "Remote ID" info.
E.g. "TEXT1", "TEXT 15", etc.

* **Task Type / Tracker Type** Select a Microsoft Project field to store "Task Type" info ("bug", "feature", "task", etc). This can be stored in any of the "free-TEXT" fields.
* **Estimated Time** "Estimated Time" can be exported to either **"Work"** or **"Duration"** field. Please analyse what you need in your case (please refer to Microsoft Project documentation).
* <a name="start_date"></a>**Start Date** <a href="#start_date">Link</a>

<a href="http://www.taskadapter.com/wp-content/uploads/2012/05/msp_start_date_mapping_options.png"><img src="http://www.taskadapter.com/wp-content/uploads/2012/05/msp_start_date_mapping_options.png" width="309" height="225" /></a>
<a href="http://www.taskadapter.com/microsoft_project#start_date"></a>

Task Adapter can save "Start date" using these constraints recognized by Microsoft Project.
Set "<no constraint>" if you don't need any constraints on the tasks. In this case when you open the exported MSP file
in MS Project, it will calculate and set "start/finish" dates for the tasks itself.
Please refer to Microsoft Project documentation to see the differences between "As soon as possible",
"Must start on" and other options for task start dates.
* <a name="msp_due_date"></a>**Due Date** <a href="#msp_due_date">Link</a>

<img src="http://www.taskadapter.com/wp-content/uploads/2012/05/msp_due_date_mapping_options.png"/>

Select **Finish** or **Deadline**.

Most people expect "Due date" field to be saved as "finish date" in Microsoft Project, so that a nice Gantt diagram
can be shown. The trick here is that MSP "ideology" is that the finish date must be calculated by MSP itself
(that's pretty much the goal of Microsoft Project as a product).
So it would be more correct to save this field to "deadline" column, but many users have requested the default
to be "Finish date".
You can un-select this field if you don't want Task Adapter to save "due date" field into Microsoft Project files at all.

