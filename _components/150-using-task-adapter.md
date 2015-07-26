---
layout: docs
title: Using Task Adapter
permalink: /docs/using-task-adapter/
---

## Using Task Adapter

* This will become a table of contents (this text will be scraped).
{:toc}

### Create a config

* To export tasks from a bug tracker like Atlassian JIRA and a Microsoft Project file,
you first need to create a "synchronization config",  which will keep settings like your JIRA server URL, login,
 password, your Microsoft Project file location, etc.

Use "New Config" button on the main application page to create a new config.

<img title="create_new_config" src="/images/uploads/create_new_config.png"/>

* Select two systems (e.g. Atlassian JIRA and Microsoft Project).
These will be the systems this "config"  transfers data between.
You can also provide a description. As you see, the headers don't say "Source" and "Destination,
but rather "System 1" and "System 2". This is to indicate that you can transfer both ways, so it does not matter
if you select JIRA on the left and Microsoft Project on the right, or the other way around.
* Once you click "Create" button, the new config file is created in your data directory (<User Home>/taskadapter folder).


### Configure.

* Once you create a config, you get "Edit Config" page. Here is what you will see for an Atlassian JIRA and Microsoft Project config:

![Edit Task Adapter config for Atlassian JIRA and Microsoft Project](/images/uploads/default_jira_msp.png)

* This page has two buttons to edit systems' settings, two "start export" buttons and a "Fields mapping" panel.
* Click the big blue buttons to configure Atlassian JIRA or Microsoft Project:

![Edit JIRA configuration Button](/images/uploads/edit_jira_button1.png)
![Edit Microsoft Project configuration Button](/images/uploads/edit_msp_button.png)

* Select task fields you want to export. You can change default "mapping" for some of them.
E.g. JIRA's "Due Date" field can be saved into "Finish" or "Deadline" field in a Microsoft Project file.
See Microsoft Project configuration page for more details.

### Export data.

* Click arrow-buttons to start data export to the  left or right system:

<img src="/images/uploads/export_left_right.png"/>

Data will be loaded from the source system and a confirmation dialog will be shown:<img src="/images/uploads/export_confirmation.png"/>
* You can change the fields mappings before the export.

Only the selected fields will be transferred to the destination system.

<img src="/images/uploads/confirm_fields_mapping1.png"/>
* The transfer result is shown on the next page with the number of tasks created or updated.


### Update Microsoft Project File

You can update a Microsoft Project XML file with the data from an external system (Redmine/JIRA/MantisBT/...).

* Either you want to export data from a Microsoft Project file to an external system OR Load data
from an external system into the MSP XML file - **In either case select "Id" field before the "save data" operation.**

![ID selected](/images/uploads/id_selected.png)

The task IDs provided by the external system will be saved in the specified field ("TEXT22" in this example)
in the Microsoft Project XML file.

* Use "Only update tasks present in the file" button:

![choose_file_operation](/images/uploads/choose_file_operation.png)

Only the tasks which have "remote IDs" field set in the MSP file will be updated.

* The selected tasks will be re-loaded from the external system (JIRA in this example) and updated in the MSP XML file.
 The other tasks in the XML file will be left unchanged.
