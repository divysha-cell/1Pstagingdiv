
# MicrosoftDefenderATP

Microsoft Defender Advanced Threat Protection (Microsoft Defender ATP) is a unified platform for preventative protection, post-breach detection, automated investigation, and response. Microsoft Defender ATP protects endpoints from cyber threats, detects advanced attacks and data breaches, automates security incidents and improves security posture. Google SecOps integration for Microsoft Defender ATP provides a list of actions to pull the data stored in Microsoft Defender ATP and use it in Google SecOps playbooks and manual actions, as well as a series of active response actions, such as isolate specific host or restrict app execution on host. In addition, integration provides a connector to ingest Microsoft Defender ATP alerts as Google SecOps Cases.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Login API Root|None|True|String|https://login.microsoftonline.com|
|Api Root|None|True|String|https://api.securitycenter.windows.com|
|Graph API Root|The base URL for the Microsoft Graph API (e.g., https://graph.microsoft.com). If provided, V2 API endpoints will be used.|False|String||
|Client ID|None|True|String||
|Client Secret|None|True|Password|*****|
|Azure Active Directory ID|None|True|String||
|Verify SSL|None|False|Boolean|True|


#### Dependencies
| |
|-|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|cryptography-43.0.1-cp39-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|anyio-4.6.2.post1-py3-none-any.whl|
|httpcore-1.0.6-py3-none-any.whl|
|TIPCommon-2.0.4-py2.py3-none-any.whl|
|proto_plus-1.25.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|h11-0.14.0-py3-none-any.whl|
|PyJWT-2.9.0-py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|google_api_python_client-2.152.0-py2.py3-none-any.whl|
|pyasn1_modules-0.4.1-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|pyparsing-3.2.0-py3-none-any.whl|
|charset_normalizer-3.4.0-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cffi-1.17.1-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|pycparser-2.22-py3-none-any.whl|
|googleapis_common_protos-1.66.0-py2.py3-none-any.whl|
|google_api_core-2.23.0-py3-none-any.whl|
|protobuf-5.28.3-cp38-abi3-manylinux2014_x86_64.whl|
|chardet-5.2.0-py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|httpx-0.27.2-py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|pyOpenSSL-24.2.1-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|pycryptodome-3.21.0-cp36-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|certifi-2024.8.30-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|google_auth-2.36.0-py2.py3-none-any.whl|
|cachetools-5.5.0-py3-none-any.whl|


## Actions
#### Get Machine Recommendations
Use the Get Machine Recommendations action to retrieve a list of security recommendations for specific machines in Microsoft Defender for Endpoint.Supported Entities: IP Address, Hostname.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Recommendations To Return|The maximum number of recommendations to return for each entity. Maximum: 100.|True|String|100|



##### JSON Results
```json
[{"Entity":"", "EntityResult": [{"id":"dummy-_-7-id-_-7-zip","productName":"7-zip","recommendationName":"Update 7-zip to version 25.01.0.0","weaknesses":12,"vendor":"7-zip","recommendedVersion":"25.01.0.0","recommendedVendor":"","recommendedProgram":"","recommendationCategory":"Application","subCategory":"","severityScore":0.0,"publicExploit":true,"activeAlert":false,"associatedThreats":[],"remediationType":"Update","status":"Active","configScoreImpact":0.0,"exposureImpact":0.0,"totalMachineCount":1,"exposedMachinesCount":1,"nonProductivityImpactedAssets":0,"relatedComponent":"7-zip","hasUnpatchableCve":false,"tags":[],"exposedCriticalDevices":0}]}]
```



#### Wait Task Status
Wait for Task Status
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Task IDs|Task IDs list. Comma-separated string|True|String||



##### JSON Results
```json
[{"status": "Succeeded", "creation_date_time_utc": "2020-02-08T03:24:52.8526634Z", "cancellation_requestor": null, "cancellation_date_time_utc": null, "id": "2e39d22e-60a7-4267-899c-a1471e800000", "last_update_date_time_utc": "2020-02-08T03:25:35.8345081Z", "related_file_info": null, "cancellation_comment": null, "requestor": "e4fc6454-754d-47f7-bbdb-045fad600000", "error_h_result": 0, "scope": "Selective", "machine_id": "fbc85cf3fbcc8bb14d1a84fcf7bbae4531f00000", "type": "Isolate", "requestor_comment": "test"}]
```



#### Create Unisolate Machine Task
Create Unisolate Machine Task
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Comment|Comment why the machine needs to be isolated|True|String||



##### JSON Results
```json
[{"status": "Pending", "creation_date_time_utc": "2020-02-08T03:25:52.9805348Z", "cancellation_requestor": null, "cancellation_date_time_utc": null, "id": "00000000-0000-0000-0000-000000000000", "last_update_date_time_utc": "2020-02-08T03:25:52.9805348Z", "related_file_info": null, "cancellation_comment": null, "requestor": "00000000-0000-0000-0000-000000000000", "error_h_result": 0, "scope": null, "machine_id": "0000000000000000000000000000000000000000", "type": "Unisolate", "requestor_comment": "test"}]
```



#### Create Stop And Quarantine File Specific Machine Task
Create Stop and Quarantine a File on Specific Machine Task
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|SHA1 File Hash to Quarantine|SHA1 File Hash to Quarantine|True|String||
|Comment|Comment to associate with the action|True|String||



##### JSON Results
```json
[{"status": "Pending", "creation_date_time_utc": "2020-02-08T03:27:01.8730344Z", "cancellation_requestor": null, "cancellation_date_time_utc": null, "id": "00000000-0000-0000-0000-000000000000", "last_update_date_time_utc": "2020-02-08T03:27:01.8730344Z", "related_file_info": {"file_identifier": "0000000000000000000000000000000000000000", "file_identifier_type": "Sha1"}, "cancellation_comment": null, "requestor": "00000000-0000-0000-0000-000000000000", "error_h_result": 0, "scope": null, "machine_id": "0000000000000000000000000000000000000000", "type": "StopAndQuarantineFile", "requestor_comment": "test"}]
```



#### List Machines
Get Machines
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Last Seen Time Frame|Time frame in hours for which to fetch Machines|False|String||
|Machine Name|Full Machine Name to look for|False|String||
|Machine IP Address|Machine IP Address to look for|False|String||
|Machine Risk Score|Machine risk score to look for. Comma-separated string.|False|String|None, Low, Medium, High|
|Machine Health Status|Machine health status to look for. Comma-separated string|False|String|Active, Inactive, ImpairedCommunication, NoSensorData, NoSensorDataImpairedCommunication|
|Machine OS Platform|Machine OS platform to look for.|False|String||
|RBAC Group ID|RBAC Group ID to look for.|False|String||



##### JSON Results
```json
[{"aad_device_id": null, "machine_tags": [], "last_external_ip_address": "2.2.2.2", "rbac_group_id": 220, "computer_dns_name": "computer_dns_name", "os_processor": "x64", "exposure_level": "Medium", "last_ip_address": "1.1.1.1", "os_build": 17134, "agent_version": "10.4860.17134.982", "risk_score": "Low", "os_version": null, "health_status": "Active", "version": "1803", "rbac_group_name": "UnassignedGroup", "first_seen": "2019-12-20T10:10:01.7952265Z", "os_platform": "Windows10", "id": "fbc85cf3fbcc8bb14d1a84fcf7bbae4531f00000", "last_seen": "2020-02-07T08:23:30.6044761Z"}, {"aad_device_id": null, "machine_tags": [], "last_external_ip_address": "2.2.2.2", "rbac_group_id": 220, "computer_dns_name": "computer_dns_name", "os_processor": "x64", "exposure_level": "Medium", "last_ip_address": "1.1.1.1", "os_build": 17134, "agent_version": "10.4860.17134.982", "risk_score": "None", "os_version": null, "health_status": "Inactive", "version": "1803", "rbac_group_name": "UnassignedGroup", "first_seen": "2019-12-20T10:53:11.4374496Z", "os_platform": "Windows10", "id": "9ec547f3da0c42676769aaf8709dbb7367100000", "last_seen": "2020-01-26T15:22:55.6940892Z"}, {"aad_device_id": null, "machine_tags": [], "last_external_ip_address": "2.2.2.2", "rbac_group_id": 220, "computer_dns_name": "computer_dns_name", "os_processor": "x64", "exposure_level": "Medium", "last_ip_address": "1.1.1.1", "os_build": 17134, "agent_version": "10.4860.17134.982", "risk_score": "High", "os_version": null, "health_status": "NoSensorData", "version": "1803", "rbac_group_name": "UnassignedGroup", "first_seen": "2019-12-20T10:29:04.4328354Z", "os_platform": "Windows10", "id": "52f45d3b4f17e2ee1e24355d774fe1f0ea600000", "last_seen": "2020-01-09T10:08:22.7982861Z"}]
```



#### Get User Related Alerts
Use the Get User Related Alerts action to list alerts associated with specific users in Microsoft Defender for Endpoint. Supported Entities: User.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Alerts To Return|The maximum number of alerts to retrieve for each user. Maximum: 100.|True|String|100|



##### JSON Results
```json
[{"Entity": "user@example.com", "EntityResult": [{"id": "alert_id_1", "incidentId": 12345, "investigationId": 67890, "assignedTo": "Admin", "severity": "Medium", "status": "New", "classification": "Unknown", "determination": "Unknown", "detectionSource": "Antivirus", "category": "Malware", "threatFamilyName": "WannaCry", "title": "Suspicious Activity Detected", "description": "Multiple failed login attempts followed by a successful one.", "alertCreationTime": "2024-03-16T12:00:00.0000000Z", "firstEventTime": "2024-03-16T11:50:00.0000000Z", "lastEventTime": "2024-03-16T11:55:00.0000000Z", "lastUpdateTime": "2024-03-16T12:05:00.0000000Z", "resolvedTime": null, "machineId": "machine_id_xyz", "comments": [], "evidence": []}]}]
```



#### Get File Related Machines
Get File Related Machines. Note: For this action only SHA1 is supported
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Machine Name|Full Machine Name to look for|False|String||
|Machine IP Address|Machine IP Address to look for|False|String||
|Machine Risk Score|Machine risk score to look for. Comma-separated string.|False|String|None, Low, Medium, High|
|Machine Health Status|Machine health status to look for. Comma-separated string|False|String|Active, Inactive, ImpairedCommunication, NoSensorData, NoSensorDataImpairedCommunication|
|Machine OS Platform|Machine OS platform to look for.|False|String||
|RBAC Group ID|RBAC Group ID to look for.|False|String||



##### JSON Results
```json
[{"EntityResult": [{"aad_device_id": null, "machine_tags": [], "last_external_ip_address": "1.1.1.1", "rbac_group_id": 220, "computer_dns_name": "EXAMPLE-HOST", "os_processor": "x64", "exposure_level": "Low", "last_ip_address": "1.1.1.1", "os_build": 18363, "agent_version": "10.6940.18362.778", "risk_score": "High", "os_version": null, "health_status": "Active", "version": "1909", "rbac_group_name": "UnassignedGroup", "first_seen": "2020-05-22T09:40:25.8490002Z", "os_platform": "Windows10", "id": "32ad71569ed6b78fc46af06aff3a48533f00c21c", "last_seen": "2020-08-10T08:40:13.8704644Z"}], "Entity": "eb3b03616eee42f16d0703f64de23e7e34fe8524"}]
```



#### Create Isolate Machine Task
Create Isolate Machine Task
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Isolation Type|Isolation type|True|List|Full|
|Comment|Comment why the machine needs to be isolated|True|String||



##### JSON Results
```json
[{"status": "Pending", "creation_date_time_utc": "2020-02-08T03:24:52.9395805Z", "cancellation_requestor": null, "cancellation_date_time_utc": null, "id": "00000000-0000-0000-0000-000000000000", "last_update_date_time_utc": "2020-02-08T03:24:52.9395805Z", "related_file_info": null, "cancellation_comment": null, "requestor": "00000000-0000-0000-0000-000000000000", "error_h_result": 0, "scope": null, "machine_id": "0000000000000000000000000000000000000000", "type": "Isolate", "requestor_comment": "test"}]
```



#### List Alerts
Get Alerts
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Time Frame|Time frame in hours for which to fetch Alerts|False|String|3|
|Status|Statuses of the alert to look for. Comma-separated string|False|String|Unknown, New, InProgress, Resolved|
|Severity|Severities of the alert to look for. Comma-separated string.|False|String||
|Category|Categories of the alert to look for. Comma-separated string.|False|String||
|Incident ID|Microsoft Defender Incident ID for which you want to find related alerts.|False|String||



##### JSON Results
```json
[{"last_update_time": "2020-02-06T17:29:59.9366667Z", "last_event_time": "2020-02-06T13:54:01.6987896Z", "classification": "TruePositive", "alert_processes": null, "investigation_state": "SuccessfullyRemediated", "threat_family_name": "Mikatz", "id": "da637165941782625606_-143200000", "category": "Malware", "severity": "High", "title": "'Mikatz' high-severity malware was detected", "comments": [], "resolved_time": "2020-02-06T17:29:29.8100012Z", "status": "Resolved", "description": "High-severity malware refers tools used by advanced Threat Activity Groups to target victims. Such Activity Groups may target individuals or institutions. They typically engage on industrial, military, diplomatic, and political espionage rather than more mundane activities such as identity theft or denial of service attacks.  Some groups engage in acts of deliberate sabotage and destruction in order to cause real-world effects, such as disruptions to the victim's operations.\n\nThis category of malware includes tools such as:\n- Exploits used to gain access to targeted computers or escalate privileges on infected computers;\n- Backdoors used to maintain persistent command and control over infected computers in a stealthy manner;\n- Lateral movement tools that permit attackers to scan the local network, locate targets of interest, and access additional computers; \n- Counter-forensics tools used to delay and disrupt incident response activities, including destructive malware that can render computers inoperable; \n- \"Weaponized\" tools that enable acts of deliberate sabotage or destruction or denial of service.", "alert_creation_time": "2020-02-06T13:56:18.2156945Z", "alert_domains": null, "alert_ips": null, "detection_source": "WindowsDefenderAv", "determination": "Other", "alert_files": [], "incident_id": 14, "investigation_id": 9, "first_event_time": "2020-02-06T13:54:01.6987896Z", "assigned_to": "Me", "alert_user": null, "machine_id": "4b4501882fb329d2c13896b0fe6c004763100000"}]
```



#### Get File Related Alerts
Deprecated. Get File Related Alerts. Note: For this action only SHA1 is supported
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Status|Statuses of the alert to look for. Comma-separated string|False|String|Unknown, New, InProgress, Resolved|
|Severity|Severities of the alert to look for. Comma-separated string.|False|String|UnSpecified, Informational, Low, Medium, High|
|Category|Categories of the alert to look for. Comma-separated string.|False|String||
|Incident ID|Microsoft Defender Incident ID for which you want to find related alerts.|False|String||



##### JSON Results
```json
[{"EntityResult": [{"last_update_time": "2020-07-13T15:45:44.7166667Z", "last_event_time": "2020-07-13T07:22:10.2377309Z", "classification": null, "alert_processes": null, "investigation_state": "UnsupportedAlertType", "threat_family_name": null, "id": "da637302519433626583_1251795154", "category": "Persistence", "severity": "Medium", "title": "Sticky Keys binary hijack detected", "comments": [], "resolved_time": null, "status": "New", "description": "Sticky keys binary hijack is a persistence technique that allows an adversary to obtain access to a system without authentication. The attacker takes advantage of a accessibility feature that allows one to invoke the feature directly from the logon screen by pressing the SHIFT key five times. If the attacker manages to swap out the underlying binary, the attacker can execute that binary without authentication.", "alert_creation_time": "2020-07-13T15:45:43.2689204Z", "alert_domains": null, "alert_ips": null, "detection_source": "WindowsDefenderAtp", "determination": null, "alert_files": [], "incident_id": 58, "investigation_id": null, "first_event_time": "2020-07-13T07:22:10.2377309Z", "assigned_to": null, "alert_user": null, "machine_id": "32ad71569ed6b78fc46af06aff3a48533f00c21c"}], "Entity": "eb3b03616eee42f16d0703f64de23e7e34fe8524"}]
```



#### Update Alert
Update Alerts
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Microsoft Defender ATP Alert ID to update.|True|String||
|Status|Status of the alert|False|List|New|
|Assigned To|User who is assigned to this alert|False|String||
|Classification|Classification to update alert with|False|List|Unknown|
|Determination|Determination to update alert with|False|List|NotAvailable|



##### JSON Results
```json
{"last_update_time": "2020-08-11T07:18:20.2166667Z", "last_event_time": "2020-08-10T16:40:00.6435038Z", "classification": "FalsePositive", "alert_processes": null, "investigation_state": "PendingApproval", "threat_family_name": null, "id": "da637326745323896920_864388402", "category": "SuspiciousActivity", "severity": "High", "title": "Love", "comments": [], "resolved_time": null, "status": "InProgress", "description": "Love", "alert_creation_time": "2020-08-10T16:42:12.2490966Z", "alert_domains": null, "alert_ips": null, "detection_source": "CustomerTI", "determination": "UnwantedSoftware", "alert_files": [], "incident_id": 78, "investigation_id": 42, "first_event_time": "2020-08-10T16:40:00.6435038Z", "assigned_to": "Automation", "alert_user": null, "machine_id": "32ad71569ed6b78fc46af06aff3a48533f00c21c"}
```



#### Get Machine Logon Users
Get Machine Log on users
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": [{"is_only_network_user": null, "logon_types": "Batch, Network, RemoteInteractive, Interactive", "id": "EXAMPLE-HOST\\admin", "first_seen": "2020-07-12T10:01:47Z", "least_prevalent_machine_id": null, "account_domain": "EXAMPLE-HOST", "account_name": "admin", "account_sid": null, "most_prevalent_machine_id": null, "log_on_machines_count": null, "is_domain_admin": true, "last_seen": "2020-08-10T14:07:07Z"}], "Entity": "EXAMPLE-HOST"}]
```



#### Get Machine Related Alerts
Deprecated. Get Machine Related Alerts
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Status|Statuses of the alert to look for. Comma-separated string|False|String|Unknown, New, InProgress, Resolved|
|Severity|Severities of the alert to look for. Comma-separated string.|False|String|UnSpecified, Informational, Low, Medium, High|
|Category|Categories of the alert to look for. Comma-separated string.|False|String||
|Incident ID|Microsoft Defender Incident ID for which you want to find related alerts.|False|String||



##### JSON Results
```json
[{"EntityResult": [{"last_update_time": "2020-05-31T10:39:41.7366667Z", "last_event_time": "2020-05-22T14:34:28.6016656Z", "classification": null, "alert_processes": null, "investigation_state": "TerminatedBySystem", "threat_family_name": null, "id": "da637257464665944733_-2050268322", "category": "Ransomware", "severity": "Medium", "title": "Ransomware associated with an exploitation campaign", "comments": [], "resolved_time": null, "status": "New", "description": "This file is a ransomware threat associated with exploitation of vulnerable internet-facing web services.  It might encrypt content on this computer, rendering it unusable to users.  In server environments, this may disrupt web services provided.", "alert_creation_time": "2020-05-22T12:14:26.5788604Z", "alert_domains": null, "alert_ips": null, "detection_source": "WindowsDefenderAtp", "determination": null, "alert_files": [], "incident_id": 36, "investigation_id": 24, "first_event_time": "2020-05-22T12:09:22.1963961Z", "assigned_to": null, "alert_user": null, "machine_id": "ac5fd76f04a07106948b39b4f3f3618554731d00"}, {"last_update_time": "2020-05-31T10:39:41.7366667Z", "last_event_time": "2020-05-22T14:34:28.6016656Z", "classification": null, "alert_processes": null, "investigation_state": "TerminatedBySystem", "threat_family_name": null, "id": "da637257464677148781_-975260009", "category": "Ransomware", "severity": "Medium", "title": "Ransomware associated with an exploitation campaign", "comments": [], "resolved_time": null, "status": "New", "description": "This file is a ransomware threat associated with exploitation of vulnerable internet-facing web services.  It might encrypt content on this computer, rendering it unusable to users.  In server environments, this may disrupt web services provided.", "alert_creation_time": "2020-05-22T12:14:27.6992552Z", "alert_domains": null, "alert_ips": null, "detection_source": "WindowsDefenderAtp", "determination": null, "alert_files": [], "incident_id": 36, "investigation_id": 24, "first_event_time": "2020-05-22T12:09:22.1963961Z", "assigned_to": null, "alert_user": null, "machine_id": "ac5fd76f04a07106948b39b4f3f3618554731d00"}], "Entity": "EXAMPLE-HOST"}]
```



#### Delete Entity Indicators
Delete entity indicators in Microsoft Defender ATP. Supported entities: Filehash, URL, IP Address. Note: only MD5, SHA1 and SHA256 hashes are supported.
Timeout - 600 Seconds



#### Get Current Task Status
Get Current Task Status
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Task IDs|Task IDs list. Comma-separated string|True|String||



##### JSON Results
```json
[{"status": "Succeeded", "creation_date_time_utc": "2020-02-08T03:24:52.8526634Z", "cancellation_requestor": null, "cancellation_date_time_utc": null, "id": "00000000-0000-0000-0000-000000000000", "last_update_date_time_utc": "2020-02-08T03:25:35.8345081Z", "related_file_info": null, "cancellation_comment": null, "requestor": "00000000-0000-0000-0000-000000000000", "error_h_result": 0, "scope": "Selective", "machine_id": "0000000000000000000000000000000000000000", "type": "Isolate", "requestor_comment": "test"}]
```



#### Enrich Entities
This action allows a user to enrich Microsoft Defender ATP hosts, ips and file hashes. Note: File hash can be in sha1 or sha256 format.
Timeout - 600 Seconds



##### JSON Results
```json
"[{\"EntityResult\": {\"aad_device_id\": \"123-123-123-123-123\", \"machine_tags\": [], \"last_external_ip_address\": \"111.111.111.111\", \"rbac_group_id\": 220, \"computer_dns_name\": \"desktop-12345\", \"os_processor\": \"x64\", \"exposure_level\": \"Medium\", \"last_ip_address\": \"111.111.111.111\", \"os_build\": 18363, \"agent_version\": \"11.111.111.1111\", \"risk_score\": \"Low\", \"os_version\": null, \"health_status\": \"Active\", \"version\": \"1909\", \"rbac_group_name\": \"UnassignedGroup\", \"first_seen\": \"2021-05-19T12:03:59.7292864Z\", \"os_platform\": \"Windows10\", \"id\": \"12345678\", \"last_seen\": \"2021-05-30T12:53:20.0938152Z\"}, \"Entity\": \"111.11.111.111\"}]"
```



#### List Indicators
List indicators in Microsoft Defender ATP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Indicators|Specify a comma-separated list of indicators that you would like to retrieve.|False|String||
|Indicator Types|Specify a comma-separated list of indicator types that you want to retrieve. Possible values: FileSha1, FileSha256, FileMd5, CertificateThumbprint, IpAddress, DomainName, Url.|False|String|FileSha1,FileSha256,FileMd5,CertificateThumbprint,IpAddress,DomainName,Url|
|Actions|Specify a comma-separated list of indicator actions that you want to use for filtering. Possible values: Warn,Block,Audit,Alert,AlertAndBlock,BlockAndRemediate,Allowed.|False|String|Warn,Block,Audit,Alert,AlertAndBlock,BlockAndRemediate,Allowed|
|Severity|Specify a comma-separated list of severities that you want to use for filtering. Possible values: Informational,Low,Medium,High.|False|String|Informational,Low,Medium,High|
|Max Results To Return|Specify how many indicators to return. Default: 50.|False|String|50|



##### JSON Results
```json
[{"id":"16","indicatorValue":"https://www.google.com","indicatorType":"Url","action":"Audit","createdBy":"45e9773c-100e-4a9f-ad37-xxxxxxx","severity":"Informational","category":1,"application":"demo-test","educateUrl":null,"bypassDurationHours":null,"title":"test","description":"test","recommendedActions":"nothing","creationTimeDateTimeUtc":"2022-02-08T14:04:11.3831384Z","expirationTime":null,"lastUpdateTime":"2022-02-08T14:13:02.177086Z","lastUpdatedBy":"45e9773c-100e-4a9f-ad37-xxxxxxxx","rbacGroupNames":[],"rbacGroupIds":[],"notificationId":null,"notificationBody":null,"version":null,"mitreTechniques":[],"historicalDetection":false,"lookBackPeriod":null,"generateAlert":true,"additionalInfo":null,"createdByDisplayName":"Gabriel Defender ATP","externalId":null,"createdBySource":"PublicApi","certificateInfo":null},{"id":"10","indicatorValue":"b753b5cbe151bba8befa6d9111bfda5a7d47ba601xxxxxxxxx","indicatorType":"FileSha256","action":"Audit","createdBy":"vasil.d@siemplifycyarx.onmicrosoft.com","severity":"High","category":1,"application":null,"educateUrl":null,"bypassDurationHours":null,"title":"אהבה","description":"אהבה","recommendedActions":"אהבה","creationTimeDateTimeUtc":"2020-07-16T13:33:24.8228025Z","expirationTime":null,"lastUpdateTime":"2020-07-16T13:33:24.8383959Z","lastUpdatedBy":null,"rbacGroupNames":[],"rbacGroupIds":[],"notificationId":null,"notificationBody":null,"version":null,"mitreTechniques":[],"historicalDetection":false,"lookBackPeriod":null,"generateAlert":true,"additionalInfo":null,"createdByDisplayName":"vasil.d@siemplifycyarx.onmicrosoft.com","externalId":null,"createdBySource":"Portal","certificateInfo":null}]
```



#### Execute Live Response Command
Use "Execute Live Response Command" action to execute a live response command in Microsoft Defender for Endpoint. Supported Entities: IP Address, Hostname. Note: Action is running as async, please adjust script timeout value in Google SecOps IDE for action, as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Command|JSON object that represents the command that needs to be executed. More information is available on this page: https://learn.microsoft.com/en-us/defender-endpoint/api/run-live-response|True|String|{
     "type": "Command",
     "params": [
          {
               "key": "string",
               "value": "string"
          }
     ]
}|
|Comment|Comment that describes the executed command.|False|String||



##### JSON Results
```json
[{"Entity": "some.host.com", "EntityResult": {"@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#MachineActions/$entity", "id": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "type": "LiveResponse", "requestor": "user@example.com", "requestorComment": "Testing Live Response API", "status": "Completed", "machineId": "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx", "computerDnsName": "some.host.com", "creationDateTimeUtc": "2023-01-01T12:00:00.0000000Z", "lastUpdateDateTimeUtc": "2023-01-01T12:01:00.0000000Z", "results": {"filepath": "/siemplify_deployment/Default/SiemplifyJobs/ACTION_1234/some.host.com_C__Users_desktop.ini"}}}]
```



#### Submit Entity Indicators
Submit entities as indicators in Microsoft Defender ATP. Supported entities: Filehash, URL, IP Address. Note: only MD5, SHA1 and SHA256 hashes are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Action|Specify the action that needs to be applied to the entities. Note: "Block And Remediate" is supported only for filehash entities.|True|List|Block|
|Severity|Specify the severity for the found entities.|True|List|High|
|Application|Specify an application that is related to the entities.|False|String||
|Indicator Alert Title|Specify what should be the title for the alert, if they are identified in the environment.|True|String||
|Description|Specify the description for the entities.|True|String|Siemplify Remediation|
|Recommended Action|Specify what should be the recommended actions for the handling of the entities.|False|String||



#### Run Advanced Hunting Query
Run Advanced Hunting Query
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|Advanced hunting query to execute|True|String||



##### JSON Results
```json
[{"InitiatingProcessParentCreationTime": "2020-01-27T11:53:03.9283127Z", "InitiatingProcessParentId": 5180, "MachineId": "fbc85cf3fbcc8bb14d1a84fcf7bbae4531f00000", "ProcessCreationTime": "2020-02-08T03:27:24.9735836Z", "ComputerName": "name", "InitiatingProcessCommandLine": "\"wuauclt.exe\" /RunHandlerComServer", "InitiatingProcessParentFileName": "svchost.exe", "InitiatingProcessSHA1": "e82ac9345fbefc100ff16d66536877502ab00000", "InitiatingProcessIntegrityLevel": "System", "SHA256": "a184ca30204239b414b8567d62b52673775f988ce52da4379c9cbf83a7400000", "InitiatingProcessCreationTime": "2020-02-08T03:27:24.8656643Z", "InitiatingProcessAccountSid": "S-1-5-18", "ProcessId": 4668, "InitiatingProcessFolderPath": "c:\\windows\\system32\\wuauclt.exe", "InitiatingProcessId": 3752, "ActionType": "ProcessCreated", "InitiatingProcessTokenElevation": "TokenElevationTypeDefault", "InitiatingProcessAccountName": "system", "ReportId": 19917, "InitiatingProcessMD5": "c8f7fa1a3a3b23df12a2bcf4b5000000", "EventTime": "2020-02-08T03:27:25.0020441Z", "SHA1": "1bfb34ddc0c8ddef6eea0ec47084376e1bf00000", "ProcessIntegrityLevel": "System", "AccountName": "system", "AppGuardContainerId": "", "InitiatingProcessSHA256": "", "ProcessTokenElevation": "TokenElevationTypeDefault", "AccountSid": "S-1-5-18", "InitiatingProcessAccountDomain": "nt authority", "MD5": "110943becfe834df37916862e0400000", "LogonId": 0, "ProcessCommandLine": "\"AM_Delta_Patch_1.309.504.0.exe\" WD /q", "FileName": "AM_Delta_Patch_1.309.504.0.exe", "InitiatingProcessFileName": "wuauclt.exe", "FolderPath": "C:\\Windows\\SoftwareDistribution\\Download\\Install\\AM_Delta_Patch_1.309.504.0.exe", "AccountDomain": "nt authority", "InitiatingProcessLogonId": null}]  

```



#### Create Run Antivirus Scan Task
Create Run AV Scan Task
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Antivirus Scan Type|Antivirus Scan Type|True|List|Full|
|Comment|Comment why an antivirus scan needs to be executed on the machine|True|String||



##### JSON Results
```json
[{"status": "Pending", "creation_date_time_utc": "2020-02-08T03:27:01.8730344Z", "cancellation_requestor": null, "cancellation_date_time_utc": null, "id": "00000000-0000-0000-0000-000000000000", "last_update_date_time_utc": "2020-02-08T03:27:01.8730344Z", "related_file_info": null, "cancellation_comment": null, "requestor": "00000000-0000-0000-0000-000000000000", "error_h_result": 0, "scope": null, "machine_id": "000000000000000000000000000000", "type": "RunAntiVirusScan", "requestor_comment": "test"}]
```



#### Get Machine Vulnerabilities
Use the Get Machine Vulnerabilities action to list vulnerabilities associated with specific machines in Microsoft Defender for Endpoint. Supported Entities: IP Address, Hostname.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Severity Filter|The severity levels used to filter the returned vulnerabilities.|False|MultipleChoiceParameter|Critical|
|Threat Filter|The threat intelligence criteria used to filter the returned vulnerabilities.|False|MultipleChoiceParameter||
|Sort By|The field used to sort the returned vulnerabilities.|False|List|Severity|
|Sort Order|The order in which the sorted results are displayed.|False|List|ASC|
|Max Vulnerabilities To Return|The maximum number of vulnerabilities to return for each entity. Maximum: 100.|True|String|100|



##### JSON Results
```json
[{"Entity": "", "EntityResult": {"@odata.type": "#microsoft.windowsDefenderATP.api.PublicVulnerabilityDto", "id": "CVE-xx-xxxx", "name": "CVE-xxxx-xxxx", "description": "Summary: The Windows Telephony Service in Microsoft Windows is vulnerable to remote code execution. An attacker can exploit this vulnerability by tricking a user into visiting a malicious website, allowing for arbitrary code execution. Impact: Successful exploitation could lead to complete system compromise and unauthorized access to sensitive information. Remediation: Apply the latest patches and updates provided by Microsoft.", "severity": "High", "cvssV3": 8.8, "cvssVector": "CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H/E:U/RL:O/RC:C", "exposedMachines": 1, "publishedOn": "2022-01-14T08:00:00Z", "updatedOn": "2022-01-14T23:45:43.5Z", "firstDetected": "2022-01-14T18:31:29Z", "patchFirstAvailable": null, "publicExploit": false, "exploitVerified": false, "exploitInKit": false, "exploitTypes": [], "exploitUris": [], "cveSupportability": "Supported", "tags": [], "epss": 0.01391, "status": "RemediationRequired"}}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds









## Connectors
#### Microsoft Defender ATP Connector
Deprecation Notice! This connector is planned to be deprecated on 30th March 2027. Visit documentation for more information. Fetch alerts and events from MS Defender ATP

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored.|False|String||
|Environment Regex Pattern|If defined - the connector will implement the specific RegEx pattern on the data from "environment field" to extract specific string. For example - extract domain from sender's address: "(?<=@)(\S+$)"|False|Int||
|Login API Root|Login API root of the Microsoft 365 Defender instance.|True|String|https://login.microsoftonline.com|
|API Root|The API Root of Microsoft Defender ATP|True|String|https://api.securitycenter.windows.com|
|Azure Active Directory ID|Azure Active Directory Tenant ID, can be viewed in Active Directory > App Registration > <Application you configured for your integration> > Directory (tenant) ID.|True|String||
|Integration Client ID|Client (Application) ID that was added for the app registration in Azure Active Directory for this integration.|True|String||
|Integration Client Secret|Secret that was entered for Azure AD app registration|True|Password|*****|
|SIEM Client ID|Client (Application) ID for the enabled SIEM integration in Microsoft Defender ATP|True|String||
|SIEM Client Secret|Secret that for the enabled SIEM integration in Microsoft Defender ATP|True|Password|*****|
|Max Alerts per Cycle|How many alerts should be processed during one connector run|True|Int|100|
|Offset Time In Hours|Fetch alerts from X hours backwards. Default value: 24 hours.|True|Int|24|
|Alert Statuses to Fetch|Specify the statuses of the incidents that should be fetched by the Siemplify server. Comma-separated string.|True|String|Unknown, New, InProgress, Resolved|
|Alert Severities to Fetch|Specify the severities of the incidents that should be fetched by the Siemplify server. Comma-separated string.|True|String|UnSpecified, Informational, Low, Medium, High|
|Proxy Server Address|Proxy server to use for connection.|False|IP||
|Proxy Server Username|Proxy server username|False|String||
|Proxy Server Password|Proxy server password|False|Password|*****|


#### Microsoft Defender ATP Connector V2
Deprecation Notice! This connector is planned to be deprecated on 30th March 2027. Visit documentation for more information. Connector can be used to fetch Defender ATP alerts with events information from 365 Defender, as Defender ATP SIEM API used in v1 connector for events is deprecated starting March 1st 2022. Connector whitelist can be used to ingest only specific types of alerts based on alert's "detectionSource" attribute value. SourceGroupIdentifier of the connector can be used to group Siemplify alerts based on Defender ATP incident id.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If environment field isn't found, environment is "".|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return value unchanged. Used to allow the user to manipulate the environment field via regex logic. If regex pattern is null or empty, or the environment value is null, the final environment result is "".|False|Int|.*|
|Login API Root|Login API root of the Microsoft 365 Defender instance.|True|String|https://login.microsoftonline.com|
|Defender ATP API Root|Api root url to use with integration. For better performance, you can use server closer to your geo location: api-us.securitycenter.windows.com api-eu.securitycenter.windows.com api-uk.securitycenter.windows.com|True|String|https://api.securitycenter.windows.com|
|365 Defender API Root|API root of the Microsoft 365 Defender instance used to get Siemplify events data.|True|String|https://api.security.microsoft.com|
|Graph API Root|The base URL for the Microsoft Graph API (e.g., https://graph.microsoft.com). If provided, V2 API endpoints will be used.|False|String||
|Azure Active Directory ID|Azure Active Directory Tenant ID, can be viewed in Active Directory > App Registration > <Application you configured for your integration> > Directory (tenant) ID.|True|String||
|Integration Client ID|Client (Application) ID that was added for app registration in Azure Active Directory for the integration.|True|String||
|Integration Client Secret|Secret that was entered for Azure AD app registration for the integration.|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Microsoft 365 Defender server is valid.|False|Boolean|true|
|Offset Time In Hours|Fetch alerts from X hours backwards.|True|Int|24|
|Max Alerts per Cycle|How many alerts should be processed during one connector run.|True|Int|10|
|Alert Statuses to Fetch|Specify the statuses of the Defender ATP alerts that should be fetched by the Siemplify server. Parameter can take multiple values as a comma separated string.|True|String|Unknown, New, InProgress, Resolved|
|Alert Severities to Fetch|Specify the severities of the Defender ATP alerts that should be fetched by the Siemplify server. Parameter can take multiple values as a comma separated string.|True|String|UnSpecified, Informational, Low, Medium, High|
|Disable Overflow|If enabled, the connector will ignore the overflow mechanism.|False|Boolean|false|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Proxy Server Address|Proxy server to use for connection.|False|IP||
|Proxy Server Username|Proxy server username|False|String||
|Proxy Server Password|Proxy server password|False|Password|*****|




