## Supported systems

*   **[JIRA](/docs/atlassian-jira)**
*   **[JIRA OnDemand](/docs/atlassian-jira)**
*   **[Redmine](/docs/redmine)**
*   **[Basecamp](/docs/basecamp)**
*   **[Basecamp Classic](/docs/basecamp)**
*   **[GitHub](/docs/github)**
*   **[MantisBT](/docs/mantisbt)**
*   **[Microsoft Project](/docs/microsoft-project/)**

For example, you can transfer tasks between:

*   Redmine and Microsoft Project
*   JIRA and Microsoft Project
*   Redmine and JIRA
*   Transfer data between two Redmine servers
*   etc

## Supported modes.

*   Between bug trackers - **create** new tasks only.
*   Between Microsoft Project and a web-based bug tracker (like Redmine, JIRA, etc) - both **create** and **update**.
 See this [detailed page explaining how to update existing tasks in your bug tracker](/docs/how-to-update-tasks-in-redmine-jira/)
  (Redmine / JIRA / what have you).


## What data can Task Adapter transfer?

This varies from system to system (e.g. list of task fields supported for Redmine bug tracker is different
from the one for Microsoft Project or JIRA). These are the basic task fields supported for most systems:

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
