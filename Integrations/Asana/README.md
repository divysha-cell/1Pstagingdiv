
# Asana

Asana is a software-as-a-service designed to improve team collaboration and work management. It helps teams manage projects and tasks in one tool. Teams can create projects, assign work to teammates, specify deadlines, and communicate about tasks directly in Asana.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Token|The personal access token|True|Password|*****|
|Base URL|Base URL|True|String|https://app.asana.com/api/1.0|


#### Dependencies
| |
|-|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|urllib3-2.5.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Get Task
Retrieves the task details
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Task ID|The task ID can be found in the URL:https://app.asana.com/0/{your_project_ID}/{your_task_ID}|True|String|<Task-Id>|



##### JSON Results
```json
{"data": {"gid": "12345", "resource_type": "task", "name": "Buy catnip", "approval_status": "pending", "assignee_status": "upcoming", "completed": false, "completed_at": "2012-02-22T02:06:58.147Z", "completed_by": {"gid": "12345", "resource_type": "user", "name": "Greg Sanchez"}, "created_at": "2012-02-22T02:06:58.147Z", "dependencies": [{"gid": "12345", "resource_type": "task"}], "dependents": [{"gid": "12345", "resource_type": "task"}], "due_at": "2019-09-15T02:06:58.147Z", "due_on": "2019-09-15", "external": {"data": "A blob of information", "gid": "my_gid"}, "hearted": true, "hearts": [{"gid": "12345", "user": {"gid": "12345", "resource_type": "user", "name": "Greg Sanchez"}}], "html_notes": "<body>Mittens <em>really</em> likes the stuff from Humboldt.</body>", "is_rendered_as_separator": false, "liked": true, "likes": [{"gid": "12345", "user": {"gid": "12345", "resource_type": "user", "name": "Greg Sanchez"}}], "memberships": [{"project": {"gid": "12345", "resource_type": "project", "name": "Stuff to buy"}, "section": {"gid": "12345", "resource_type": "section", "name": "Next Actions"}}], "modified_at": "2012-02-22T02:06:58.147Z", "notes": "Mittens really likes the stuff from Humboldt.", "num_hearts": 5, "num_likes": 5, "num_subtasks": 3, "resource_subtype": "default_task", "start_on": "2019-09-14", "assignee": {"gid": "12345", "resource_type": "user", "name": "Greg Sanchez"}, "custom_fields": [{"gid": "12345", "resource_type": "custom_field", "currency_code": "EUR", "custom_label": "gold pieces", "custom_label_position": "suffix", "description": "Development team priority", "enabled": true, "enum_options": [{"gid": "12345", "resource_type": "enum_option", "color": "blue", "enabled": true, "name": "Low"}], "enum_value": {"gid": "12345", "resource_type": "enum_option", "color": "blue", "enabled": true, "name": "Low"}, "format": "custom", "has_notifications_enabled": true, "is_global_to_workspace": true, "name": "Status", "number_value": 5.2, "precision": 2, "resource_subtype": "text", "text_value": "Some Value", "type": "text"}], "followers": [{"gid": "12345", "resource_type": "user", "name": "Greg Sanchez"}], "parent": {"gid": "12345", "resource_type": "task", "name": "Bug Task"}, "permalink_url": "https://app.asana.com/0/resource/123456789/list", "projects": [{"gid": "12345", "resource_type": "project", "name": "Stuff to buy"}], "tags": [{"gid": "59746", "name": "Grade A"}], "workspace": {"gid": "12345", "resource_type": "workspace", "name": "My Company Workspace"}}}
```



#### Update Task
Updates a given task in Asana
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Task ID|The task ID can be found in the URL:https://app.asana.com/0/{your_project_ID}/{your_task_ID}|True|String|<Task-Id>|
|Due Date|The due date is in the format YYYY-MM-DD|False|String|2020-10-08|
|Description|The task description|False|String|Your new description for this task|
|Assignee|The user's email of the person you would like to re-assign the task to. Note: This is case sensitive|False|String|email@gmail.com|



