
# FreshworksFreshservice

Freshservice is a cloud-based IT Help Desk and service management solution that enables organizations to simplify their IT operations. The solution offers features that include a ticketing system, self-service portal and knowledge-base.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https://yourdomain.freshservice.com|
|API Key||True|Password|*****|
|Verify SSL||False|Boolean|true|


#### Dependencies
| |
|-|
|certifi-2026.4.22-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.6.3-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|


## Actions
#### Add a Ticket Note
Add a note to a Freshservice ticket. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Specify ticket ID to return conversations for.|True|String||
|Note Type|Specify the type of note action should add to the ticket.|False|List|Private|
|Note Text|Specify note text to add to ticket.|True|String||



##### JSON Results
```json
[{"conversation": {"id": "XXXXXXXXX", "user_id": "XXXXXXXXX", "from_email": "XXXXXX@XXXXXXXXXXXXXXXXXX.XXXXXXXXXXXX.XXXXXX", "cc_emails": [], "bcc_emails": [], "body": "XXXXXXXXXXXX", "body_text": "XXXXXX", "ticket_id": "XXXXXX", "to_emails": ["XXXX.XXXXXX@XXXXXXXX.XX"], "attachments": [], "created_at": "XXXXXXXXXXXX", "updated_at": "XXXXXXXXXXXX"}}]
```



#### Update Ticket Time Entry
Update a time entry for a Freshservice ticket. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Specify ticket ID to update a time entry for.|True|String||
|Time Entry ID|Specify time entry ID to update.|True|String||
|Agent Email|Specify agent email for whom to change a ticket time entry.|False|String||
|Note|Specify a note for the ticket time entry.|False|String||
|Time Spent|Specify time spent for ticket time entry. Format: {hh:mm}|False|String||
|Billable|If enabled, ticket time entry will be marked as billable.|False|Boolean|false|
|Custom Fields|Specify a JSON object that contains custom fields to add to the ticket time entry. Action appends new custom fields to any existing for ticket time entry. Example format: {"key1":"value1","key2":"value2"}|False|String||



##### JSON Results
```json
[{"time_entry": {"id": "XXXXXXXXXXX", "created_at": "XXXX-XX-XXTXX:XX:XXZ", "updated_at": "XXXX-XX-XXTXX:XX:XXZ", "start_time": "XXXX-XX-XXTXX:XX:XXZ", "timer_running": "false", "billable": "true", "time_spent": "00:00", "executed_at": "XXXX-XX-XXTXX:XX:XXZ", "task_id": "None", "note": "XXXXXXX", "agent_id": "XXXXXXXXXXX", "custom_fields": {"XXX": "XXXX"}}}]
```



#### Update Agent
Update existing Freshservice Agent. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Agent ID|Specify agent id to update.|True|String||
|Email|Specify the email of the agent to update.|False|String||
|First Name|Specify the first name of the agent to update.|False|String||
|Last Name|Specify the last name of the agent to update.|False|String||
|Is occasional|If enabled, agent will be updated as an occasional agent, otherwise it will be a full-time agent.|False|Boolean|false|
|Can See All Tickets From Associated Departments|If enabled, agent will be able to see all tickets from Associated departments.|False|Boolean|false|
|Departments|Specify department names associated with the agent. Parameter accepts multiple values as a comma separated string.|False|String||
|Location|Specify location name associated with the agent.|False|String||
|Group Memberships|Specify group names agent should be a member of.|False|String||
|Roles|Specify roles to add to agent. Parameter accepts multiple values as a comma separated string. Example: {'role_id':170000XXXXX,'assignment_scope': 'entire_helpdesk'}|False|String||
|Job Title|Specify agent job title.|False|String||
|Custom Fields|Specify a JSON object that contains custom fields to add to the agent. Action appends new custom fields to any existing for an agent. Example format: {"key1":"value1","key2":"value2"}|False|String||



