
# SOCRadar

Bidirectional integration between SOCRadar Extended Threat Intelligence (XTI) and Google SecOps SOAR. Ingests SOCRadar alarms as cases, provides IOC enrichment, threat feed collection, rapid reputation lookups, and full alarm lifecycle management. Support: integration@socradar.io

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|SOCRadar API base URL.|True|String|https://platform.socradar.com/api|
|API Key|SOCRadar platform API key with Incident API V4 permissions.|True|Password|*****|
|Company ID|SOCRadar company identifier (numeric).|True|String|None|
|Verify SSL|Enable SSL certificate verification for API requests.|False|Boolean|true|
|IOC Enrichment API Key|Separate API key for SOCRadar IOC Enrichment (credit-based add-on). Leave empty to skip enrichment actions.|False|Password|*****|
|Rapid Reputation API Key|Separate API key for SOCRadar Rapid Reputation (add-on). Provides quick reputation lookups for IPs, domains, URLs, and hashes. Leave empty to skip.|False|Password|*****|


#### Dependencies
| |
|-|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|certifi-2026.5.20-py3-none-any.whl|
|urllib3-2.7.0-py3-none-any.whl|
|idna-3.16-py3-none-any.whl|
|requests-2.34.2-py3-none-any.whl|


## Actions
#### Remove Tag
Remove a tag from a SOCRadar alarm (toggle-based API).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alarm ID|The SOCRadar alarm ID.|True|String||
|Tag|Tag to remove.|True|String||



#### Get Threat Feed
Fetch IOCs from one or more SOCRadar Threat Feed collections by UUID. Returns IOC values with type, confidence score, seen count, and first/last seen dates.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Collection UUIDs|Comma-separated SOCRadar Threat Feed collection UUIDs.|True|String||
|Max IOCs Per Feed|Maximum number of IOCs to return per feed. Default 1000.|False|String|1000|
|IOC Type Filter|Comma-separated IOC types to include: hash, ip, domain, url. Leave empty for all.|False|String||



#### Change Alarm Status
Change the status of a SOCRadar alarm. Valid statuses: OPEN (0), INVESTIGATING (1), RESOLVED (2), PENDING_INFO (4), LEGAL_REVIEW (5), VENDOR_ASSESSMENT (6), FALSE_POSITIVE (9), DUPLICATE (10), PROCESSED_INTERNALLY (11), MITIGATED (12), NOT_APPLICABLE (13).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Status|New status name or code.|True|String||
|Alarm ID|The SOCRadar alarm ID.|True|String||
|Comments|Optional comment for the status change.|False|String||
|Email|Email of the user making the change.|False|String||
|Update Related Findings|Whether to update the status of related findings.|False|Boolean|true|



#### Get Alarm Details
Fetch full details of a single SOCRadar alarm by ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alarm ID|The SOCRadar alarm ID to retrieve.|True|String||



#### Change Assignee
Assign user(s) to a SOCRadar alarm by email or user ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alarm ID|The SOCRadar alarm ID.|True|String||
|User Emails|Comma-separated email addresses of users to assign.|False|String||
|User IDs|Comma-separated user IDs to assign.|False|String||



#### Add Comment
Add a comment to a SOCRadar alarm.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alarm ID|The SOCRadar alarm ID.|True|String||
|Comment|Comment text to add.|True|String||
|User Email|Email of the user posting the comment.|False|String||



#### Rapid Reputation
Quick reputation lookup for an entity (IP, hostname, URL, or hash) using the SOCRadar Rapid Reputation API. Returns score, severity, whitelisting status, and threat intelligence sources. Requires the Rapid Reputation API Key.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Entity Value|The entity to check (e.g. 37.46.210.230, evil.com, or a file hash).|True|String||
|Entity Type|Type of entity: ip, hostname, url, or hash.|True|String|ip|



#### Change Severity
Change the severity of a SOCRadar alarm (LOW, MEDIUM, HIGH, CRITICAL).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alarm ID|The SOCRadar alarm ID.|True|String||
|Severity|New severity: LOW, MEDIUM, HIGH, or CRITICAL.|True|String||



