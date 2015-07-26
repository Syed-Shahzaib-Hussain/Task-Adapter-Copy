---
layout: docs
title: Redmine
permalink: /docs/redmine/
---

## Redmine

* This will become a table of contents (this text will be scraped).
{:toc}

### General info

**Note: REST API must be enabled in your Redmine for this connector to work.**

<a href="#rest_api">How to enable REST API in Redmine</a>

* Task Adapter version 2.3 was tested with Redmine 2.0.3 and 2.1.0.
 **Some** features will work with the older Redmine versions 1.3.0-1.4.4, but you would need to unselect
 many fields in "Fields Mapping dialog", which old Redmine does not support (e.g. "Issue relations").
 Task Adapter **will NOT work with Redmine older than 1.3.0.**
* Can export data from Redmine to Microsoft Project (or any other connector supported by Task Adapter,
 e.g. Atlassian JIRA, ChiliProject).
* Can import data from Microsoft Project or any other Task Adapter connector to Redmine.
* Subtasks - unlimited nesting
* See <a href="#dialog">configuration dialog below</a> for the list of supported Redmine task fields.

### Performance

Tested on a regular desktop computer with Intel Core i5 CPU.

Saving 200 tasks to Redmine takes 8m:35s (515 seconds), which gives around ~0.38 task/sec.

Loading 3750 tasks takes 82 sec (~45 tasks/sec)

Save/load speed changes pretty much linearly when tasks number changes.

### Redmine configuration dialog

![Redmine configuration dialog](/images/uploads/edit_redmine4.png)

* **Description** Arbitrary text, which will be later shown in the configs list.

* **Server URL** Complete Redmine URL, including protocol prefix (https or http) and port number (when using a non-standard port).
 Example: http://myserver.mydomain.com:3000/myredmine

* **Use API Access Key** Select this option if you want to use "API Access key" instead of login and password.

* **API Access Key** Provide the "API Access key" if the option above is selected.

* **Use Login and Password ** Select this option if you want to use regular Redmine login info for authorization.

* **Login** Redmine login name

* **Password** Redmine password

* **Project key** The Project Key (String) in your Redmine you want this config to work with.
  Note: this is NOT a project name, which can be long and have spaces in it, etc.
  It is the project **Key**. You can find it in Redmine web URLs:

![Redmine project Key](/images/uploads/redmine_project_key.png)

or just browse "Available projects" list.

Use **"..." button** to see available projects.
<img src="/images/uploads/select_project.png" alt="select Redmine project"/>

* **<a id="query_id" name="query_id"></a>Query ID** <a href="#query_id">Link</a>
Task Adapter works with "custom queries" saved in your Redmine.
Open your Redmine web page, create and save a "custom query" and check its ID using hints on this screenshot:

<img src="/images/uploads/where_to_find_query_id_in_redmine.png" alt="find saved query ID in Redmine" />
* <a name="find_assignees"></a>**Find users based on assignee's name** <a href="#find_assignees">Link</a>
 This option can be useful when you need to export a new MSP project file to Redmine.

Task Adapter can load Redmine's users by resource names specified in the MSP file and assign the new tasks to them.
Here's how Task Adapter finds the proper user in Redmine:

First, it assumes that the MSP resource name represents Redmine's **user login name**.
If no Redmine user is found with such login name, then the resource name is compared to the Redmine user **Full Name**.

So, the MSP resource name must be equal to Redmine Login or Full Name for this feature to work.

Note: this operation requires **'Redmine Admin' permission**.
* **Save issue relations.** Select this option to save issues' relations ("follows/precedes") to Redmine.
 This only affects **saving** data to Redmine, not **loading** it.
* **Default task type **Tracker name (like "Bug", "Feature", "Support", "Task", ...) to use when creating new tasks.
This tracker type must exist in your Redmine installation.

### How to enable REST API in Redmine

**REST API must be enabled in your Redmine for this connector to work.**

![how to enable REST API in Redmine bug tracker](/images/uploads/redmine_enable_rest_api.png)

