---
layout: docs
title: Using Task Adapter
permalink: /docs/using-task-adapter/
---

## Using Task Adapter

* <a href="#create_config_file">Create a config</a>
* <a href="#configure">Configure</a>
* <a href="#export_data">Export Data</a>
* <a href="#update_msp_file">Update MSP File</a>

## <a name="create_config_file"></a>Create a config

* To export tasks from a bug tracker like Atlassian JIRA and a Microsoft Project file,
you first need to create a "synchronization config",  which will keep settings like your JIRA server URL, login,
 password, your Microsoft Project file location, etc.

Use "New Config" button on the main application page to create a new config.

<a href="/images/uploads/create_new_config.png"><img class="alignnone size-full wp-image-452" title="create_new_config" src="/images/uploads/create_new_config.png"  width="298" height="286" /></a></p>
* Select two systems (e.g. Atlassian JIRA and Microsoft Project). These will be the systems this "config"  transfers data between. You can also provide a description. As you see, the headers don't say "Source" and "Destination, but rather "System 1" and "System 2". This is to indicate that you can transfer both ways, so it does not matter if you select JIRA on the left and Microsoft Project on the right, or the other way around.
* Once you click "Create" button, the new config file is created in your data directory (<User Home>/taskadapter folder).


## <a name="configure"></a>Configure.

* Once you create a config, you get "Edit Config" page. Here is what you will see for an Atlassian JIRA and Microsoft Project config:

<a href="/images/uploads/default_jira_msp.png"><img class="alignnone size-full wp-image-451" title=""Edit config" for Atlassian JIRA and Microsoft Project" src="/images/uploads/default_jira_msp.png" Edit config" for Atlassian JIRA and Microsoft Project" width="768" height="430" /></a></p>

* This page has two buttons to edit systems' settings, two "start export" buttons and a "Fields mapping" panel.
* Click the big blue buttons to configure Atlassian JIRA or Microsoft Project:

<img class="alignnone size-full wp-image-455" title="edit_jira_button" src="/images/uploads/edit_jira_button1.png"  width="298" height="40" />  <img class="alignnone size-full wp-image-454" title="edit_msp_button" src="/images/uploads/edit_msp_button.png"  width="296" height="40" /></p>
* Select task fields you want to export. You can change default "mapping" for some of them. E.g. JIRA's "Due Date" field can be saved into "Finish" or "Deadline" field in a Microsoft Project file. See Microsoft Project configuration page for more details.

## <a name="export_data"></a>Export data.

* Click arrow-buttons to start data export to the  left or right system:

<img src="/images/uploads/export_left_right.png"/>

Data will be loaded from the source system and a confirmation dialog will be shown:<img class="alignnone size-full wp-image-152" title="export_confirmation" src="/images/uploads/export_confirmation.png"  width="422" height="362" /></p>
* You can change the fields mappings before the export.

Only the selected fields will be transferred to the destination system.

<img src="/images/uploads/confirm_fields_mapping1.png"/>
* The transfer result is shown on the next page with the number of tasks created or updated.


## <a id="update_msp_file" name="update_msp_file"></a>Update MSP File

<a href="#update_msp_file">Link to this page</a></p>

You can update a Microsoft Project XML file with the data from an external system (Redmine/JIRA/MantisBT/...).

* Either you want to export data from a Microsoft Project file to an external system OR Load data
from an external system into the MSP XML file - **In either case select "Id" field before the "save data" operation.**

![ID selected](/images/uploads/id_selected.png)

The task IDs provided by the external system will be saved in the specified field ("TEXT22" in this example) in the Microsoft Project XML file.

* Use "Only update tasks present in the file" button:

![choose_file_operation](/images/uploads/choose_file_operation.png)

Only the tasks which have "remote IDs" field set in the MSP file will be updated.

* The selected tasks will be re-loaded from the external system (JIRA in this example) and updated in the MSP XML file. The other tasks in the XML file will be left unchanged.
