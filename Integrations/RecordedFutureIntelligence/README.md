
# RecordedFutureIntelligence

Recorded Future's unique technology collects and analyzes vast amounts of data to deliver relevant cyber threat insights in real-time. For support please contact support@recordedfuture.com

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|ApiUrl||True|String|https://api.recordedfuture.com|
|ApiKey||True|Password|*****|
|SandboxApiUrl||False|String|https://sandbox.recordedfuture.com|
|SandboxApiKey||False|Password|*****|
|Verify SSL||False|Boolean|true|
|CollectiveInsights||False|Boolean|true|


#### Dependencies
| |
|-|
|python_dotenv-1.1.1-py3-none-any.whl|
|six-1.17.0-py2.py3-none-any.whl|
|protobuf-6.31.1-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|httpcore-1.0.9-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|proto_plus-1.26.1-py3-none-any.whl|
|wheel-0.45.1-py3-none-any.whl|
|google_auth_httplib2-0.3.0-py3-none-any.whl|
|urllib3-2.5.0-py3-none-any.whl|
|markdown_strings-3.4.0-py2.py3-none-any.whl|
|antlr4-python3-runtime-4.9.3.tar.gz|
|idna-3.10-py3-none-any.whl|
|pydantic_settings-2.14.0-py3-none-any.whl|
|pyopenssl-25.3.0-py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|hatching-triage-0.2.0.tar.gz|
|more_itertools-10.2.0-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|tomli-2.2.1-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|TIPCommon-2.3.6-py3-none-any.whl|
|simplejson-3.20.1-cp311-cp311-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|google_api_core-2.25.1-py3-none-any.whl|
|requests_toolbelt-1.0.0-py2.py3-none-any.whl|
|annotated_types-0.7.0-py3-none-any.whl|
|pyparsing-3.2.3-py3-none-any.whl|
|googleapis_common_protos-1.70.0-py3-none-any.whl|
|pycparser-2.22-py3-none-any.whl|
|typing_extensions-4.14.0-py3-none-any.whl|
|google_auth-2.47.0-py3-none-any.whl|
|setuptools-80.9.0-py3-none-any.whl|
|EnvironmentCommon-1.0.3-py3-none-any.whl|
|appdirs-1.4.4-py2.py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|ply-3.11-py2.py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|stix2_patterns-2.0.0-py2.py3-none-any.whl|
|anyio-4.9.0-py3-none-any.whl|
|cryptography-46.0.7-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|pytz-2025.2-py2.py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|pydantic-2.11.7-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|typing_inspection-0.4.1-py3-none-any.whl|
|click-8.1.8-py3-none-any.whl|
|pydantic_core-2.33.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|psengine-2.8.0-py3-none-any.whl|
|jsonpath_ng-1.6.1-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|google_api_python_client-2.188.0-py3-none-any.whl|
|stix2-3.0.1-py2.py3-none-any.whl|


## Actions
#### Search Detection Rules
Search for detection rules based on various filter criteria.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Detection Rule Type|Types of detection rules to search for.|False|String|None|
|Filter on Target Entities|If the action should filter the search on the Target Entities.|False|Boolean|None|
|Entity ID|A comma separated list of entities that may be associated with a given detection rule. All values in the list must be valid Recorded Future entity IDs.|False|String|None|
|Created Before|Filter for rules created before this date or relative date.|False|String|None|
|Created After|Filter for rules created after this date or relative date.|False|String|None|
|Updated Before|Filter for rules updated before this date or relative date.|False|String|None|
|Updated After|Filter for rules updated after this date or relative date.|False|String|None|
|Detection Rule ID|Filter by document ID.|False|String|None|
|Detection Rule Title|Filter by Detection Rule title.|False|String|None|
|Tagged Entities|Whether to filter by tagged entities.|False|Boolean|None|
|Max Results|Limit the total number of results returned.|False|String|None|



##### JSON Results
```json
[{"id": "doc:aaaaa", "type": "yara", "title": "Detection Rule Title", "description": "Detection Rule Description", "created": "2022-09-27T15:27:18.379000Z", "updated": "2022-09-27T15:29:36.873000Z", "rules": [{"entities": [{"id": "D0Ak-s", "name": "Ransomware", "type": "MalwareCategory"}], "content": "Rule Content", "file_name": "rule.yar"}]}]
```



#### Enrich IP
Query Recorded Future to get intelligence about the IP address.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Risk Score Threshold|Represents the minimum malicious risk score for an IP to be marked malicious. Has a range of 0-99. Below is the band levels:  Very Malicious: 90-99  Malicious: 65-89  Suspicious: 25-64  Unusual: 5-24  No Malicious content: 0|True|String|25|
|Include Links|If enabled, action will get information about links.|False|Boolean|false|
|Enable Collective Insights|If enabled, contribute detections back to Recorded Future.|False|Boolean|true|



##### JSON Results
```json
[{"Entity": "1.1.1.1", "EntityResult": [{"entity": {"id": "ip:1.1.1.1", "name": "1.1.1.1", "type": "IpAddress"}, "intelCard": "https://app.recordedfuture.com/live/sc/entity/ip%3A1.1.1.1", "location": {"organization": "Huawei Cloud Service data center", "cidr": {"id": "ip:1.1.1.1/17", "name": "1.1.1.1/17", "type": "IpAddress"}, "location": {"continent": "Asia", "country": "China", "city": "Guangzhou"}, "asn": "AS55990"}, "risk": {"criticalityLabel": "Very Malicious", "riskString": "12/79", "rules": 12, "criticality": 4, "riskSummary": "12 of 79 Risk Rules currently observed.", "score": 99, "evidenceDetails": [{"mitigationString": "", "evidenceString": "29 sightings on 3 sources: Twitter, Recorded Future Command & Control List, GitHub. 8 related intrusion methods including Interactsh LDAP Server, Cobalt Strike, Trojan, Offensive Security Tools (OST), Banking Trojan. Most recent link (Jun 27, 2024): https://github.com/drb-ra/C2IntelFeeds/commit/a2a3ba86630ad312b2eb014400d6aac83cc1f888", "rule": "Historically Linked to Intrusion Method", "criticality": 1, "timestamp": "2024-06-27T21:26:07.630Z", "criticalityLabel": "Unusual"}, {"mitigationString": "", "evidenceString": "45 sightings on 3 sources: ThreatFox Infrastructure Analysis, DHS Automated Indicator Sharing, Malware Patrol. ThreatFox identified 124.71.84.65:8899 as possible TA0011 (Command and Control) for Sliver on January 01, 2024. Most recent link (Jan 1, 2024): https://threatfox.abuse.ch/ioc/1106265", "rule": "Historical Suspected C&C Server", "criticality": 1, "timestamp": "2024-01-01T07:51:06.000Z", "criticalityLabel": "Unusual"}, {"mitigationString": "", "evidenceString": "330 sightings on 2 sources: Recorded Future Malicious Infrastructure Management Validation, Recorded Future Malicious Infrastructure Management Validation.", "rule": "Historical Malicious Infrastructure Admin Server", "criticality": 1, "timestamp": "2024-07-09T08:08:00.637Z", "criticalityLabel": "Unusual"}, {"mitigationString": "", "evidenceString": "293 sightings on 1 source: DHS Automated Indicator Sharing. 293 reports including Malicious IPv4 address, from Forescout Research - Vedere Labs (Jun 29, 2024).", "rule": "Historically Reported by DHS AIS", "criticality": 1, "timestamp": "2024-06-29T12:00:46.284Z", "criticalityLabel": "Unusual"}, {"mitigationString": "", "evidenceString": "8 sightings on 3 sources: redpacketsecurity.com, PasteBin, Twitter. Most recent link (May 13, 2024): https://pastebin.com/VJwG1yHY", "rule": "Historically Reported as a Defanged IP", "criticality": 1, "timestamp": "2024-05-13T12:57:05.000Z", "criticalityLabel": "Unusual"}, {"mitigationString": "", "evidenceString": "1 sighting on 1 source: External Sensor Data Analysis. 124.71.84.65 was identified as botnets in External Sensor data. Reported to Recorded Future on Feb 11, 2024.", "rule": "Historical Botnet Traffic", "criticality": 1, "timestamp": "2024-02-11T10:04:46.433Z", "criticalityLabel": "Unusual"}, {"mitigationString": "", "evidenceString": "Previous sightings on 4 sources: Recorded Future Analyst Community Trending Indicators, Recently Viewed Integrations Indicators, RAT Controller \u2013 Shodan / Recorded Future, Cobalt Strike Default Certificate Detected - Shodan / Recorded Future. Observed between Sep 24, 2023, and Jun 6, 2024.", "rule": "Historically Reported in Threat List", "criticality": 1, "timestamp": "2024-07-25T09:20:50.134Z", "criticalityLabel": "Unusual"}, {"mitigationString": "", "evidenceString": "341 sightings on 2 sources: Recorded Future Command & Control Reports, Recorded Future Command & Control List. 124.71.84.65:443 was reported as a command and control server for cobalt strike on Apr 11, 2024", "rule": "Historically Reported C&C Server", "criticality": 2, "timestamp": "2024-04-13T08:22:57.282Z", "criticalityLabel": "Suspicious"}, {"mitigationString": "", "evidenceString": "3 sightings on 1 source: GitHub. 3 related intrusion methods: Trojan, Banking Trojan, QakBot. Most recent link (Jul 20, 2024): https://github.com/drb-ra/C2IntelFeeds/commit/8ffba7ff283af2e28231fe5d42691e33bb1383af", "rule": "Recently Linked to Intrusion Method", "criticality": 2, "timestamp": "2024-07-20T23:02:00.653Z", "criticalityLabel": "Suspicious"}, {"mitigationString": "", "evidenceString": "3001 sightings on 1 source: Recorded Future Command & Control Validation. Recorded Future analysis validated 124.71.84.65:8899 as a command and control server for Sliver on Jul 23, 2024", "rule": "Previously Validated C&C Server", "criticality": 2, "timestamp": "2024-07-23T10:38:16.000Z", "criticalityLabel": "Suspicious"}, {"mitigationString": "", "evidenceString": "20 sightings on 1 source: Recorded Future Malicious Infrastructure Management Validation.", "rule": "Recent Malicious Infrastructure Admin Server", "criticality": 3, "timestamp": "2024-07-25T08:08:12.328Z", "criticalityLabel": "Malicious"}, {"mitigationString": "", "evidenceString": "1 sighting on 1 source: Recorded Future Command & Control Validation. Recorded Future analysis validated 124.71.84.65:8899 as a command and control server for Sliver on Jul 24, 2024", "rule": "Validated C&C Server", "criticality": 4, "timestamp": "2024-07-24T10:38:19.000Z", "criticalityLabel": "Very Malicious"}]}, "timestamps": {"lastSeen": "2024-07-20T23:02:00.764Z", "firstSeen": "2022-12-09T20:10:23.511Z"}, "links": {"Indicators & Detection Rules": [], "Actors, Tools & TTPs": [{"id": "mitre:TA0011", "name": "TA0011", "type": "MitreAttackIdentifier"}, {"id": "aaa7zE", "name": "Sliver", "type": "Malware"}, {"id": "plT8qj", "name": "Viper Pentesting Tool", "type": "Malware"}]}}]}]
```



#### Lookup Credentials
Identity - Lookup credential data for a set of subjects.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Subjects|An email or a list of emails to be queried.|False|String|None|
|Filter on Target Entities|If the action should filter the search on the Target Entities.|False|Boolean|None|
|First Downloaded GTE|First date when these credentials were received and indexed by Recorded Future.|False|String|None|
|Latest Downloaded GTE|Latest date when these credentials were received and indexed by Recorded Future.|False|String|None|
|Exfiltration Date GTE|Date when the infostealer malware exfiltrated data from the victim device.|False|String|None|
|Properties|Password properties.|False|String|None|
|Breach Name|The name of a breach.|False|String|None|
|Breach Date|The date of a breach.|False|String|None|
|Dump Name|The name of a database dump.|False|String|None|
|Dump Date|The date of a database dump.|False|String|None|
|Username Properties|Username properties. Only valid value is 'Email'.|False|String|None|
|Authorization Technologies|Authorization technologies to filter by.|False|String|None|
|Authorization Protocols|Authorization protocols to filter by.|False|String|None|
|Malware Families|Known infostealer malware families.|False|String|None|
|Organization ID|An organization ID if utilizing a multi-org setup.|False|String|None|
|Max Results|The maximum number of credential records returned.|False|String|None|



##### JSON Results
```json
[{"identity": {"subjects": ["j.doe@example-corp.com"]}, "count": 0, "credentials": [{"subject": "j.doe@example-corp.com", "authorization_service": {"url": "https://signin.example-corp.com/login", "domain": "example-corp.com", "fqdn": "signin.example-corp.com", "protocols": ["HTTPS"], "technology": [{"id": "tech-wordpress", "name": "WordPress", "category": "CMS"}]}, "authorization_services": [{"url": "https://signin.example-corp.com/login", "domain": "example-corp.com", "fqdn": "signin.example-corp.com", "protocols": ["HTTPS"], "technology": [{"id": "tech-wordpress", "name": "WordPress", "category": "CMS"}]}], "exposed_secret": {"type": "Password", "effectively_clear": true, "hashes": [{"algorithm": "SHA1", "hash": "5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8"}], "details": {"clear_text_value": "password123", "clear_text_hint": "p***3", "properties": ["Letter"]}}, "compromise": {"exfiltration_date": "2025-01-10T18:00:00Z"}, "cookies": [{"dns": ".example.com", "name": "session_id", "http": true, "expiration": "2025-08-25T09:57:39Z", "secure": true, "value": "3a2d5f8b-9e4c-4a1d-b8f9-c6e7d8f9a0b1"}], "malware_family": {"id": "mal-vidar", "name": "Vidar Stealer"}, "dumps": [{"name": "Antiscam Log 2024-07-22", "type": "Stealer Log", "source": "dump-antiscam-2024-07-22-045", "description": "Log data from Antiscam malware campaign.", "infrastructure": {"ip": "203.0.113.55"}, "compromise": {"os": "Windows 11", "os_username": "victim_user", "malware_file": "C:\\Windows\\Temp\\update.exe", "timezone": "(UTC+02:00) Helsinki, Kyiv, Riga, Sofia, Tallinn, Vilnius", "computer_name": "DESKTOP-A1B2C3D", "uac": "UAC-Limited", "antivirus": ["Avast"], "exfiltration_date": "2025-07-21T12:00:00Z"}, "location": {"country": {"name": "UNITED_STATES", "displayName": "United States", "countryCode": "USA", "alpha2Code": "US", "alpha3Code": "USA"}, "city": "New York", "address": "123 Main Street, Apt 4B", "address1": "123 Main Street", "address2": "Apt 4B", "state": "NY", "postal_code": "10001", "zip": "10001"}, "breaches": [{"name": "SocialNet Breach", "domain": "socialnet.com", "type": "Database Breach", "breached": "2023-11-01T00:00:00Z", "start": "2023-10-15T00:00:00Z", "stop": "2023-10-20T00:00:00Z", "precision": "YEAR", "description": "User database with emails and hashed passwords was compromised.", "site_description": "Social networking platform."}], "downloaded": "2025-07-22T08:00:00Z"}], "first_downloaded": "2025-07-25T09:30:00Z", "latest_downloaded": "2025-07-25T09:30:00Z", "source_type": "MalwareLogs"}]}]
```



#### Update Playbook Alert
Update playbook alert in Recorded Future.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Playbook Alert ID|Specify the ID of the playbook alert that needs to be updated.|True|String||
|Playbook Alert Category|Specify the category of the playbook alert that needs to be updated.|False|String||
|Assign To|Specify to whom to assign the alert. You must provide a user uhash.|False|String||
|Log Entry|Specify a comment to be added on the update action.|False|String||
|Status|Specify the new status for the alert.|False|List|None|
|Priority|Specify the new priority for the alert.|False|List|None|
|Reopen Strategy|Specify the reopen strategy for the alert.|False|List|None|



##### JSON Results
```json
{"success": {"id": "task:5d242d94-eaa4-4c9d-baba-97feb0e61111"}}
```



#### Remove List Entities
Get a list by its ID. Use this method to retrieve list info.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List ID|The ID for the list.|True|String|None|
|Entity ID|ID of the entity to add.|False|String|None|
|Entity Name|Name of the entity to add.|False|String|None|
|Entity Type|Type of the entity to add.|False|String|None|



##### JSON Results
```json
{"removed": ["ip:2.2.2.2"], "unchanged": ["ip:1.1.1.1"], "error": [{"message": "Error details", "id": "bad_id"}]}
```



#### Lookup Password
Checks if specified passwords were exposed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Algorithm|The algorithm used for the password hash.|True|String|None|