##### JSON Results
```json
{"data": {"gid": "12345", "resource_type": "task", "name": "Buy catnip", "approval_status": "pending", "assignee_status": "upcoming", "completed": false, "completed_at": "2012-02-22T02:06:58.147Z", "completed_by": {"gid": "12345", "resource_type": "user", "name": "Greg Sanchez"}, "created_at": "2012-02-22T02:06:58.147Z", "dependencies": [{"gid": "12345", "resource_type": "task"}], "dependents": [{"gid": "12345", "resource_type": "task"}], "due_at": "2019-09-15T02:06:58.147Z", "due_on": "2019-09-15", "external": {"data": "A blob of information", "gid": "my_gid"}, "hearted": true, "hearts": [{"gid": "12345", "user": {"gid": "12345", "resource_type": "user", "name": "Greg Sanchez"}}], "html_notes": "<body>Mittens <em>really</em> likes the stuff from Humboldt.</body>", "is_rendered_as_separator": false, "liked": true, "likes": [{"gid": "12345", "user": {"gid": "12345", "resource_type": "user", "name": "Greg Sanchez"}}], "memberships": [{"project": {"gid": "12345", "resource_type": "project", "name": "Stuff to buy"}, "section": {"gid": "12345", "resource_type": "section", "name": "Next Actions"}}], "modified_at": "2012-02-22T02:06:58.147Z", "notes": "Mittens really likes the stuff from Humboldt.", "num_hearts": 5, "num_likes": 5, "num_subtasks": 3, "resource_subtype": "default_task", "start_on": "2019-09-14", "assignee": {"gid": "12345", "resource_type": "user", "name": "Greg Sanchez"}, "custom_fields": [{"gid": "12345", "resource_type": "custom_field", "currency_code": "EUR", "custom_label": "gold pieces", "custom_label_position": "suffix", "description": "Development team priority", "enabled": true, "enum_options": [{"gid": "12345", "resource_type": "enum_option", "color": "blue", "enabled": true, "name": "Low"}], "enum_value": {"gid": "12345", "resource_type": "enum_option", "color": "blue", "enabled": true, "name": "Low"}, "format": "custom", "has_notifications_enabled": true, "is_global_to_workspace": true, "name": "Status", "number_value": 5.2, "precision": 2, "resource_subtype": "text", "text_value": "Some Value", "type": "text"}], "followers": [{"gid": "12345", "resource_type": "user", "name": "Greg Sanchez"}], "parent": {"gid": "12345", "resource_type": "task", "name": "Bug Task"}, "permalink_url": "https://app.asana.com/0/resource/123456789/list", "projects": [{"gid": "12345", "resource_type": "project", "name": "Stuff to buy"}], "tags": [{"gid": "59746", "name": "Grade A"}], "workspace": {"gid": "12345", "resource_type": "workspace", "name": "My Company Workspace"}}}
```



#### Add User To Workspace
Add a user to a specific workspace
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Workspace Name|The workspace to which you want to add the user.Note: It is case sensitive!|True|String|Your Workspace Name|
|User's Email|The email address of the user you want to add|True|String|email@gmail.com|



##### JSON Results
```json
{"data": {"gid": "12345", "resource_type": "user", "name": "Greg Sanchez", "email": "gsanchez@example.com", "photo": {"image_128x128": "https://...", "image_21x21": "https://...", "image_27x27": "https://...", "image_36x36": "https://...", "image_60x60": "https://..."}, "workspaces": [{"gid": "12345", "resource_type": "workspace", "name": "My Company Workspace"}]}}
```



#### Create Task
Create a task for a specific project 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Task Subject|The new task subject|True|String|Your Task Subject|
|Assignee|The user to whom you will assign the task.Note: This is case sensitive!|False|String||
|Due Date|The due date is in the format YYYY-MM-DD|False|String||
|Description|The description of the new task|True|String|Your task description|
|Project Name|The name of the project to which you want to assign the task.Note: this is case sensitive|True|String|Your Project Name |



##### JSON Results
```json
{"data": {"gid": "12345", "resource_type": "task", "name": "Buy catnip", "approval_status": "pending", "assignee_status": "upcoming", "completed": false, "completed_at": "2012-02-22T02:06:58.147Z", "completed_by": {"gid": "12345", "resource_type": "user", "name": "Greg Sanchez"}, "created_at": "2012-02-22T02:06:58.147Z", "dependencies": [{"gid": "12345", "resource_type": "task"}], "dependents": [{"gid": "12345", "resource_type": "task"}], "due_at": "2019-09-15T02:06:58.147Z", "due_on": "2019-09-15", "external": {"data": "A blob of information", "gid": "my_gid"}, "hearted": true, "hearts": [{"gid": "12345", "user": {"gid": "12345", "resource_type": "user", "name": "Greg Sanchez"}}], "html_notes": "<body>Mittens <em>really</em> likes the stuff from Humboldt.</body>", "is_rendered_as_separator": false, "liked": true, "likes": [{"gid": "12345", "user": {"gid": "12345", "resource_type": "user", "name": "Greg Sanchez"}}], "memberships": [{"project": {"gid": "12345", "resource_type": "project", "name": "Stuff to buy"}, "section": {"gid": "12345", "resource_type": "section", "name": "Next Actions"}}], "modified_at": "2012-02-22T02:06:58.147Z", "notes": "Mittens really likes the stuff from Humboldt.", "num_hearts": 5, "num_likes": 5, "num_subtasks": 3, "resource_subtype": "default_task", "start_on": "2019-09-14", "assignee": {"gid": "12345", "resource_type": "user", "name": "Greg Sanchez"}, "custom_fields": [{"gid": "12345", "resource_type": "custom_field", "currency_code": "EUR", "custom_label": "gold pieces", "custom_label_position": "suffix", "description": "Development team priority", "enabled": true, "enum_options": [{"gid": "12345", "resource_type": "enum_option", "color": "blue", "enabled": true, "name": "Low"}], "enum_value": {"gid": "12345", "resource_type": "enum_option", "color": "blue", "enabled": true, "name": "Low"}, "format": "custom", "has_notifications_enabled": true, "is_global_to_workspace": true, "name": "Status", "number_value": 5.2, "precision": 2, "resource_subtype": "text", "text_value": "Some Value", "type": "text"}], "followers": [{"gid": "12345", "resource_type": "user", "name": "Greg Sanchez"}], "parent": {"gid": "12345", "resource_type": "task", "name": "Bug Task"}, "permalink_url": "https://app.asana.com/0/resource/123456789/list", "projects": [{"gid": "12345", "resource_type": "project", "name": "Stuff to buy"}], "tags": [{"gid": "59746", "name": "Grade A"}], "workspace": {"gid": "12345", "resource_type": "workspace", "name": "My Company Workspace"}}}
```



