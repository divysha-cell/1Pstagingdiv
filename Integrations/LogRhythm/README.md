
# LogRhythm

LogRhythm's security intelligence and analytics platform enables organizations to detect, contain and neutralize cyber threats with threat lifecycle management.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|None|True|String|https://{IP}:{PORT}|
|API Token|None|True|Password|*****|
|Verify SSL|None|False|Boolean|False|


#### Dependencies
| |
|-|
|charset_normalizer-3.3.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|idna-3.7-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|arrow-1.3.0-py3-none-any.whl|
|six-1.16.0-py2.py3-none-any.whl|
|certifi-2024.7.4-py3-none-any.whl|
|types_python_dateutil-2.9.0.20240316-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|


## Actions
#### List Entity Events
List events related to entities in LogRhythm. Supported entities: Hostname, IP Address, User, CVE, Hash, URL. Note: Action is running as async, please adjust script timeout value in Siemplify IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Time Frame|Specify a time frame for the results. If “Custom” is selected, you also need to provide “Start Time”.|False|List|Last Hour|
|Start Time|Specify the start time for the results. This parameter is mandatory, if “Custom” is selected for the “Time Frame” parameter. Format: ISO 8601. Example: 2021-04-23T12:38Z|False|String||
|End Time|Specify the end time for the results. Format: ISO 8601. If nothing is provided and “Custom” is selected for the “Time Frame” parameter then this parameter will use current time.|False|String||
|Sort Order|Specify the sorting logic for the query.|False|List|Datetime ASC|
|Max Events To Return|Specify how many events to return. Default: 50|False|String|50|



##### JSON Results
```json
[{"Entity":"EntityIdentifier", "EntityResult": [{"kBytes":1111.021111625,"kBytesIn":2500,"kBytesOut":21.011111625,"outboundKBytes":21.011111625,"impactedHostTotalKBytes":1111.021111625,"keyField":"messageId","count":1,"classificationId":1111,"classificationName":"Error","classificationTypeName":"Operations","commonEventName":"HTTP 504 : Server Error - Gateway Time-Out","commonEventId":1111,"direction":3,"directionName":"External","entityId":2,"entityName":"EchoTestEntity","rootEntityId":2,"rootEntityName":"EchoTestEntity","impactedEntityId":-100,"impactedEntityName":"Global Entity","impactedHost":"111.1.1.11","impactedInterface":"0","impactedIp":"111.1.1.11","impactedPort":80,"impactedZoneName":"External","indexedDate":1621111021111,"insertedDate":1621111431111,"logDate":1621111139789,"logMessage":"CISCONGFW EVENT Ev_Id=436 Ev","logSourceHost":"EchoTestHost","logSourceHostId":2,"logSourceHostName":"EchoTestHost","logSourceId":15,"logSourceName":"Echo_2_1000107","logSourceType":1000007,"logSourceTypeName":"Flat File - Cisco NGFW","messageId":"23066","messageTypeEnum":2,"mpeRuleId":1176829,"mpeRuleName":"HTTP 504 : Server Error : Gateway Timeout","normalDate":1621111431191,"normalDateMin":1621111431191,"normalMsgDateMax":1621111431191,"normalDateHour":1629122400000,"originEntityId":-100,"originEntityName":"Global Entity","originHostId":-1,"originHost":"111.1.1.11","originInterface":"0","originIp":"111.1.1.11","originPort":14042,"originZone":3,"originZoneName":"External","priority":38,"process":"5","processId":300003,"protocolId":6,"protocolName":"TCP","serviceId":1388,"serviceName":"HTTP","portProtocol":"HTTP","session":"436","severity":"57","url":"http://www.google.com/","vendorMessageId":"504","version":"2","status":"504"}]}]
```



#### Get Alarm Details
Get alarm details in LogRhythm
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alarm IDs|Specify a comma-separated list of alarm IDs for which we need to retrieve details.|True|String||
|Max Events To Fetch|Specify how many events to return. Default: 50.|False|String|50|