##### JSON Results
```json
[{"password": {"algorithm": "SHA256", "hash_prefix": "6eeb059362f68f51b634eda277d5b5a5f5761a9742b70493bc0e6860b0f9a394"}, "exposure_status": "Uncommon"}, {"password": {"algorithm": "SHA1", "hash_prefix": "a9c26fb1cdff1b4a509905f30980fd0584956a63"}, "exposure_status": "Uncommon"}]
```



#### Entity Lookup
Look up a Recorded Future ID for entity details.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Entity ID|Recorded Future ID to look up.|True|String|None|



##### JSON Results
```json
{"id": "ANtblN", "type": "Organization", "attributes": {"name": "Entity Name", "common_names": ["Entity Common Name"], "alias": ["Entity Alias"], "is_threat_actor": true}}
```



#### Create Auto Sigma Rule
Create a new Auto Sigma rule based on the query provided.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job Name|The job name.|True|String|None|
|Query|The filtering query to perform.|True|String|None|
|Start Date|The earliest date to include in the query.|True|String|None|
|End Date|The latest date to include in the query.|False|String|None|



##### JSON Results
```json
{"jobId": "string", "name": "string", "created": "2025-03-18T08:57:24.855198", "modified": "2025-03-18T08:57:24.855198", "status": "CREATED", "query": "sample.tags == \"family:redline\"", "startDate": "2024-11-01", "endDate": "2024-11-30", "nMatchedHashes": 0, "familyCounts": {"family:cobaltstrike": 100, "family:xmrig": 5}, "sigma_rules": [{"rule": "string", "rule_id": "string", "stats": {"n_hashes": 100, "overlap": 100, "family_counts": {"family:cobaltstrike": 100, "family:xmrig": 5}}, "status": "True Positive", "modified": "2025-03-18T08:57:24.855198"}], "patterns": [{"image": "string", "cmd_pattern": "string", "matched_cmds": ["string"], "stats": {"n_hashes": 100, "overlap": 100, "family_counts": {"family:cobaltstrike": 100, "family:xmrig": 5}}}]}
```



#### Search List
The operation finds lists based on a query.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Name|List name to search.|False|String|None|
|List Type|List type to filter by. Ignored if None.|False|String|None|
|Max Results|Maximum number of lists to return.|False|String|25|



##### JSON Results
```json
[{"id": "report:aaaaaa", "name": "Watch List Name", "type": "tech_stack", "created": "2022-05-06T08:19:31.407000Z", "updated": "2025-11-07T09:37:38.453000Z", "owner_id": "uhash:1234567", "owner_name": "Owner Name", "organisation_id": "uhash:7654321", "organisation_name": "Organisation Name", "owner_organisation_details": {"organisations": [{"organisation_id": "uhash:1234567", "organisation_name": "Organisation Name"}], "enterprise_id": "uhash:12345678", "enterprise_name": "Enterprise Name"}}]
```



#### Add List Entities
Add SecOps entities to a list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List ID|The ID for the list.|True|String|None|
|Entity ID|ID of the entity to add.|False|String|None|
|Entity Name|Name of the entity to add.|False|String|None|
|Entity Type|Type of the entity to add.|False|String|None|



##### JSON Results
```json
{"added": ["Jp8zD1"], "unchanged": ["ip:2.2.2.2"], "error": [{"message": "Error details", "id": "bad_id"}]}
```



#### Fetch Incident Report
Get a detailed exposure incident report for a single malware log, including compromised credentials, device details, and malware attribution.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Source|The raw archive name containing malware log data.|True|String|None|
|Include Details|Whether to include infected machine details.|False|Boolean|true|
|Organization ID|The org_id in multi-org setup.|False|String|None|
|Max Results|Maximum number of credentials to return.|False|String|None|



##### JSON Results
```json
{"credentials": [{"authorization_domain": "login.microsoftonline.com", "email_or_login": "admin_user", "password": "CompanySecret!2024", "password_sha1": "2ef7bde608ce5404e97d5f042f95f89f1c232871", "domain_category": "Cloud Provider", "domain_technology": "Microsoft Office 365", "contains_cookies": true, "contains_active_cookies": true, "contains_high_risk_technologies": true}], "details": {"malware_family": "RedLine Stealer", "os": "Windows 10 Pro", "os_username": "jsmith", "malware_file": "C:\\Users\\jsmith\\AppData\\Local\\Temp\\winmgr.exe", "timezone": "America/New_York", "uac": "UAC-Admin", "exfiltration_date": "2025-07-24T14:30:00Z", "antivirus": "Windows Defender", "ip_address": "198.51.100.14", "postal_code": "90210", "country": "United States"}}
```



#### Lookup Hostname Credentials
Identity - Find credentials compromised from a specific hostname.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Hostname|The hostname of a compromised machine.|False|String|None|
|Filter on Target Entities|If the action should filter the search on the Target Entities.|False|Boolean|None|
|First Downloaded GTE|First date when these credentials were received and indexed by Recorded Future.|False|String|None|
|Latest Downloaded GTE|Latest date when these credentials were received and indexed by Recorded Future.|False|String|None|
|Exfiltration Date GTE|Date when the infostealer malware exfiltrated data from the victim device.|False|String|None|
|Properties|Password properties.|False|String|None|
|Breach Name|The name of a breach.|False|String|None|
|Breach Date|The date of a breach.|False|String|None|
|Dump Name|The name of a database dump.|False|String|None|
|Dump Date|The date of a database dump.|False|String|None|
|Username Properties|Username properties. Only valid value is 'Email'.|False|String|None|
|Authorization Technologies|Authorization technologies to filter by.|False|String|None|
|Authorization Protocols|Authorization protocols to filter by.|False|String|None|
|Malware Families|Known infostealer malware families.|False|String|None|
|Organization ID|An organization ID if utilizing a multi-org setup.|False|String|None|
|Max Results|The maximum number of credential records returned.|False|String|None|



##### JSON Results
```json
[{"identity": {"subjects": ["j.doe@example-corp.com"]}, "count": 0, "credentials": [{"subject": "j.doe@example-corp.com", "authorization_service": {"url": "https://signin.example-corp.com/login", "domain": "example-corp.com", "fqdn": "signin.example-corp.com", "protocols": ["HTTPS"], "technology": [{"id": "tech-wordpress", "name": "WordPress", "category": "CMS"}]}, "authorization_services": [{"url": "https://signin.example-corp.com/login", "domain": "example-corp.com", "fqdn": "signin.example-corp.com", "protocols": ["HTTPS"], "technology": [{"id": "tech-wordpress", "name": "WordPress", "category": "CMS"}]}], "exposed_secret": {"type": "Password", "effectively_clear": true, "hashes": [{"algorithm": "SHA1", "hash": "5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8"}], "details": {"clear_text_value": "password123", "clear_text_hint": "p***3", "properties": ["Letter"]}}, "compromise": {"exfiltration_date": "2025-01-10T18:00:00Z"}, "cookies": [{"dns": ".example.com", "name": "session_id", "http": true, "expiration": "2025-08-25T09:57:39Z", "secure": true, "value": "3a2d5f8b-9e4c-4a1d-b8f9-c6e7d8f9a0b1"}], "malware_family": {"id": "mal-vidar", "name": "Vidar Stealer"}, "dumps": [{"name": "Antiscam Log 2024-07-22", "type": "Stealer Log", "source": "dump-antiscam-2024-07-22-045", "description": "Log data from Antiscam malware campaign.", "infrastructure": {"ip": "203.0.113.55"}, "compromise": {"os": "Windows 11", "os_username": "victim_user", "malware_file": "C:\\Windows\\Temp\\update.exe", "timezone": "(UTC+02:00) Helsinki, Kyiv, Riga, Sofia, Tallinn, Vilnius", "computer_name": "DESKTOP-A1B2C3D", "uac": "UAC-Limited", "antivirus": ["Avast"], "exfiltration_date": "2025-07-21T12:00:00Z"}, "location": {"country": {"name": "UNITED_STATES", "displayName": "United States", "countryCode": "USA", "alpha2Code": "US", "alpha3Code": "USA"}, "city": "New York", "address": "123 Main Street, Apt 4B", "address1": "123 Main Street", "address2": "Apt 4B", "state": "NY", "postal_code": "10001", "zip": "10001"}, "breaches": [{"name": "SocialNet Breach", "domain": "socialnet.com", "type": "Database Breach", "breached": "2023-11-01T00:00:00Z", "start": "2023-10-15T00:00:00Z", "stop": "2023-10-20T00:00:00Z", "precision": "YEAR", "description": "User database with emails and hashed passwords was compromised.", "site_description": "Social networking platform."}], "downloaded": "2025-07-22T08:00:00Z"}], "first_downloaded": "2025-07-25T09:30:00Z", "latest_downloaded": "2025-07-25T09:30:00Z", "source_type": "MalwareLogs"}]}]
```



#### Add Analyst Note
Add an analyst note to previously enriched entities in Siemplify, to Recorded Future entities. Action will add the note to the relevant scope entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Note Title|Specify the title for the note|True|String|Note Title|
|Note Text|Specify the Text for the note|True|String|Note Text|
|Topic|Specify the relevant Note topic from the list, if needed.|False|List|None|



##### JSON Results
```json
{"note_id": "doc:aaaaaaa"}
```



#### Create List
This operation creates a new list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Name|The name of the new list.|True|String|None|
|List Type|The type of list to create.|False|List|entity|



##### JSON Results
```json
{"id_": "report:BE2oLCK", "name": "gsecops soar test", "type_": "entity", "created": "2026-02-26T22:03:07.888000Z", "updated": "2026-02-26T22:03:07.888000Z", "owner_id": "uhash:6fyfhapHEs", "owner_name": "Google SecOps SOAR", "organisation_id": "uhash:5zQaSyRpA1", "organisation_name": "Professional Services Development", "owner_organisation_details": {"owner_id": "uhash:6fyfhapHEs", "owner_name": "Google SecOps SOAR", "organisations": [], "enterprise_id": "uhash:5zQaSyRpA1", "enterprise_name": "Professional Services Development"}}
```



#### Update Alert
Update alert in Recorded Future.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify the ID of the alert that needs to be updated.|True|String||
|Assign To|Specify to whom to assign the alert. You can provide id, username, user hash, or email.|False|String||
|Note|Specify a note that should be updated on the alert.|False|String||
|Status|Specify the new status for the alert.|False|List|None|



##### JSON Results
```json
{"success": {"id": "jU2F_w"}}
```



#### Detonate URL
Submits a URL to the Recorded Future Sandbox for analysis.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Profile|Specify the Sandbox profile.|False|String||



##### JSON Results
```json
{"Entity": "https://example.com/here.php", "EntityResult": {"version": "0.3.1", "build": "77bbc21", "sample": {"id": "260123-tbr1911111", "score": 4, "target": "https://example.com/here.php", "created": "2026-01-23T15:53:19Z", "completed": "2026-01-23T15:55:51Z"}, "tasks": [{"sample": "260123-tbr1911111", "kind": "behavioral", "name": "behavioral1", "status": "reported", "tags": ["discovery"], "score": 4, "target": "https://example.com/here.php", "backend": "sbx4m106", "resource": "win10v2004-20260115-en", "os": "windows10-2004-x64", "timeout": 150, "sigs": 10}, {"sample": "260123-tbr1911111", "kind": "static", "name": "static1", "status": "reported", "score": 1}, {"sample": "260123-tbr1911111", "kind": "urlscan", "name": "urlscan1", "status": "reported", "score": 1}], "analysis": {"score": 4, "tags": ["discovery"]}, "targets": [{"tasks": ["behavioral1"], "score": 4, "target": "https://example.com/here.php", "tags": ["discovery"], "signatures": [{"label": "fw_programfiles", "name": "Drops file in Program Files directory", "score": 4}, {"label": "browser_information_discovery", "name": "Browser Information Discovery", "score": 3, "ttp": ["T1217"], "tags": ["discovery"], "desc": "Enumerate browser information."}, {"label": "reg_hw_processor", "name": "Checks processor information in registry", "ttp": ["T1012", "T1082"], "desc": "Processor information is often read in order to detect sandboxing environments."}, {"label": "reg_hw_system", "name": "Enumerates system info in registry", "ttp": ["T1012", "T1082"]}, {"label": "reg_hku_write", "name": "Modifies data under HKEY_USERS"}, {"label": "reg_software_classes", "name": "Modifies registry class"}, {"name": "Suspicious behavior: EnumeratesProcesses"}, {"name": "Suspicious behavior: NtCreateUserProcessBlockNonMicrosoftBinary"}, {"name": "Suspicious use of FindShellTrayWindow"}, {"name": "Suspicious use of WriteProcessMemory"}], "iocs": {"urls": ["https://example.com/here.php"], "domains": ["example.com"], "ips": ["8.8.8.8"]}}], "signatures": [{"label": "fw_programfiles", "name": "Drops file in Program Files directory", "score": 4}, {"label": "browser_information_discovery", "name": "Browser Information Discovery", "score": 3, "ttp": ["T1217"], "tags": ["discovery"], "desc": "Enumerate browser information."}, {"label": "reg_hw_processor", "name": "Checks processor information in registry", "ttp": ["T1012", "T1082"], "desc": "Processor information is often read in order to detect sandboxing environments."}, {"label": "reg_hw_system", "name": "Enumerates system info in registry", "ttp": ["T1012", "T1082"]}, {"label": "reg_hku_write", "name": "Modifies data under HKEY_USERS"}, {"label": "reg_software_classes", "name": "Modifies registry class"}, {"name": "Suspicious behavior: EnumeratesProcesses"}, {"name": "Suspicious behavior: NtCreateUserProcessBlockNonMicrosoftBinary"}, {"name": "Suspicious use of FindShellTrayWindow"}, {"name": "Suspicious use of WriteProcessMemory"}]}}
```



#### Get List Status
Get status information about list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List ID|The ID for the list.|True|String|None|



##### JSON Results
```json
{"id_": "report:mfLASl", "name": "List Name", "type_": "tech_stack", "created": "2022-05-06T08:19:31.407000Z", "updated": "2025-11-07T09:37:38.453000Z", "owner_id": "uhash:69sKLfTGsS", "owner_name": "Professional Services Development", "organisation_id": "uhash:5zQaSyRpA1", "organisation_name": "Professional Services Development", "owner_organisation_details": {"owner_id": null, "owner_name": null, "organisations": [{"organisation_id": "uhash:69sKLfTGsS", "organisation_name": "Professional Services Development"}], "enterprise_id": "uhash:5zQaSyRpA1", "enterprise_name": "Professional Services Development"}}
```



#### Search Hash Malware Intelligence
Query Recorded Future to get intelligence about hashes that have been already reported in the Sandbox.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|My Enterprise|Specify if the sample hash should be searched in your enterprise submissions only.|False|Boolean|false|
|Start Date|Specify the starting date to lookback. Accept format like 2026-01-23 or -1d|False|String|-30d|
|End Date|Specify the ending date to lookback. Accept format like 2026-01-23 or -1d. None means today.|False|String||



