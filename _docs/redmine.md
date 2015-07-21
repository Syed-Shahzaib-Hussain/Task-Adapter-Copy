---
layout: docs
title: Redmine
author:
  display_name: admin
  login: admin
  email: alskor@gmail.com
  url: ''
author_login: admin
author_email: alskor@gmail.com
wordpress_id: 52
wordpress_url: http://www.taskadapter.com/wp/?page_id=52
date: '2012-05-24 05:48:50 -0700'
date_gmt: '2012-05-24 05:48:50 -0700'
categories: []
---
**Note: "REST API" must be enabled in your Redmine for this connector to work.**
<a href="#rest_api">How to enable REST API in Redmine</a>

<p><a href="#general">General info<br />
</a><a href="#performance">Performance<br />
</a><a href="#dialog">Configuration dialog</a></p>
<p><a id="general" name="general"></a><strong>General info </strong></p>
<ul>
<li>Task Adapter version 2.3 was tested with Redmine 2.0.3 and 2.1.0. <strong>Some</strong> features will work with the older Redmine versions 1.3.0-1.4.4, but you would need to unselect many of the fields in "Fields Mapping dialog", which the old Redmine does not support (e.g. "Issue relations"). Task Adapter <strong>will NOT work with Redmine older than 1.3.0.</strong></li>
<li>Can export data from Redmine to Microsoft Project (or any other connector supported by Task Adapter, e.g. Atlassian Jira, ChiliProject).</li>
<li>Can import data from Microsoft Project or any other Task Adapter connector to Redmine.</li>
<li>Subtasks - unlimited nesting</li>
<li>See <a href="#dialog">configuration dialog below</a> for the list of supported Redmine task fields.</li><br />
</ul><br />
<strong><a id="performance" name="performance"></a>Performance</strong></p>
<p>Saving 200 tasks to Redmine takes 8m:35s (515 seconds), which gives around ~0.38 task/sec.<br />
Loading 3750 tasks takes 82 sec (~45 tasks/sec)<br />
Save/load speed changes pretty much linearly when tasks number changes.</p>
<p><a id="dialog" name="dialog"></a><strong>Redmine configuration dialog</strong></p>
<p><a href="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_redmine4.png"><img class="alignnone size-full wp-image-465" title="edit_redmine" src="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_redmine4.png" alt="" width="792" height="518" /></a></p>
<ul>
<li><strong>Description</strong>&nbsp;Arbitrary text, which will be later shown in the configs list.</li>
<li><strong>Server URL</strong> Complete Redmine URL, including protocol prefix (https or http) and port number (when using a non-standard port).<br />
<em>Example: <a href="http://localhost:3000/">http://localhost:3000</a></em></li><br />
</ul></p>
<ul>
<li><strong>Use API Access Key </strong>Select this option if you want to use "API Access key" instead of login and password.</li>
<li><strong>API Access Key</strong> Provide the "API Access key" if the option above is selected.</li><br />
</ul></p>
<ul>
<li><strong>Use Login and Password </strong>&nbsp;Select this option if you want to use regular Redmine login info for authorization.</li>
<li><strong>Login</strong> Redmine login name</li>
<li><strong>Password</strong> Redmine password</li><br />
</ul></p>
<ul>
<li><strong>Project key</strong> The Project Key (String) in your Redmine you want this config to work with. Note: this is NOT a project name, which can be long and have spaces in it, etc. It is the project <strong>Key</strong>. You can find it in Redmine web URLs:<br />
<img src="http://www.taskadapter.com/wp-content/uploads/2012/05/redmine_project_key.png" alt="Redmine project Key" /><br />
or just browse "Available projects" list. Use <strong>"..." button</strong> to see available projects.<img class="alignnone size-full wp-image-139" title="select_project" src="http://www.taskadapter.com/wp-content/uploads/2012/05/select_project.png" alt="select Redmine project" width="372" height="336" /></li></p>
<li><strong><a id="query_id" name="query_id"></a>Query ID</strong> <a href="#query_id">Link</a>&nbsp;Task Adapter works with "custom queries" saved in your Redmine. Open your Redmine web page, create and save a "custom query" and check its ID using hints on this screenshot:<br />
<img src="http://www.taskadapter.com/wp-content/uploads/2012/05/where_to_find_query_id_in_redmine.png" alt="find saved query ID in Redmine" /></li></p>
<li><strong><a id="find_assignees" name="find_assignees"></a>Find users based on assignee's name</strong> <a href="#find_assignees">Link</a>&nbsp;This option can be useful when you need to export a new MSP project file to Redmine.<br />
Task Adapter can load Redmine's users by resource names specified in the MSP file and assign the new tasks to them.Here's how Task Adapter finds the proper user in Redmine:<br />
First, it assumes that the MSP resource name represents Redmine's <strong>user login name</strong>. If no Redmine user is found with such login name, then the resource name is compared to the Redmine user <strong>Full Name</strong>.<br />
So, the MSP resource name must be equal to Redmine Login or Full Name for this feature to work.<br />
Note: this operation requires <strong>'Redmine Admin' permission</strong>.</li></p>
<li><strong>Save issue relations.&nbsp;</strong>Select this option to save issues' relations ("follows/precedes") to Redmine.&nbsp;This only affects <strong>saving</strong> data to Redmine, not <strong>loading</strong> it.</li>
<li><strong>Default task type&nbsp;</strong>Tracker name (like "Bug", "Feature", "Support", "Task", ...) to use when creating new tasks. This tracker type must exist in your Redmine installation.</li><br />
</ul><br />
<a id="rest_api" name="rest_api"></a><strong>How to enable REST API in Redmine</strong></p>

**Note: "REST API" must be enabled in your Redmine for this connector to work.**

<p><img src="http://www.taskadapter.com/wp-content/uploads/2012/05/redmine_enable_rest_api.png" alt="how to enable REST API in Redmine bug tracker" /></p>