##### JSON Results
```json
[{"alarmRuleID":98,"alarmId":18755,"personId":-100,"alarmDate":"2021-08-17T13:36:39.78","alarmStatus":0,"alarmStatusName":"New","entityId":2,"entityName":"EchoTestEntity","alarmRuleName":"LogRhythm Agent Heartbeat Missed","lastUpdatedID":-100,"lastUpdatedName":"LogRhythm Administrator","dateInserted":"2021-08-17T13:36:39.807","dateUpdated":"2021-08-17T13:36:39.86","associatedCases":[],"lastPersonID":null,"eventCount":1,"eventDateFirst":"2021-08-17T13:36:37.057","eventDateLast":"2021-08-17T13:36:37.057","rbpMax":39,"rbpAvg":39,"smartResponseActions":null,"alarmDataCached":"N","alarmEventsDetails":[{"account":"admin5","action":"","amount":null,"bytesIn":null,"bytesOut":null,"classificationId":2600,"classificationName":"Compromise","classificationTypeName":"Security","command":"","commonEventId":1031412,"cve":"","commonEventName":"AIE: CSC: Disabled Account Auth Success","count":1,"directionId":0,"directionName":"Unknown","domain":"","duration":0,"entityId":-1000001,"entityName":"","group":"","impactedEntityId":-100,"impactedEntityName":"Global Entity","impactedHostId":-1,"impactedHostName":"","impactedInterface":"","impactedIP":null,"impactedLocation":{"countryCode":"","name":"","latitude":0,"locationId":0,"locationKey":"","longitude":0,"parentLocationId":0,"recordStatus":"Deleted","regionCode":"","type":"NULL","dateUpdated":"0001-01-01T00:00:00"},"impactedMAC":"","impactedName":"","impactedNATIP":"","impactedNATPort":null,"impactedNetwork":{"beginIPRange":{"value":""},"dateUpdated":"0001-01-01T00:00:00","riskThreshold":"","endIPRange":{"value":""},"entityId":0,"hostZone":"Unknown","locationId":0,"longDesc":"","name":"","networkId":0,"recordStatus":"Deleted","shortDesc":""},"impactedPort":-1,"impactedZone":"Unknown","itemsPacketsIn":0,"itemsPacketsOut":0,"logDate":"2021-08-16T09:51:16.993","login":"admin5","logMessage":"","logSourceHostId":-1000001,"logSourceHostName":"AI Engine Server","logSourceName":"AI Engine","logSourceTypeName":"LogRhythm AI Engine","messageId":173885,"mpeRuleId":-1,"mpeRuleName":"","normalDateMax":"0001-01-01T00:00:00","objectName":"","objectType":"","originEntityId":-100,"originEntityName":"Global Entity","originHostId":-1,"originHostName":"","originInterface":"","originIP":null,"originLocation":{"countryCode":"","name":"","latitude":0,"locationId":0,"locationKey":"","longitude":0,"parentLocationId":0,"recordStatus":"Deleted","regionCode":"","type":"NULL","dateUpdated":"0001-01-01T00:00:00"},"originMAC":"","originName":"","originNATIP":"","originNATPort":null,"originNetwork":{"beginIPRange":{"value":""},"dateUpdated":"0001-01-01T00:00:00","riskThreshold":"","endIPRange":{"value":""},"entityId":0,"hostZone":"Unknown","locationId":0,"longDesc":"","name":"","networkId":0,"recordStatus":"Deleted","shortDesc":""},"originPort":-1,"originZone":"Unknown","parentProcessId":"","parentProcessName":"","parentProcessPath":"","policy":"","priority":91,"process":"","processId":-1,"protocolId":-1,"protocolName":"","quantity":0,"rate":0,"reason":"","recipient":"","result":"","responseCode":"","sender":"","session":"","recipientIdentityId":null,"recipientIdentityName":""}]}]
```



#### Attach File To Case
Attach file to case in LogRhythm. Note: Action is running as async, please adjust script timeout value in Siemplify IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case ID|Specify the ID of the case to which you want to attach files.|True|String||
|File Paths|Specify a comma-separate list of absolute file paths.|True|String||
|Note|Specify a note that should be added to the case alongside the file.|False|String||



##### JSON Results
```json
[{"number":"xxx","dateCreated":"2021-09-04T14:30:43.62Z","dateUpdated":"2021-09-04T14:30:43.62Z","createdBy":{"number":-100,"name":"LogRhythm Administrator","disabled":false},"lastUpdatedBy":{"number":-100,"name":"LogRhythm Administrator","disabled":false},"type":"file","status":"completed","statusMessage":null,"text":"test doc","pinned":false,"datePinned":null,"file":{"name":"tesst.txt","size":8}}]
```