##### JSON Results
```json
[{"Entity": "173bd2fc717b38527a57fad443aac11c49aef61f5f84e175872db53a99d2fd4e", "EntityResult": [{"file": "173bd2fc717b38527a57fad443aac11c49aef61f5f84e175872db53a99d2fd4e", "id": "173bd2fc717b38527a57fad443aac11c49aef61f5f84e175872db53a99d2fd4e-260114-aqb4tafy5f-behavioral1", "task": "behavioral1", "dynamic": {"dumped": [], "dumped_count": 0, "extracted": [{"config": {"c2": ["http://example.com"], "credentials": [], "decoy": [], "dns": [], "family": "cobaltstrike", "keys": [], "listen_for": [], "mutex": [], "rule": "CobaltStrike64", "tags": [], "webinject": []}, "dumped_file": "memory/5316-0-0x000001F1CD3F0000-0x000001F1CD3F1000-memory.dmp", "resource": "behavioral1/memory/5316-0-0x000001F1CD3F0000-0x000001F1CD3F1000-memory.dmp"}, {"config": {"c2": ["8.8.8.8"], "credentials": [], "decoy": [], "dns": [], "family": "metasploit", "keys": [], "listen_for": [], "mutex": [], "rule": "MetasploitStager", "tags": [], "version": "metasploit_stager", "webinject": []}, "dumped_file": "memory/5316-0-0x000001F1CD3F0000-0x000001F1CD3F1000-memory.dmp", "resource": "behavioral1/memory/5316-0-0x000001F1CD3F0000-0x000001F1CD3F1000-memory.dmp"}], "network": {"dns": [{"flow_id": 6, "request_domain": ["g.bing.com"], "request_domain_fld": ["bing.com"], "request_domain_tld": ["com"], "request_type": ["IN A"], "response_domain": ["g.bing.com"], "response_domain_fld": ["bing.com"], "response_domain_tld": ["com"], "response_type": ["IN A"], "response_value": ["8.8.8.8"]}, {"flow_id": 47, "request_domain": ["tse1.mm.bing.net"], "request_domain_fld": ["bing.net"], "request_domain_tld": ["net"], "request_type": ["IN A"], "response_domain": ["mm-mm.bing.net.trafficmanager.net"], "response_domain_fld": ["bing.net"], "response_domain_tld": ["net"], "response_type": ["IN CNAME"], "response_value": ["8.8.8.8"]}, {"flow_id": 55, "request_domain": ["c.pki.goog"], "request_domain_fld": ["pki.goog"], "request_domain_tld": ["goog"], "request_type": ["IN A"], "response_domain": ["c.pki.goog"], "response_domain_fld": ["google.com"], "response_domain_tld": ["goog"], "response_type": ["IN A"], "response_value": ["8.8.8.8"]}], "dns_count": 1, "flows": [{"dst_ip": "8.8.8.8", "dst_port": 53, "id": 6, "layer_7": ["dns"], "proto": "udp"}], "flows_count": 1, "http": [{"flow": 7, "sequence": [{"index": 1, "request": {"headers": ["host: g.bing.com", "accept-encoding: gzip, deflate", "user-agent: WindowsShellClient/9.0.40929.0 (Windows)"], "method": "GET", "request": "GET /neg/0?action=impression&rlink=https%3A%2F%2Fwww.bing.com%2Faclick%3Fld%3De8oslJXf4-NhZcDJdUJRfeVzVUCUwWDSNY1DQ7fONUSLRUSSuZWb9CIzOBhlNjSjabErTFTRct_gSpEX3TTnZUAjpxGiFDjsR6axecxkuR-16oNGGV8xgQ2zlIj8WHCs1lxExWmhZxnv_ORw_R9invbuuvJVLw5_63jj4U-ERfg-aFiVmw%26u%3DbWljcm9zb2Z0LWVkZ2UlM2FodHRwcyUzYSUyZiUyZnd3dy5taWNyb3NvZnQuY29tJTJmbWljcm9zb2Z0LTM2NSUyZmJ1eSUyZmNvbXBhcmUtYWxsLW1pY3Jvc29mdC0zNjUtcHJvZHVjdHMlM2ZPQ0lEJTNkY21tNmNyMTkxM20lMjZmb3JtJTNkTTUwMDZY%26rlid%3D38077aef22e91de5980f13ba495ddd1f&TIME=20251231T183040Z&CID=533126158&EID=533126158&tids=15000&adUnitId=11730597&localId=w:2FD4D7EC-4347-87A6-34AF-A3199BBC538B&deviceId=6825865688752331&muid=2FD4D7EC434787A634AFA3199BBC538B HTTP/2.0", "url": "https://g.bing.com/neg/0?action=impression&rlink=https%3A%2F%2Fwww.bing.com%2Faclick%3Fld%3De8oslJXf4-NhZcDJdUJRfeVzVUCUwWDSNY1DQ7fONUSLRUSSuZWb9CIzOBhlNjSjabErTFTRct_gSpEX3TTnZUAjpxGiFDjsR6axecxkuR-16oNGGV8xgQ2zlIj8WHCs1lxExWmhZxnv_ORw_R9invbuuvJVLw5_63jj4U-ERfg-aFiVmw%26u%3DbWljcm9zb2Z0LWVkZ2UlM2FodHRwcyUzYSUyZiUyZnd3dy5taWNyb3NvZnQuY29tJTJmbWljcm9zb2Z0LTM2NSUyZmJ1eSUyZmNvbXBhcmUtYWxsLW1pY3Jvc29mdC0zNjUtcHJvZHVjdHMlM2ZPQ0lEJTNkY21tNmNyMTkxM20lMjZmb3JtJTNkTTUwMDZY%26rlid%3D38077aef22e91de5980f13ba495ddd1f&TIME=20251231T183040Z&CID=533126158&EID=533126158&tids=15000&adUnitId=11730597&localId=w:2FD4D7EC-4347-87A6-34AF-A3199BBC538B&deviceId=6825865688752331&muid=2FD4D7EC434787A634AFA3199BBC538B"}, "response": {"headers": ["cache-control: no-cache, must-revalidate", "pragma: no-cache", "expires: Fri, 01 Jan 1990 00:00:00 GMT", "set-cookie: MUID=2AF5D68AF38866192E02C06BF2466722; domain=.bing.com; expires=Mon, 08-Feb-2027 00:25:34 GMT; path=/; SameSite=None; Secure; Priority=High;", "strict-transport-security: max-age=31536000; includeSubDomains; preload", "access-control-allow-origin: *", "x-cache: CONFIG_NOCACHE", "accept-ch: Sec-CH-UA-Arch, Sec-CH-UA-Bitness, Sec-CH-UA-Full-Version, Sec-CH-UA-Full-Version-List, Sec-CH-UA-Mobile, Sec-CH-UA-Model, Sec-CH-UA-Platform, Sec-CH-UA-Platform-Version", "x-msedge-ref: Ref A: B35168FEDE1047359F276C0D318CD4E8 Ref B: LON281181714054 Ref C: 2026-01-14T00:25:34Z", "date: Wed, 14 Jan 2026 00:25:33 GMT"], "response": "HTTP/2.0 204", "status": "204"}}, {"index": 2, "request": {"headers": ["host: g.bing.com", "accept-encoding: gzip, deflate", "user-agent: WindowsShellClient/9.0.40929.0 (Windows)", "cookie: MUID=2AF5D68AF38866192E02C06BF2466722; _EDGE_S=SID=1F8800DF742C62953942163E750463BB"], "method": "GET", "request": "GET /neg/0?action=impression&rlink=https%3A%2F%2Fwww.bing.com%2Faclick%3Fld%3De8oslJXf4-NhZcDJdUJRfeVzVUCUwWDSNY1DQ7fONUSLRUSSuZWb9CIzOBhlNjSjabErTFTRct_gSpEX3TTnZUAjpxGiFDjsR6axecxkuR-16oNGGV8xgQ2zlIj8WHCs1lxExWmhZxnv_ORw_R9invbuuvJVLw5_63jj4U-ERfg-aFiVmw%26u%3DbWljcm9zb2Z0LWVkZ2UlM2FodHRwcyUzYSUyZiUyZnd3dy5taWNyb3NvZnQuY29tJTJmbWljcm9zb2Z0LTM2NSUyZmJ1eSUyZmNvbXBhcmUtYWxsLW1pY3Jvc29mdC0zNjUtcHJvZHVjdHMlM2ZPQ0lEJTNkY21tNmNyMTkxM20lMjZmb3JtJTNkTTUwMDZY%26rlid%3D38077aef22e91de5980f13ba495ddd1f&TIME=20251231T183040Z&CID=533126158&EID=&tids=15000&adUnitId=11730597&localId=w:2FD4D7EC-4347-87A6-34AF-A3199BBC538B&deviceId=6825865688752331&muid=2FD4D7EC434787A634AFA3199BBC538B HTTP/2.0", "url": "https://g.bing.com/neg/0?action=impression&rlink=https%3A%2F%2Fwww.bing.com%2Faclick%3Fld%3De8oslJXf4-NhZcDJdUJRfeVzVUCUwWDSNY1DQ7fONUSLRUSSuZWb9CIzOBhlNjSjabErTFTRct_gSpEX3TTnZUAjpxGiFDjsR6axecxkuR-16oNGGV8xgQ2zlIj8WHCs1lxExWmhZxnv_ORw_R9invbuuvJVLw5_63jj4U-ERfg-aFiVmw%26u%3DbWljcm9zb2Z0LWVkZ2UlM2FodHRwcyUzYSUyZiUyZnd3dy5taWNyb3NvZnQuY29tJTJmbWljcm9zb2Z0LTM2NSUyZmJ1eSUyZmNvbXBhcmUtYWxsLW1pY3Jvc29mdC0zNjUtcHJvZHVjdHMlM2ZPQ0lEJTNkY21tNmNyMTkxM20lMjZmb3JtJTNkTTUwMDZY%26rlid%3D38077aef22e91de5980f13ba495ddd1f&TIME=20251231T183040Z&CID=533126158&EID=&tids=15000&adUnitId=11730597&localId=w:2FD4D7EC-4347-87A6-34AF-A3199BBC538B&deviceId=6825865688752331&muid=2FD4D7EC434787A634AFA3199BBC538B"}, "response": {"headers": ["cache-control: no-cache, must-revalidate", "pragma: no-cache", "expires: Fri, 01 Jan 1990 00:00:00 GMT", "strict-transport-security: max-age=31536000; includeSubDomains; preload", "access-control-allow-origin: *", "x-cache: CONFIG_NOCACHE", "accept-ch: Sec-CH-UA-Arch, Sec-CH-UA-Bitness, Sec-CH-UA-Full-Version, Sec-CH-UA-Full-Version-List, Sec-CH-UA-Mobile, Sec-CH-UA-Model, Sec-CH-UA-Platform, Sec-CH-UA-Platform-Version", "x-msedge-ref: Ref A: 12102ACE805B48E0A1DC802E0077AEB5 Ref B: LON281181714054 Ref C: 2026-01-14T00:25:34Z", "date: Wed, 14 Jan 2026 00:25:34 GMT"], "response": "HTTP/2.0 204", "status": "204"}}]}], "ips": [{"asn": "AS16625", "cc": "GB", "ip": "104.78.173.167"}], "ips_count": 20}, "processes": [{"cmd": "rundll32.exe C:\\Users\\Admin\\AppData\\Local\\Temp\\payload.dll,#1", "image": "C:\\Windows\\system32\\rundll32.exe", "pid": 5316, "procid": 84, "procid_parent": 54}], "registry_count": 0, "signatures": [{"desc": "Detected malicious payload which is part of Cobaltstrike.", "indicators": [], "name": "Cobaltstrike", "label": "cobaltstrike", "score": 10, "tags": ["trojan", "backdoor", "family:cobaltstrike"], "ttp": []}], "signatures_count": 5}, "metadata": {"industries": [], "sectors": [], "source": "triage_public"}, "pe": {"exports": ["Exec", "key", "keyLen", "sc", "xdec"], "header": {"dll_characteristics": ["IMAGE_DLLCHARACTERISTICS_HIGH_ENTROPY_VA"], "file_characteristics": ["IMAGE_FILE_EXECUTABLE_IMAGE"]}, "imphash": "e98718d3ee79297035cbb3d089dc93f3", "imports": [{"dll_name": "kernel32", "imports": ["CreateThread"]}], "sections": [{"characteristics": ["IMAGE_SCN_CNT_CODE"], "name": ".text", "raw_data_offset": 1024, "raw_data_size": 5632, "virtual_size": 5480}], "signatures": [], "timestamp": 1768009464}, "sample": {"completed": "2026-01-14T00:28:03.000Z", "created": "2026-01-14T00:24:34.000Z", "id": "260114-aqb4tafy5f", "score": 10, "tags": ["windows:4", "windows", "arch:x64", "backdoor", "family:cobaltstrike", "family:metasploit", "trojan", "x64"]}, "static": {"exts": [".dll"], "sha1": "8084306d632bbe48651fe9b63aa71000c4e173c4", "md5": "c6783a0d72bac8299609c5073c4a0b69", "sha256": "173bd2fc717b38527a57fad443aac11c49aef61f5f84e175872db53a99d2fd4e", "sha512": "1b89afc0c7542c38f963f6d54a30cbc17a7c43480ebc947d59e76f0e44f40084bb43b9db32eec8dd8619a989ae1da0c0f49021d8caab79fa92d58ba8dc959dd8", "size": 13312, "ssdeep": "192:+189Z/J9VE+lrHo3DOV6k3EZVjYwsvg+8yV6B/A97I3hwcN:+18L/J9/EDCEZewsvh86iA97I3hwcN", "tags": ["windows:4", "windows", "x64", "arch:x64"], "target": "payload.dll", "extracted": [], "registry_count": 0, "signatures": [{"desc": "Checks for missing Authenticode signature.", "indicators": [], "name": "Unsigned PE", "label": "unsigned_pe", "score": 3, "tags": [], "ttp": []}], "signatures_count": 1}}]}]
```



#### Entity Match
Matches entity by name and (optionally) type.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Entity Name|This mandatory free text search field is used to match against entity names.|True|String|None|
|Entity Type|A comma separated string of types is optional. If in use, the Match operation will only try to match on entities that meet any of the type criteria.|False|String|None|
|Limit|This optional field is used to limit the max number of responses returned (maximum 100).|False|String|10|



##### JSON Results
```json
[{"entity": "Entity Name", "is_found": true, "content": {"id": "JVlhYg", "name": "Entity Name", "type": "Organization"}}]
```



#### Enrich Hash
Query Recorded Future to get intelligence about the hash.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Risk Score Threshold|Represents the minimum malicious risk score for a Hash to be marked malicious. Has a range of 0-89. Has the bands levels:  No Suspicious/Malicious content: 0  Unusual: 5-24  Suspicious: 25-64  Malicious: 65-89|True|String|25|
|Include Links|If enabled, action will get information about links.|False|Boolean|false|
|Enable Collective Insights|If enabled, contribute detections back to Recorded Future.|False|Boolean|true|



##### JSON Results
```json
[{"Entity": "07c70968c66c93b6d6c9a90255e1c81a3b385632c83f53f69534b3f55212ced9", "EntityResult": [{"entity": {"id": "hash:07c70968c66c93b6d6c9a90255e1c81a3b385632c83f53f69534b3f55212ced9", "name": "07c70968c66c93b6d6c9a90255e1c81a3b385632c83f53f69534b3f55212ced9", "type": "Hash"}, "intelCard": "https://app.recordedfuture.com/live/sc/entity/hash%3A07c70968c66c93b6d6c9a90255e1c81a3b385632c83f53f69534b3f55212ced9", "risk": {"criticalityLabel": "Malicious", "riskString": "6/17", "rules": 6, "criticality": 3, "riskSummary": "6 of 17 Risk Rules currently observed.", "score": 89, "evidenceDetails": [{"mitigationString": "", "evidenceString": "Previous sightings on 1 source: Recorded Future Analyst Community Trending Indicators. Observed between Nov 1, 2023, and Nov 2, 2023.", "rule": "Historically Reported in Threat List", "criticality": 1, "timestamp": "2024-07-19T03:02:09.151Z", "criticalityLabel": "Unusual"}, {"mitigationString": "", "evidenceString": "10 sightings on 1 source: cyble.com. 1 related attack vector: Reflective DLL Injection. Most recent link (Sep 22, 2023): https://cyble.com/blog/evasive-noescape-ransomware-uses-reflective-dll-injection/", "rule": "Linked to Attack Vector", "criticality": 2, "timestamp": "2023-09-22T05:00:51.270Z", "criticalityLabel": "Suspicious"}, {"mitigationString": "", "evidenceString": "2 sightings on 1 source: Insikt Group.", "rule": "Linked to Cyber Attack", "criticality": 2, "timestamp": "2023-07-28T21:26:21.507Z", "criticalityLabel": "Suspicious"}, {"mitigationString": "", "evidenceString": "97 sightings on 3 sources: cyble.com, Insikt Group, CERT-IN India. 2 related malware families: NoEscape, Ransomware. Most recent link (Oct 6, 2023): https://www.cert-in.org.in/s2cMainServlet?pageid=PUBVA01&VACODE=CIVA-2023-2154", "rule": "Linked to Malware", "criticality": 2, "timestamp": "2023-10-06T00:00:00.000Z", "criticalityLabel": "Suspicious"}, {"mitigationString": "", "evidenceString": "7 sightings on 5 sources: Recorded Future Sandbox, Polyswarm Sandbox Analysis, Recorded Future Triage Malware Analysis, PolySwarm PolyUnite, PolySwarm. Malware sandbox report for 07c70968c66c93b6d6c9a90255e1c81a3b385632c83f53f69534b3f55212ced9 on October 08, 2023.   Score: 10 (Known bad). No malware detections. Contains: 6 ATT&CK behaviors, 0 command and control indicators, and 4 signatures. Most recent link (Jun 5, 2023): https://polyswarm.network/scan/results/file/07c70968c66c93b6d6c9a90255e1c81a3b385632c83f53f69534b3f55212ced9", "rule": "Positive Malware Verdict", "criticality": 3, "timestamp": "2023-06-05T00:42:04.000Z", "criticalityLabel": "Malicious"}, {"mitigationString": "", "evidenceString": "2 sightings on 1 source: Insikt Group. 2 reports including Insikt Validated TTP: Detecting NoEscape Ransomware Using Sigma and YARA. Most recent link (Jul 28, 2023): https://app.recordedfuture.com/portal/analyst-note/doc:sJl6II", "rule": "Reported by Insikt Group", "criticality": 3, "timestamp": "2023-07-28T00:00:00.000Z", "criticalityLabel": "Malicious"}]}, "timestamps": {"lastSeen": "2024-07-19T03:00:51.047Z", "firstSeen": "2023-07-17T23:28:08.769Z"}, "hashAlgorithm": "SHA-256", "links": {"Actors, Tools & TTPs": [{"id": "mitre:T1053.005", "name": "T1053.005", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1057", "name": "T1057", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1070.002", "name": "T1070.002", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1070.004", "name": "T1070.004", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1083", "name": "T1083", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1112", "name": "T1112", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1120", "name": "T1120", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1134", "name": "T1134", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1135", "name": "T1135", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1486", "name": "T1486", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1489", "name": "T1489", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1490", "name": "T1490", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1548.002", "name": "T1548.002", "type": "MitreAttackIdentifier"}, {"id": "rXVuTR", "name": "N0_Esc4pe", "type": "Person"}, {"id": "rXMfyJ", "name": "NoEscape", "type": "Malware"}]}}]}]
```



