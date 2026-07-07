
# RSAArcher

The RSA Archer Platform provides a centralized, flexible foundation that you can use to automate, integrate, manage and report on your organization's risk.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root||True|IP_OR_HOST|http://x.x.x.x/rsaarcher|
|Instance Name||True|String||
|Username||True|String||
|Password||True|Password|*****|
|Verify SSL||False|Boolean||


#### Dependencies
| |
|-|
|six-1.17.0-py2.py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|xmltodict-0.13.0-py2.py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|python_dateutil-2.8.2-py2.py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Add Incident Journal Entry
Add a journal entry to the Security Incident in RSA Archer.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Destination Content ID|Specify a content id of the security incident to which you want to add journal entry.|True|String||
|Text|Specify the text for the journal entry.|True|String||



##### JSON Results
```json
{"RequestedObject": {"Id": "26xxx6"}, "ValidationMessages": [], "IsSuccessful": "true", "Links": []}
```



#### Get Incident Details
Retrieve information about the incident from RSA Archer.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Content ID|Specify ID of the content for which you want to retrieve details.|True|String||
|Application Name|Specify an application name for the incident. Default: Incidents.|False|String|Incidents|



##### JSON Results
```json
{"Incident_Analysis_Q8": [], "Open_TasksActivities": [], "Incident_Analysis_Q1": [], "Incident_Analysis_Q3": [], "Incident_Analysis_Q2": [], "Incident_Analysis_Q5": [], "Incident_Analysis_Q4": [], "DateTime_Reported": "2020-11-26T10:04:23+02:00", "Incident_Analysis_Q6": [], "Override_Rejected_Submission": ["No"], "Notification_Execution": [], "Data_Encrypted": [], "Escalated_Incident_Status": [], "Customer_Data": [], "Discovery_Policy_Enabled": [], "Total_Hours": 0, "DLP_Source_Product": [], "Workflow_Assignees": [], "Region": [], "Inherited_RP": [], "Incident_Result": ["To Be Determined"], "Incident_Analysis_Q7": [], "Google_Map": "", "Incidents_Id": 250886, "Facility": [], "Workflow_Stage": [], "Individuals_Involved": [], "Date_Created": "2020-11-26T10:04:23.08+02:00", "Zip_Code": null, "Impacted_Information_Assess": [], "Related_Incidents1": [], "Batch_File_Format": [], "Responder_Hours_Entry": [], "Priority": ["High"], "Source": [], "Default_Record_Permissions": ["IM: Admin", "IM: Read Only", "BCM: Admin"], "Law_Enforcement_Case_No": null, "Incident_Analysis_Score": 0, "Status_Prior_Value": [], "Business_Impact_Analysis_Archive": [], "Affected_Business_Unit": [], "DLP_Policy": [], "Incident_Analysis_Severity": ["Low"], "Current_Status": [], "Incident_Summary": null, "Encryption_Details": null, "Law_Enforcement_Agent": null, "Estimated_Hours": 0, "DateTime_Occurred": null, "Category": [], "Law_Enforcement_Agency": null, "Corrective_Actions": null, "Legal_Involvement_Details": null, "Range_Type": [], "Status_Change": ["No"], "Related_Incidents": [], "Investigations": [], "@odata.context": "http://xxx.xx.xx.xx/RSAarcher/contentapi/Incidents(250886)/$metadata#Incidents/$entity", "Filing_Name": null, "Recovery_": 0, "Inherited_Permissions_Engagement_Stakeho": [], "Organization_Affected_By_Incident": [], "Incident_ID": 29, "Days_Open": 0, "From_Date__Time": null, "Inherited_Permissions_Supplier_Request_F": [], "Legal_Involvement": [], "Notify_Crisis_Team": [" No, do not send an email notification"], "Recovery_Description": null, "Additional_Notification_Recipients": [], "Involved_Third_Parties": [], "Incident_Owner": [], "State": [], "Incident_Trend": [], "Top_Offending_Users": [], "Loss_Events": [], "City": null, "Last_Updated": "2020-11-26T10:04:23.08+02:00", "Incident_Status": ["New"], "Emergency_Notifications": [], "Notify_Incident_Owner": ["No, do not send an email notification to the incident owner"], "Loss_Description": null, "Inherited_From_Third_Party_Profile": [], "Incident_Resolution_Detail": null, "Cause": null, "Desktop_Policy_Enabled": [], "Policy_Enabled": [], "Address": null, "Customer_Data_Details": null, "Loss": 0, "Country": [], "Business_Continuity_Plans": [], "Incident_Details": null, "Is_BSA_Bank_Secrecy_Act_reporting_requir": ["No"], "Network_Policy_Enabled": [], "Reported_to_Police": [], "DateTime_Closed": null, "Incident_Manager": [], "Additional_Access": [], "Risks": []}
```



