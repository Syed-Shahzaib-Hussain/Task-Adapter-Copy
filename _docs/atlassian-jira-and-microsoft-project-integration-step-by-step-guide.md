---
layout: docs
title: JIRA and Microsoft Project integration - step by step guide
permalink: /docs/atlassian-jira/atlassian-jira-and-microsoft-project-integration-step-by-step-guide/
author:
  display_name: admin
  login: admin
  email: alskor@gmail.com
  url: ''
author_login: admin
author_email: alskor@gmail.com
wordpress_id: 103
wordpress_url: http://www.taskadapter.com/wp/?page_id=103
date: '2012-05-25 00:55:40 -0700'
date_gmt: '2012-05-25 00:55:40 -0700'
categories: []
tags: []
comments: []
---

### User story: "I have a Microsoft Project plan and I want to export the tasks to my JIRA".

First, <a href="user-guide/installation">install and start Task Adapter</a>. Then follow these steps:

* <a href="http://www.taskadapter.com/user-guide/using-task-adapter/#create_config_file">Create a config</a>
* <a href="http://www.taskadapter.com/user-guide/using-task-adapter/#configure">Configure</a>
* <a href="http://www.taskadapter.com/user-guide/using-task-adapter/#export_data">Export tasks</a>
* Optional - <a href="http://www.taskadapter.com/user-guide/using-task-adapter/#update_msp_file">Update MSP File</a>