##### JSON Results
```json
{"agent": {"active": true, "address": null, "background_information": null, "can_see_all_tickets_from_associated_departments": true, "created_at": "2021-07-14T07:51:11Z", "custom_fields": {"aaaa": "aaaaa"}, "department_ids": [12345, 12345], "email": "aaaa.aaa@a.aaa", "external_id": null, "first_name": "aaaa", "has_logged_in": false, "id": 12345, "job_title": "DEVDEV", "language": "en", "last_active_at": null, "last_login_at": null, "last_name": "aaaaa", "location_id": 12345, "mobile_phone_number": null, "occasional": true, "reporting_manager_id": null, "role_ids": [12345, 12345], "roles": [{"role_id": 123345, "assignment_scope": "member_groups", "groups": []}, {"role_id": 123435, "assignment_scope": "entire_helpdesk", "groups": []}], "scopes": {"ticket": null, "problem": null, "change": null, "release": null, "asset": null, "solution": null, "contract": null}, "scoreboard_level_id": 5, "signature": "<p><br></p>\n", "time_format": "12h", "time_zone": "Eastern Time (US & Canada)", "updated_at": "2021-07-14T14:12:54Z", "work_phone_number": null, "group_ids": [12345, 12345], "member_of": [12345, 12345], "observer_of": []}}
```



#### List Ticket Conversations
List Freshservice ticket conversations based on the specified search criteria. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Specify ticket ID to return conversations for.|True|String||
|Rows per Page|Specify how many ticket conversations should be returned per page for Freshservice pagination.|False|String|30|
|Start at Page|Specify starting from which page ticket conversations should be returned with Freshservice pagination.|False|String|1|
|Max Rows to Return|Specify how many ticket conversations action should return in total.|False|String|30|



##### JSON Results
```json
[{"conversations": [{"id": "XXXXXXXX", "user_id": "XXXXXXXX", "to_emails": ["XXXX-XXXX@XXXXXXXXXXXX.XXXXXXXX.XXX"], "body": "XXXXXXXX", "body_text": "XXXXXXXX", "ticket_id": "X", "created_at": "XXXXXXXX", "updated_at": "XXXXXXXX", "incoming": "XXXX", "private": "XXXX", "support_email": "XXXX@XXXXXXXXXXXX.XXXXXXXX.XXX", "source": "X", "from_email": "XXXX@XXXXXXXXXXXX.XXXXXXXX.XXX", "cc_emails": [], "bcc_emails": [], "attachments": [], "user_email": "XXX.XXXXXXXX@XXXXX.XX", "source_name": "XXXX"}]}]
```



#### List Agents
List Freshservice agents based on the specified search criteria. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Agent Email|Specify the email address to return agent records for.|False|String||
|Agent State|Specify agent states to return.|False|List|All|
|Include not Active Agents|If enabled, results will include not active agent records.|False|Boolean|false|
|Rows per Page|Specify how many agent records should be returned per page for Freshservice pagination.|False|String|30|
|Start at Page|Specify starting from which page agent records should be returned with Freshservice pagination|False|String|1|
|Max Rows to Return|Specify how many agent records action should return in total.|False|String|30|



##### JSON Results
```json
[{"agents": [{"active": true, "address": null, "background_information": null, "can_see_all_tickets_from_associated_departments": true, "created_at": "123456", "custom_fields": {"aaaa": "aaaa"}, "department_ids": [12345, 12345], "email": "aaaa@aaaaa.aaa", "external_id": null, "first_name": "aaaa", "has_logged_in": false, "id": 123456, "job_title": "Dev", "language": "en", "last_active_at": null, "last_login_at": null, "last_name": "a", "location_id": 123456, "mobile_phone_number": null, "occasional": true, "reporting_manager_id": null, "role_ids": [123456, 123456], "roles": [{"role_id": 123456, "assignment_scope": "member_groups", "groups": []}, {"role_id": 123456, "assignment_scope": "entire_helpdesk", "groups": []}], "scopes": {"ticket": null, "problem": null, "change": null, "release": null, "asset": null, "solution": null, "contract": null}, "scoreboard_level_id": 1, "signature": "<p><br></p>\n", "time_format": "12h", "time_zone": "Eastern Time (US & Canada)", "updated_at": "123456", "work_phone_number": null, "group_ids": [12345, 12345], "member_of": [12345, 12345], "observer_of": [], "department_names": ["aaaa", "aaaa"], "location_name": "America", "member_group_names": ["aaaaaa", "aaaaa Team"], "agent_role_names": ["aaaa", "aaaaa"]}]}]
```



