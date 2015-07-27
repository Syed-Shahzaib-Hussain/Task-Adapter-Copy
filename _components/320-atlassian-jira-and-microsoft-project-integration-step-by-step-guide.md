---
layout: docs
title: JIRA and Microsoft Project integration - step by step guide
permalink: /docs/atlassian-jira/atlassian-jira-and-microsoft-project-integration-step-by-step-guide/
---

## User story: "I have a Microsoft Project plan and I want to export the tasks to my JIRA".

First, [install and start Task Adapter](/docs/installation). Then follow these steps:

* [Create a config](/docs/using-task-adapter/#create_config_file)
* [Configure](/docs/using-task-adapter/#configure)
* [Export tasks](/docs/using-task-adapter/#export_data)
* Optional - [Update Microsoft Project File](/docs/using-task-adapter/#update_msp_file)

## <a name="create_config_file"></a>Create a config

To export tasks from a bug tracker like JIRA or a Microsoft Project file, you first need to create a "synchronization config"
 which will keep settings like your JIRA server URL, login, password, your Microsoft Project file location, etc.

Use "New Config" button on the main application page to create a new config.

![Create config](/images/uploads/create_new_config.png)

Select two systems (Atlassian JIRA and Microsoft Project in this example).
You can also provide a description. As you see, the headers don&rsquo;t say "Source" and "Destination,
but rather "System 1" and "System 2".
This is to indicate that you can transfer both ways, so it does not matter if you select JIRA on the left
and Microsoft Project on the right, or the other way around.
Once you click "Create" button, the new config file is created in your data directory (<User Home>/taskadapter folder).


## Configure.

Here is what you will see for a new Atlassian JIRA and Microsoft Project config:

![Edit config for Atlassian JIRA and Microsoft Project](/images/uploads/default_jira_msp.png)

This page has two buttons to edit settings, two "start export" buttons and a "Fields mapping" panel.

Click the big blue buttons to configure Atlassian JIRA or Microsoft Project:

![Edit JIRA](/images/uploads/edit_jira_button1.png)
![Edit Microsoft Project](/images/uploads/edit_msp_button.png)

Configure Atlassian JIRA settings, like JIRA server URL, your JIRA login name and password.

![Edit Atlassian JIRA settings](/images/uploads/edit_jira1.png)

Here's the [complete description of the JIRA configuration dialog](/docs/atlassian-jira).

Close the JIRA configuration panel.
Now click "Microsoft Project" button to open the project settings. Provide the file location -

![Edit Microsoft Project settings in Task Adapter local mode](/images/uploads/edit_msp_local.png)

(This is the panel you see when you run Task Adapter in "local" mode. The server mode has a bit different one.)

Now close the Microsoft Project panel.
You're back to "Edit Config" screen. Select task fields you want to export.

You can change default mapping for some of them. E.g. JIRA's "Due Date" field can be saved into
"Finish" or "Deadline" field in a Microsoft Project file. See Microsoft Project configuration page for more details.

![Edit config for Atlassian JIRA and Microsoft Project]("/images/uploads/default_jira_msp.png)

## <a name="export_data"></a>Export tasks.

Click arrow-buttons to start export to the  left or right system:
![Export left right](/images/uploads/export_left_right.png)

A confirmation dialog is shown when the tasks are loaded from the source system:

![Export confirmation](/images/uploads/export_confirmation.png)

You can change the fields mappings before the export.  Only the selected fields will be transferred to the destination system.

![Confirm Fields Mapping](/images/uploads/confirm_fields_mapping1.png)

The transfer result is shown on the next page with the number of tasks created or updated.


Open your JIRA web page in the browser to see the new tasks:
<img src="/images/uploads/jira_web_ui.png" />

## <a id="update_msp_file" name="update_msp_file"></a>Update MSP File

[Link to this page](/docs/using-task-adapter/#update_msp_file)

You can update a Microsoft Project XML file with the data from an external system (Redmine/JIRA/MantisBT).

Either you want to export data from a Microsoft Project file to an external system OR Load data from an external
 system into the MSP XML file  - **In either case select "Id" field before the "save data" operation.**
 <img title="id_selected"  src="/images/uploads/id_selected.png"/>
 The task IDs provided by the external system will be saved in the specified field
 ("TEXT22" in this example) in the Microsoft Project XML file.

Use "Only update tasks present in the file" button:

![Choose File Operation](/images/uploads/choose_file_operation.png)

Only the tasks which have "remote IDs" field set in the MSP file will be updated.
The selected tasks will be re-loaded from the external system (JIRA in this example) and updated in the MSP XML file.
 The other tasks in the XML file will be left unchanged.

</ol>

