---
layout: docs
title: Using Task Adapter
author:
  display_name: admin
  login: admin
  email: alskor@gmail.com
wordpress_id: 12
wordpress_url: http://www.taskadapter.com/wp/?page_id=12
date: '2012-05-24 05:23:59 -0700'
date_gmt: '2012-05-24 05:23:59 -0700'
categories: []
---
<ul>
<li><a href="#create_config_file">Create a config</a></li>
<li><a href="#configure">Configure</a></li>
<li><a href="#export_data">Export Data</a></li>
<li><a href="#update_msp_file">Update MSP File</a></li><br />
</ul></p>
<h2><a id="create_config_file" name="create_config_file"></a>Create a config</h2></p>
<ol>
<li>To export tasks from a bug tracker like Atlassian Jira and a Microsoft Project file, you first need to create a "synchronization config", &nbsp;which will keep settings like your Jira server URL, login, password, your Microsoft Project file location, etc.<br />
Use "New Config" button on the main application page to create a new config.<br />
<a href="http://www.taskadapter.com/wp-content/uploads/2012/05/create_new_config.png"><img class="alignnone size-full wp-image-452" title="create_new_config" src="http://www.taskadapter.com/wp-content/uploads/2012/05/create_new_config.png" alt="" width="298" height="286" /></a></li></p>
<li>Select two systems (e.g. Atlassian Jira and Microsoft Project). These will be the systems this "config" &nbsp;transfers data between. You can also provide a description. As you see, the headers don't say "Source" and "Destination, but rather "System 1" and "System 2". This is to indicate that you can transfer both ways, so it does not matter if you select Jira on the left and Microsoft Project on the right, or the other way around.</li>
<li>Once you click "Create" button, the new config file is created in your data directory (<User Home>/taskadapter folder).</li><br />
</ol></p>
<h2><a id="configure" name="configure"></a>Configure.</h2></p>
<ol>
<li>Once you create a config, you get "Edit Config"&nbsp;page. Here is what you will see for an Atlassian Jira and Microsoft Project config:<br />
<a href="http://www.taskadapter.com/wp-content/uploads/2012/05/default_jira_msp.png"><img class="alignnone size-full wp-image-451" title=""Edit config" for Atlassian Jira and Microsoft Project" src="http://www.taskadapter.com/wp-content/uploads/2012/05/default_jira_msp.png" alt=""Edit config" for Atlassian Jira and Microsoft Project" width="768" height="430" /></a></li></p>
<li>This page has two buttons to edit systems' settings, two "start export" buttons and a "Fields mapping" panel.</li>
<li>Click the big blue buttons to configure Atlassian Jira or Microsoft Project:<br />
<img class="alignnone size-full wp-image-455" title="edit_jira_button" src="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_jira_button1.png" alt="" width="298" height="40" />&nbsp; <img class="alignnone size-full wp-image-454" title="edit_msp_button" src="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_msp_button.png" alt="" width="296" height="40" /></li></p>
<li>Select task fields you want to export. You can change default "mapping" for some of them. E.g. Jira's "Due Date" field can be saved into "Finish" or "Deadline" field in a Microsoft Project file. See Microsoft Project configuration page for more details.</li><br />
</ol></p>
<h2><a id="export_data" name="export_data"></a>Export data.</h2></p>
<ol>
<li>Click arrow-buttons to start data export to the &nbsp;left or right system:<br />
<img class="alignnone size-full wp-image-456" title="export_left_right" src="http://www.taskadapter.com/wp-content/uploads/2012/05/export_left_right.png" alt="" width="134" height="42" /><br />
Data will be loaded from the source system and a confirmation dialog will be shown:<img class="alignnone size-full wp-image-152" title="export_confirmation" src="http://www.taskadapter.com/wp-content/uploads/2012/05/export_confirmation.png" alt="" width="422" height="362" /></li></p>
<li>You can change the fields mappings before the export.<br />
Only the selected fields will be transferred to the destination system.<br />
<img class="alignnone size-full wp-image-459" title="confirm_fields_mapping" src="http://www.taskadapter.com/wp-content/uploads/2012/05/confirm_fields_mapping1.png" alt="" width="430" height="246" /></li></p>
<li>The transfer result is shown on the next page with the number of tasks created or updated.</li><br />
</ol></p>
<h2><a id="update_msp_file" name="update_msp_file"></a>Update MSP File</h2><br />
<a href="#update_msp_file">Link to this page</a></p>
<p>You can update a Microsoft Project XML file with the data from an external system (Redmine/Jira/Mantis...).</p>
<ol>
<li>Either you want to export data from a Microsoft Project file to an external system OR Load data from an external system into the MSP XML file -<strong>In either case select "Id" field before the "save data" operation.</strong><a href="http://www.taskadapter.com/wp-content/uploads/2012/05/id_selected.png"><img class="alignnone size-full wp-image-460" title="id_selected" src="http://www.taskadapter.com/wp-content/uploads/2012/05/id_selected.png" alt="" width="454" height="254" /></a>
<p>The task IDs provided by the external system will be saved in the specified field ("TEXT22" in this example) in the Microsoft Project XML file.</li></p>
<li>Use "Only update tasks present in the file" button:<br />
<img class="alignnone size-full wp-image-157" title="choose_file_operation" src="http://www.taskadapter.com/wp-content/uploads/2012/05/choose_file_operation.png" alt="" width="466" height="174" /><br />
Only the tasks which have "remote IDs" field set in the MSP file will be updated.</li></p>
<li>The selected tasks will be re-loaded from the external system (Jira in this example) and updated in the MSP XML file. The other tasks in the XML file will be left unchanged.</li><br />
</ol></p>