#### Create Agent
Create a new Freshservice Agent. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job Title|Specify agent job title.|False|String||
|Email|Specify the email of the agent to create.|True|String||
|First Name|Specify the first name of the agent to create.|True|String||
|Last Name|Specify the last name of the agent to create.|False|String||
|Is occasional|If enabled, agent will be created as an occasional agent, otherwise full-time agent will be created.|False|Boolean|false|
|Can See All Tickets From Associated Departments|If enabled, agent will be able to see all tickets from Associated departments.|False|Boolean|false|
|Departments|Specify department names associated with the agent. Parameter accepts multiple values as a comma separated string.|False|String||
|Location|Specify location name associated with the agent.|False|String||
|Group Memberships|Specify group names agent should be a member of.|False|String||
|Roles|Specify roles to add to agent. Parameter accepts multiple values as a comma separated string. Example: {'role_id':17000023338,'assignment_scope': 'entire_helpdesk'}|True|String||
|Custom Fields|Specify a JSON object that contains custom fields to add to the agent. Action appends new custom fields to any existing for an agent. Example format: {"key1":"value1","key2":"value2"}|False|String||



##### JSON Results
```json
{"agent": {"active": true, "address": null, "background_information": null, "can_see_all_tickets_from_associated_departments": true, "created_at": "2021-07-14T07:56:22Z", "custom_fields": {"test": "testvalue"}, "department_ids": [123456, 123456], "email": "amiaaa@a.c1", "external_id": null, "first_name": "amit", "has_logged_in": false, "id": 123456, "job_title": "Dev", "language": "en", "last_active_at": null, "last_login_at": null, "last_name": "a", "location_id": 123456, "mobile_phone_number": null, "occasional": true, "reporting_manager_id": null, "role_ids": [123456, 123456], "roles": [{"role_id": 123456, "assignment_scope": "assigned_items", "groups": []}, {"role_id": 123456, "assignment_scope": "assigned_items", "groups": []}], "scopes": {"ticket": null, "problem": null, "change": null, "solution": null, "contract": null, "asset": null}, "scoreboard_level_id": 1, "signature": null, "time_format": "12h", "time_zone": "Eastern Time (US & Canada)", "updated_at": "2021-07-14T07:56:22Z", "work_phone_number": null, "group_ids": [123456, 123456], "member_of": [123456, 123456], "observer_of": []}}
```



#### Update Requester
Update existing Freshservice Requester. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Requester ID|Specify requester id to update.|True|String||
|Email|Specify the email of the requester to update.|False|String||
|First Name|Specify the first name of the requester to update.|False|String||
|Last Name|Specify the last name of the requester to update.|False|String||
|Can See All Tickets From Associated Departments|If enabled, requester will be able to see all tickets from associated departments.|False|Boolean|false|
|Departments|Specify department names associated with the requester. Parameter accepts multiple values as a comma separated string.|False|String||
|Location|Specify location name associated with the requester.|False|String||
|Job Title|Specify requester job title.|False|String||
|Custom Fields|Specify a JSON object that contains custom fields to add to the requester. Action appends new custom fields to any existing for requester. Example format: {"key1":"value1","key2":"value2"}|False|String||



##### JSON Results
```json
[{"requester": {"active": "XXXX", "address": "XXXX", "background_information": "XXXX", "can_see_all_tickets_from_associated_departments": "XXXX", "created_at": "2021-XX-XXT10:11:46Z", "custom_fields": {"test": "XXXXXXXX"}, "department_ids": ["1700001XXXX"], "external_id": "None", "first_name": "XXXXX", "has_logged_in": "false", "id": "170022XXXX", "job_title": "XXXXXXXXX", "language": "XX", "last_name": "XXXXXXX", "location_id": "1700002XXXX", "mobile_phone_number": "XXXX", "primary_email": "XXXXXXX@XXXXX.com", "reporting_manager_id": "XXXXX", "secondary_emails": [], "time_format": "12h", "time_zone": "EasternTime(US&Canada)", "updated_at": "2021-XX-XXT10:11:46Z", "work_phone_number": "XXXX", "location_name": "XXXXXXXXXX", "department_names": ["XXXXXXXX"]}}]
```



#### Add Ticket Time Entry
Add a time entry to a Freshservice ticket. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Specify ticket ID to add a time entry for.|True|String||
|Agent Email|Specify agent email for whom to add a ticket time entry.|True|String||
|Note|Specify a note to add to the ticket time entry.|False|String||
|Time Spent|Specify time spent for ticket time entry. Format: {hh:mm}|True|String||
|Billable|If enabled, ticket time entry will be marked as billable.|False|Boolean|false|
|Custom Fields|Specify a JSON object that contains custom fields to add to the ticket time entry. Action appends new custom fields to any existing for ticket time entry. Example format: {"key1":"value1","key2":"value2"}|False|String||