#### Get List Entities
This operation returns the entities in a specific list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List ID|The ID for the list.|True|String|None|



##### JSON Results
```json
[{"entity": {"id": "ip:1.1.1.1", "name": "1.1.1.1", "type": "IpAddress"}, "context": {"annotation": ""}, "status": "ready", "added": "2026-01-27T00:11:30.505000Z"}]
```



#### Enrich CVE
Query Recorded Future to get intelligence about the CVE.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Risk Score Threshold|Represents the minimum malicious risk score for a CVE to be marked malicious. Has a range of 0-99. Has the following levels:  Very Critical: 90-99  Critical: 80-89  High: 65-79  Medium: 25-64  Low: 5-24  None: 0|True|String|25|
|Include Links|If enabled, action will get information about links.|False|Boolean|false|
|Enable Collective Insights|If enabled, contribute detections back to Recorded Future.|False|Boolean|true|



##### JSON Results
```json
[{"Entity": "CVE-2014-0160", "EntityResult": [{"entity": {"id": "K5GW38", "name": "CVE-2014-0160", "type": "CyberVulnerability", "description": "The (1) TLS and (2) DTLS implementations in OpenSSL 1.0.1 before 1.0.1g do not properly handle Heartbeat Extension packets, which allows remote attackers to obtain sensitive information from process memory via crafted packets that trigger a buffer over-read, as demonstrated by reading private keys, related to d1_both.c and t1_lib.c, aka the Heartbleed bug."}, "intelCard": "https://app.recordedfuture.com/live/sc/entity/K5GW38", "risk": {"criticalityLabel": "High", "riskString": "13/23", "rules": 13, "criticality": 3, "riskSummary": "13 of 23 Risk Rules currently observed.", "score": 79, "evidenceDetails": [{"mitigationString": "", "evidenceString": "38 sightings on 19 sources including: eurosecglobal.de, infura-ipfs.io, AlienVault | Indicators, DOCPlayer, MyNavi News. 10 related malware families including AsyncRAT, PittyTiger, njRAT, Orcus RAT, Revenge RAT. Most recent link (Mar 17, 2024): https://otx.alienvault.com/indicator/ip/1.1.1.1", "rule": "Historically Linked to Remote Access Trojan", "criticality": 1, "timestamp": "2024-03-17T02:50:54.334Z", "criticalityLabel": "Low"}, {"mitigationString": "", "evidenceString": "161 sightings on 93 sources including: BitCity, weebly.com, Slashdot, TMCnet | IT Security News, Image OCR. 16 related malware families including Ryuk Ransomware, Simplelocker, GandCrab, Life Ransomware, Cryptolocker. Most recent tweet: Module 13: Case Studies Target: Equifax Breach Target: Stuxnet Attack Target: Sony Pictures Hack Target: Ashley Madison Data Breach Target: NotPetya Target: WannaCry Ransomware Target: TJX Hack Target: Heartbleed Vulnerability Target: OPM Data Breach Target: DNC Hack. Most recent link (Feb 23, 2024): https://twitter.com/cybercitad31/statuses/1760898086849630391", "rule": "Historically Linked to Ransomware", "criticality": 1, "timestamp": "2024-02-23T05:23:14.000Z", "criticalityLabel": "Low"}, {"mitigationString": "", "evidenceString": "1256 sightings on 485 sources including: PasteBin, Reddit InfoSec Comments, FreeBufCOM, F5 Labs All, venafi.com. Most recent tweet: Exploit Shellshock vulnerability CVE 2014-6271 using Metasploit #bash #DHCP #heartbleed #metasploit #openssh #qmail #shellshock https://t.co/IPRcyXU7pm. Most recent link (Jul 11, 2024): https://twitter.com/neoslabsec/statuses/1811473637981192578", "rule": "Linked to Historical Cyber Exploit", "criticality": 1, "timestamp": "2024-07-11T18:52:25.000Z", "criticalityLabel": "Low"}, {"mitigationString": "", "evidenceString": "1388 sightings on 309 sources including: PasteBin, Reddit InfoSec Comments, FreeBufCOM, XSS (ex DamageLab) Forum, GlobeNewswire | UNITED STATES. 138 related malware families including Blood, Loader, denial of service, CryptoGraphic, ICS Malware. Most recent tweet: Exploit Shellshock vulnerability CVE 2014-6271 using Metasploit #bash #DHCP #heartbleed #metasploit #openssh #qmail #shellshock https://t.co/IPRcyXU7pm. Most recent link (Jul 11, 2024): https://twitter.com/neoslabsec/statuses/1811473637981192578", "rule": "Historically Linked to Malware", "criticality": 1, "timestamp": "2024-07-11T18:52:25.000Z", "criticalityLabel": "Low"}, {"mitigationString": "", "evidenceString": "344 sightings on 71 sources including: PasteBin, Reddit InfoSec Comments, Telegram - Other Channels, CSOonline.com | Security News, tuxcare.com. Most recent tweet: @mualafjelita @mx00711 @AryBandung seingetnya ya, winnt unicode remote exec scanner, nmap sudah pasti, bbrp tools buat nuke, openssl heartbleed bug (bikin ssh vulnerable), phishing tools, kalo nama2nya ya lupa, suka war pake IRC bots, koleksi zombie servers, bbrp bikin sendiri krn awal2nya suka programming. Most recent link (Sep 16, 2022): https://twitter.com/gggbxng/statuses/1570838542515052544", "rule": "Historically Linked to Penetration Testing Tools", "criticality": 1, "timestamp": "2022-09-16T18:14:27.000Z", "criticalityLabel": "Low"}, {"mitigationString": "", "evidenceString": "2 sightings on 2 sources: Embedded Computing Design | Latest Updates, @vladris. Most recent tweet: CrowdStrike does sound like a named zero-day, eg. HeartBleed Most recent link (Jul 20, 2024): https://twitter.com/vladris/statuses/1814485317899923823", "rule": "Linked to Recent Cyber Exploit", "criticality": 1, "timestamp": "2024-07-20T02:19:45.000Z", "criticalityLabel": "Low"}, {"mitigationString": "", "evidenceString": "2 sightings on 1 source: Insikt Group. 2 reports including Anony0wor is soliciting forum members for the Onliner Spambot database dump. Most recent link (Sep 01, 2017): https://app.recordedfuture.com/portal/analyst-note/doc:VaN5BG", "rule": "Historically Reported by Insikt Group", "criticality": 1, "timestamp": "2017-09-01T00:00:00.000Z", "criticalityLabel": "Low"}, {"mitigationString": "", "evidenceString": "8 sightings on 1 source: Insikt Group. 8 reports including Recorded Future CVE Monthly | October 2022. Most recent link (Nov 08, 2022): https://app.recordedfuture.com/portal/analyst-note/doc:otlc2P", "rule": "Historically Referenced by Insikt Group", "criticality": 1, "timestamp": "2022-11-08T00:00:00.000Z", "criticalityLabel": "Low"}, {"mitigationString": "", "evidenceString": "3 sightings on 2 sources: Telegram - Other Channels, @TaylorGerring. 6 related malware families including DDOS Toolkit, WebShell, Offensive Security Tools (OST), Metasploit Framework, Backdoor Shell. Most recent tweet: News of CrowdStrike makes me feel thankful to have exited IT While at Ethereum in April 2014, HeartBleed was disclosed during a flight from Zurich to Toronto Around the same time, I began leading security initiatives for the crowdsale and planned for DDoS mitigation https://t.co/SEFDiypoKU. Most recent link (Jul 19, 2024): https://twitter.com/TaylorGerring/statuses/1814275982536159557", "rule": "Recently Linked to Malware", "criticality": 2, "timestamp": "2024-07-19T12:27:56.000Z", "criticalityLabel": "Medium"}, {"mitigationString": "", "evidenceString": "3 sightings on 2 sources: Telegram - Other Channels, GitHub. Most recent link (Jul 25, 2024): https://github.com/Abkhalid17/inter-peak_CS-EH_03/commit/0d62f1af6f1fd6770240ac3e1dc4938739241285", "rule": "Recently Linked to Penetration Testing Tools", "criticality": 2, "timestamp": "2024-07-25T08:20:41.344Z", "criticalityLabel": "Medium"}, {"mitigationString": "", "evidenceString": "4 sightings on 1 source: ExploitDB. 1 execution type: Remote. Most recent link (Apr 24, 2014): https://www.exploit-db.com/exploits/32998", "rule": "Historical Verified Proof of Concept Available Using Remote Execution", "criticality": 2, "timestamp": "2014-04-24T00:00:00.000Z", "criticalityLabel": "Medium"}, {"mitigationString": "", "evidenceString": "1 sighting on 1 source: Recorded Future Vulnerability Analysis via National Vulnerability Database. CVSS v3.1 Score (6.7) calculated using NIST reported CVSS Base Score (7.5) and Recorded Future Temporal Metrics. Base vector string: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N/A:N. Temporal vector string: E:F/RL:X/RC:U. Most recent link (Jul 2, 2024): https://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2014-0160", "rule": "NIST Severity: Medium", "criticality": 2, "timestamp": "2024-07-02T17:50:53.614Z", "criticalityLabel": "Medium"}, {"mitigationString": "", "evidenceString": "1 sighting on 1 source: Recorded Future Vulnerability Analysis. 1 all-time daily sighting. Last observed on Jul 2, 2023. Sample hash: 54ec999997684bcc48b86b172316f698adcad178255118ea2eb3d9f3f434f676.", "rule": "Historically Exploited in the Wild by Malware", "criticality": 3, "timestamp": "2023-07-02T00:00:00.000Z", "criticalityLabel": "High"}]}, "timestamps": {"lastSeen": "2024-07-25T18:30:11.752Z", "firstSeen": "2014-04-07T22:55:03.893Z"}, "links": {"Actors, Tools & TTPs": [{"id": "oPC3f7", "name": "APT24", "type": "Organization"}, {"id": "T_2DVa", "name": "anony0wor", "type": "Person"}, {"id": "Omzj-U", "name": "Credential Dumping", "type": "AttackVector"}, {"id": "LShz7z", "name": "MM RAT", "type": "Malware"}, {"id": "Sn0YNg", "name": "Onliner", "type": "Malware"}, {"id": "LShz7p", "name": "Paladin RAT", "type": "Malware"}]}}]}]
```



#### Search Credentials
Identity - Search credential data for a set of domains.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Domains|One or more domains to be queried.|False|String|None|
|Filter on Target Entities|If the action should filter the search on the Target Entities.|False|Boolean|None|
|Domain Types|Domain type filter - 'Email', 'Authorization', or both.|False|String|None|
|First Downloaded GTE|First date when these credentials were received and indexed by Recorded Future.|False|String|None|
|Latest Downloaded GTE|Latest date when these credentials were received and indexed by Recorded Future.|False|String|None|
|Exfiltration Date GTE|Date when the infostealer malware exfiltrated data from the victim device.|False|String|None|
|Properties|Password properties.|False|String|None|
|Breach Name|The name of a breach.|False|String|None|
|Breach Date|The date of a breach.|False|String|None|
|Dump Name|The name of a database dump.|False|String|None|
|Dump Date|The date of a database dump.|False|String|None|
|Username Properties|Username properties. Only valid value is 'Email'.|False|String|None|
|Authorization Technologies|Authorization technologies to filter by.|False|String|None|
|Authorization Protocols|Authorization protocols to filter by.|False|String|None|
|Malware Families|Known infostealer malware families.|False|String|None|
|Organization ID|An organization ID if utilizing a multi-org setup.|False|String|None|
|Max Results|The maximum number of credential records returned.|False|String|None|



##### JSON Results
```json
[{"login": "email@example.com", "domain": "example.com"}, {"login": "admin@example.com", "domain": "example.com"}]
```



#### Create Auto YARA Rule
Create a new Auto YARA rule based on the hashes and/or query provided.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job Name|The job name.|True|String|None|
|Query|The filtering query to perform.|False|String|None|



##### JSON Results
```json
{"job": {"coverage": {"covered_hashes": ["string"], "uncovered_hashes": ["string"]}, "created": "2025-03-18T08:57:24.855198", "job_id": "string", "name": "string", "patterns": [{"ascii": ["string"], "matching_hashes": ["string"], "pattern": "string"}], "status": "CREATED", "query": "sample.tags == \"family:redline\"", "yara_rule_str": "string"}}
```



#### Refresh Playbook Alert
Updates information in a case created by the Playbook Alerts Connector with new data from the Recorded Future platform
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Playbook Alert ID|Specify the ID of the playbook alert for which you would like to fetch details|True|String||
|Category|The Category of the Playbook Alert. Possible values are domain_abuse, cyber_vulnerability, code_repo_leakage, third_party_risk, identity_novel_exposures, and geopolitics_facility|True|String||



##### JSON Results
```json
{"playbook_alert_id": "task:1ce58e62-de8a-471b-81d4-c98743376937", "panel_status": {"status": "New", "priority": "Moderate", "created": "2024-11-05T15:33:25.392Z", "updated": "2024-11-05T15:34:40.652Z", "case_rule_id": "report:oT8Yal", "case_rule_label": "Domain Abuse", "owner_id": "uhash:oDJ5LVWfXL", "owner_name": "Enterprise - Moise", "organisation_id": "uhash:5zQaSyRpA1", "organisation_name": "Professional Services Development", "owner_organisation_details": {"organisations": [{"organisation_id": "uhash:oDJ5LVWfXL", "organisation_name": "Enterprise - Moise"}], "enterprise_id": "uhash:5zQaSyRpA1", "enterprise_name": "Professional Services Development"}, "entity_id": "idn:s.kitca.com", "entity_name": "s.kitca.com", "entity_criticality": "Medium", "risk_score": 26, "context_list": [{"context": "Active Mail Server"}, {"context": "Domain for sale"}], "targets": ["idn:kiteca.com"], "actions_taken": []}, "panel_action": [], "panel_evidence_summary": {"explanation": "Alert was created as a result of a triggered typosquat detection", "resolved_record_list": [{"entity": "idn:mail.h-email.net", "risk_score": 10, "criticality": "Low", "record_type": "MX", "context_list": [{"context": "Active Mail Server"}]}, {"entity": "idn:ns1.parkingcrew.net", "risk_score": 20, "criticality": "Low", "record_type": "NS", "context_list": []}, {"entity": "ip:1.1.1.1", "risk_score": 36, "criticality": "Medium", "record_type": "A", "context_list": []}, {"entity": "idn:ns2.parkingcrew.net", "risk_score": 15, "criticality": "Low", "record_type": "NS", "context_list": []}], "screenshots": [{"description": "An image associated with the Playbook Alert", "image_id": "img:ca92035d-a5b3-49a6-9a0e-a8583a7c0599", "created": "2024-11-05T15:44:51.959Z", "availability": "Available", "tag": "Domain for sale"}], "screenshot_mentions": []}, "panel_evidence_dns": {"ip_list": [{"entity": "ip:1.1.1.1", "risk_score": 36, "criticality": "Medium", "record_type": "A", "context_list": []}], "mx_list": [{"entity": "idn:mail.h-email.net", "risk_score": 10, "criticality": "Low", "record_type": "MX", "context_list": [{"context": "Active Mail Server"}]}], "ns_list": [{"entity": "idn:ns1.parkingcrew.net", "risk_score": 20, "criticality": "Low", "record_type": "NS", "context_list": []}, {"entity": "idn:ns2.parkingcrew.net", "risk_score": 15, "criticality": "Low", "record_type": "NS", "context_list": []}]}, "panel_evidence_whois": {"body": [{"provider": "sub_domain_whois", "entity": "idn:s.kitca.com", "attribute": "attr:whois", "value": {"privateRegistration": false, "status": "clientDeleteProhibited clientRenewProhibited clientTransferProhibited clientUpdateProhibited", "nameServers": ["idn:ns1.parkingcrew.net", "idn:ns2.parkingcrew.net"], "registrarName": "GoDaddy.com, LLC", "createdDate": "2013-07-12T00:00:00.000Z"}, "added": "2024-07-11T00:26:54.263Z"}, {"provider": "sub_domain_whois", "entity": "idn:s.kitca.com", "attribute": "attr:whoisContacts", "value": {"type": "technicalContact"}, "added": "2024-07-11T00:26:54.263Z"}, {"provider": "sub_domain_whois", "entity": "idn:s.kitca.com", "attribute": "attr:whoisContacts", "value": {"type": "administrativeContact"}, "added": "2024-07-11T00:26:54.263Z"}, {"provider": "sub_domain_whois", "entity": "idn:s.kitca.com", "attribute": "attr:whoisContacts", "value": {"type": "registrant"}, "added": "2024-07-11T00:26:54.263Z"}]}, "panel_log": [{"id": "uuid:b42cb447-6d81-4d65-860a-291b6505eb22", "created": "2024-11-05T15:34:40.652Z", "modified": "2024-11-05T15:34:40.652Z", "action_priority": "Moderate", "changes": {"priority_change": {"old": "Informational", "new": "Moderate", "type": "priority_change"}}, "context": {"type": "domain_abuse", "changes": [{"old": "Informational", "new": "Moderate", "type": "priority_change"}, {"domain": "idn:s.kitca.com", "removed": [], "added": [{"id": "idn:mail.h-email.net", "assessments": [{"id": "attr:typosquatVerdictActiveMailServer", "level": 2}]}], "type": "malicious_dns_change"}]}}], "panel_log_v2": [{"id": "uuid:b42cb447-6d81-4d65-860a-291b6505eb22", "created": "2024-11-05T15:34:40.652Z", "changes": [{"old": "Informational", "new": "Moderate", "type": "priority_change"}, {"domain": "s.kitca.com", "removed": [], "added": [{"id": "idn:mail.h-email.net", "assessments": [{"id": "Active Mail Server", "level": 2}]}], "type": "malicious_dns_change"}]}], "category": "domain_abuse", "linked_cases": [1351, 1353, 1356]}
```



