
# Houdin-io

Houdin.io provides automated AI cyber threat analysis, reducing the time and effort required to analyze and respond to cyber threats.

This connector allows you to connect Houdin.io with your SOAR platform, enabling automated threat analysis and response workflows.

Support Contact: support@houdin.io

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Key|Your Houdin API key. Used to launch scans, retrieve data, etc.|True|Password|*****|
|Verify SSL|Enable or disable SSL verification.|False|Boolean|true|



## Actions
#### Scan Artifact
Launch a Houdin scan on a given artifact, and retrieve all results. The action returns automatically when your scan is done. Compatible types are: Public IPv4/IPv6, URL, Domain, MD5, SHA1, SHA256 Note: Action is running as async, adjust script timeout value in Google SecOps IDE for action, as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|artifact|An artifact to scan on the Houdin.io platform. Currently supported types: IPv4, IPv6, URL, Domain, MD5, SHA1, SHA256|True|String|test.com|
|scanOn|(Optional) An array of scanners you want Houdin to use.|False|MultipleChoiceParameter||



##### JSON Results
```json
{"scanID": "houdin-1232085c-d4cc-43df-b841-e49e81520a3e", "clientID": "6848b13cd6d2453c384404a0", "status": "Done", "artifact": "malicious.com", "scanOn": ["vt", "urlscan", "alienvault", "abuseipdb", "triage", "mesmer"], "scanResults": {"vt": {"result": {"data": {"id": "malicious.com", "type": "domain", "attributes": {"reputation": -60, "last_analysis_stats": {"malicious": 12, "suspicious": 0, "undetected": 28, "harmless": 54}}}}}, "urlscan": {"result": {"results": [{"task": {"url": "http://malicious.com/payload.ps1"}, "page": {"status": "200"}, "_id": "01983b58-ffc8-777d-903b-fa813685774d"}], "total": 253}}, "alienvault": {"result": {"general": {"indicator": "malicious.com", "type": "domain", "pulse_info": {"count": 4}}}}, "abuseipdb": {"result": {"ipAddress": "149.28.227.54", "abuseConfidenceScore": 0, "countryCode": "US", "totalReports": 0}}, "triage": {"result": {"lastScan": {"analysis": {"score": 5}, "sample": {"id": "240312-mnz43seh3s", "target": "http://malicious.com", "score": 5}}}}, "mesmer": {"result": {"observable": "malicious.com", "globalScore": "9", "summary": "The domain malicious.com is confirmed malicious with multiple reports.", "tags": [{"value": "Trojan", "color": "red", "source": "vt"}, {"value": "Malware", "color": "red", "source": "alienvault"}]}}}, "scanTime": "2025-07-27T17:28:30.905Z", "expiresAfter": "2025-08-24T17:28:30.905Z"}
```



#### Enrich Entities
Scan compatible entities on Houdin.io, and add enrichment results for each one. Compatible types are: Public IPv4/IPv6, URL, Domain, MD5, SHA1, SHA256 Note: Action is running as async, adjust script timeout value in Google SecOps IDE for action, as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|scanOn|(Optional) An array of scanners you want Houdin to use.|False|MultipleChoiceParameter||



##### JSON Results
```json
[{"Entity": "malicious.com", "EntityResult": {"scanID": "houdin-1232085c-d4cc-43df-b841-e49e81520a3e", "clientID": "6848b13cd6d2453c384404a0", "status": "Done", "artifact": "malicious.com", "scanOn": ["vt", "urlscan", "alienvault", "abuseipdb", "triage", "mesmer"], "scanResults": {"vt": {"result": {"data": {"id": "malicious.com", "type": "domain", "attributes": {"reputation": -60, "last_analysis_stats": {"malicious": 12, "suspicious": 0, "undetected": 28, "harmless": 54}}}}}, "urlscan": {"result": {"results": [{"task": {"url": "http://malicious.com/payload.ps1"}, "page": {"status": "200"}, "_id": "01983b58-ffc8-777d-903b-fa813685774d"}], "total": 253}}, "alienvault": {"result": {"general": {"indicator": "malicious.com", "type": "domain", "pulse_info": {"count": 4}}}}, "abuseipdb": {"result": {"ipAddress": "149.28.227.54", "abuseConfidenceScore": 0, "countryCode": "US", "totalReports": 0}}, "triage": {"result": {"lastScan": {"analysis": {"score": 5}, "sample": {"id": "240312-mnz43seh3s", "target": "http://malicious.com", "score": 5}}}}, "mesmer": {"result": {"observable": "malicious.com", "globalScore": "9", "summary": "The domain malicious.com is confirmed malicious with multiple reports.", "tags": [{"value": "Trojan", "color": "red", "source": "vt"}, {"value": "Malware", "color": "red", "source": "alienvault"}]}}}, "scanTime": "2025-07-27T17:28:30.905Z", "expiresAfter": "2025-08-24T17:28:30.905Z"}}]
```



#### Ping
Test the connectivity to the Houdin.io API.
Timeout - 600 Seconds



##### JSON Results
```json
{}
```