#### Update Alarm
Update Alarm in LogRhythm.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alarm ID|Specify the ID of the alarm that needs to be updated in LogRhythm.|True|String||
|Status|Specify the status for the alarm.|False|List|Select One|
|Risk Score|Specify a new risk score for the alarm. Maximum: 100.|False|String||



#### Create Case
Create a case in LogRhythm.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Specify the name for the case.|True|String||
|Priority|Specify the priority for the case.|True|List|1|
|Due Date|Specify the due date for the case. Format: ISO 8601. Example: 2021-04-23T12:38Z|False|String||
|Description|Specify a description for the case.|False|String||



##### JSON Results
```json
"{\"id\":\"Bxx10xxx-xxx-xxx-xx-8xxxFxx7xxx\",\"number\":2,\"externalId\":\"\",\"dateCreated\":\"2021-08-11T12:37:42.8942168Z\",\"dateUpdated\":\"2021-08-11T12:37:42.8942168Z\",\"dateClosed\":null,\"owner\":{\"number\":-100,\"name\":\"LogRhythm Administrator\",\"disabled\":false},\"lastUpdatedBy\":{\"number\":-100,\"name\":\"LogRhythm Administrator\",\"disabled\":false},\"name\":\"System Compromise\",\"status\":{\"name\":\"Created\",\"number\":1},\"priority\":1,\"dueDate\":\"2019-08-24T14:15:22Z\",\"resolution\":null,\"resolutionDateUpdated\":null,\"resolutionLastUpdatedBy\":null,\"summary\":\"Investigated a potential system compromise. More details at http://example.com/.\",\"entity\":{\"number\":-100,\"name\":\"Global Entity\",\"fullName\":\"Global Entity\"},\"collaborators\":[{\"number\":-100,\"name\":\"LogRhythm Administrator\",\"disabled\":false}],\"tags\":[]}"
```



#### Add Alarm To Case
Add alarm to case in LogRhythm.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case ID|Specify the ID of the case to which you want to add alarms.|True|String||
|Alarm IDs|Specify a comma-separated list of alarms that need to be added to the case.|True|String||



##### JSON Results
```json
"[{\"number\":23,\"dateCreated\":\"2021-08-11T09:02:17.0066667Z\",\"dateUpdated\":\"2021-08-11T09:02:17.0066667Z\",\"createdBy\":{\"number\":-100,\"name\":\"LogRhythm Administrator\",\"disabled\":false},\"lastUpdatedBy\":{\"number\":-100,\"name\":\"LogRhythm Administrator\",\"disabled\":false},\"type\":\"alarm\",\"status\":\"completed\",\"statusMessage\":null,\"text\":\"\",\"pinned\":false,\"datePinned\":null,\"alarm\":{\"alarmId\":15298,\"alarmDate\":\"2021-07-30T02:07:29.813+03:00\",\"alarmRuleId\":1000,\"alarmRuleName\":\"AIE: ISO-27001: File Monitoring Event-File Changes\",\"dateInserted\":\"2021-07-30T02:07:29.82+03:00\",\"entityId\":-100,\"entityName\":\"Global Entity\",\"riskBasedPriorityMax\":1}},{\"number\":24,\"dateCreated\":\"2021-08-11T09:03:18.65Z\",\"dateUpdated\":\"2021-08-11T09:03:18.65Z\",\"createdBy\":{\"number\":-100,\"name\":\"LogRhythm Administrator\",\"disabled\":false},\"lastUpdatedBy\":{\"number\":-100,\"name\":\"LogRhythm Administrator\",\"disabled\":false},\"type\":\"alarm\",\"status\":\"completed\",\"statusMessage\":null,\"text\":\"\",\"pinned\":false,\"datePinned\":null,\"alarm\":{\"alarmId\":15297,\"alarmDate\":\"2021-07-30T02:07:28.353+03:00\",\"alarmRuleId\":1419,\"alarmRuleName\":\"AIE: CCF: FIM General Activity\",\"dateInserted\":\"2021-07-30T02:07:29.82+03:00\",\"entityId\":1,\"entityName\":\"Primary Site\",\"riskBasedPriorityMax\":0}}]"
```