#### Search Dump
Search metadata for data dumps and breach databases by name.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Names|The name(s) of a database dump to search for.|True|String|None|
|Max Results|Maximum number of credentials to return.|False|String|None|



##### JSON Results
```json
[{"name": "Antiscam Log 2024-07-22", "type": "Stealer Log", "source": "dump-antiscam-2024-07-22-045", "description": "Log data from Antiscam malware campaign.", "infrastructure": {"ip": "203.0.113.55"}, "compromise": {"os": "Windows 11", "os_username": "victim_user", "malware_file": "C:\\Windows\\Temp\\update.exe", "timezone": "(UTC+02:00) Helsinki, Kyiv, Riga, Sofia, Tallinn, Vilnius", "computer_name": "DESKTOP-A1B2C3D", "uac": "UAC-Limited", "antivirus": ["Avast"], "exfiltration_date": "2025-07-21T12:00:00Z"}, "location": {"country": {"name": "UNITED_STATES", "displayName": "United States", "countryCode": "USA", "alpha2Code": "US", "alpha3Code": "USA"}, "city": "New York", "address": "123 Main Street, Apt 4B", "address1": "123 Main Street", "address2": "Apt 4B", "state": "NY", "postal_code": "10001", "zip": "10001"}, "breaches": [{"name": "SocialNet Breach", "domain": "socialnet.com", "type": "Database Breach", "breached": "2023-11-01T00:00:00Z", "start": "2023-10-15T00:00:00Z", "stop": "2023-10-20T00:00:00Z", "precision": "YEAR", "description": "User database with emails and hashed passwords was compromised.", "site_description": "Social networking platform."}], "downloaded": "2025-07-22T08:00:00Z"}]
```



#### Detonate File
Submits a File to the Recorded Future Sandbox for analysis.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Path|Specify the file path.|True|String||
|File Source|Destination to pull files from. By default, the action attempts to pull the file from Google Cloud storage bucket. Saving an attachment to the local file system is a fallback option.|True|List|None|
|Profile|Specify the Sandbox profile.|False|String||
|Password|Password for the archive sample.|False|String||



##### JSON Results
```json
{"Entity": "https://example.com/here.php", "EntityResult": {"version": "0.3.1", "build": "77bbc21", "sample": {"id": "260123-tbr1911111", "score": 4, "target": "https://example.com/here.php", "created": "2026-01-23T15:53:19Z", "completed": "2026-01-23T15:55:51Z"}, "tasks": [{"sample": "260123-tbr1911111", "kind": "behavioral", "name": "behavioral1", "status": "reported", "tags": ["discovery"], "score": 4, "target": "https://example.com/here.php", "backend": "sbx4m106", "resource": "win10v2004-20260115-en", "os": "windows10-2004-x64", "timeout": 150, "sigs": 10}, {"sample": "260123-tbr1911111", "kind": "static", "name": "static1", "status": "reported", "score": 1}, {"sample": "260123-tbr1911111", "kind": "urlscan", "name": "urlscan1", "status": "reported", "score": 1}], "analysis": {"score": 4, "tags": ["discovery"]}, "targets": [{"tasks": ["behavioral1"], "score": 4, "target": "https://example.com/here.php", "tags": ["discovery"], "signatures": [{"label": "fw_programfiles", "name": "Drops file in Program Files directory", "score": 4}, {"label": "browser_information_discovery", "name": "Browser Information Discovery", "score": 3, "ttp": ["T1217"], "tags": ["discovery"], "desc": "Enumerate browser information."}, {"label": "reg_hw_processor", "name": "Checks processor information in registry", "ttp": ["T1012", "T1082"], "desc": "Processor information is often read in order to detect sandboxing environments."}, {"label": "reg_hw_system", "name": "Enumerates system info in registry", "ttp": ["T1012", "T1082"]}, {"label": "reg_hku_write", "name": "Modifies data under HKEY_USERS"}, {"label": "reg_software_classes", "name": "Modifies registry class"}, {"name": "Suspicious behavior: EnumeratesProcesses"}, {"name": "Suspicious behavior: NtCreateUserProcessBlockNonMicrosoftBinary"}, {"name": "Suspicious use of FindShellTrayWindow"}, {"name": "Suspicious use of WriteProcessMemory"}], "iocs": {"urls": ["https://example.com/here.php"], "domains": ["example.com"], "ips": ["8.8.8.8"]}}], "signatures": [{"label": "fw_programfiles", "name": "Drops file in Program Files directory", "score": 4}, {"label": "browser_information_discovery", "name": "Browser Information Discovery", "score": 3, "ttp": ["T1217"], "tags": ["discovery"], "desc": "Enumerate browser information."}, {"label": "reg_hw_processor", "name": "Checks processor information in registry", "ttp": ["T1012", "T1082"], "desc": "Processor information is often read in order to detect sandboxing environments."}, {"label": "reg_hw_system", "name": "Enumerates system info in registry", "ttp": ["T1012", "T1082"]}, {"label": "reg_hku_write", "name": "Modifies data under HKEY_USERS"}, {"label": "reg_software_classes", "name": "Modifies registry class"}, {"name": "Suspicious behavior: EnumeratesProcesses"}, {"name": "Suspicious behavior: NtCreateUserProcessBlockNonMicrosoftBinary"}, {"name": "Suspicious use of FindShellTrayWindow"}, {"name": "Suspicious use of WriteProcessMemory"}]}}
```



#### Enrich URL
Query Recorded Future to get intelligence about the URL.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Risk Score Threshold|Represents the minimum malicious risk score for a URL to be marked malicious. Has a range of 0-99. Below is the band levels:  Very Malicious: 90-99  Malicious: 65-89  Suspicious: 25-64  Unusual: 5-24  No Malicious content: 0|True|String|25|
|Include Links|If enabled, action will get information about links.|False|Boolean|false|
|Enable Collective Insights|If enabled, contribute detections back to Recorded Future.|False|Boolean|true|



##### JSON Results
```json
[{"Entity": "https://send.exploit.in/", "EntityResult": [{"entity": {"id": "url:https://send.exploit.in/", "name": "https://send.exploit.in/", "type": "URL"}, "intelCard": "https://app.recordedfuture.com/live/sc/entity/url%3Ahttps%3A%2F%2Fsend.exploit.in%2F", "risk": {"criticalityLabel": "Unusual", "riskString": "3/35", "rules": 3, "criticality": 1, "riskSummary": "3 of 35 Risk Rules currently observed.", "score": 24, "evidenceDetails": [{"mitigationString": "", "evidenceString": "83 sightings on 18 sources including: Infoblox, SOCRadar Cyber Intelligence, Google Play Store, CyberInt | Blog, US CERT CISA Alerts. Most recent link (Jun 10, 2024): https://cyberint.com/blog/threat-intelligence/japan-threat-landscape-report/", "rule": "Historically Reported as a Defanged URL", "criticality": 1, "timestamp": "2024-06-10T00:00:00.000Z", "criticalityLabel": "Unusual"}, {"mitigationString": "", "evidenceString": "6 sightings on 1 source: External Sensor Data Analysis. https://send.exploit.in/ is suspected to be a malware site URL/Domain that navigates to malicious content including executables, drive-by infections sites, malicious scripts, viruses, trojans, or code.", "rule": "Historically Suspected Malware Distribution", "criticality": 1, "timestamp": "2024-05-30T17:31:31.424Z", "criticalityLabel": "Unusual"}, {"mitigationString": "", "evidenceString": "1 sighting on 1 source: Insikt Group. 1 report: CISA Releases Advisory on LockBit 3.0 TTPs. Most recent link (Mar 21, 2023): https://app.recordedfuture.com/portal/analyst-note/doc:qd_m7U", "rule": "Historically Reported by Insikt Group", "criticality": 1, "timestamp": "2023-03-21T00:00:00.000Z", "criticalityLabel": "Unusual"}]}, "timestamps": {"lastSeen": "2024-07-01T23:59:59.000Z", "firstSeen": "2024-07-01T00:00:00.000Z"}, "links": {"Actors, Tools & TTPs": [{"id": "mitre:T1027", "name": "T1027", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1059.001", "name": "T1059.001", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1059.003", "name": "T1059.003", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1070.004", "name": "T1070.004", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1078", "name": "T1078", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1082", "name": "T1082", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1102", "name": "T1102", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1133", "name": "T1133", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1189", "name": "T1189", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1190", "name": "T1190", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1480.001", "name": "T1480.001", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1485", "name": "T1485", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1486", "name": "T1486", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1489", "name": "T1489", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1490", "name": "T1490", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1491.001", "name": "T1491.001", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1547", "name": "T1547", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1566", "name": "T1566", "type": "MitreAttackIdentifier"}, {"id": "mitre:T1567", "name": "T1567", "type": "MitreAttackIdentifier"}, {"id": "mitre:TA0002", "name": "TA0002", "type": "MitreAttackIdentifier"}, {"id": "mitre:TA0004", "name": "TA0004", "type": "MitreAttackIdentifier"}, {"id": "fRjfoI", "name": "Drive-by compromise", "type": "AttackVector"}, {"id": "0eyAM", "name": "Phishing", "type": "AttackVector"}, {"id": "l-ZWx4", "name": "Lockbit 3.0", "type": "Malware"}]}}]}]
```



#### Fetch Detection Rule
Fetch a detection rule based on its ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Rule ID|Detection rule ID to look up.|True|String|None|



##### JSON Results
```json
{"id": "doc:aaaaa", "type": "yara", "title": "Detection Rule Title", "description": "Detection Rule Description", "created": "2022-09-27T15:27:18.379000Z", "updated": "2022-09-27T15:29:36.873000Z", "rules": [{"entities": [{"id": "D0Ak-s", "name": "Ransomware", "type": "MalwareCategory"}], "content": "Rule Content", "file_name": "rule.yar"}]}
```



#### Enrich Host
Query Recorded Future to get intelligence about the Host.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Risk Score Threshold|Represents the minimum malicious risk score for a Host to be marked malicious. Has a range of 0-99. Below is the band levels:  Very Malicious: 90-99  Malicious: 65-89  Suspicious: 25-64  Unusual: 5-24  No Malicious content: 0|True|String|25|
|Include Links|If enabled, action will get information about links.|False|Boolean|false|
|Enable Collective Insights|If enabled, contribute detections back to Recorded Future.|False|Boolean|true|



##### JSON Results
```json
[{"Entity": "ntrshvquunyzxevkucs.com", "EntityResult": [{"entity": {"id": "idn:ntrshvquunyzxevkucs.com", "name": "ntrshvquunyzxevkucs.com", "type": "InternetDomainName"}, "intelCard": "https://app.recordedfuture.com/live/sc/entity/idn%3Antrshvquunyzxevkucs.com", "risk": {"criticalityLabel": "Very Malicious", "riskString": "6/52", "rules": 6, "criticality": 4, "riskSummary": "6 of 52 Risk Rules currently observed.", "score": 94, "evidenceDetails": [{"mitigationString": "", "evidenceString": "10 sightings on 2 sources: External Sensor Data Analysis, Bitdefender. ntrshvquunyzxevkucs.com is observed to be a malware site domain that navigates to malicious content including executables, drive-by infection sites, malicious scripts, viruses, trojans, or code.", "rule": "Historically Detected Malware Operation", "criticality": 1, "timestamp": "2022-01-21T00:00:00.000Z", "criticalityLabel": "Unusual"}, {"mitigationString": "", "evidenceString": "1 sighting on 1 source: @DGAFeedAlerts. Most recent tweet: New dircrypt Dom: ntrshvquunyzxevkucs[.]com IP: 80[.]92[.]65[.]188 NS: https://t.co/F8xbRMAf2C https://t.co/JxUb8f0Cir. Most recent link (Oct 21, 2021): https://twitter.com/DGAFeedAlerts/statuses/1451293292587593729", "rule": "Historically Reported as a Defanged DNS Name", "criticality": 1, "timestamp": "2021-10-21T21:04:19.000Z", "criticalityLabel": "Unusual"}, {"mitigationString": "", "evidenceString": "Previous sightings on 2 sources: Bambenek Consulting C&C Blocklist, Recently Viewed Integrations Indicators. Observed between Mar 5, 2023, and Mar 8, 2023.", "rule": "Historically Reported in Threat List", "criticality": 1, "timestamp": "2024-07-25T05:37:09.188Z", "criticalityLabel": "Unusual"}, {"mitigationString": "", "evidenceString": "1 sighting on 1 source: Bitdefender. Detected malicious behavior from an endpoint agent via global telemetry. Last observed on Jan 21, 2022.", "rule": "Historically Suspected Malware Operation", "criticality": 1, "timestamp": "2022-01-21T00:00:00.000Z", "criticalityLabel": "Unusual"}, {"mitigationString": "", "evidenceString": "1 sighting on 1 source: External Sensor Data Analysis. ntrshvquunyzxevkucs.com is observed to be a malware site domain that navigates to malicious content including executables, drive-by infection sites, malicious scripts, viruses, trojans, or code.", "rule": "Recently Detected Malware Operation", "criticality": 3, "timestamp": "2024-07-18T05:26:23.354Z", "criticalityLabel": "Malicious"}, {"mitigationString": "", "evidenceString": "1 sighting on 1 source: Bambenek Consulting C&C Blocklist.", "rule": "Recent C&C DNS Name", "criticality": 4, "timestamp": "2024-07-25T05:37:09.159Z", "criticalityLabel": "Very Malicious"}]}, "timestamps": {"lastSeen": "2024-07-17T19:47:20.526Z", "firstSeen": "2019-04-02T18:30:05.054Z"}, "links": {}}]}]
```



#### Get Playbook Alert Details
Fetch information about specific Playbook Alert and return results to the case. Use action to get more information available regarding Recorded Future PlaybookAlerts - Updated DNS Records, new vulnerability stages, etc...
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Playbook Alert ID|Specify the ID of the playbook alert for which you would like to fetch details|True|String||
|Category|The Category of the Playbook Alert. Possible values are domain_abuse, cyber_vulnerability, code_repo_leakage, third_party_risk, identity_novel_exposures, and geopolitics_facility|True|String||