##### JSON Results
```json
[{"time_entry": {"id": "XXXXXXXXXXX", "created_at": "XXXX-XX-XXTXX:XX:XXZ", "updated_at": "XXXX-XX-XXTXX:XX:XXZ", "start_time": "XXXX-XX-XXTXX:XX:XXZ", "timer_running": "false", "billable": "true", "time_spent": "00:00", "executed_at": "XXXX-XX-XXTXX:XX:XXZ", "task_id": "None", "note": "XXXXXXX", "agent_id": "XXXXXXXXXXX", "custom_fields": {"XXX": "XXXX"}}}]
```



#### Create Ticket
Create a Freshservice ticket. Note: as of now, Freshservice API supports only creation of tickets with the type "Incident" and the ticket's priority is dynamically calculated according to the "Urgency" and "Impact" values, same as in FreshService's UI. Additionally, if file attachments to add are provided, the total size of the attachments must not exceed 15MB.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Subject|Specify subject field for created ticket.|True|String||
|Description|Specify description field for created ticket.|True|String||
|Requester Email|Specify requester email for created ticket.|True|String||
|Agent Assign To|Specify the agent email to assign the ticket to.|False|String||
|Group Assign To|Specify the group name to assign the ticket to.|False|String||
|Department Name|Specify the name of the department for the ticket. This parameter is case sensitive.|False|String||
|Priority|Specify priority to assign to the ticket.|True|List|Medium|
|Urgency|Specify urgency to assign to the ticket.|False|List|Medium|
|Impact|Specify impact to assign to the ticket.|False|List|Medium|
|Tags|Specify tags to assign to the ticket. Parameter accepts multiple values as a comma separated string.|False|String||
|Custom Fields|Specify a JSON object that contains custom fields to add to the ticket. Action appends new custom fields to any existing for a ticket. Example format: {"key1":"value1","key2":"value2"}|False|String||
|File Attachments to Add|Specify the full path for the file to be uploaded with the ticket. Parameter accepts multiple values as a comma separated string. The total size of the attachments must not exceed 15MB|False|String||



##### JSON Results
```json
[{"ticket": {"cc_emails": [], "fwd_emails": [], "reply_cc_emails": [], "fr_escalated": "XXXX", "spam": "XXXX", "email_config_id": "None", "group_id": "XXXXXX", "priority": "X", "priority_name": "XXXXX", "requester_id": "XXXXXX", "requested_for_id": "XXXXXX", "responder_id": "XXXXXX", "source": "X", "source_name": "XXXXX", "status": "X", "status_name": "XXXXX", "subject": "XXXXX", "to_emails": "XXXX", "department_id": "XXXX", "id": "XX", "type": "Incident", "due_by": "XXXXXXXXXX", "fr_due_by": "XXXXXXXX", "is_escalated": "XXXXX", "description": "XXXXX", "description_text": "XXXXX", "category": "XXX", "sub_category": "XXXX", "item_category": "XXXX", "custom_fields": {"XXXX": "XXXX"}, "created_at": "XXXXXXX", "updated_at": "XXXXXXX", "tags": ["XXXXX", "XXXX"], "attachments": []}}]
```



#### Deactivate Agent
Deactivate Freshservice agent. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Agent ID|Specify agent id to deactivate.|True|String||



##### JSON Results
```json
{"agent": {"active": false, "address": null, "background_information": null, "can_see_all_tickets_from_associated_departments": false, "created_at": "2021-07-20T12:26:17Z", "custom_fields": {"aaaa": "aaaa"}, "department_ids": [1, 2], "email": "aaaa.aaaa@a.aaaaa", "external_id": null, "first_name": "aaaaa", "has_logged_in": false, "id": 12345, "job_title": "Dev", "language": "en", "last_active_at": null, "last_login_at": null, "last_name": "aaaaa", "location_id": 12345, "mobile_phone_number": null, "occasional": true, "reporting_manager_id": null, "role_ids": [12345], "roles": [{"role_id": 12345, "assignment_scope": "assigned_items", "groups": [1, 2]}], "scopes": {"ticket": null, "contract": null, "asset": null}, "scoreboard_level_id": 1, "signature": null, "time_format": "12h", "time_zone": "Eastern Time (US & Canada)", "updated_at": "2021-07-20T12:26:17Z", "work_phone_number": null, "group_ids": [1, 2], "member_of": [1, 2], "observer_of": []}}
```