#### Update Incident
Update an incident
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Content ID|Content Id of the incident to update.|True|String||
|Application Name|Specify an application name for the incident. Default: Incidents.|False|String|Incidents|
|Incident Summary|The new summary of the incident.|False|String||
|Incident Details|The new details (decsription) of the incident.|False|String||
|Incident Owner|The new owner of the incident.|False|String||
|Incident Status|The new status of the incident.|False|String||
|Priority|The new priority of the incident.|False|String||
|Category|The new category of the incident.|False|String||
|Custom Fields|Specify a JSON object of fields that need to be updated. Example: {“Category”:“Malware”}.|False|String||
|Custom Mapping File|Specify an absolute path to the file that contains all of the required mapping. If “Remote File“ is enabled, then provide a URL that contains the mapping file. Please refer to action documentation for the additional information.|False|String||
|Remote File|If enabled, action will treat value provided in “Custom Mapping File“ as a URL and try to fetch a file from it.|False|Boolean|false|



##### JSON Results
```json
{"Incident_Analysis_Q8": [], "Open_TasksActivities": [], "Incident_Analysis_Q1": [], "Incident_Analysis_Q3": [], "Incident_Analysis_Q2": [], "Incident_Analysis_Q5": [], "Incident_Analysis_Q4": [], "DateTime_Reported": "2020-11-26T10:04:23+02:00", "Incident_Analysis_Q6": [], "Override_Rejected_Submission": ["No"], "Notification_Execution": [], "Data_Encrypted": [], "Escalated_Incident_Status": [], "Customer_Data": [], "Discovery_Policy_Enabled": [], "Total_Hours": 0, "DLP_Source_Product": [], "Workflow_Assignees": [], "Region": [], "Inherited_RP": [], "Incident_Result": ["To Be Determined"], "Incident_Analysis_Q7": [], "Google_Map": "", "Incidents_Id": 250886, "Facility": [], "Workflow_Stage": [], "Individuals_Involved": [], "Date_Created": "2020-11-26T10:04:23.08+02:00", "Zip_Code": null, "Impacted_Information_Assess": [], "Related_Incidents1": [], "Batch_File_Format": [], "Responder_Hours_Entry": [], "Priority": ["High"], "Source": [], "Default_Record_Permissions": ["IM: Admin", "IM: Read Only", "BCM: Admin"], "Law_Enforcement_Case_No": null, "Incident_Analysis_Score": 0, "Status_Prior_Value": [], "Business_Impact_Analysis_Archive": [], "Affected_Business_Unit": [], "DLP_Policy": [], "Incident_Analysis_Severity": ["Low"], "Current_Status": [], "Incident_Summary": null, "Encryption_Details": null, "Law_Enforcement_Agent": null, "Estimated_Hours": 0, "DateTime_Occurred": null, "Category": [], "Law_Enforcement_Agency": null, "Corrective_Actions": null, "Legal_Involvement_Details": null, "Range_Type": [], "Status_Change": ["No"], "Related_Incidents": [], "Investigations": [], "@odata.context": "http://xxx.xx.xx.xx/RSAarcher/contentapi/Incidents(250886)/$metadata#Incidents/$entity", "Filing_Name": null, "Recovery_": 0, "Inherited_Permissions_Engagement_Stakeho": [], "Organization_Affected_By_Incident": [], "Incident_ID": 29, "Days_Open": 0, "From_Date__Time": null, "Inherited_Permissions_Supplier_Request_F": [], "Legal_Involvement": [], "Notify_Crisis_Team": [" No, do not send an email notification"], "Recovery_Description": null, "Additional_Notification_Recipients": [], "Involved_Third_Parties": [], "Incident_Owner": [], "State": [], "Incident_Trend": [], "Top_Offending_Users": [], "Loss_Events": [], "City": null, "Last_Updated": "2020-11-26T10:04:23.08+02:00", "Incident_Status": ["New"], "Emergency_Notifications": [], "Notify_Incident_Owner": ["No, do not send an email notification to the incident owner"], "Loss_Description": null, "Inherited_From_Third_Party_Profile": [], "Incident_Resolution_Detail": null, "Cause": null, "Desktop_Policy_Enabled": [], "Policy_Enabled": [], "Address": null, "Customer_Data_Details": null, "Loss": 0, "Country": [], "Business_Continuity_Plans": [], "Incident_Details": null, "Is_BSA_Bank_Secrecy_Act_reporting_requir": ["No"], "Network_Policy_Enabled": [], "Reported_to_Police": [], "DateTime_Closed": null, "Incident_Manager": [], "Additional_Access": [], "Risks": []}
```



#### Create Incident
Create a new incident
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident Summary|The summary of the new incident.|False|String||
|Application Name|Specify an application name for the incident. Default: Incidents.|False|String|Incidents|
|Incident Details|The details (description) of the new incident.|False|String||
|Incident Owner|The owner of the new incident.|False|String||
|Incident Status|The status of the new incident.|False|String||
|Priority|The priority of the new incident.|False|String||
|Category|The category of the new incident.|False|String||
|Custom Fields|Specify a JSON object of fields that need to be used, when creating an incident . Example: {“Category”:“Malware”}.|False|String||
|Custom Mapping File|Specify an absolute path to the file that contains all of the required mapping. If “Remote File“ is enabled, then provide a URL that contains the mapping file. Please refer to action documentation for the additional information.|False|String||
|Remote File|If enabled, action will treat value provided in “Custom Mapping File“ as a URL and try to fetch a file from it.|False|Boolean|false|