##### JSON Results
```json
{"playbook_alert_id": "task:ba62d37e-9a52-411d-af56-0aa37a54aea5", "panel_log_v2": [], "panel_status": {"status": "New", "priority": "High", "created": "2026-01-21T20:05:53.223000Z", "updated": "2026-01-21T20:05:53.223000Z", "case_rule_id": "report:s8LnBp", "case_rule_label": "Novel Identity Exposure", "owner_organisation_details": {"organisations": [{"organisation_id": "str", "organisation_name": "str"}], "enterprise_id": "str", "enterprise_name": "str"}, "entity_id": "email:str", "entity_name": "str", "actions_taken": [], "targets": [{"name": "str"}, {"name": "str"}]}, "panel_evidence_summary": {"assessments": [{"name": "Technology", "criticality": "High"}, {"name": "Malware", "criticality": "Moderate"}], "subject": "str", "exposed_secret": {"type": "clear", "effectively_clear": true, "hashes": [{"algorithm": "SHA1", "hash": "ebaa984bac5709361a949956a1d0f5217e31da44"}, {"algorithm": "SHA256", "hash": "08afacae72eab420b05aaac38e553472136752c55ebd13ba27e72524ae242df5"}, {"algorithm": "NTLM", "hash": "bf702a9e599de07290c9097851b184b3"}, {"algorithm": "MD5", "hash": "ddc8c94843c5bbec9531b22f5d80242f"}], "details": {"properties": ["Letter", "Number", "UpperCase", "LowerCase", "AtLeast8Characters"], "clear_text_hint": "Al"}}, "dump": {"name": "str", "description": "str"}, "authorization_url": "str", "compromised_host": {"exfiltration_date": "2026-01-21T13:54:21Z", "os": "Windows 11 Pro", "os_username": "str", "malware_file": "str", "timezone": "UTC+05:00", "computer_name": "WORKSTATION"}, "malware_family": {"id": "YuDlEm", "name": "Vidar"}, "infrastructure": {"ip": "str"}, "technologies": [{"name": "Simple Mail Transfer Protocol", "id": "JSLFIT"}, {"name": "Outlook Web Access", "id": "hc7D", "category": "JSLFIT"}]}}
```



#### Lookup IP Credentials
Identity - Lookup credentials associated with a specified IP address or an IP range.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|IP|A subject IP address.|False|String|None|
|Filter on Target Entities|If the action should filter the search on the Target Entities.|False|Boolean|None|
|Range GTE|An IP address lower bound included.|False|String|None|
|Range GT|An IP address lower bound excluded.|False|String|None|
|Range LTE|An IP address upper bound included.|False|String|None|
|Range LT|An IP address upper bound excluded.|False|String|None|
|First Downloaded GTE|First date when these credentials were received and indexed by Recorded Future.|False|String|None|
|Latest Downloaded GTE|Latest date when these credentials were received and indexed by Recorded Future.|False|String|None|
|Exfiltration Date GTE|Date when the infostealer malware exfiltrated data from the victim device.|False|String|None|
|Properties|Password properties.|False|String|None|
|Breach Name|The name of a breach.|False|String|None|
|Breach Date|The date of a breach.|False|String|None|
|Dump Name|The name of a database dump.|False|String|None|
|Dump Date|The date of a database dump.|False|String|None|
|Username Properties|Username properties. Only valid value is 'Email'.|False|String|None|
|Authorization Technologies|Authorization technologies to filter by.|False|String|None|
|Authorization Protocols|Authorization protocols to filter by.|False|String|None|
|Malware Families|Known infostealer malware families.|False|String|None|
|Organization ID|An organization ID if utilizing a multi-org setup.|False|String|None|
|Max Results|The maximum number of credential records returned.|False|String|None|



##### JSON Results
```json
[{"identity": {"subjects": ["j.doe@example-corp.com"]}, "count": 0, "credentials": [{"subject": "j.doe@example-corp.com", "authorization_service": {"url": "https://signin.example-corp.com/login", "domain": "example-corp.com", "fqdn": "signin.example-corp.com", "protocols": ["HTTPS"], "technology": [{"id": "tech-wordpress", "name": "WordPress", "category": "CMS"}]}, "authorization_services": [{"url": "https://signin.example-corp.com/login", "domain": "example-corp.com", "fqdn": "signin.example-corp.com", "protocols": ["HTTPS"], "technology": [{"id": "tech-wordpress", "name": "WordPress", "category": "CMS"}]}], "exposed_secret": {"type": "Password", "effectively_clear": true, "hashes": [{"algorithm": "SHA1", "hash": "5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8"}], "details": {"clear_text_value": "password123", "clear_text_hint": "p***3", "properties": ["Letter"]}}, "compromise": {"exfiltration_date": "2025-01-10T18:00:00Z"}, "cookies": [{"dns": ".example.com", "name": "session_id", "http": true, "expiration": "2025-08-25T09:57:39Z", "secure": true, "value": "3a2d5f8b-9e4c-4a1d-b8f9-c6e7d8f9a0b1"}], "malware_family": {"id": "mal-vidar", "name": "Vidar Stealer"}, "dumps": [{"name": "Antiscam Log 2024-07-22", "type": "Stealer Log", "source": "dump-antiscam-2024-07-22-045", "description": "Log data from Antiscam malware campaign.", "infrastructure": {"ip": "203.0.113.55"}, "compromise": {"os": "Windows 11", "os_username": "victim_user", "malware_file": "C:\\Windows\\Temp\\update.exe", "timezone": "(UTC+02:00) Helsinki, Kyiv, Riga, Sofia, Tallinn, Vilnius", "computer_name": "DESKTOP-A1B2C3D", "uac": "UAC-Limited", "antivirus": ["Avast"], "exfiltration_date": "2025-07-21T12:00:00Z"}, "location": {"country": {"name": "UNITED_STATES", "displayName": "United States", "countryCode": "USA", "alpha2Code": "US", "alpha3Code": "USA"}, "city": "New York", "address": "123 Main Street, Apt 4B", "address1": "123 Main Street", "address2": "Apt 4B", "state": "NY", "postal_code": "10001", "zip": "10001"}, "breaches": [{"name": "SocialNet Breach", "domain": "socialnet.com", "type": "Database Breach", "breached": "2023-11-01T00:00:00Z", "start": "2023-10-15T00:00:00Z", "stop": "2023-10-20T00:00:00Z", "precision": "YEAR", "description": "User database with emails and hashed passwords was compromised.", "site_description": "Social networking platform."}], "downloaded": "2025-07-22T08:00:00Z"}], "first_downloaded": "2025-07-25T09:30:00Z", "latest_downloaded": "2025-07-25T09:30:00Z", "source_type": "MalwareLogs"}]}]
```



#### Fetch List
Get a list by its ID. Use this method to retrieve list info.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List ID|The ID for the list.|True|String|None|



##### JSON Results
```json
{"id_": "report:mfLASl", "name": "List Name", "type_": "tech_stack", "created": "2022-05-06T08:19:31.407000Z", "updated": "2025-11-07T09:37:38.453000Z", "owner_id": "uhash:69sKLfTGsS", "owner_name": "Professional Services Development", "organisation_id": "uhash:5zQaSyRpA1", "organisation_name": "Professional Services Development", "owner_organisation_details": {"owner_id": null, "owner_name": null, "organisations": [{"organisation_id": "uhash:69sKLfTGsS", "organisation_name": "Professional Services Development"}], "enterprise_id": "uhash:5zQaSyRpA1", "enterprise_name": "Professional Services Development"}}
```



#### Enrich IOC
Query Recorded Future to get intelligence about the IOC
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Risk Score Threshold|Represents the minimum malicious risk score for each entity to be marked is suspicious.|True|String|25|
|Include Links|If enabled, action will get information about links.|False|Boolean|false|
|Enable Collective Insights|If enabled, contribute detections back to Recorded Future.|False|Boolean|true|



##### JSON Results
```json
[{"Entity": "ntrshvquunyzxevkucs.com", "EntityResult": [{"entity": {"id": "idn:ntrshvquunyzxevkucs.com", "name": "ntrshvquunyzxevkucs.com", "type": "InternetDomainName"}, "intelCard": "https://app.recordedfuture.com/live/sc/entity/idn%3Antrshvquunyzxevkucs.com", "risk": {"criticalityLabel": "Very Malicious", "riskString": "6/52", "rules": 6, "criticality": 4, "riskSummary": "6 of 52 Risk Rules currently observed.", "score": 94, "evidenceDetails": [{"mitigationString": "", "evidenceString": "10 sightings on 2 sources: External Sensor Data Analysis, Bitdefender. ntrshvquunyzxevkucs.com is observed to be a malware site domain that navigates to malicious content including executables, drive-by infection sites, malicious scripts, viruses, trojans, or code.", "rule": "Historically Detected Malware Operation", "criticality": 1, "timestamp": "2022-01-21T00:00:00.000Z", "criticalityLabel": "Unusual"}, {"mitigationString": "", "evidenceString": "1 sighting on 1 source: @DGAFeedAlerts. Most recent tweet: New dircrypt Dom: ntrshvquunyzxevkucs[.]com IP: 80[.]92[.]65[.]188 NS: https://t.co/F8xbRMAf2C https://t.co/JxUb8f0Cir. Most recent link (Oct 21, 2021): https://twitter.com/DGAFeedAlerts/statuses/1451293292587593729", "rule": "Historically Reported as a Defanged DNS Name", "criticality": 1, "timestamp": "2021-10-21T21:04:19.000Z", "criticalityLabel": "Unusual"}, {"mitigationString": "", "evidenceString": "Previous sightings on 2 sources: Bambenek Consulting C&C Blocklist, Recently Viewed Integrations Indicators. Observed between Mar 5, 2023, and Mar 8, 2023.", "rule": "Historically Reported in Threat List", "criticality": 1, "timestamp": "2024-07-25T05:37:09.188Z", "criticalityLabel": "Unusual"}, {"mitigationString": "", "evidenceString": "1 sighting on 1 source: Bitdefender. Detected malicious behavior from an endpoint agent via global telemetry. Last observed on Jan 21, 2022.", "rule": "Historically Suspected Malware Operation", "criticality": 1, "timestamp": "2022-01-21T00:00:00.000Z", "criticalityLabel": "Unusual"}, {"mitigationString": "", "evidenceString": "1 sighting on 1 source: External Sensor Data Analysis. ntrshvquunyzxevkucs.com is observed to be a malware site domain that navigates to malicious content including executables, drive-by infection sites, malicious scripts, viruses, trojans, or code.", "rule": "Recently Detected Malware Operation", "criticality": 3, "timestamp": "2024-07-18T05:26:23.354Z", "criticalityLabel": "Malicious"}, {"mitigationString": "", "evidenceString": "1 sighting on 1 source: Bambenek Consulting C&C Blocklist.", "rule": "Recent C&C DNS Name", "criticality": 4, "timestamp": "2024-07-25T05:37:09.159Z", "criticalityLabel": "Very Malicious"}]}, "timestamps": {"lastSeen": "2024-07-17T19:47:20.526Z", "firstSeen": "2019-04-02T18:30:05.054Z"}, "links": {}}]}]
```



#### Enrich IOCs Bulk
Query Recorded Future to get intelligence about IOCs in bulk using the SOAR API
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Enable Collective Insights|If enabled, contribute detections back to Recorded Future.|False|Boolean|true|



