---
layout: docs
title: Mantis Bug Tracker integration
author:
  display_name: admin
  login: admin
wordpress_id: 101
wordpress_url: http://www.taskadapter.com/wp/?page_id=101
date: '2012-05-25 00:54:52 -0700'
date_gmt: '2012-05-25 00:54:52 -0700'
categories: []
---
<div id="main">
<div id="block-system-main">
<div id="node-39">
<div>We believe the configuration dialog for Mantis Bug Tracker is pretty self-explanatory:<br />
<a href="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_mantis1.png"><img class="alignnone size-full wp-image-486" title="edit_mantis" src="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_mantis1.png" alt="" width="388" height="480" /></a></div></p>
<div></div></p>
<div></div></p>
<div>
<p><strong>Description</strong>&nbsp;&nbsp;Any label you want to help you identify this Mantis BT config.</p>
<p><strong>Server URL</strong>&nbsp;&nbsp;Mantis BT server URL. Sample value: "http://server:8099/mantisbt-1.2.8". This must include full path, port number (if different from default 80) and the location on the server ("/mantis-1.2.8" in this example).</p>
<p><strong>Login</strong>&nbsp;&nbsp;Your Mantis BT login.</p>
<p><strong>Password</strong>&nbsp;Your Mantis BT password.</p>
<p><strong>Project key</strong>&nbsp; Project key in your Mantis BT.</p>
<p><strong>Find users based on assignee's name</strong>&nbsp;&nbsp;This option can be useful when you need to export a new Microsoft project file to Mantis BT.<br />
Task Adapter can load user names from Mantis BT using the "resource names" specified in the Microsoft Project file and assign the new tasks to them. Here&rsquo;s how Task Adapter finds the proper user in Mantis BT:<br />
First, it assumes that the MSP resource name represents the <strong>user login name</strong>. If no user is found in Mantis with such login name, then the resource name is compared to the Mantis' user&nbsp;<strong>Full Name</strong>.<br />
So, the Microsoft Project resource name must be equal to Mantis Login or Full Name for this feature to work.<br />
Note: this operation requires&nbsp;<strong>&lsquo;Mantis Admin&rsquo; permission</strong>.</p>
<p></div><br />
</div><br />
</div><br />
</div><br />
&nbsp;</p>
