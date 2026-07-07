
# NessusScanner

Nessus is deployed by millions of users worldwide to identify vulnerabilities, policy-violating configurations and malware that attackers use to penetrate your or your customer's network.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|None|True|String|https://{ip-address}:{port}|
|Access Key|None|True|String||
|Secret Key|None|True|Password|*****|



## Actions
#### Get Scans
Fetch a list of existing scans
Timeout - 600 Seconds



##### JSON Results
```json
{"Scans": [{"status": "completed", "control": true, "uuid": "00000-000000-00000-0000000000-00000000000", "read": true, "last_modification_date": 1538656691, "enabled": true, "creation_date": 1521364372, "user_permissions": 000, "folder_id": 100, "starttime": null, "shared": false, "owner": "admin", "timezone": null, "rrules": null, "type": "local", "id": 000, "name": "Nessus-test"}]}
```



#### Create Scan
Create a new scan in Nessus with a template
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Scan Name|Scan display name.|True|String||
|Scan Template Title|Scan template title value.|True|String||
|Description|Description content.|False|String||



##### JSON Results
```json
{"dashboard_file": null, "scanner_id": 1, "last_modification_date": 1548175315, "creation_date": 1548175315, "user_permissions": 000, "owner": "admin", "timezone": null, "id": 000, "description": "", "uuid": "template-000-000-000-000-0000000", "sms": null, "shared": 0, "type": "public", "owner_id": 2, "rrules": null, "scan_time_window": null, "container_id": 0, "tag_id": 000, "notification_filters": null, "default_permisssions": 0, "emails": null, "name": "test", "custom_targets": "1.1.1.1", "enabled": true, "use_dashboard": false, "starttime": null, "policy_id": 000}
```



#### Launch Scan
Launch scan on the Nessus server
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Scan Name|Scam display name.|True|String||



#### Get Scan Templates
Get all scan templates from the server
Timeout - 600 Seconds



##### JSON Results
```json
{"Templates": [{"name": "wannacry", "title": "WannaCryRansomware", "is_agent": null, "unsupported": false, "manager_only": false, "desc": "RemoteandlocalchecksforMS17-010.", "subscription_only": false, "uuid": "00000-000000-0000-00000-00000000000"}]}
```



#### Get Scan Report
Get a full report on the scan results
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Scan Name|Scan display name.|True|String||



##### JSON Results
```json
{"info": {"control": true, "edit_allowed": true, "hasaudittrail": true, "user_permissions": 000, "alt_targets_used": null, "targets": "1.1.1.1", "uuid": "000000-00000-00000-00000-000000000", "hostcount": 1, "object_id": 000, "acls": [{"display_name": "admin", "name": "admin", "owner": 1, "type": "user", "id": 2, "permissions": 000}], "policy": "AdvancedScan", "no_target": null, "scanner_name": "LocalScanner", "scan_end": 1521367948, "status": "completed", "scanner_end": 1521367945, "timestamp": 1521367948, "scan_type": "local", "scan_start": 1521367553, "folder_id": 100, "name": "Nessus", "haskb": true, "pci-can-upload": false, "scanner_start": 1521367553}, "remediations": {"num_cves": 5, "remediations": null, "num_impacted_hosts": 0, "num_hosts": 1, "num_remediated_cves": 0}, "vulnerabilities": [{"count": 1, "severity": 0, "plugin_family": "Windows", "vuln_index": 109, "severity_index": 0, "plugin_name": "WindowsTerminalServicesEnabled", "plugin_id": 10940}], "notes": null, "compliance": [], "hosts": [{"info": 80, "scanprogresscurrent": 1927, "medium": 10, "scanprogresstotal": 1927, "totalchecksconsidered": 1927, "host_index": 0, "hostname": "1.1.1.1", "numchecksconsidered": 1927, "high": 0, "score": 1120, "low": 4, "severitycount": {"item": [{"count": 80, "severitylevel": 0}]}, "host_id": 2, "progress": "1927-1927/95562-95562", "critical": 0, "severity": 94}], "filters": [{"control": {"regex": "^[0-9]+$", "readable_regex": "NUMBER", "type": "entry"}, "operators": ["eq", "neq", "match"], "readable_name": "BugtraqID", "name": "bid"}], "comphosts": [], "history": [{"status": "completed", "uuid": "000000-0000-0000-00000-0000000", "history_id": 260, "creation_date": 1519209387, "scheduler": 0, "last_modification_date": 1519209860, "alt_targets_used": false, "type": "local", "owner_id": 0}]}
```



#### Ping
Test Connectivity
Timeout - 600 Seconds






## Jobs

#### LaunchScanAndGetAReport
Job for initiating scan in Nessus and get scan report

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Api Root|True|String||
|Access Key|True|String||
|Secret Key|True|String||
|Scan Name|True|String||
|Scan Download Path|True|String||