##### JSON Results
```json
[{"Entity": "CVE-2021-44228", "EntityResult": [{"risk": {"score": 99, "level": 5, "context": {"malware": {"score": 90, "rule": {"count": 1, "maxCount": 1}}, "public": {"summary": [{"level": 5, "count": 1}, {"level": 1, "count": 10}, {"level": 2, "count": 4}, {"level": 4, "count": 1}], "score": 99, "mostCriticalRule": "Exploited in the Wild by Recently Active Malware", "rule": {"maxCount": 23}}}, "rule": {"count": 17, "mostCritical": "Exploited in the Wild by Recently Active Malware", "maxCount": 25, "evidence": {"relatedNote": {"count": 1, "timestamp": "2025-11-14T00:00:00.000Z", "description": "70 sightings on 1 source: <e id=source:VKz42X>Insikt Group</e>. 70 reports including Symantec Links Campaign Targeting US Policy Organization to Multiple China-Linked Threat Groups; Recorded Future Attributes to TAG-159. Most recent link (Nov 14, 2025): https://app.recordedfuture.com/portal/analyst-note/doc:BAgMIYu", "rule": "Historically Referenced by Insikt Group", "sightings": 70, "mitigation": "", "level": 1}, "ransomwareExploit": {"count": 1, "timestamp": "2024-09-27T00:00:00.000Z", "description": "4 sightings on 1 source: <e id=source:VKz42X>Insikt Group</e>. Vulnerability known to be exploited by these ransomware groups and/or tools: <e id=g0eFmJ>Conti Gang</e>, <e id=luzJUr>ALPHV Ransomware Group</e>, <e id=eTMnra>CL0P Ransomware Group</e>. Last observed Sep 27, 2024.", "rule": "Vulnerability Exploited by Ransomware", "sightings": 4, "mitigation": "", "level": 1}, "linkedToCyberExploit": {"count": 4036, "timestamp": "2025-12-31T04:31:20.000Z", "description": "21,514 sightings on 4035 sources including: <e id=source:j0U6oV>LogRhythm</e>, <e id=source:cJKBXh>Habr | \u0412\u0441\u0435 \u043f\u0443\u0431\u043b\u0438\u043a\u0430\u0446\u0438\u0438</e>, <e id=source:cJKKK3>Help Net Security | News</e>, <e id=idn:prohoster.info>prohoster.info</e>, <e id=source:mDB208>Valneva | Financial Reports</e>. Most recent tweet: <e id=TIREu7>@2sush</e> <e id=bgcc8>Standard</e> !!! For reference The <e id=J1PKS5>Log4j</e> vulnerability (<i id=HFCcAAAsvPr><e id=kvXvR5>Log4Shell</e>, <e id=kvXvR5>CVE-2021-44228</e>) became public in December 2021, but it existed in code since <t>2013</t> and was actively exploited</i> from at least December 1, 2021, before its official report. Most recent link (Dec 31, 2025): https://twitter.com/_jaydeepkarale/statuses/2006221609401749968", "rule": "Linked to Historical Cyber Exploit", "sightings": 21514, "mitigation": "", "level": 1}, "recentScannerUptake": {"count": 2, "timestamp": "2026-01-10T18:07:28.603Z", "description": "49 sightings on 2 sources: <e id=source:Y7TWfI>Telegram - Other Channels</e>, <e id=source:MIKjae>GitHub</e>. Most recent link (Jan 10, 2026): https://github.com/sanvisharma850/institute-verify/commit/f9a956c9e9be53fd6fdb74733e5e3ddff1a560fa", "rule": "Recently Linked to Penetration Testing Tools", "sightings": 49, "mitigation": "", "level": 2}, "linkedToRAT": {"count": 306, "timestamp": "2025-11-16T20:43:32.000Z", "description": "1666 sightings on 306 sources including: <e id=source:cJKeNH>CSOonline.com | Security News</e>, <e id=source:m4wN3b>UFO Labs Forum</e>, <e id=source:POs2tz>FreeBufCOM</e>, <e id=source:KZFCph>XSS (ex DamageLab) Forum</e>, <e id=source:xbfXTc>Youm7 | Latest Updates</e>. 81 related malware families including <e id=JHqDDD>Zeroaccess</e>, <e id=QCqLd4>HyperBro</e>, <e id=KLhRL_>njRAT</e>, <e id=RAQbTW>Orcus RAT</e>, <e id=svYiVc>ValleyRAT</e>. Most recent tweet: Ghostemperor Webworm Threats: <e id=kvXvR5>Log4shell</e>_vuln, <e id=CJx-bY>Dll</e>_sideloading_technique, Deed_rat, <e id=jc5TL_>Dcsync</e>_technique, Lolbin_technique, Credential_harvesting_technique, Credential_dumping_technique, Victims: Nonprofit policy institution Industry: Government, Critical_infrastructure <e id=CO_n5>Geo</e>: <e id=B_FNa>China</e>, Chinese CVEs: <e id=lx10TG>CVE-2022-26134</e> \\[[Vulners](<e id=url:https://vulners.com/cve/CVE-2022-26134>https://t.co/w83coCbpPb</e>)] - <e id=JbX7Bo>CVSS</e> V3.1: *Unknown*, - Vulners: Exploitation: Unknown <e id=kvXvR5>CVE-2021-44228</e> \\[[Vulners](<e id=url:https://vulners.com/cve/CVE-2021-44228>https://t.co/iWpK5920T2</e>)] - <e id=JbX7Bo>CVSS</e> V3.1: *Unknown*, - Vulners: Exploitation: Unknown <e id=UybOj5>CVE-2017-17562</e> \\[[Vulners](<e id=url:https://vulners.com/cve/CVE-2017-17562>https://t.co/LNpUg5JhTE</e>)] - <e id=JbX7Bo>CVSS</e> V3.1: *Unknown*, - Vulners: Exploitation: Unknown <e id=UAhYzz>CVE-2017-9805</e> \\[[Vulners](<e id=url:https://vulners.com/cve/CVE-2017-9805>https://t.co/dMIgyL0fKs</e>)] - <e id=JbX7Bo>CVSS</e> V3.1: *Unknown*, - Vulners: Exploitation: Unknown TTPs: \u2694\ufe0fTactics: 10 \ufe0fTechnics: 19 IOCs: - File: 5 - IP: 1 - Hash: 10 - Url: 1 Software: <e id=Cn2qG0>Confluence</e>, <e id=bfC7F>Apache</e> <e id=CTGYto>Struts</e>, <e id=kTmAbX>Active Directory</e> <e id=VtA2mk>Algorithms</e>: md5, sha1, sha256 Programming Languages: <e id=Sw-YC9>powershell</e> <e id=K1t1nS>#threatreport</e>: <t>In April 2025</t>, the advanced persistent. Most recent link (Nov 16, 2025): https://twitter.com/rst_cloud/statuses/1990158819054235648", "rule": "Historically Linked to Remote Access Trojan", "sightings": 1666, "mitigation": "", "level": 1}, "linkedToRansomware": {"count": 771, "timestamp": "2025-12-24T23:58:38.000Z", "description": "3874 sightings on 771 sources including: <e id=source:QhLYm5>Reddit InfoSec Comments</e>, <e id=source:POs2tz>FreeBufCOM</e>, <e id=idn:newsworldpress.com>newsworldpress.com</e>, <e id=source:j0U6oV>LogRhythm</e>, <e id=idn:sdxcentral.com>sdxcentral.com</e>. 153 related malware families including <e id=jQYVGc>BlackMatter Ransomware</e>, <e id=h-Xzzl>Nitro Ransomware</e>, <e id=SL0r9i>Luna</e>, <e id=RHoDKR>Anatel</e>, <e id=dcHaT8>WannaRen</e>. Most recent tweet: 'Twas Patch Tuesday Eve and all through the <e id=a4crhL>SOC</e>, hushed Not <e id=I2FSXY>an analyst</e> was sleeping through any <e id=K60k77>@SlackHQ</e> <e id=B_r5l3>knock</e>-brush The <e id=KeivNd>#hackers</e> were snuggled in their soft gaming chairs <e id=JQPdY1>Reading</e> tweets from <e id=K5nCn5>@SwiftOnSecurity</e> with little fanfare When all of the sudden arose such an alert That <e id=I2FSXY>an analyst</e> spilled eggnog on their <e id=M2xmWB>@DEFCON</e> t-shirt! Was it <e id=Stvvb_>Lazarus</e> or <e id=EG-pEP>Pandas</e> or a <e id=L37nw->Fancy Bear</e>? Maybe Mimikatz or <e id=ThrypD>notPetya</e> or some <e id=J0Nl-p>ransomware</e>? As the analysts worked, the <e id=quwUm>snow</e> fell on the room Blanketing the whole datacenter while they talked on a <e id=OwAAif>@Zoom</e> The <e id=a4crhL>SOC</e> sipped their hot drinks, keyboards tapped and mice clicked <e id=BGBjTM>Critical infrastructure</e> being attacked via <e id=kvXvR5>log4shell</e> for kicks The patter of <e id=CIQ28R>reindeer</e> footsteps on the roof Triggered an alarm (because of course the building is burglar-proof) As INTERPOL arrested <e id=gh6sH>Santa</e>, he exclaimed with dismay, \"It's <t>Winter</t> in <e id=PABn9r>#lnfosec</e>; I'm <e id=dYau8>just</e> trying to deliver an 0-day!\" Most recent link (Dec 24, 2025): https://twitter.com/aprilwright/statuses/2003978657241423882", "rule": "Historically Linked to Ransomware", "sightings": 3874, "mitigation": "", "level": 1}, "linkedToExploitKit": {"count": 8, "timestamp": "2025-11-26T18:11:04.952Z", "description": "18 sightings on 8 sources including: <e id=idn:substack.com>substack.com</e>, <e id=idn:secoperations.pt>secoperations.pt</e>, <e id=source:k4B6xb>The Cyber Beat</e>, <e id=source:lthm-2>Codebook</e>, <e id=source:jbUons>Malpedia Library</e>. 19 related malware families including <e id=Ze0xsz>Spelevo</e>, <e id=NGPNSi>Kaixin EK</e>, <e id=OXqBbF>Sundown Exploit Kit</e>, <e id=SulhVx>Nebula Exploit Kit</e>, <e id=KGL2mk>CK Exploit Kit (Net Boom)</e>. Most recent link (Nov 26, 2025): https://github.com/CyberX94/cyber-forensics-glossary/commit/11ad003f042f2ce6a243bf4e874dcd936c672017", "rule": "Historically Linked to Exploit Kit", "sightings": 18, "mitigation": "", "level": 1}, "analystNote": {"count": 1, "timestamp": "2025-11-14T00:00:00.000Z", "description": "34 sightings on 1 source: <e id=source:VKz42X>Insikt Group</e>. 34 reports including Symantec Links Campaign Targeting US Policy Organization to Multiple China-Linked Threat Groups; Recorded Future Attributes to TAG-159. Most recent link (Nov 14, 2025): https://app.recordedfuture.com/portal/analyst-note/doc:BAgMIYu", "rule": "Historically Reported by Insikt Group", "sightings": 34, "mitigation": "", "level": 1}, "nistCritical": {"count": 1, "timestamp": "2025-10-27T18:40:38.735Z", "description": "1 sighting on 1 source: <e id=source:cJPLvf>Recorded Future Vulnerability Analysis via National Vulnerability Database</e>. CVSS v3.1 Score (10.0) calculated using <e id=source:KsicdL>NIST</e> reported CVSS Base Score (10.0) and Recorded Future Temporal Metrics. Base vector string: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:C/C:H/I:H/A:H.  Temporal vector string: E:H/RL:X/RC:C. Most recent link (Oct 27, 2025): https://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2021-44228", "rule": "NIST Severity: Critical", "sightings": 1, "mitigation": "", "level": 4}, "linkedToIntrusionMethod": {"count": 2790, "timestamp": "2025-12-15T14:36:14.000Z", "description": "15,501 sightings on 2790 sources including: <e id=source:sl9FxO>Elastic Security Labs</e>, <e id=source:Jv_xrR>PasteBin</e>, <e id=source:QhLYm5>Reddit InfoSec Comments</e>, <e id=idn:cybernoz.com>cybernoz.com</e>, <e id=source:B-i>LeMondeInformatique</e>. 585 related malware families including <e id=dXkwxG>Kinsing</e>, <e id=qfQAi5>DcRat (qwqdanchun version)</e>, <e id=lRALi_>CharmPower</e>, <e id=mQ6Ge5>Enemybot</e>, <e id=ONtsS0>ICS Malware</e>. Most recent tweet: New <e id=JXRyOT>React</e> vulns leak secrets, invite <e id=0f-N9>DoS</e> attacks React Server Components has three new CVEs on top of the already exploited React2Shell bug that allow attackers to hang servers via crafted <e id=JRV6gr>HTTP</e> requests and, in some <e id=hD9iMp>cases</e>, expose hardcoded secrets. These affect multiple react-server-dom-* packages in versions 19.0.0-19.2.2, including prior \"patched\" releases, so organizations are urged to update again and treat the situation with <e id=kvXvR5>Log4Shell</e>-level seriousness. <e id=url:https://www.theregister.com/2025/12/12/new_react_secretleak_bugs/>https://t.co/jHUgPf57wd</e>. Most recent link (Dec 15, 2025): https://twitter.com/johndjohnson/statuses/2000575634242998495", "rule": "Historically Linked to Malware", "sightings": 15501, "mitigation": "", "level": 1}, "linkedToRecentIntrusionMethod": {"count": 5, "timestamp": "2026-01-15T16:30:20.026Z", "description": "111 sightings on 5 sources: <e id=source:J7cfgB>George Washington University - Media</e>, <e id=source:roLoLW>BreachForums 2</e>, <e id=source:letQZt>Image OCR</e>, <e id=source:tvS3t3>DarkForums</e>, <e id=source:MIKjae>GitHub</e>. 43 related malware families including <e id=dXkwxG>Kinsing</e>, <e id=Koaobw>WebShell</e>, <e id=SHSGrF>PortReuse</e>, <e id=mHx4mB>Fire Chili rootkit</e>, <e id=OiuwL9>Burp Collaborator</e>. Most recent link (Jan 15, 2026): https://github.com/ssl-vpc/vault/commit/d6ce77ec221061f4c5ce7cfe53e14fbc6b1ac8e9", "rule": "Recently Linked to Malware", "sightings": 111, "mitigation": "", "level": 2}, "recentPocUnverified": {"count": 3, "timestamp": "2025-12-24T03:28:03.000Z", "description": "4 sightings on 3 sources: <e id=source:dAj1OE>Medium</e>, <e id=source:PXFNki>google.com</e>, <e id=source:QuRAQm>Tenable</e>. Most recent link (Dec 24, 2025): https://medium.com/s2wblog/detailed-analysis-of-recent-trends-in-known-exploited-vulnerabilities-c81678a47f39?source=rss----30a8766b5c42---4", "rule": "Recent Unverified Proof of Concept Available", "sightings": 4, "mitigation": "", "level": 2}, "recentMalwareActivity": {"count": 1, "timestamp": "2026-01-14T00:00:00.000Z", "description": "163 sightings on 1 source: <e id=source:6W0Gqe>Recorded Future Vulnerability Analysis</e>. Activity seen on 28 out of the last 28 days with 1219 all-time daily sightings. Last observed on Jan 14, 2026. Sample hash: <e id=hash:0d5aae9ca89f7329590591199f382d9c12248b3cb02fa7d73167fb87c5e2646a>0d5aae9ca89f7329590591199f382d9c12248b3cb02fa7d73167fb87c5e2646a</e>.", "rule": "Exploited in the Wild by Recently Active Malware", "sightings": 163, "mitigation": "", "level": 5}, "linkedToRecentRAT": {"count": 3, "timestamp": "2026-01-09T21:06:00.000Z", "description": "4 sightings on 3 sources: <e id=source:Y7TWfI>Telegram - Other Channels</e>, <e id=source:MIKjae>GitHub</e>, <e id=Qse9Q7>@rst_cloud</e>. 3 related malware families: <e id=Yzaz0L>AsyncRAT</e>, <e id=JG4Q05>Gh0st RAT</e>, <e id=LnK3Q6>Cobalt Strike Beacon</e>. Most recent tweet: active threat defense | <t>08-01-2026</t> Source: <e id=url:https://aws.amazon.com/blogs/security/real-time-malware-defense-leveraging-aws-network-firewall-active-threat-defense/>https://t.co/P14pXz4VLa</e> ... \\[[Vulners](<e id=url:https://vulners.com/cve/CVE-2021-26084>https://t.co/On9IMfb1L7</e>)] - <e id=JbX7Bo>CVSS</e> V3.1: *Unknown*, - Vulners: Exploitation: Unknown <e id=uAVNtx>CVE-2024-21893</e> \\[[Vulners](<e id=url:https://vulners.com/cve/CVE-2024-21893>https://t.co/9Fidk1RjSK</e>)] - <e id=JbX7Bo>CVSS</e> V3.1: *Unknown*, - Vulners: Exploitation: Unknown <e id=2h7lbT>CVE-2025-24016</e> \\[[Vulners](<e id=url:https://vulners.com/cve/CVE-2025-24016>https://t.co/NNy4WSZmIO</e>)] - <e id=JbX7Bo>CVSS</e> V3.1: *Unknown*, - Vulners: Exploitation: Unknown <e id=kAIvOZ>CVE-2021-41773</e> \\[[Vulners](<e id=url:https://vulners.com/cve/CVE-2021-41773>https://t.co/g8tpLSuNeI</e>)] - <e id=JbX7Bo>CVSS</e> V3.1: *Unknown*, - Vulners: Exploitation: Unknown <e id=kvXvR5>CVE-2021-44228</e> \\[[Vulners](<e id=url:https://vulners.com/cve/CVE-2021-44228>https://t.co/iWpK5920T2</e>)] - <e id=JbX7Bo>CVSS</e> V3.1: *Unknown*, - Vulners: Exploitation: Unknown <e id=ikR-mN>CVE-2021-33690</e> \\[[Vulners](<e id=url:https://vulners.com/cve/CVE-2021-33690>https://t.co/tvasuFgaLM</e>)] - <e id=JbX7Bo>CVSS</e> V3.1: *Unknown*, - Vulners: Exploitation: Unknown <e id=5QfVMy>CVE-2025-34028</e> \\[[Vulners](<e id=url:https://vulners.com/cve/CVE-2025-34028>https://t.co/n5P9ClmgsW</e>)] - <e id=JbX7Bo>CVSS</e> V3.1: *Unknown*, - Vulners: Exploitation: Unknown <e id=8B3jwZ>CVE-2025-20337</e> \\[[Vulners](<e id=url:https://vulners.com/cve/CVE-2025-20337>https://t.co/x6uYJawalG</e>)] - <e id=JbX7Bo>CVSS</e> V3.1: *Unknown*, - Vulners: Exploitation: Unknown <e id=6VoCY0>CVE-2025-48703</e> \\[[Vulners](<e id=url:https://vulners.com/cve/CVE-2025-48703>https://t.co/qwUegzk8w9</e>)] - <e id=JbX7Bo>CVSS</e> V3.1: *Unknown*, - Vulners: Exploitation: Unknown <e id=z_Y_HK>CVE-2024-51567</e>. Most recent link (Jan 9, 2026): https://twitter.com/rst_cloud/statuses/2009733416061653112", "rule": "Recently Linked to Remote Access Trojan", "sightings": 4, "mitigation": "", "level": 2}, "linkedToRecentCyberExploit": {"count": 9, "timestamp": "2026-01-02T08:46:27.000Z", "description": "19 sightings on 9 sources including: <e id=idn:thedailytechfeed.com>thedailytechfeed.com</e>, <e id=source:J7cfgB>George Washington University - Media</e>, <e id=source:wVsvXj>Habr.com | \u041f\u043e\u0441\u043b\u0435\u0434\u043d\u0438\u0435 \u041e\u0431\u043d\u043e\u0432\u043b\u0435\u043d\u0438\u044f</e>, <e id=idn:zyrosite.com>zyrosite.com</e>, <e id=source:jIlT9i>CN-SEC Chinese Network</e>. Most recent tweet: Vendors slapping \"AI <e id=C3hdq>Quantum</e> Blockchain Zero Trust\" on slides praying nobody asks about <e id=BDmJL2>basic</e> event correlation. Bonus points for \"<e id=B_nHi>AI</e>-powered <i id=HFCcgABUJ4Q>zero-day protection\" that <e id=CCzw8>still</e> can't detect <e id=kvXvR5>Log4Shell</e></i> in <t>2025</t>. But hey, the deck looks futuristic. <e id=url:https://twitter.com/CisoRaging77913/status/2007010587776356581/photo/1>https://t.co/WRd6UvNhaP</e>. Most recent link (Jan 2, 2026): https://twitter.com/CisoRaging77913/statuses/2007010587776356581", "rule": "Linked to Recent Cyber Exploit", "sightings": 19, "mitigation": "", "level": 1}, "pocUnverified": {"count": 13, "timestamp": "2024-06-15T18:00:23.000Z", "description": "50 sightings on 13 sources including: <e id=source:lcI4oe>Vulners | Feed</e>, <e id=source:J6UzbO>Bleeping Computer Forums</e>, <e id=source:KVP0jz>Fortinet</e>, <e id=source:KcN2Oa>Steve (GRC) Gibsons Blog</e>, <e id=idn:gitbook.io>gitbook.io</e>. Most recent tweet: <e id=url:https://github.com/kozmer/log4j-shell-poc>https://t.co/HerdwLfzqr</e> A <i id=HFAPAACPsMv>Proof-Of-Concept for the <e id=kvXvR5>CVE-2021-44228</e></i> vulnerability. Most recent link (Jun 15, 2024): https://twitter.com/ala_garbaa_pro/statuses/1802038460523438275", "rule": "Historical Unverified Proof of Concept Available", "sightings": 50, "mitigation": "", "level": 1}, "scannerUptake": {"count": 94, "timestamp": "2025-12-09T09:15:08.000Z", "description": "3115 sightings on 94 sources including: <e id=source:QhLYm5>Reddit InfoSec Comments</e>, <e id=source:Y7TWfI>Telegram - Other Channels</e>, <e id=source:cJKeNH>CSOonline.com | Security News</e>, <e id=source:POs2tz>FreeBufCOM</e>, <e id=source:SjX7Fc>Cyberscoop</e>. Most recent tweet: <e id=JFmVA9>Burp Suite</e>\u306eActiveScan++\u304c\u91cd\u5927\u306aReact2Shell\u8106\u5f31\u6027\u306e\u691c\u77e5\u306b\u5bfe\u5fdc\u3057\u3001\u30bc\u30ed\u30c7\u30a4\u653b\u6483\u3092\u65e9\u671f\u306b\u5bdf\u77e5\u3067\u304d\u308b\u3088\u3046\u306b\u306a\u3063\u305f\u3002 React\u30a2\u30d7\u30ea\u306e<e id=JQ3ldp>SSRF</e>\u9023\u9396\u3067RCE\u306b\u81f3\u308b\u6b20\u9665\u3092\u81ea\u52d5\u30b9\u30ad\u30e3\u30f3\u3067\u767a\u898b\u3067\u304d\u308b\u3088\u3046\u306b\u306a\u308a\u3001\u73fe\u5834\u306e\u9632\u5fa1\u529b\u304c\u5411\u4e0a\u3059\u308b\u3068\u671f\u5f85\u3055\u308c\u308b\u3002 \u4eca\u56de\u306e\u66f4\u65b0\u3067\u306f\u3001React\u30a2\u30d7\u30ea\u306b\u304a\u3051\u308b\u30b5\u30fc\u30d0\u5074\u3067\u306e\u30ea\u30af\u30a8\u30b9\u30c8\u60aa\u7528\u306b\u3088\u308a\u4efb\u610f\u30b3\u30de\u30f3\u30c9\u5b9f\u884c\u3078\u3064\u306a\u304c\u308b\u554f\u984c\u306b\u5bfe\u5fdc\u3057\u3001\u901a\u5e38\u306e\u30b9\u30ad\u30e3\u30f3\u904b\u7528\u306e\u307e\u307e\u3067\u5371\u967a\u306a\u6319\u52d5\u3092\u691c\u51fa\u53ef\u80fd\u3068\u306a\u3063\u305f\u3002 <e id=R53O1>ActiveScan++</e>\u306f\u6a19\u6e96\u306e<e id=RK67Cj>\u30a2\u30af\u30c6\u30a3\u30d6</e>\uff0f\u30d1\u30c3\u30b7\u30d6\u691c\u67fb\u3092\u62e1\u5f35\u3057\u3001\u30db\u30b9\u30c8\u30d8\u30c3\u30c0\u30fc\u64cd\u4f5c\u306b\u3088\u308b\u30d1\u30b9\u30ef\u30fc\u30c9\u30ea\u30bb\u30c3\u30c8\u6c5a\u67d3\u3001\u30ad\u30e3\u30c3\u30b7\u30e5\u6c5a\u67d3\u3001DNS\u30ea\u30d0\u30a4\u30f3\u30c7\u30a3\u30f3\u30b0\u306a\u3069\u3001\u4e00\u822c\u7684\u306a\u30b9\u30ad\u30e3\u30ca\u30fc\u304c\u898b\u9003\u3057\u3084\u3059\u3044\u5fae\u5999\u306a\u6319\u52d5\u3092\u4f4e\u8ca0\u8377\u3067\u6d17\u3044\u51fa\u3059\u3002 \u3055\u3089\u306b\u3001<e id=HFFT7l>Shellshock</e>\u3084<e id=kvXvR5>Log4Shell</e>\u306a\u3069\u8457\u540d\u306a\u8106\u5f31\u6027\u306b\u52a0\u3048\u3001React2Shell\u304c\u65b0\u305f\u306b\u5bfe\u8c61\u3068\u306a\u308a\u3001<e id=LQEhvp>Unicode</e>\u56de\u907f\u691c\u77e5\u3001\u30d5\u30a1\u30b8\u30f3\u30b0\u6642\u306e\u30d1\u30c3\u30b7\u30d6\u691c\u67fb\u81ea\u52d5\u767a\u706b\u3001HTTP\u57fa\u672c\u8a8d\u8a3c\u306e\u633f\u5165\u70b9\u8ffd\u52a0\u306a\u3069\u3001\u30c6\u30b9\u30bf\u30fc\u5411\u3051\u306e\u6a5f\u80fd\u304c\u5f37\u5316\u3055\u308c\u305f\u3002 \u5229\u7528\u306f\u5bb9\u6613\u3067\u3001\u901a\u5e38\u306e\u30a2\u30af\u30c6\u30a3\u30d6\u30b9\u30ad\u30e3\u30f3\u3092\u5b9f\u884c\u3059\u308b\u3060\u3051\u3067\u7d50\u679c\u304c\u91cd\u307f\u4ed8\u3051\u3055\u308c\u3066<e id=6Nim_K>\u30c0\u30c3\u30b7\u30e5\u30dc\u30fc\u30c9</e>\u306b\u8868\u793a\u3055\u308c\u308b\u3002 React\u5468\u8fba\u3067<e id=JQ3ldp>SSRF</e>\u60aa\u7528\u304c\u5897\u3048\u308b\u4e2d\u3001\u958b\u767a\u5074\u306b\u306f\u5165\u529b\u691c\u8a3c\u3068\u30ea\u30af\u30a8\u30b9\u30c8\u306e\u30db\u30ef\u30a4\u30c8\u30ea\u30b9\u30c8\u5316\u304c\u6c42\u3081\u3089\u308c\u308b\u3002 <e id=url:https://cybersecuritynews.com/burp-suite-react2shell-vulnerabilities/>https://t.co/iuwoONG2dR</e>\u3002 Most recent link (Dec 9, 2025): https://twitter.com/yousukezan/statuses/1998320497441034563", "rule": "Historically Linked to Penetration Testing Tools", "sightings": 3115, "mitigation": "", "level": 1}}, "summary": [{"level": 5, "count": 1}, {"level": 1, "count": 11}, {"level": 2, "count": 4}, {"level": 4, "count": 1}]}}, "entity": {"id": "kvXvR5", "name": "CVE-2021-44228", "type": "CyberVulnerability", "description": "Apache Log4j2 2.0-beta9 through 2.15.0 (excluding security releases 2.12.2, 2.12.3, and 2.3.1) JNDI features used in configuration, log messages, and parameters do not protect against attacker controlled LDAP and other JNDI related endpoints. An attacker who can control log messages or log message parameters can execute arbitrary code loaded from LDAP servers when message lookup substitution is enabled. From log4j 2.15.0, this behavior has been disabled by default. From version 2.16.0 (along with 2.12.2, 2.12.3, and 2.3.1), this functionality has been completely removed. Note that this vulnerability is specific to log4j-core and does not affect log4net, log4cxx, or other Apache Logging Services projects."}}]}]
```