<h2><a id="create_config_file" name="create_config_file"></a>Create a config</h2></p>
<ol>
<li>To export tasks from a bug tracker like JIRA or a Microsoft Project file, you first need to create a &ldquo;synchronization config&rdquo;, &nbsp;which will keep settings like your Jira server URL, login, password, your Microsoft Project file location, etc.<br />
Use &ldquo;New Config&rdquo; button on the main application page to create a new config.<br />
<a href="http://www.taskadapter.com/wp-content/uploads/2012/05/create_new_config.png"><img title="create_new_config" alt="" src="http://www.taskadapter.com/wp-content/uploads/2012/05/create_new_config.png" width="298" height="286" /></a></li></p>
<li>Select two systems (Atlassian Jira and Microsoft Project in this example). You can also provide a description. As you see, the headers don&rsquo;t say &ldquo;Source&rdquo; and &ldquo;Destination, but rather &ldquo;System 1&Prime; and &ldquo;System 2&Prime;. This is to indicate that you can transfer both ways, so it does not matter if you select Jira on the left and Microsoft Project on the right, or the other way around.</li>
<li>Once you click &ldquo;Create&rdquo; button, the new config file is created in your data directory (<User Home>/taskadapter folder).</li><br />
</ol><br />
</div><br />
</div></p>
<div>
<h2>Configure.</h2></p>
<ol>
<li>Here is what you will see for a new Atlassian Jira and Microsoft Project config:<br />
<a href="http://www.taskadapter.com/wp-content/uploads/2012/05/default_jira_msp.png"><img title=""Edit config" for Atlassian Jira and Microsoft Project" alt=""Edit config" for Atlassian Jira and Microsoft Project" src="http://www.taskadapter.com/wp-content/uploads/2012/05/default_jira_msp.png" width="768" height="430" /></a></li></p>
<li>This page has two buttons to edit systems&rsquo; settings, two &ldquo;start export&rdquo; buttons and a &ldquo;Fields mapping&rdquo; panel.</li>
<li>Click the big blue buttons to configure Atlassian Jira or Microsoft Project:<br />
<img title="edit_jira_button" alt="" src="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_jira_button1.png" width="298" height="40" />&nbsp;&nbsp;<img title="edit_msp_button" alt="" src="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_msp_button.png" width="296" height="40" /></li></p>
<li>Configure Atlassian Jira settings, like Jira server URL, your Jira login name and password.<br />
<a href="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_jira1.png"><img title="edit_jira" alt="Edit Atlassian Jira settings" src="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_jira1.png" width="790" height="754" /></a>Here's the&nbsp;<a title="Atlassian Jira" href="http://www.taskadapter.com/user-guide/atlassian-jira/">complete description of the Jira configuration dialog</a>.</li></p>
<li>Close the Jira configuration panel.</li>
<li>Now click "Microsoft Project" button to open the project settings. Provide the file location -<br />
<a href="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_msp_local.png"><img class="alignnone size-full wp-image-471" title="edit_msp_local" alt="Edit Microsoft Project settings (Task Adapter local mode)" src="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_msp_local.png" width="458" height="374" /></a><br />
(This is the panel you see when you run Task Adapter in "local" mode. The server mode has a bit different one).</li></p>
<li>Now close the Microsoft Project panel.</li>
<li>You're back to "Edit Config" screen.&nbsp;Select task fields you want to export.<br />
You can change default &ldquo;mapping&rdquo; for some of them. E.g. Jira&rsquo;s &ldquo;Due Date&rdquo; field can be saved into &ldquo;Finish&rdquo; or &ldquo;Deadline&rdquo; field in a Microsoft Project file. See Microsoft Project configuration page for more details.<br />
<a href="http://www.taskadapter.com/wp-content/uploads/2012/05/default_jira_msp.png"><img class="alignnone size-full wp-image-451" title=""Edit config" for Atlassian Jira and Microsoft Project" alt=""Edit config" for Atlassian Jira and Microsoft Project" src="http://www.taskadapter.com/wp-content/uploads/2012/05/default_jira_msp.png" width="768" height="430" /></a></li><br />
</ol></p>
<h2><a id="export_data" name="export_data"></a>Export tasks.</h2></p>
<div>Click arrow-buttons to start export to the &nbsp;left or right system: &nbsp;&nbsp;<img title="export_left_right" alt="" src="http://www.taskadapter.com/wp-content/uploads/2012/05/export_left_right.png" width="134" height="42" /></div></p>
<div>A confirmation dialog is shown when the tasks are&nbsp;loaded from the source system:</div></p>
<div></div></p>
<div><img title="export_confirmation" alt="" src="http://www.taskadapter.com/wp-content/uploads/2012/05/export_confirmation.png" width="422" height="362" /></div></p>
<div></div></p>
<div>You can change the fields mappings before the export. &nbsp;Only the selected fields will be transferred to the destination system.</div></p>
<div></div></p>
<div><img title="confirm_fields_mapping" alt="" src="http://www.taskadapter.com/wp-content/uploads/2012/05/confirm_fields_mapping1.png" width="430" height="246" /></div></p>
<div></div></p>
<div>The transfer result is shown on the next page with the number of tasks created or updated.</div></p>
<div></div></p>
<div>Open your Jira web page in the browser to see the new tasks:</div></p>
<div>
<div id="node-42">
<p><img alt="" src="http://www.taskadapter.com/wp-content/uploads/2012/05/jira_web_ui.png" /></p>
<div></div><br />
</div><br />
</div></p>
<h2><a id="update_msp_file" name="update_msp_file"></a>Update MSP File</h2><br />
<a href="http://www.taskadapter.com/user-guide/using-task-adapter/#update_msp_file">Link to this page</a></p>
<p>You can update a Microsoft Project XML file with the data from an external system (Redmine/Jira/Mantis&hellip;).</p>
<ol>
<li>Either you want to export data from a Microsoft Project file to an external system OR Load data from an external system into the MSP XML file &nbsp;-&nbsp;<strong>In either case select &ldquo;Id&rdquo; field before the &ldquo;save data&rdquo; operation.</strong><a href="http://www.taskadapter.com/wp-content/uploads/2012/05/id_selected.png"><img title="id_selected" alt="" src="http://www.taskadapter.com/wp-content/uploads/2012/05/id_selected.png" width="454" height="254" /></a>The task IDs provided by the external system will be saved in the specified field (&ldquo;TEXT22&Prime; in this example) in the Microsoft Project XML file.</li>
<li>Use &ldquo;Only update tasks present in the file&rdquo; button:<br />
<img title="choose_file_operation" alt="" src="http://www.taskadapter.com/wp-content/uploads/2012/05/choose_file_operation.png" width="466" height="174" /><br />
Only the tasks which have &ldquo;remote IDs&rdquo; field set in the MSP file will be updated.</li></p>
<li>The selected tasks will be re-loaded from the external system (Jira in this example) and updated in the MSP XML file. The other tasks in the XML file will be left unchanged.</li><br />
</ol>