##### JSON Results
```json
{"Incident_Analysis_Q8": [], "Open_TasksActivities": [], "Incident_Analysis_Q1": [], "Incident_Analysis_Q3": [], "Incident_Analysis_Q2": [], "Incident_Analysis_Q5": [], "Incident_Analysis_Q4": [], "DateTime_Reported": "2020-11-26T10:04:23+02:00", "Incident_Analysis_Q6": [], "Override_Rejected_Submission": ["No"], "Notification_Execution": [], "Data_Encrypted": [], "Escalated_Incident_Status": [], "Customer_Data": [], "Discovery_Policy_Enabled": [], "Total_Hours": 0, "DLP_Source_Product": [], "Workflow_Assignees": [], "Region": [], "Inherited_RP": [], "Incident_Result": ["To Be Determined"], "Incident_Analysis_Q7": [], "Google_Map": "", "Incidents_Id": 250886, "Facility": [], "Workflow_Stage": [], "Individuals_Involved": [], "Date_Created": "2020-11-26T10:04:23.08+02:00", "Zip_Code": null, "Impacted_Information_Assess": [], "Related_Incidents1": [], "Batch_File_Format": [], "Responder_Hours_Entry": [], "Priority": ["High"], "Source": [], "Default_Record_Permissions": ["IM: Admin", "IM: Read Only", "BCM: Admin"], "Law_Enforcement_Case_No": null, "Incident_Analysis_Score": 0, "Status_Prior_Value": [], "Business_Impact_Analysis_Archive": [], "Affected_Business_Unit": [], "DLP_Policy": [], "Incident_Analysis_Severity": ["Low"], "Current_Status": [], "Incident_Summary": null, "Encryption_Details": null, "Law_Enforcement_Agent": null, "Estimated_Hours": 0, "DateTime_Occurred": null, "Category": [], "Law_Enforcement_Agency": null, "Corrective_Actions": null, "Legal_Involvement_Details": null, "Range_Type": [], "Status_Change": ["No"], "Related_Incidents": [], "Investigations": [], "@odata.context": "http://xxx.xx.xx.xx/RSAarcher/contentapi/Incidents(250886)/$metadata#Incidents/$entity", "Filing_Name": null, "Recovery_": 0, "Inherited_Permissions_Engagement_Stakeho": [], "Organization_Affected_By_Incident": [], "Incident_ID": 29, "Days_Open": 0, "From_Date__Time": null, "Inherited_Permissions_Supplier_Request_F": [], "Legal_Involvement": [], "Notify_Crisis_Team": [" No, do not send an email notification"], "Recovery_Description": null, "Additional_Notification_Recipients": [], "Involved_Third_Parties": [], "Incident_Owner": [], "State": [], "Incident_Trend": [], "Top_Offending_Users": [], "Loss_Events": [], "City": null, "Last_Updated": "2020-11-26T10:04:23.08+02:00", "Incident_Status": ["New"], "Emergency_Notifications": [], "Notify_Incident_Owner": ["No, do not send an email notification to the incident owner"], "Loss_Description": null, "Inherited_From_Third_Party_Profile": [], "Incident_Resolution_Detail": null, "Cause": null, "Desktop_Policy_Enabled": [], "Policy_Enabled": [], "Address": null, "Customer_Data_Details": null, "Loss": 0, "Country": [], "Business_Continuity_Plans": [], "Incident_Details": null, "Is_BSA_Bank_Secrecy_Act_reporting_requir": ["No"], "Network_Policy_Enabled": [], "Reported_to_Police": [], "DateTime_Closed": null, "Incident_Manager": [], "Additional_Access": [], "Risks": []}
```



#### Ping
Test Connectivity
Timeout - 600 Seconds






## Jobs

#### Sync Security Incidents
This job will synchronize security incidents in RSA Archer and Siemplify.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|API Root|True|String|http://x.x.x.x/RSAarcher|
|Instance Name|True|String||
|Username|True|String||
|Password|True|Password|*****|
|Sync Fields|True|String||
|Verify SSL|False|Boolean|true|



## Connectors
#### RSA Archer - Security Incidents Connector
Pull Security Incidents from RSA Archer.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|API Root of the RSA Archer instance.|True|String|http://x.x.x.x/RSAarcher|
|Instance Name|Name of the RSA Archer instance.|True|String||
|Username|Username of the RSA Archer account. |True|String||
|Password|Password of the RSA Archer account.|True|Password|*****|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve security incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Max Security Incidents To Fetch|How many security incidents to process per one connector iteration.|False|Int|50|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Process Security Alerts|If enabled, connector will process Security Alerts related to the Security Incident.|False|Boolean|true|
|Process Incident Journal|If enabled, connector will process Incident Journal related to the Security Incident.|False|Boolean|true|
|Time Format|Specify, what should be the time format for the searching of Security Incidents.|True|String|%Y-%m-%d %H:%M:%S|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the RSA Archer server is valid.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