#### Search Links
Search for technically validated relationships between threat intelligence entities in the Recorded Future Intelligence Cloud.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Entities|One or more Recorded Future entity IDs to look up links for.|False|String|None|
|Filter on Target Entities|If the action should filter the search on the Target Entities.|False|Boolean|None|
|Sections|Filter results to these link section IDs.|False|String|None|
|Entity Types|Restrict linked entities to these entity types (e.g. "type:IpAddress").|False|String|None|
|Sources|Limit to source type(s) - "technical", "insikt", or both if argument omitted.|False|String|None|
|Timeframe|Technical-link timeframe (e.g. "-30d", default "-30d", max "-90d").|False|String|None|
|Events|Restrict technical links to these event types (e.g. "type:MalwareAnalysis").|False|String|None|
|Connected Entities|Only return technical links that connect to these entities.|False|String|None|
|Search Scope|Result-volume scope - "small", "medium" (default), or "large".|False|List|medium|
|Max Entity Results|Max linked entities returned per entity type (>= 1 <= 1,000,000,000).|False|String|None|



##### JSON Results
```json
[{"entity": {"type": "type:Malware", "id": "JLHNoH", "name": "Cobalt Strike"}, "links": [{"type": "type:IpAddress", "id": "ip:8.8.8.8", "name": "8.8.8.8", "source": "technical", "section": "iU_ZsI", "attributes": [{"id": "risk_score", "value": 90}, {"id": "criticality", "value": "Malicious"}, {"id": "display_name", "value": "T1001 (Data Obfuscation)"}, {"id": "threat_actor", "value": true}]}], "error": {"message": "The entity was not found", "status_code": 404}}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Get Alert Details
Fetch information about specific Alert and return results to the case. Use action to get more information available regarding Recorded Future Alerts - Documents, Related Entities, Evidence, etc...
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify the ID of the alert for which you would like to fetch details|True|String||



##### JSON Results
```json
{"data": {"review": {"assignee": null, "noteAuthor": null, "note": null, "status": "no-action", "noteDate": null}, "entities": [{"entity": {"id": "idn:gmaxx.com.xxxsepehlxxx.com", "name": "gmaxx.com.xxxsepehlexxx.com", "type": "InternetDomainName"}, "risk": {"criticalityLabel": "Suspicious", "score": null, "documents": [{"references": [{"fragment": "A certificate for the domain gmail.com.sabsepehlelic.com has been registered", "entities": [{"id": "idn:gmaxx.com.xxxsepehlxxx.com", "name": "gmaxx.com.xxxsepehlexxx.com", "type": "InternetDomainName"}], "language": "eng"}], "source": {"id": "xxx_4-", "name": "New Certificate Registrations", "type": "Source"}, "url": null, "title": "Certificate Registration"}], "evidence": [{"mitigationString": "", "timestamp": "2020-09-28T02:36:23.924Z", "criticalityLabel": "Suspicious", "evidenceString": "1 sighting on 1 source: New Certificate Registrations. Certificate registered on Sep 28, 2020.", "rule": "Newly Registered Certificate With Potential for Abuse - DNS Sandwich", "criticality": 2}, {"mitigationString": "", "timestamp": "2020-09-28T02:36:25.000Z", "criticalityLabel": "Suspicious", "evidenceString": "Identified by Recorded Future as potential typosquatting: DNS Sandwich similarity found between gmail.com.sabsepehlelic.com and 1 possible target: gmail.com.", "rule": "Recent Typosquat Similarity - DNS Sandwich", "criticality": 2}], "criticality": 2}, "trend": {}, "documents": []}, {"entity": {"id": "idn:www.xxail.com.xxxsepehxxxx.com", "name": "www.xxail.com.xxxsepehxxxx.com", "type": "InternetDomainName"}, "risk": {"criticalityLabel": "Suspicious", "score": null, "documents": [{"references": [{"fragment": "A certificate for the domain www.xxail.com.xxxsepehxxxx.com has been registered", "entities": [{"id": "idn:www.xxail.com.xxxsepehxxxx.com", "name": "www.xxail.com.xxxsepehxxxx.com", "type": "InternetDomainName"}], "language": "eng"}], "source": {"id": "xxx_4-", "name": "New Certificate Registrations", "type": "Source"}, "url": null, "title": "Certificate Registration"}], "evidence": [{"mitigationString": "", "timestamp": "2020-09-28T02:36:23.924Z", "criticalityLabel": "Suspicious", "evidenceString": "1 sighting on 1 source: New Certificate Registrations. Certificate registered on Sep 28, 2020.", "rule": "Newly Registered Certificate With Potential for Abuse - DNS Sandwich", "criticality": 2}, {"mitigationString": "", "timestamp": "2020-09-28T02:36:25.000Z", "criticalityLabel": "Suspicious", "evidenceString": "Identified by Recorded Future as potential typosquatting: DNS Sandwich similarity found between www.xxail.com.xxxsepehxxxx.com and 1 possible target: gmail.com.", "rule": "Recent Typosquat Similarity - DNS Sandwich", "criticality": 2}], "criticality": 2}, "trend": {}, "documents": []}], "url": "https://xxx.xxxxedfutxxxx.com/live/sc/notification/?id=feRxxx", "rule": {"url": "https://xxx.xxxxedfutxxxx.com/live/sc/ViewIdkobra_view_report_item_alert_editor?view_opts=%7B%22reportId%22%3A%22eOFFb0%22%2C%22bTitle%22%3Atrue%2C%22title%22%3A%22Infrastructure+and+Brand+Risk%2C+Potential+Typosquatting+Watch+List+Domains%22%7D&state.bNavbar=false", "name": "Infrastructure and Brand Risk, Potential Typosquatting Watch List Domains", "id": "eOFxxx"}, "triggered": "2020-09-28T10:13:40.466Z", "id": "feRxxx", "counts": {"references": 2, "entities": 2, "documents": 1}, "title": "Infrastructure and Brand Risk, Potential Typosquatting Watch List Domains ...", "type": "ENTITY"}}
```









## Connectors
#### Recorded Future - Playbook Alerts Tracking Connector
Pull Playbook Alert Updates from Recorded Future. Must check one of 'New Assessment Added' 'Playbook Alert Reopened' 'Priority Increased' 'Entity Added' for cases to be created

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API URL|API Root of the Recorded Future instance.|True|String|https://api.recordedfuture.com|
|API Key|API Key from Recorded Future.|True|Password|*****|
|Search Max Hours Backwards|Amount of hours from where to fetch Playbook Alerts since last updated.|False|Int|1|
|Playbook Alert Categories|Specify the Playbook Alert Categories that should be fetched by the SecOps server. Parameter can take multiple values as a comma separated string. Possible values: domain_abuse, cyber_vulnerability, code_repo_leakage, third_party_risk, identity_novel_exposures, geopolitics_facility.|False|String|domain_abuse, cyber_vulnerability, code_repo_leakage, third_party_risk, identity_novel_exposures, geopolitics_facility|
|Playbook Alert Statuses|Specify the Playbook Alert Statuses that should be fetched by the SecOps server. Parameter can take multiple values as a comma separated string. Possible values: New, InProgress, Resolved, Dismissed.|False|String||
|Playbook Alert Priorities|Specify the Playbook Alert Priorities that should be fetched by the SecOps server. Parameter can take multiple values as a comma separated string. Possible values: Informational, Moderate, High.|False|String||
|Playbook Alert Reopened|Create a new case when a Playbook Alert is Reopened.|False|Boolean|false|
|Priority Increased|Create a new case when a Playbook Alert priority increases. If enabled, set the priority threshold via the 'Priority Increased Threshold' parameter.|False|Boolean|false|
|New Assessment Added|Create a new case when a Playbook Alert has a new assessment added.|False|Boolean|false|
|Entity Added|Create a new case when Playbook Alert entities are added.|False|Boolean|false|
|Max Alerts To Fetch|How many alerts to process per one connector iteration.|False|Int|100|
|Severity|Severity will be one from the following values Low, Medium, High, Critical. Will be assigned to Siemplify alerts created from this connector.|True|String|Medium|
|Enable Overflow|If enabled, uses Google 'oveflow' to deduplicate similar alerts.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Recorded Future server is valid.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|


#### Recorded Future - Classic Alerts Connector
Pull Classic alerts from Recorded Future. 
Allowlist and denylist work with Recorded Future rule names.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API URL|API Root of the Recorded Future instance.|True|String|https://api.recordedfuture.com|
|API Key|API Key from Recorded Future.|True|Password|*****|
|Fetch Max Hours Backwards|Amount of hours from where to fetch events.|False|Int|1|
|Alert Statuses|Specify the Alert Statuses that should be fetched by the SecOps server. Parameter can take multiple values as a comma separated string. Possible values: New, Pending, Resolved, Dismissed.|False|String|New|
|Max Alerts To Fetch|How many alerts to process per one connector iteration.|False|Int|100|
|Severity|Severity will be one from the following values Low, Medium, High, Critical. Will be assigned to Siemplify alerts created from this connector.|True|String|Medium|
|Use whitelist as a blacklist|If enabled, allowlist will be used as a denylist.|False|Boolean|false|
|Enable Overflow|If enabled, uses Google 'oveflow' to deduplicate similar alerts.|False|Boolean|false|
|Extract all Entities|If enabled, extracts all entities from the Alert events. Otherwise only the primary event entity.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Recorded Future server is valid.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|


#### Recorded Future - Playbook Alerts Connector
Pull Playbook Alerts from Recorded Future

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API URL|API Root of the Recorded Future instance.|True|String|https://api.recordedfuture.com|
|API Key|API Key from Recorded Future.|True|Password|*****|
|Fetch Max Hours Backwards|Amount of hours from where to fetch events.|False|Int|1|
|Playbook Alert Categories|Specify the Playbook Alert Categories that should be fetched by the SecOps server. Parameter can take multiple values as a comma separated string. Possible values: domain_abuse, cyber_vulnerability, code_repo_leakage, third_party_risk, identity_novel_exposures, geopolitics_facility, malware_report.|False|String|domain_abuse, cyber_vulnerability, code_repo_leakage, third_party_risk, identity_novel_exposures, geopolitics_facility, malware_report|
|Playbook Alert Statuses|Specify the Playbook Alert Statuses that should be fetched by the SecOps server. Parameter can take multiple values as a comma separated string. Possible values: New, InProgress, Resolved, Dismissed.|False|String||
|Playbook Alert Priorities|Specify the Playbook Alert Priorities that should be fetched by the SecOps server. Parameter can take multiple values as a comma separated string. Possible values: Informational, Moderate, High.|False|String||
|Max Alerts To Fetch|How many alerts to process per one connector iteration.|False|Int|100|
|Severity|If selected, Severity will override the severity from RF for alerts created by this connector. Must be from the following values Low, Medium, High, Critical. |False|String||
|Enable Overflow|If enabled, uses Google 'oveflow' to deduplicate similar alerts.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Recorded Future server is valid.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