#### Remove User From Workspace
Removes a given user from a workspace in Asana
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Workspace Name|The workspace from which you want to remove the userNote: It is case sensitive!|True|String|Your Workspace Name|
|User's Email|The email address of the user you want to remove.|True|String|email@gmail.com|



##### JSON Results
```json
{}
```



#### List My Tasks
Lists all the tasks associated with a user in Asana
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User's Email|The email of the user you would like to retrieve tasks for in Asana|True|String|email@gmail.com|
|Workspace Name|The workspace name.Note: This is case sensitive|True|String|Your Workspace Name|
|Completed Status|Marking the checkbox will retrieve only the tasks that were completed by the user. |False|Boolean|false|



##### JSON Results
```json
{"Task name: task 1": {"data": {"gid": "11111111", "assignee": {"gid": "123456", "name": "Firstname Lastname", "resource_type": "user"}, "assignee_status": "inbox", "completed": false, "completed_at": null, "created_at": "2020-10-07T13:44:40.643Z", "due_at": null, "due_on": "2020-10-09", "followers": [{"gid": "123456", "name": "Firstname Lastname", "resource_type": "user"}], "hearted": false, "hearts": [], "liked": false, "likes": [], "memberships": [{"project": {"gid": "88888888", "name": "Test Project", "resource_type": "project"}, "section": {"gid": "99999999", "name": "Untitled section", "resource_type": "section"}}], "modified_at": "2020-10-08T12:39:42.693Z", "name": "task 1", "notes": "The new task", "num_hearts": 0, "num_likes": 0, "parent": null, "permalink_url": "https://app.asana.com/0/88888888/11111111", "projects": [{"gid": "555555", "name": "Test Project", "resource_type": "project"}], "resource_type": "task", "start_on": null, "tags": [], "resource_subtype": "default_task", "workspace": {"gid": "444444", "name": "WorkspaceName", "resource_type": "workspace"}}}}
```



#### List Project Tasks
Lists all the tasks associated with a specific project
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project Name|The name of the project from which you would like to fetch all the tasks|True|String|Your Project Name|
|Completed Status|Marking the checkbox will retrieve only the tasks that were completed by the user. |False|Boolean|false|



##### JSON Results
```json
{"Task name: task 1": {"data": {"gid": "11111111", "assignee": {"gid": "123456", "name": "Firstname Lastname", "resource_type": "user"}, "assignee_status": "inbox", "completed": false, "completed_at": null, "created_at": "2020-10-07T13:44:40.643Z", "due_at": null, "due_on": "2020-10-09", "followers": [{"gid": "123456", "name": "Firstname Lastname", "resource_type": "user"}], "hearted": false, "hearts": [], "liked": false, "likes": [], "memberships": [{"project": {"gid": "88888888", "name": "Test Project", "resource_type": "project"}, "section": {"gid": "99999999", "name": "Untitled section", "resource_type": "section"}}], "modified_at": "2020-10-08T12:39:42.693Z", "name": "task 1", "notes": "The new task", "num_hearts": 0, "num_likes": 0, "parent": null, "permalink_url": "https://app.asana.com/0/88888888/11111111", "projects": [{"gid": "555555", "name": "Test Project", "resource_type": "project"}], "resource_type": "task", "start_on": null, "tags": [], "resource_subtype": "default_task", "workspace": {"gid": "444444", "name": "WorkspaceName", "resource_type": "workspace"}}}}
```



#### Ping
Testing connectivity with Asana
Timeout - 600 Seconds



##### JSON Results
```json
{}
```









