Task Adapter transfers tasks between Redmine, ChiliProject, JIRA, Microsoft Project (XML files) and other bug tracking / task management systems. You can transfer data between any two systems from the list below:

## Supported systems

*   **Basecamp** - Supported, but no User Guide page yet.
*   **Basecamp Classic** - Supported, but no User Guide page yet.
*   **[GitHub](/github)**
*   **[MantisBT](user-guide/mantis-bug-tracker-integration)**
*   **[Microsoft Project](/microsoft-project-integration/)**
*   **[JIRA](/atlassian-jira)**
*   **[JIRA OnDemand](/atlassian-jira)**
*   **[Redmine](user-guide/redmine)**

For example, you can transfer tasks between:

*   Redmine and Microsoft Project
*   JIRA and Microsoft Project
*   Redmine and JIRA
*   Transfer data between two Redmine servers
*   etc

## Supported modes.

*   Between bug trackers - **create** new tasks only.
*   Between Microsoft Project and a web-based bug tracker (like Redmine, JIRA, etc) - both **create** and **update**. See this [detailed page explaining how to update existing tasks in your bug tracker](http://www.taskadapter.com/user-guide/using-task-adapter/how-to-update-tasks-in-redmine-jira/) (Redmine / JIRA / what have you).


## What data can Task Adapter transfer?

This varies from system to system (e.g. list of task fields supported for Redmine bug tracker is different from the one for Microsoft Project or JIRA). These are the basic task fields supported for most systems:

*   Task Summary
*   Task description
*   Percent complete
*   Time estimate (hours)
*   Assignee name (can require admin permissions for some systems)
*   Task Status (new, assigned, in progress, closed, etc.)
*   Task Type (bug, feature, task, etc)
*   Relations between tasks (e.g. "task 1 precedes task 2") - this is currently supported for Redmine and Microsoft Project only.
*   Task Due Date ("finish date" or "estimated finish date")
*   Task Start Date
*   Priority (High, Normal, Low, etc).

[Compare Task Adapter with other systems.](/compare-task-adapter-with-other-systems)