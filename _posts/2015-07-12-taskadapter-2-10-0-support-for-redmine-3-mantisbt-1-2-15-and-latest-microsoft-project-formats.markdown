---
layout: post
status: publish
published: true
title: 'TaskAdapter 2.10.0: Support for Redmine 3, MantisBT 1.2.15 and latest Microsoft
  Project formats'
author:
  display_name: admin
  login: admin
  email: alskor@gmail.com
  url: ''
author_login: admin
author_email: alskor@gmail.com
wordpress_id: 773
wordpress_url: http://www.taskadapter.com/?p=773
date: '2015-07-12 17:40:54 -0700'
date_gmt: '2015-07-12 17:40:54 -0700'
categories:
- redmine
- redmine java api
- release
- microsoft project
- mantisbt
tags: []

---
Good news, everyone! Big changes in TaskAdapter 2.10.0:

### Support for Redmine 3.0.x.  
 Redmine 3.0.x introduced new dates format that previous TaskAdapter versions could not parse. This required us releasing a new version of Redmine Java API libarary and integrating it into TaskAdapter. Enjoy Redmine 3.0.x integration!

### Support for MantisBT 1.2.15.  
 TaskAdapter was already tested to work with MantisBT previously, and now it is using the latest MantisBT native integration library, which should bring more stability.

Also, a bug was fixed where tasks created in MantisBT could not be updated by TaskAdapter later.

### Better support for latest Microsoft Project formats.  
 Microsoft Project 2010, Microsoft Project 2013 and Microsoft Project 2016\. This version will include multiple bugfixes and improvements to make reading and writing these files more reliable.

### Some GUI bugfixes.  
 A newer version of the UI library is used, which resolves some minor UI bugs.

### Better logging.  
 When something goes wrong, TaskAdapter will now provide more user-friendly messages in the output (both UI and console log).