#### List Requesters
List requesters registered in Freshservice based on the specified search criteria. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Requester Email|Specify the email address to return requester records for.|False|String||
|Rows per Page|Specify how many requester records should be returned per page for Freshservice pagination.|False|String|30|
|Start at Page|Specify starting from which page requester records should be returned with Freshservice pagination.|False|String|1|
|Max Rows to Return|Specify how many requester records action should return in total.|False|String|30|



##### JSON Results
```json
[{"requesters": [{"active": true, "address": null, "background_information": null, "can_see_all_tickets_from_associated_departments": false, "created_at": "12345", "custom_fields": {"aaaa": null}, "department_ids": [12345, 12345], "external_id": null, "first_name": "aaa", "has_logged_in": true, "id": 21345, "job_title": null, "language": "en", "last_name": "aaaa", "location_id": 12344, "mobile_phone_number": null, "primary_email": "aaaa@aaaa.aaa", "reporting_manager_id": null, "secondary_emails": [], "time_format": "12h", "time_zone": "Eastern Time (US & Canada)", "updated_at": "12345", "work_phone_number": null, "department_names": ["aaaa", "aaaaa"], "location_name": "America"}]}]
```



#### List Ticket Time Entries
List Freshservice tickets time entries based on the specified search criteria. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Specify ticket ID to return time entries for.|True|String||
|Agent Email|Specify agent email to list ticket time entries for.|True|String||
|Rows per Page|Specify how many ticket time entries should be returned per page for Freshservice pagination.|False|String|30|
|Start at Page|Specify starting from which page ticket time entries should be returned with Freshservice pagination.|False|String|1|
|Max Rows to Return|Specify how many ticket time entries action should return in total.|False|String|30|



##### JSON Results
```json
[{"time_entries": [{"id": "XXXXXXXX", "created_at": "XXXXX-XX-XXTXX:XX:XXZ", "updated_at": "XXXXX-XX-XXTXX:XX:XXZ", "start_time": "XXXXX-XX-XXTXX:XX:XXZ", "timer_running": "XXXX", "billable": "XXXX", "time_spent": "00:00", "executed_at": "XXXXX-XX-XXTXX:XX:XXZ", "task_id": "None", "note": "XXXXXXXXXXXXXXX", "agent_id": "XXXXXXXX", "custom_fields": {"XXXX": "XXXX"}}]}]
```



#### List Tickets
List Freshservice tickets base on the specified search criteria. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket Type|Specify ticket type to return.|False|List|All|
|Requester|Specify the requester email of tickets to return.|False|String||
|Include Stats|If enabled, action will return additional stats on the tickets.|False|Boolean|False|
|Search for Last X hours|Specify the timeframe to search tickets for.|False|String||
|Rows per Page|Specify how many tickets should be returned per page for Freshservice pagination.|False|String|30|
|Start at Page|Specify starting from which page tickets should be returned with Freshservice pagination.|False|String|1|
|Max Rows to Return|Specify how many tickets action should return in total.|False|String|30|
|Workspace ID|Specify the ID of the workspace that should be used to list tickets. If nothing is provided, the action will list tickets only from the primary workspace. To list tickets from all workspaces provide “0” in the parameter.|False|String||



##### JSON Results
```json
[{"tickets": [{"subject": "XXXX", "group_id": "XXXXXX", "department_id": "XXXXX", "category": "XXXXX", "sub_category": "XXXXX", "item_category": "XXXXX", "requester_id": "XXXXXX", "responder_id": "XXXXX", "due_by": "XXXXXXXXXX", "fr_escalated": "XXXXX", "deleted": "XXXXX", "spam": "XXXXX", "email_config_id": "XXXXX", "fwd_emails": [], "reply_cc_emails": [], "cc_emails": [], "is_escalated": "XXXXX", "fr_due_by": "XXXXXXXXXX", "id": "XX", "priority": "X", "priority_name": "XXXXX", "status": "X", "status_name": "XXXXX", "source": "X", "source_name": "XXXXX", "created_at": "XXXXXXXXXX", "updated_at": "XXXXXXXXXX", "requested_for_id": "XXXXXXXXXX", "to_emails": "XXXXX", "type": "XXXXX", "description": "XXXXX", "description_text": "XXXXX", "custom_fields": {"test": "XXXXX", "my_field": "XXXXX"}, "requester": {"email": "XXXXX.XXXXX@XXXXX.XX", "id": "XXXXXXXXXX", "mobile": "XXXXX", "name": "XXXXXXXXXX", "phone": "XXXXX"}}]}]
```



