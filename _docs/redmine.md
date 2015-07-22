---
layout: docs
title: Redmine
author:
  display_name: admin
---

**Note: "REST API" must be enabled in your Redmine for this connector to work.**
<a href="#rest_api">How to enable REST API in Redmine</a>

<p><a href="#general">General info

</a><a href="#performance">Performance

</a><a href="#dialog">Configuration dialog</a></p>
<p><a id="general" name="general"></a>**General info **</p>
<ul>
<li>Task Adapter version 2.3 was tested with Redmine 2.0.3 and 2.1.0. **Some** features will work with the older Redmine versions 1.3.0-1.4.4, but you would need to unselect many of the fields in "Fields Mapping dialog", which the old Redmine does not support (e.g. "Issue relations"). Task Adapter **will NOT work with Redmine older than 1.3.0.**</li>
<li>Can export data from Redmine to Microsoft Project (or any other connector supported by Task Adapter, e.g. Atlassian JIRA, ChiliProject).</li>
<li>Can import data from Microsoft Project or any other Task Adapter connector to Redmine.</li>
<li>Subtasks - unlimited nesting</li>
<li>See <a href="#dialog">configuration dialog below</a> for the list of supported Redmine task fields.</li>

</ul>

**<a id="performance" name="performance"></a>Performance**</p>
<p>Saving 200 tasks to Redmine takes 8m:35s (515 seconds), which gives around ~0.38 task/sec.

Loading 3750 tasks takes 82 sec (~45 tasks/sec)

Save/load speed changes pretty much linearly when tasks number changes.</p>
<p><a id="dialog" name="dialog"></a>**Redmine configuration dialog**</p>
<p><a href="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_redmine4.png"><img class="alignnone size-full wp-image-465" title="edit_redmine" src="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_redmine4.png"  width="792" height="518" /></a></p>
<ul>
<li>**Description** Arbitrary text, which will be later shown in the configs list.</li>
<li>**Server URL** Complete Redmine URL, including protocol prefix (https or http) and port number (when using a non-standard port).

<em>Example: <a href="http://localhost:3000/">http://localhost:3000</a></em></li>

</ul></p>
<ul>
<li>**Use API Access Key **Select this option if you want to use "API Access key" instead of login and password.</li>
<li>**API Access Key** Provide the "API Access key" if the option above is selected.</li>

</ul></p>
<ul>
<li>**Use Login and Password ** Select this option if you want to use regular Redmine login info for authorization.</li>
<li>**Login** Redmine login name</li>
<li>**Password** Redmine password</li>

</ul></p>
<ul>
<li>**Project key** The Project Key (String) in your Redmine you want this config to work with. Note: this is NOT a project name, which can be long and have spaces in it, etc. It is the project **Key**. You can find it in Redmine web URLs:

<img src="http://www.taskadapter.com/wp-content/uploads/2012/05/redmine_project_key.png" alt="Redmine project Key" />

or just browse "Available projects" list. Use **"..." button** to see available projects.<img class="alignnone size-full wp-image-139" title="select_project" src="http://www.taskadapter.com/wp-content/uploads/2012/05/select_project.png" alt="select Redmine project" width="372" height="336" /></li></p>
<li>**<a id="query_id" name="query_id"></a>Query ID** <a href="#query_id">Link</a> Task Adapter works with "custom queries" saved in your Redmine. Open your Redmine web page, create and save a "custom query" and check its ID using hints on this screenshot:

<img src="http://www.taskadapter.com/wp-content/uploads/2012/05/where_to_find_query_id_in_redmine.png" alt="find saved query ID in Redmine" /></li></p>
<li>**<a id="find_assignees" name="find_assignees"></a>Find users based on assignee's name** <a href="#find_assignees">Link</a> This option can be useful when you need to export a new MSP project file to Redmine.

Task Adapter can load Redmine's users by resource names specified in the MSP file and assign the new tasks to them.Here's how Task Adapter finds the proper user in Redmine:

First, it assumes that the MSP resource name represents Redmine's **user login name**. If no Redmine user is found with such login name, then the resource name is compared to the Redmine user **Full Name**.

So, the MSP resource name must be equal to Redmine Login or Full Name for this feature to work.

Note: this operation requires **'Redmine Admin' permission**.</li></p>
<li>**Save issue relations. **Select this option to save issues' relations ("follows/precedes") to Redmine. This only affects **saving** data to Redmine, not **loading** it.</li>
<li>**Default task type **Tracker name (like "Bug", "Feature", "Support", "Task", ...) to use when creating new tasks. This tracker type must exist in your Redmine installation.</li>

</ul>

<a id="rest_api" name="rest_api"></a>**How to enable REST API in Redmine**</p>

**Note: "REST API" must be enabled in your Redmine for this connector to work.**

<img src="http://www.taskadapter.com/wp-content/uploads/2012/05/redmine_enable_rest_api.png" alt="how to enable REST API in Redmine bug tracker" />