#### List Case Evidence
List case evidence in LogRhythm.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case ID|Specify the ID of the case for which you want to return a list of evidence.|True|String||
|Status Filter|Specify a comma-separated list of status filters for the evidence. Possible values: pending, completed, failed. If nothing is provided, action will return evidence from all statuses.|False|String||
|Type Filter|Specify a comma-separated list of type filters for the evidence. Possible values: alarm, userEvents, log, note, file. If nothing is provided, action will return evidence from all types.|False|String||
|Max Evidences To Return|Specify how much evidence to return. Default: 50.|False|String|50|



##### JSON Results
```json
[{"number":0,"dateCreated":"2021-09-02T09:00:37.7333333Z","dateUpdated":"2021-09-02T09:00:37.7333333Z","createdBy":{"number":-100,"name":"LogRhythm Administrator","disabled":false},"lastUpdatedBy":{"number":-100,"name":"LogRhythm Administrator","disabled":false},"type":"alarm","status":"completed","statusMessage":null,"text":"","pinned":false,"datePinned":null,"alarm":{"alarmId":"152xxx","alarmDate":"2021-07-30T02:07:28.353+03:00","alarmRuleId":"14xxx","alarmRuleName":"AIE: CCF: FIM General Activity","dateInserted":"2021-07-30T02:07:29.82+03:00","entityId":1,"entityName":"Primary Site","riskBasedPriorityMax":50}},{"number":0,"dateCreated":"2021-09-01T17:28:39.7Z","dateUpdated":"2021-09-01T17:28:39.7Z","createdBy":{"number":-100,"name":"LogRhythm Administrator","disabled":false},"lastUpdatedBy":{"number":-100,"name":"LogRhythm Administrator","disabled":false},"type":"file","status":"completed","statusMessage":null,"text":"Test file","pinned":false,"datePinned":null,"file":{"name":"filename.txt","size":8}}]
```



#### Update Case
Update a case in LogRhythm.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case ID|Specify the id of the case that needs to be updated.|True|String||
|Name|Specify a new name for the case.|False|String||
|Priority|Specify a new priority for the case.|False|List|Select One|
|Due Date|Specify a new due date for the case. Format: ISO 8601. Example: 2021-04-23T12:38Z|False|String||
|Description|Specify a new description for the case.|False|String||
|Resolution|Specify how the case was resolved.|False|String||
|Status|Specify the new status for the case.|False|List|Select One|



##### JSON Results
```json
"{\"id\":\"Bxx10xxx-xxx-xxx-xx-8xxxFxx7xxx\",\"number\":2,\"externalId\":\"\",\"dateCreated\":\"2021-08-11T12:37:42.8942168Z\",\"dateUpdated\":\"2021-08-11T12:48:52.9765558Z\",\"dateClosed\":null,\"owner\":{\"number\":-100,\"name\":\"LogRhythm Administrator\",\"disabled\":false},\"lastUpdatedBy\":{\"number\":-100,\"name\":\"LogRhythm Administrator\",\"disabled\":false},\"name\":\"System Compromise\",\"status\":{\"name\":\"Created\",\"number\":1},\"priority\":1,\"dueDate\":\"2019-08-24T14:15:22Z\",\"resolution\":null,\"resolutionDateUpdated\":null,\"resolutionLastUpdatedBy\":null,\"summary\":\"Investigated a potential system compromise. More details at http://example.com/.\",\"entity\":{\"number\":-100,\"name\":\"Global Entity\",\"fullName\":\"Global Entity\"},\"collaborators\":[{\"number\":-100,\"name\":\"LogRhythm Administrator\",\"disabled\":false}],\"tags\":[]}"
```



#### Enrich Entities
Enrich entities using information from LogRhythm. Supported entities: Hostname, IP Address.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Create Insight|If enabled, action will create an insight containing all of the retrieved information about the entity.|False|Boolean|true|



##### JSON Results
```json
[{"Entity":"EntityIdentifier", "EntityResult": {"id":2,"entity":{"id":2,"name":"EntityIdentifier"},"name":"EntityIdentifier","shortDesc":"LogRhythm ECHO","riskLevel":"None","threatLevel":"None","threatLevelComments":"","recordStatusName":"Active","hostZone":"Internal","location":{"id":-1},"os":"Windows","osVersion":"Microsoft Windows NT 6.2.9200.0","useEventlogCredentials":false,"osType":"Server","dateUpdated":"2021-04-14T09:18:17.677Z","hostRoles":[],"hostIdentifiers":[{"type":"IPAddress","value":"22.2.2.22","dateAssigned":"2021-04-14T09:17:31Z"},{"type":"WindowsName","value":"EntityIdentifier","dateAssigned":"2021-04-14T09:17:31Z"}]}}]
```