#### Enrich Indicator
Enrich an indicator (IP, domain, hash, URL) using the SOCRadar IOC Enrichment API. Returns threat score, severity, categorization, classifications, history, and optionally AI insights. Requires the IOC Enrichment API Key.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Indicator|The indicator value to enrich (IP address, domain, hash, or URL).|True|String||
|Include AI Insight|Set to true to include AI-generated threat insight. Increases response time and credit usage.|False|String|false|
|Fields|Comma-separated fields: indicator_details, indicator_history, indicator_relations, indicator_ai_insight. Leave empty for default.|False|String||



#### Ask Analyst
Request assistance from a SOCRadar analyst for an alarm.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alarm ID|The SOCRadar alarm ID.|True|String||
|Comment|Message for the SOCRadar analyst team.|True|String||



#### Enrich Indicator STIX
Enrich an indicator and return results in STIX 2.1 bundle format. Requires the IOC Enrichment API Key.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Indicator|The indicator value to enrich (IP address, domain, hash, or URL).|True|String||
|Show Credit Details|Set to true to include API credit usage details in the response.|False|String|false|



#### Add Tag
Add a tag to a SOCRadar alarm.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alarm ID|The SOCRadar alarm ID.|True|String||
|Tag|Tag to add.|True|String||



#### Get Assignee Options
List all users available for alarm assignment in the SOCRadar company.
Timeout - 600 Seconds



#### Get Assignee
Get the current assignee(s) of a SOCRadar alarm.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alarm ID|The SOCRadar alarm ID.|True|String||



#### Ping
Test connectivity to the SOCRadar API.
Timeout - 600 Seconds






## Jobs

#### Sync IOC Feeds
Scheduled job that fetches IOCs from configured SOCRadar Threat Feed collections and writes them to Chronicle SIEM reference lists. Creates one list per IOC type (ip, domain, hash, url). Run daily to keep threat intelligence feeds current.


|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Collection UUIDs|True|String||
|Max IOCs Per Feed|False|Int|5000|
|Reference List Prefix|False|String|SOCRadar_IOC|
|API Root|True|String|https://platform.socradar.com/api|
|API Key|True|Password|*****|
|Company ID|True|String||
|Verify SSL|False|Boolean|true|



## Connectors
#### SOCRadar Alarms Connector
Polling connector that ingests SOCRadar alarms as Google SecOps SOAR cases. Extracts indicator events (IPs, domains, URLs, emails, hashes) for entity mapping. Severity mapped to risk-score bands (CRITICAL=90, HIGH=70, MEDIUM=50, LOW=30, INFO=10). Supports filtering by severity, status, main type, sub type, tags, and assignees.


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Name of the field where the environment name is stored. If empty, uses default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the environment field value.|False|String|.*|
|API Root|SOCRadar API base URL.|True|String|https://platform.socradar.com/api|
|API Key|SOCRadar platform API key with Incident API V4 permissions.|True|Password|*****|
|Company ID|SOCRadar company identifier (numeric).|True|String||
|Verify SSL|Enable SSL certificate verification for API requests.|False|Boolean|true|
|Max Alerts Per Cycle|Maximum number of alarms to ingest per polling cycle.|False|Int|100|
|Extract Indicators|Extract IOCs (IP, URL, Email, MD5, SHA1, SHA256) from alarm content as separate indicator events for entity mapping. Default true.|False|Boolean|true|
|Severity Filter|Comma-separated severity levels to fetch: LOW, MEDIUM, HIGH, CRITICAL. Leave empty for all.|False|String||
|Status Filter|Status filter: OPEN, CLOSED, ON_HOLD. Default: OPEN.|False|String|OPEN|
|Main Type Filter|Comma-separated alarm main types. E.g.: Attack Surface Management, Deep & Dark Web Monitoring. Leave empty for all.|False|String||
|Sub Type Filter|Comma-separated alarm sub-types. E.g.: Stolen Credentials On Dark Web Bot Market. Leave empty for all.|False|String||
|Tags Filter|Comma-separated tags to filter alarms by. Leave empty for all.|False|String||
|Assignees Filter|Comma-separated assignee names or emails to filter alarms by. Leave empty for all.|False|String||




