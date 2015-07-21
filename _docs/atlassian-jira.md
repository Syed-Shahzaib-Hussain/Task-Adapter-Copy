---
layout: docs
title: JIRA configuration
permalink: /docs/atlassian-jira/
author:
  display_name: admin
  login: admin
  email: alskor@gmail.com
wordpress_id: 77
wordpress_url: http://www.taskadapter.com/wp/?page_id=77
date: '2012-05-25 00:27:34 -0700'
date_gmt: '2012-05-25 00:27:34 -0700'
---

## JIRA Integration

<div id="block-system-main">
<div id="node-37">
<p>Task Adapter can load and save data from/to JIRA using its&nbsp;<strong>"Remote API access". Please make sure this feature is enabled in your JIRA installation. </strong>Use the following menu sequence in your JIRA: Administration >> General Configuration >> Accept remote API calls.</p>
<p>Sample usage: load tasks from your JIRA&nbsp;using some saved filter and then save them to another system supported by Task Adapter, like <a href="/user-guide/microsoft-project">Microsoft Project</a> or Github.</p>
<p><a href="#general">General info<br />
</a><a href="#dialog">JIRA configuration dialog</a></p>
<p><strong><a id="general" name="general"></a>General info</strong></p>
<p>The minimum supported JIRA&nbsp;version is 5.0.</p>
<p><strong>JIRA&nbsp;configuration dialog</strong></p>
<p><a href="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_jira1.png"><img class="alignnone size-full wp-image-467" title="edit_jira" alt="" src="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_jira1.png" width="790" height="754" /></a></p>
<ul>
<li><strong>Description</strong>&nbsp;Any text to help you identify this configuration later.</li>
<li><strong>Server URL &nbsp;</strong>JIRA server URL, including propotol prefix (https or http) and port number (when using a non-standard port).<br />
Example: <em>http://my_jira_server:8080 .&nbsp;</em>It can also include the URL mapping if JIRA&nbsp;is installed NOT in the web server root, e.g.: <em>http://some_shared_server/jira</em></li></p>
<li><strong>User name &nbsp;</strong>JIRA login name.</li>
<li><strong>Password &nbsp;</strong>JIRA&nbsp;account password.</li>
<li><strong>Project Key&nbsp;</strong>The "key" of your JIRA&nbsp;project. Click "..." button to see the list of available projects in your JIRA&nbsp;installation.<a href="http://www.taskadapter.com/wp-content/uploads/2012/05/select_project.png"><img class="alignnone size-full wp-image-139" title="select_project" alt="Select Jira project" src="http://www.taskadapter.com/wp-content/uploads/2012/05/select_project.png" width="372" height="336" /></a></li>
<li><strong>Query ID &nbsp;</strong>This connector uses "search queries" saved in your JIRA&nbsp;. You need to create a "search filter" in your JIRA&nbsp;and save it.<img alt="Save Atlassian Jira filter" src="http://www.taskadapter.com/wp-content/uploads/2012/05/save_filter.png" border="1" /><br />
Unfortunately, JIRA&nbsp;remote API requires admin privileges to load list of existing filters, so Task Adapter does not perform this operation (otherwise many people wouldn't be able to use the JIRA&nbsp;Connector). Users have to lookup the ID of the new Saved Filter using the JIRA web UI. This can be improved soon, but until then please use this instruction to get the saved Filter ID:<img alt="Atlassian Jira saved filters" src="http://www.taskadapter.com/wp-content/uploads/2012/05/find_filter_id.png" border="1" />Sorry for the inconvenience.See <a href="http://confluence.atlassian.com/display/JIRA/Saving+Searches+('Issue+Filters')" target="_blank">JIRA documentation page</a> for more details on how to manage "saved filters" in JIRA.</li></p>
<li><strong>Project Component &nbsp;</strong>If this parameter is set, Task Adapter will set the "Component" field for all new tasks it creates in Jira to the specified value.This parameter is <strong>NOT used when loading data from Jira</strong>.Click "..." button to see the list of the available project components in your JIRA project.</li>
<li><strong>Set 'Affected Version' to &nbsp;</strong>If this parameter is set, Task Adapter will set the "Affected version" field for all new tasks it creates in Jira to the specified value.This parameter is <strong>NOT used when loading data from JIRA</strong>.</li>
<li><strong>Set 'Fix For Version' to &nbsp;</strong>If this parameter is set, Task Adapter will set the "Fix for version" field for all new tasks it creates in Jira to the specified value.This parameter is <strong>NOT used when loading data from JIRA</strong>.</li>
<li><strong>Custom Fields &nbsp;</strong>ID and value of custom fields, which Task Adapter needs to set for all new tasks it creates in JIRA.These 'custom fields' are <strong>NOT used when loading data from JIRA</strong>.</li>
<li><strong>Configure Priorities<br />
</strong><img class="alignnone size-full wp-image-163" title="priorities" alt="Task Adapter task priorities mapping for Atlassian Jira" src="http://www.taskadapter.com/wp-content/uploads/2012/05/priorities.png" width="400" height="276" /></li><br />
</ul>