#### Deactivate Requester
Deactivate Freshservice requester. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Requester ID|Specify requester id to deactivate.|True|String||



#### Update Ticket
Update a Freshservice ticket based on provided action input parameters. Note that if new tags for the ticket are provided, due to the Freshservice API limitations action replaces existing tags in the ticket, not appending new ones to existing. Additionally, if file attachments to add are provided, the total size of the attachments must not exceed 15MB
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Specify ticket id to update.|True|String||
|Status|Specify new status for the ticket.|False|List|Not Changed|
|Subject|Specify subject field to update.|False|String||
|Description|Specify description field to update.|False|String||
|Requester Email|Specify requester email to update.|False|String||
|Agent Assign To|Specify the agent email to update.|False|String||
|Group Assign To|Specify the group name to update.|False|String||
|Priority|Specify priority to update.|False|List|Not Changed|
|Urgency|Specify urgency to update.|False|List|Not Changed|
|Impact|Specify impact to update.|False|List|Not Changed|
|Tags|Specify tags to replace in the ticket. Parameter accepts multiple values as a comma separated string. Note that due to the Freshservice API limitations action replaces existing tags in the ticket, not appending new ones to existing.|False|String||
|Custom Fields|Specify a JSON object that contains custom fields to add to the ticket. Action appends new custom fields to any existing for a ticket. Example format: {"key1":"value1","key2":"value2"}|False|String||
|File Attachments to Add|Specify the full path for the file to be uploaded with the ticket. Parameter accepts multiple values as a comma separated string. The total size of the attachments must not exceed 15MB|False|String||



##### JSON Results
```json
[{"ticket": {"cc_emails": [], "fwd_emails": [], "reply_cc_emails": [], "spam": "XXXX", "email_config_id": "XXXXX", "fr_escalated": "XXXX", "group_id": "XXXXXX", "priority": "X", "priority_name": "XXXXX", "requester_id": "XXXXXXX", "requested_for_id": "XXXXXXX", "responder_id": "XXXXXXX", "source": "X", "source_name": "XXXXX", "status": "X", "status_name": "XXXXX", "subject": "XXXXXXXXXXXXXX", "description": "XXXXXXXXXXXXXX", "description_text": "XXXXXXXXXXXXXX", "category": "XXXXXXX", "sub_category": "XXXXXXX", "item_category": "XXXXXXX", "custom_fields": {"test": "XXXXXXX", "my_field": "XXXXXXX"}, "id": "XX", "type": "Incident", "to_emails": "XXXXXXX", "department_id": "XXXXXXX", "is_escalated": "XXXXXXX", "tags": ["XXXXXXX"], "due_by": "XXXXXXX", "fr_due_by": "XXXXXXX", "created_at": "XXXXXXX", "updated_at": "XXXXXXX", "attachments": []}}]
```



#### Delete Ticket Time Entry
Delete a time entry for a Freshservice ticket. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Specify ticket ID to delete a time entry for.|True|String||
|Time Entry ID|Specify time entry ID to delete.|True|String||



#### Create Requester
Create a new Freshservice requester. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Email|Specify the email of the requester to create.|True|String||
|First Name|Specify the first name of the requester to create.|True|String||
|Last Name|Specify the last name of the requester to create.|False|String||
|Can See All Tickets From Associated Departments|If enabled, requester will be able to see all tickets from associated departments.|False|Boolean|false|
|Departments|Specify department names associated with the requester. Parameter accepts multiple values as a comma separated string.|False|String||
|Location|Specify location name associated with the requester.|False|String||
|Job Title|Specify requester job title.|False|String||
|Custom Fields|Specify a JSON object that contains custom fields to add to the requester. Action appends new custom fields to any existing for requester. Example format: {"key1":"value1","key2":"value2"}|False|String||