#### Download Case Files
Download files related to the case in LogRhythm.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case ID|Specify the id of the case from which you want to download files.|True|String||
|Download Folder Path|Specify the path to the folder, where you want to store the case files.|True|String||
|Overwrite|If enabled, action will overwrite the file with the same name.|False|Boolean|false|



##### JSON Results
```json
{"absolute_file_paths": ["test_file1.txt", "test_file2.txt"]}
```



#### Add Comment To Alarm
Add comment to alarm in LogRhythm.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alarm ID|Specify the ID of the alarm to which you need to add a comment in LogRhythm.|True|String||
|Comment|Specify a comment that needs to be added to the alarm.|True|String||



#### Ping
Test connectivity to the LogRhythm with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Add Note To Case
Add a note to the case in LogRhythm.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case ID|Specify the ID of the case to which you want to add a note.|True|String||
|Note|Specify a note that should be added to the case.|True|String||



##### JSON Results
```json
"{\"number\":29,\"dateCreated\":\"2021-xx-11T12:21:11.xx4730xx\",\"dateUpdated\":\"2021-xx-11T12:21:11.xx4730xx\",\"createdBy\":{\"number\":-100,\"name\":\"LogRhythm Axx\",\"disabled\":false},\"lastUpdatedBy\":{\"number\":-100,\"name\":\"LogRhythm Axx\",\"disabled\":false},\"type\":\"note\",\"status\":\"completed\",\"statusMessage\":null,\"text\":\"axxxx\",\"pinned\":false,\"datePinned\":null}"
```






## Jobs

#### Sync Alarm Comments
This job will synchronize comments in LogRhythm alarms and Siemplify cases. Note: job will only sync LogRhythm alarms with status “New”, “Open”, “Working” and “Escalated”.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Api Root|True|String|https:/{{IP}}:8501|
|Api Token|True|Password|*****|
|Verify SSL|False|Boolean|true|

#### Sync Closed Cases
This job will synchronize closed LogRhythm cases and Siemplify alerts. Note: in LogRhythm statuses “Completed” and “Resolved” are treated as closed.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Api Root|True|String|https:/{{IP}}:8501|
|Api Token|True|Password|*****|
|Verify SSL|False|Boolean|true|
|Max Hours Backwards|False|String|24|

#### Sync Closed Alarms
This job will synchronize closed LogRhythm alarms and Siemplify alerts. Note: in LogRhythm statuses “Closed”, “Closed False Alarm”, “Closed Resolved”, “Closed Unresolved”, “Closed Reported”, “Closed Monitor” are treated as closed.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Api Root|True|String|https:/{{IP}}:8501|
|Api Token|True|Password|*****|
|Verify SSL|False|Boolean|true|
|Max Hours Backwards|False|String|24|

#### Sync Case Comments
This job will synchronize comments in LogRhythm cases and Siemplify cases. Note: job will only sync LogRhythm cases with status "Created", "Incident" and "Mitigated".

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Api Root|True|String|https:/{{IP}}:8501|
|Api Token|True|Password|*****|
|Verify SSL|False|Boolean|true|



## Connectors
#### LogRhythm Cases Connector
Pull cases from LogRhythm.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|Api Root|API root of the LogRhythm instance.|True|String|https:/{{IP}}:8501|
|Api Token|LogRhythm API token|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the LogRhythm server is valid.|False|Boolean|false|
|Alerts Count Limit|How many cases to process per one connector iteration.|True|Int|10|
|Max Days Backwards|Number of days before the first connector iteration to retrieve cases from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|Int|1|
|Lowest Priority To Fetch|The lowest priority that needs to be used to fetch cases. If nothing is provided, cases with all priorities will be ingested. Possible values: from 1 to 5.|False|Int||
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|


#### LogRhythm - Rest API Alarms Connector
Pull alerts from LogRhythm using Rest API. Note: this connector is only supported for LogRhythm version 7.7+.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API root of the LogRhythm instance.|True|String|https://{IP}:8501|
|API Token|LogRhythm API token.|True|Password|*****|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Max Alarms To Fetch|How many alerts to process per one connector iteration.|False|Int|10|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the LogRhythm server is valid.|False|Boolean|false|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




