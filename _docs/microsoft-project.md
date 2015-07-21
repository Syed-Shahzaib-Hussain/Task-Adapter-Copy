---
layout: docs
title: Microsoft Project
author:
  display_name: admin
  login: admin
  email: alskor@gmail.com
wordpress_id: 95
wordpress_url: http://www.taskadapter.com/wp/?page_id=95
date: '2012-05-25 00:49:14 -0700'
date_gmt: '2012-05-25 00:49:14 -0700'
categories: []
---
<p>Task Adapter supports Microsoft Project XML files (also known as "MSPDI" - Microsoft's XML file format for storing project data).</p>
<p>The following applications can load and save data from/to MSPDI format:</p>
<ul>
<li>Microsoft Project 2002-2013;</li>
<li>Merlin Project Management (Mac OS);</li>
<li>Serena OpenProj;</li>
<li>many others.</li><br />
</ul><br />
Task Adapter supports unlimited nesting for tasks in the project plan.</p>
<p>Microsoft Project configuration dialog (Task Adapter is running locally on your machine, so-called "Local mode"):<br />
<a href="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_msp_local.png"><img class="alignnone size-full wp-image-471" title="edit_msp_local" alt="" src="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_msp_local.png" width="458" height="374" /></a></p>
<p>Microsoft Project configuration dialog (Task Adapter is running on some remote server - "Server mode"):<br />
<a href="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_msp_server.png"><img class="alignnone size-full wp-image-472" title="edit_msp_server" alt="" src="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_msp_server.png" width="460" height="400" /></a></p>
<ul>
<li><strong>Description</strong>&nbsp;Any text to help you identify this MSP file later.</li>
<li><strong>File name &nbsp;</strong>Full or relative path to the MSP XML file. If the file does not exist, it will be created when exporting data from Task Adapter. If a relative path is provided, it will be created in the folder where you unpacked Task Adapter to.<br />
Note that Task Adapter cannot create Microsoft Project files in MPP format, so there are two separate fields for "Input file" and "Output file". You should normally provide the same name in both fields if you're using Microsoft Project's XML file format.<br />
Otherwise, you can provide an "MPP" file in "Input file" and an XML file name in "Output file".</li></p>
<li><strong>MSP Text Fields to use for some internal stuff &nbsp;</strong>This section shows in READ-ONLY mode the MSP fields used by Task Adapter to store some internal flags.</li><br />
</ul><br />
Some task fields from Redmine or Jira can be saved to more than one field in Microsoft Project. For example, Jira's "Due Date" can be saved into "Finish" or "Deadline" in Microsoft Project. The project file will behave differently in Microsoft Project, depending on these settings, so you need to analyse the fields mappings and select what's best for you. It all depends on your needs.<br />
<a href="http://www.taskadapter.com/wp-content/uploads/2012/05/redmine_msp_fields_mapping.png"><img class="alignnone size-full wp-image-473" title="redmine_msp_fields_mapping" alt="" src="http://www.taskadapter.com/wp-content/uploads/2012/05/redmine_msp_fields_mapping.png" width="436" height="324" /></a><br />
<a id="fields_mapping" name="fields_mapping"></a>Only the selected fields will be exported when saving data into this MS Project file. <a href="#fields_mapping">Link</a></p>
<ul>
<li><strong><a id="save_remote_ids" name="save_remote_ids"></a>&nbsp;Id</strong>&nbsp;<a href="#save_remote_ids">Link</a>&nbsp;When you load a Microsoft Project file into Task Adapter and then export tasks into Redmine / Atlassian Jira / Chiliproject/etc.. , Task Adapter can remember the IDs of the created tasks. These "remote IDs" are stored in the Microsoft Project file itself (assuming that the option is&nbsp;<em>selected</em>).<br />
This way you can later edit the project file (using Microsoft&nbsp;Project), load it to Task Adapter again and re-export tasks to the same Redmine/Jira/..., so that the tasks without "remote IDs" will be&nbsp;<strong>created</strong>&nbsp;and the old ones (which have been previously created in Redmine/jira/...) will be&nbsp;<strong>updated</strong>. This is convenient if you want to export data from the same Microsoft Project file several times and don't want to create duplicate tasks in your Redmine/Jira/...<br />
At the same time, it can be confusing if you export data into Redmine/Jira, then delete the new tasks on the server and try exporting data from the same MSP file again. Task Adapter will report that it can't update non-existing tasks. This is because it assumes that MSP tasks with saved "Remote IDs" should already exist in the export destination point.<em>Unselect&nbsp;</em>this option if you want Task Adapter to always create NEW tasks from the same MSP file.If selected, you need to configure which text field to use in a Microsoft Project file&nbsp;to store "Remote ID" info. E.g. "TEXT1", "TEXT 15", etc.</li></p>
<li><strong>Task Type / Tracker Type &nbsp;</strong>Select a Microsoft Project field to store "Task Type" info ("bug", "feature", "task", etc). This can be stored in any of the "free-TEXT" fields.</li>
<li><strong>Estimated Time &nbsp;</strong>"Estimated Time" can be exported to either <strong>"Work"</strong> or <strong>"Duration"</strong> field. Please analyse what you need in your case (please refer to Microsoft Project documentation).</li>
<li><strong><a id="start_date" name="start_date"></a>Start Date</strong> <a href="#start_date">Link<br />
</a><a href="http://www.taskadapter.com/wp-content/uploads/2012/05/msp_start_date_mapping_options.png"><img class="alignnone size-full wp-image-175" title="msp_start_date_mapping_options" alt="" src="http://www.taskadapter.com/wp-content/uploads/2012/05/msp_start_date_mapping_options.png" width="309" height="225" /></a><a href="http://www.taskadapter.com/microsoft_project#start_date"><br />
</a>Task Adapter can save "Start date" using some constraints recognized by Microsoft Project. Set "<no constraint>" if you don't need any constraints on the tasks. In this case when you open the exported MSP file in MS Project, it will calculate and set "start/finish" dates for the tasks itself. Please refer to Microsoft Project documentation to see the differences between "As soon as possible", "Must start on" and other options for task start dates.</li></p>
<li><strong><a id="msp_due_date" name="msp_due_date"></a>"Due Date"</strong> <a href="#msp_due_date">Link<br />
</a><img class="alignnone size-full wp-image-176" title="msp_due_date_mapping_options" alt="" src="http://www.taskadapter.com/wp-content/uploads/2012/05/msp_due_date_mapping_options.png" width="305" height="86" />Select <em>Finish</em> or <em>Deadline</em>.<br />
Most people expect "Due date" field should be saved to "finish date" field in Microsoft Project, so that a nice Gantt diagram can be shown. The trick here is that MSP "ideology" is that the finish date must be calculated by MSP itself (that's pretty much the whole goal of Microsoft Project as a product). So it would be more correct to save this field to "deadline" column, but many users have requested the default to be "Finish date".You can un-select this field if you don't want Task Adapter to save "due date" field into Microsoft Project files at all.</li><br />
</ul></p>