##### JSON Results
```json
[{"requester": {"active": "XXXX", "address": "XXXX", "background_information": "XXXX", "can_see_all_tickets_from_associated_departments": "XXXX", "created_at": "2021-XX-XXT10:11:46Z", "custom_fields": {"test": "XXXXXXXX"}, "department_ids": ["1700001XXXX"], "external_id": "None", "first_name": "XXXXX", "has_logged_in": "false", "id": "170022XXXX", "job_title": "XXXXXXXXX", "language": "XX", "last_name": "XXXXXXX", "location_id": "1700002XXXX", "mobile_phone_number": "XXXX", "primary_email": "XXXXXXX@XXXXX.com", "reporting_manager_id": "XXXXX", "secondary_emails": [], "time_format": "12h", "time_zone": "EasternTime(US&Canada)", "updated_at": "2021-XX-XXT10:11:46Z", "work_phone_number": "XXXX", "location_name": "XXXXXXXXXX", "department_names": ["XXXXXXXX"]}}]
```



#### Add a Ticket Reply
Add a reply to a Freshservice ticket. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Specify ticket ID to return conversations for.|True|String||
|Reply Text|Specify reply text to add to ticket.|True|String||



##### JSON Results
```json
[{"conversation": {"id": "XXXXXXXXX", "user_id": "XXXXXXXXX", "from_email": "XXXXXX@XXXXXXXXXXXXXXXXXX.XXXXXXXXXXXX.XXXXXX", "cc_emails": [], "bcc_emails": [], "body": "XXXXXXXXXXXX", "body_text": "XXXXXX", "ticket_id": "XXXXXX", "to_emails": ["XXXX.XXXXXX@XXXXXXXX.XX"], "attachments": [], "created_at": "XXXXXXXXXXXX", "updated_at": "XXXXXXXXXXXX"}}]
```



#### Ping
Test connectivity to the Freshservice instance with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds






## Jobs

#### Freshservice Sync Tickets Conversations Job
Sync conversations (considered both replies and notes) between Siemplify alert's case and corresponding Freshservice ticket. Sync mechanism works in both ways, Siemplify → Freshservice and Freshservice → Siemplify. Note: The job supports Siemplify cases with the "Freshservice" tag only.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|API Root|True|String|https://yourdomain.freshservice.com|
|API Key|True|Password|*****|
|Verify SSL|False|Boolean|true|
|Offset time in hours|True|String|24|
|Siemplify Comment Prefix|True|String|SIEMPLIFY:|
|Freshservice Comment Prefix|True|String|Freshservice Comment Sync Job:|
|Conversation Types To Sync|True|String|Replies, Notes|
|Fetch Private Notes?|False|Boolean|false|
|Sync Comment from Siemplify as X|True|String|Private Note|

#### Freshservice Sync Tickets Closure Job
Close tickets in Freshservice if corresponding Siemplify alerts were closed.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|API Root|True|String|https://yourdomain.freshservice.com|
|API Key|True|Password|*****|
|Offset time in hours|True|String|24|
|Verify SSL|False|Boolean|true|
|Default Ticket Description|True|String|Ticket is closed by the Siemplify Freshservice Sync Tickets Closure Job.|



## Connectors
#### Freshservice Tickets Connector
Connector can be used to fetch Freshservice tickets to create Siemplify alerts from. Connector whitelist can be used to ingest only specific types of tickets - Incident or Service Request

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|Freshservice instance API Root.|True|String|https://yourdomain.freshservice.com|
|API Key|Freshservice API Key to use in integration.|True|Password|*****|
|Verify SSL|If enabled, integration will try to verify that API Root is configured with a valid certificate.|False|Boolean|true|
|Offset time in hours|Number of hours before the first connector iteration to retrieve tickets from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|Int|24|
|Max Tickets Per Cycle|How many tickets should be processed during one connector run.|True|Int|30|
|Minimum Priority to Fetch|Minimum priority of the ticket to be ingested to Siemplify, for example, Low or Medium. Possible values: Low, Medium, High, Urgent|False|String|Medium|
|Tickets Status to Fetch|Ticket statuses to be ingested to Siemplify. Parameter accepts multiple values as a comma separated string. Possible values: Open, Pending, Resolved, Closed|False|String|Open, Closed|
|Use dynamic list as a blocklist|If enabled, dynamic list will be used as a blocklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|
|Workspace ID|ID of the workspace that should be used to fetch tickets. If nothing is provided, the action will fetch tickets only from the primary workspace. To fetch tickets from all workspaces provide “0” in the parameter.|False|String||




