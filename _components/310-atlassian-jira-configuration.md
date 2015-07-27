---
layout: docs
title: JIRA configuration
permalink: /docs/atlassian-jira-configuration/
---

* This will become a table of contents (this text will be scraped).
{:toc}

## {{ page.title }}

Task Adapter interacts with JIRA using its **Remote API access**. Please make sure this feature is
enabled in your JIRA installation.

Use the following menu sequence in your JIRA: Administration >> General Configuration >> Accept remote API calls.

Sample usage: load tasks from your JIRA using some saved filter and then save them to another system supported by
 Task Adapter, like <a href="/docs/microsoft-project">Microsoft Project</a> or Github.


The minimum supported JIRA version is 5.0.

## JIRA configuration dialog

![Edit JIRA](/images/uploads/edit_jira1.png)

* **Description** Any text to help you identify this configuration later.
* **Server URL** JIRA server URL, including propotol prefix (https or http) and port number (when using a non-standard port).

Example: http://my_jira_server:8080 . It can also include the URL mapping if JIRA is installed NOT in the web server root, e.g.: http://some_shared_server/jira

* **User name** JIRA login name.
* **Password** JIRA account password.
* **Project Key** The "key" of your JIRA project. Click "..." button to see the list of available projects
  in your JIRA installation.
  ![Select JIRA project](/images/uploads/select_project.png)

* **Query ID** This connector uses "search queries" saved in your JIRA .
 You need to create a "search filter" in your JIRA and save it. <img alt="Save Atlassian JIRA filter" src="/images/uploads/save_filter.png" border="1" />

JIRA remote API requires admin privileges to load list of existing filters, so Task Adapter does not perform this
operation (otherwise many people wouldn't be able to use the JIRA Connector).
Users have to lookup the ID of the new Saved Filter using the JIRA web UI. This can be improved soon, but until then
 please use this instruction to get the saved Filter ID:

<img alt="Atlassian JIRA saved filters" src="/images/uploads/find_filter_id.png" border="1" />

See <a href="http://confluence.atlassian.com/display/JIRA/Saving+Searches+('Issue+Filters')" target="_blank">JIRA documentation page</a> for more details on how to manage "saved filters" in JIRA.

* **Project Component** If this parameter is set, Task Adapter will set the "Component" field for all new tasks
 it creates in JIRA to the specified value. This parameter is **NOT used when loading data from JIRA**.
 Click "..." button to see the list of the available project components in your JIRA project.
* **Set 'Affected Version' to** If this parameter is set, Task Adapter will set the "Affected version" field
 for all new tasks it creates in JIRA to the specified value. This parameter is **NOT used when loading data from JIRA**.
* **Set 'Fix For Version' to** If this parameter is set, Task Adapter will set the "Fix for version" field for
 all new tasks it creates in JIRA to the specified value. This parameter is **NOT used when loading data from JIRA**.
* **Custom Fields** ID and value of custom fields, which Task Adapter needs to set for all new tasks it creates in JIRA.
 These 'custom fields' are **NOT used when loading data from JIRA**.
* **Configure Priorities**

![Task Adapter task priorities mapping for Atlassian JIRA](/images/uploads/priorities.png)

