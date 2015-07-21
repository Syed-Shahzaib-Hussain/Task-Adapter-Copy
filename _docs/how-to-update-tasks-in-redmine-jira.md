---
layout: docs
title: How to update tasks in Redmine / JIRA
author:
  display_name: admin
---

## Use-case:

You have a Microsoft Project XML&nbsp;file that you want to export to your bug tracker (like Redmine or JIRA). After this you want to make some changes in the project file and send updates to the bug tracker rather than creating a bunch of almost-duplicated tasks.</p>

## Steps:

Open the sync config page.&nbsp;In Task Fields Mapping section there is "Id" field:</p>
<p><img src="https://ci4.googleusercontent.com/proxy/jHPWJRvnL8a08Nac3zgyuZVHnmNXdlNFhy5SGdZt4ScEA9_u37w76wwq-0rVVKSJpxVNQWb5NgD6hrcBywHn7P7mcv8_R8wrjZH6InH_dvUgd6jiwih3iGaMgA=s0-d-e1-ft#http://www.taskadapter.com/wp-content/uploads/2012/05/id_selected.png" alt="" /></p>
<div>Select this field before you start your first export from MSP to Redmine / JIRA. You can leave the default "TEXT22" value unchanged.</div></p>
<div>Start the export.</div></p>
<div>TaskAdapter will create tasks in the target system and then save the newly created task IDs (like "123" for Redmine or "MYPROJECT-123" for JIRA) in the specified custom field (&ldquo;TEXT22&Prime; in this example) in the Microsoft Project XML file.</div></p>
<div>You can then open this XML file in Microsoft Project again, make some changes, then export as XML. Say, you put it into the same location already known to TaskAdapter. Then next time you perform export from this file to Redmine / JIRA, the tasks that were previously created will be updated rather than duplicated and the ones that are new will be created.</div></p>
<div></div></p>

## How to see custom fields in Microsoft Project.

<div>These custom fields (like Text22) are not shown in Microsoft Project by default, but you can view them by clicking on "Add New column" header and selecting a field you want:</div></p>
<div></div></p>
<div><a href="http://www.taskadapter.com/wp-content/uploads/2015/07/add_column.png"><img class="alignnone size-full wp-image-759" src="http://www.taskadapter.com/wp-content/uploads/2015/07/add_column.png" alt="add_column" width="718" height="112" /></a></div></p>
<div></div></p>
<div>Start typing "Text" to filter out other fields and see all custom ones:</div></p>
<div></div></p>
<div><a href="http://www.taskadapter.com/wp-content/uploads/2015/07/fields.png"><img class="alignnone size-full wp-image-760" src="http://www.taskadapter.com/wp-content/uploads/2015/07/fields.png" alt="fields" width="842" height="155" /></a></div></p>
<div></div></p>
<div>You can see that before the first export from this Microsoft Project XML file Text22 field is empty:</div></p>
<div><a href="http://www.taskadapter.com/wp-content/uploads/2015/07/empty.png"><img class="alignnone size-full wp-image-761" src="http://www.taskadapter.com/wp-content/uploads/2015/07/empty.png" alt="empty" width="726" height="83" /></a></div></p>
<div></div></p>
<div>But once you export data to Redmine or JIRA (or any other system TaskAdapter supports), you can reopen the XML file in Microsoft Project and see that Text22 field contains the IDs produced by the target system (Redmine in this case):</div></p>
<div></div></p>
<div><a href="http://www.taskadapter.com/wp-content/uploads/2015/07/filled.png"><img class="alignnone size-full wp-image-762" src="http://www.taskadapter.com/wp-content/uploads/2015/07/filled.png" alt="filled" width="739" height="85" /></a></div></p>
<div></div></p>
<div></div></p>
<div>This is how TaskAdapter knows that these tasks were previously exported to the target system and it can update them rather than re-create next time you perform export from your XML file to Redmine / JIRA.</div></p>
<div></div></p>
<div>You can see the newly created tasks in Redmine web UI:</div></p>
<div><a href="http://www.taskadapter.com/wp-content/uploads/2015/07/redmine_tasks.jpg"><img class="alignnone size-full wp-image-764" src="http://www.taskadapter.com/wp-content/uploads/2015/07/redmine_tasks.jpg" alt="redmine_tasks" width="652" height="114" /></a></div></p>
<div></div></p>
<div>Here are sample IDs produced by JIRA:</div></p>
<div><a href="http://www.taskadapter.com/wp-content/uploads/2015/07/jira_ids.png"><img class="alignnone size-full wp-image-763" src="http://www.taskadapter.com/wp-content/uploads/2015/07/jira_ids.png" alt="jira_ids" width="742" height="83" /></a></div></p>
<div></div></p>
<div>And here is how these tasks look in JIRA web UI:</div></p>
<div><a href="http://www.taskadapter.com/wp-content/uploads/2015/07/jira_tasks.jpg"><img class="alignnone size-full wp-image-765" src="http://www.taskadapter.com/wp-content/uploads/2015/07/jira_tasks.jpg" alt="jira_tasks" width="771" height="261" /></a></div></p>
<div></div></p>
