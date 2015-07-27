---
layout: docs
title: How to update tasks in Redmine / JIRA
permalink: /docs/how-to-update-tasks-in-redmine-jira/
---

## Use-case:

You have a Microsoft Project XML file that you want to export to your bug tracker (like Redmine or JIRA).
After this you want to make some changes in the project file and send updates to the bug tracker rather
than creating a bunch of almost-duplicated tasks.

## Steps:

Open the sync config page. In Task Fields Mapping section there is "Id" field:
![Task Fields mapping panel with ID field selected](/images/uploads/id_selected.png)

Select this field before you start your first export from MSP to Redmine / JIRA.
You can leave the default "TEXT22" value unchanged.

Start the export.
TaskAdapter will create tasks in the target system and then save the newly created task IDs
(like "123" for Redmine or "MYPROJECT-123" for JIRA) in the specified custom field ("TEXT22" in this example)
in the Microsoft Project XML file.
You can then open this XML file in Microsoft Project again, make some changes, then export as XML.
Say, you put it into the same location already known to TaskAdapter.
Then next time you perform export from this file to Redmine / JIRA, the tasks that were previously created
will be updated rather than duplicated and the ones that are new will be created.


## How to see custom fields in Microsoft Project.

These custom fields (like Text22) are not shown in Microsoft Project by default,
 but you can view them by clicking on "Add New column" header and selecting a field you want:

![Add Column](/images/uploads/add_column.png)


Start typing "Text" to filter out other fields and see all custom ones:


![Fields](/images/uploads/fields.png)

You can see that before the first export from this Microsoft Project XML file Text22 field is empty:
![Empty field](/images/uploads/empty.png)

But once you export data to Redmine or JIRA (or any other system TaskAdapter supports),
you can reopen the XML file in Microsoft Project and see that Text22 field contains the IDs produced
 by the target system (Redmine in this case):

![Microsoft Project Table cells TEXT22 field filled with remote IDs from Redmine](/images/uploads/filled.png)

This is how TaskAdapter knows that these tasks were previously exported to the target system and it can update
 them rather than re-create next time you perform export from your XML file to Redmine / JIRA.

You can see the newly created tasks in Redmine web UI:

![Redmine tasks](/images/uploads/redmine_tasks.jpg)

Here are sample IDs produced by JIRA:

![JIRA ids in Microsoft Project text field TEXT 22](/images/uploads/jira_ids.png)

And here is how these tasks look in JIRA web UI:
![JIRA tasks](/images/uploads/jira_tasks.jpg)

