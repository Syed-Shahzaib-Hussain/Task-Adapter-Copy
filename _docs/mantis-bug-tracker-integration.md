---
layout: docs
title: Mantis Bug Tracker integration
permalink: /docs/mantis-bug-tracker-integration/
author:
  display_name: admin
---

# Configure Task Adapter for MantisBT

The configuration dialog for MantisBT (Mantis Bug Tracker) should be pretty self-explanatory:

<a href="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_mantis1.png"><img class="alignnone size-full wp-image-486" title="edit_mantis" src="http://www.taskadapter.com/wp-content/uploads/2012/05/edit_mantis1.png" alt="" width="388" height="480" /></a>

* **Description** - Any label you want to help you identify this MantisBT config.
* **Server URL** - MantisBT server URL. Sample value: "http://server:8099/mantisbt-1.2.8". This must include full path, port number (if different from default 80) and the location on the server ("/mantis-1.2.8" in this example).
* **Login** - Your MantisBT login.
* **Password** - Your MantisBT password.
* **Project key** - Project key in your MantisBT.
* **Find users based on assignee's name** - This option can be useful when you need to export a new Microsoft project file to MantisBT.
Task Adapter can load user names from MantisBT using the "resource names" specified in the Microsoft Project file and assign the new tasks to them. Here&rsquo;s how Task Adapter finds the proper user in MantisBT:

First, it assumes that the MSP resource name represents the **user login name**. If no user is found in Mantis with such login name, then the resource name is compared to the Mantis' user **Full Name**.

So, the Microsoft Project resource name must be equal to Mantis Login or Full Name for this feature to work.
Note: this operation requires **Mantis Admin** permission.

