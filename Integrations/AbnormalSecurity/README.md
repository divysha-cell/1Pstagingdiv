
# AbnormalSecurity

Abnormal Security uses AI to protect organizations from email attacks. This integration enables automated ingestion of threats and cases as SOAR alerts, plus search and remediation of malicious email messages through the Abnormal Security API. For support, contact: support@abnormalsecurity.com

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API URL|The base URL of the Abnormal Security API. US customers use https://api.abnormalplatform.com (default). EU customers use https://eu.rest.abnormalsecurity.com.|True|String|https://api.abnormalplatform.com|
|API Key|The API key used to authenticate with the Abnormal Security API.|True|Password|*****|
|Verify SSL|If enabled, SSL certificates will be verified for API requests.|False|Boolean|true|


#### Dependencies
| |
|-|
|certifi-2026.4.22-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.6.3-py3-none-any.whl|
|requests-2.33.1-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|


## Actions
#### List Threats
Retrieve a paginated list of threats from Abnormal Security. Use the Filter parameter to narrow results by time range (e.g. receivedTime gte 2025-01-01T00:00:00Z) or other supported fields.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter|Optional filter expression. Example: receivedTime gte 2025-01-01T00:00:00Z|False|String||
|Page Size|Number of threats to return per page (max 100).|False|String|100|
|Page Number|Page number to retrieve.|False|String|1|



##### JSON Results
```json
{"threats": [{"threatId": "184712ab-6d8b-47b3-89d3-a314efef79e2", "abxMessageId": 4551618356913732076, "abxMessageIdStr": "4551618356913732076", "abxPortalUrl": "https://portal.abnormalsecurity.com/home/threat-center/remediation-history/4551618356913732076", "subject": "Phishing Email", "fromAddress": "support@secure-reply.org", "toAddresses": "example@company.com", "receivedTime": "2025-01-15T17:42:59Z", "attackType": "Phishing", "autoRemediated": true, "postRemediated": false}, {"threatId": "9a3c7b21-ff12-4e8a-b2c1-d8e3f5a09123", "abxMessageId": 3871244056913731000, "abxMessageIdStr": "3871244056913731000", "abxPortalUrl": "https://portal.abnormalsecurity.com/home/threat-center/remediation-history/3871244056913731000", "subject": "Your invoice is ready", "fromAddress": "billing@fake-invoices.net", "toAddresses": "finance@company.com", "receivedTime": "2025-01-14T09:15:30Z", "attackType": "Invoice Fraud", "autoRemediated": false, "postRemediated": true}], "pageNumber": 1, "nextPageNumber": 2}
```



#### Search Messages
Search for email messages across your organization based on threat indicators such as time range, sender email, or subject. Returns a list of matching messages that can be passed to Remediate Messages for automated response.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Start Time|Search start time in ISO 8601 format (e.g. 2025-01-01T00:00:00Z). Leave empty to default to 24 hours before now (UTC).|False|String||
|End Time|Search end time in ISO 8601 format (e.g. 2025-01-02T00:00:00Z). Leave empty to default to now (UTC).|False|String||
|Sender Email|Filter results to messages from this sender email address.|False|String||
|Subject|Filter results to messages containing this subject.|False|String||
|Tenant IDs|Comma-separated list of tenant IDs to scope the search. Leave empty to search across all tenants.|False|String||



##### JSON Results
```json
{"results": [{"customer_id": 100, "tenant_id": 123, "received_time": "2025-01-15T10:30:00Z", "subject": "Urgent: Wire Transfer Request", "sender": "attacker@malicious.com", "sender_display_name": "John Doe", "mailbox_name": "user@company.com", "mailbox_display_name": "User Name", "current_folder_name": "Inbox", "raw_message_id": "AAMkAGI2THVSAAA=", "native_user_id": "user@company.com", "cloud_message_id": "abx:CloudMessage:123:456", "internet_message_id": "<message123@sender.com>", "abnormal_message_id": "abc123def456", "abnormal_message_uuid": "uuid-123-456", "decision_category": "attack", "judgement": "attack"}], "total": 1, "pageNumber": 1, "pageSize": 100, "nextPageNumber": null, "metadata": {"trace_id": "abc-123-def-456", "response_time": "2025-01-15T10:30:05Z"}}
```



#### Get Threat Links
Retrieve the list of URLs/links observed in the messages of an Abnormal Security threat. Useful for enriching investigations with the URLs the attacker used.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threat ID|The unique identifier of the threat to act on. When the action is run with scope on a ThreatSignature entity, this resolves to the entity's identifier (the Abnormal threat_id).|True|String|[Event.event_extracted_event.abx_body.threat_id]|



##### JSON Results
```json
{"threatId": "abc-123", "links": [{"url": "http://phishing.example.com/login", "verdict": "MALICIOUS", "category": "credential_phishing"}]}
```



#### Mark Case Not An Attack
Acknowledge an Abnormal Security case as benign / not an attack. Convenience action for `Post Case Action` with action=acknowledge_not_an_attack hard-coded.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case ID|The unique identifier of the Abnormal Case (Account Takeover / abuse-mailbox case) to act on. Cases are a distinct resource from threats and do not appear in the SIEM threat-log event body, so this field does not auto-fill from a threat event. Enter the case ID directly, or chain it from a prior List Cases / Get Case step.|True|String||



##### JSON Results
```json
{"activity_log_id": "act-markcasenotanattack-001", "status": "pending", "submitted_time": "2026-05-13T10:00:00Z"}
```



#### Resolve Case
Acknowledge an Abnormal Security case as resolved. Convenience action for `Post Case Action` with action=acknowledge_resolved hard-coded.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case ID|The unique identifier of the Abnormal Case (Account Takeover / abuse-mailbox case) to act on. Cases are a distinct resource from threats and do not appear in the SIEM threat-log event body, so this field does not auto-fill from a threat event. Enter the case ID directly, or chain it from a prior List Cases / Get Case step.|True|String||



##### JSON Results
```json
{"activity_log_id": "act-resolvecase-001", "status": "pending", "submitted_time": "2026-05-13T10:00:00Z"}
```



#### Get Threat Attachments
Retrieve the list of attachments associated with an Abnormal Security threat. Useful for forensics workflows where an analyst needs to enumerate attachment metadata before deciding on remediation.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threat ID|The unique identifier of the threat to act on. When the action is run with scope on a ThreatSignature entity, this resolves to the entity's identifier (the Abnormal threat_id).|True|String|[Event.event_extracted_event.abx_body.threat_id]|



##### JSON Results
```json
{"threatId": "abc-123", "attachments": [{"attachmentName": "invoice.pdf", "attachmentSize": 102400, "sha256": "e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855", "mimeType": "application/pdf", "verdict": "MALICIOUS"}]}
```



#### Mark Case Action Required
Flag an Abnormal Security case as needing analyst attention. Convenience action for `Post Case Action` with action=action_required hard-coded.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case ID|The unique identifier of the Abnormal Case (Account Takeover / abuse-mailbox case) to act on. Cases are a distinct resource from threats and do not appear in the SIEM threat-log event body, so this field does not auto-fill from a threat event. Enter the case ID directly, or chain it from a prior List Cases / Get Case step.|True|String||



##### JSON Results
```json
{"activity_log_id": "act-markcaseactionrequired-001", "status": "pending", "submitted_time": "2026-05-13T10:00:00Z"}
```



#### Delete Messages
Delete the specified messages from recipient mailboxes. Convenience action for `Remediate Messages` with action=delete hard-coded — easier to discover in playbooks.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Source|Source mailbox for the messages. Valid values: abnormal, quarantine.|True|String|abnormal|
|Messages JSON|JSON array of message objects to delete, from the JsonResult of a prior Search Messages action. Each object must include tenant_id, raw_message_id, mailbox_name, native_user_id, subject, sender, and received_time. A single message ID is not sufficient — to act on the message behind a single threat, use the Remediate Threat action instead.|True|String||
|Remediation Reason|Reason for remediation. Valid values: false_negative, unsolicited, other, groups_remediation, quarantine_release.|True|String|false_negative|
|Tenant IDs|Optional comma-separated tenant IDs.|False|String||



##### JSON Results
```json
{"activity_log_id": "act-deletemessages-001", "status": "pending", "submitted_time": "2026-05-13T10:00:00Z"}
```



#### Get Case
Retrieve full details of a specific Abnormal Security case by its ID, including case status, severity, affected employees, and analysis summary.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case ID|The unique identifier of the Abnormal Case (Account Takeover / abuse-mailbox case) to act on. Cases are a distinct resource from threats and do not appear in the SIEM threat-log event body, so this field does not auto-fill from a threat event. Enter the case ID directly, or chain it from a prior List Cases / Get Case step.|True|String||



##### JSON Results
```json
{"caseId": 1234, "description": "Potential Account Takeover", "affectedEmployee": "Jane Smith", "firstObserved": "2025-01-15T08:00:00Z", "customerVisibleTime": "2025-01-15T08:05:00Z", "threatIds": ["184712ab-6d8b-47b3-89d3-a314efef79e2"], "analysis": "Multiple failed login attempts followed by successful login from unusual location", "case_status": "Action Required", "remediation_status": "Not remediated", "severity_level": "HIGH", "confidence": "HIGH"}
```



#### List Cases
Retrieve a paginated list of cases from Abnormal Security. Use the Filter parameter to narrow results by time range or status (e.g. createdTime gte 2025-01-01T00:00:00Z).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter|Optional filter expression. Example: createdTime gte 2025-01-01T00:00:00Z|False|String||
|Page Size|Number of cases to return per page (max 100).|False|String|100|
|Page Number|Page number to retrieve.|False|String|1|



##### JSON Results
```json
{"cases": [{"caseId": 1234, "description": "Potential Account Takeover", "severity_level": "HIGH", "confidence": "HIGH", "last_modified": "2025-01-15T09:00:00Z"}, {"caseId": 1235, "description": "Suspicious Email Forwarding Rule", "severity_level": "MEDIUM", "confidence": "MEDIUM", "last_modified": "2025-01-14T14:30:00Z"}], "pageNumber": 1, "nextPageNumber": 2}
```



#### Get Case Analysis
Retrieve the detailed analysis for an Abnormal Security case, including findings, attack signals, and supporting evidence beyond what Get Case returns.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case ID|The unique identifier of the Abnormal Case (Account Takeover / abuse-mailbox case) to act on. Cases are a distinct resource from threats and do not appear in the SIEM threat-log event body, so this field does not auto-fill from a threat event. Enter the case ID directly, or chain it from a prior List Cases / Get Case step.|True|String||



##### JSON Results
```json
{"caseId": "case-001", "analysis": {"summary": "Business email compromise targeting finance team", "attackType": "BEC", "confidenceScore": 95, "indicators": ["spoofed_sender", "wire_transfer_request"]}}
```



#### Post Threat Action
Take a remediation action on an Abnormal Security threat. Use 'remediate' to remediate detected messages, or 'unremediate' to reverse a remediation. When run on a Threat Signature entity, the Threat ID is auto-filled from the entity.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threat ID|The unique identifier of the threat to act on. When the action is run with scope on a ThreatSignature entity, this resolves to the entity's identifier (the Abnormal threat_id).|True|String|[Event.event_extracted_event.abx_body.threat_id]|
|Action|Action to take on the threat. Valid values: remediate, unremediate.|True|String|remediate|
|Message IDs|Comma-separated list of specific message IDs to act on within the threat. Leave empty to act on all messages.|False|String|[Event.event_extracted_event.abx_body.abx_message_id_str]|



##### JSON Results
```json
{"success": true, "threat_id": "abc123", "action": "remediate", "message_ids": ["msg-001", "msg-002"], "timestamp": "2026-05-08T12:00:00Z"}
```



#### Post Case Action
Update the status of an Abnormal Security case. Use 'action_required' to flag a case for attention, 'acknowledge' to mark it as reviewed, or 'close' to close the case.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case ID|The unique identifier of the Abnormal Case (Account Takeover / abuse-mailbox case) to act on. Cases are a distinct resource from threats and do not appear in the SIEM threat-log event body, so this field does not auto-fill from a threat event. Enter the case ID directly, or chain it from a prior List Cases / Get Case step.|True|String||
|Action|Action to take on the case. Valid values: action_required, acknowledge_resolved, acknowledge_in_progress, acknowledge_not_an_attack.|True|String|action_required|



##### JSON Results
```json
{"success": true, "case_id": "12345", "action": "acknowledge_resolved", "timestamp": "2026-05-08T12:00:00Z"}
```



#### Get Threat
Retrieve full details of a specific Abnormal Security threat by its ID, including attack type, confidence score, disposition, affected messages, and available remediation actions.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threat ID|The unique identifier of the threat to act on. When the action is run with scope on a ThreatSignature entity, this resolves to the entity's identifier (the Abnormal threat_id).|True|String|[Event.event_extracted_event.abx_body.threat_id]|



##### JSON Results
```json
{"threatId": "184712ab-6d8b-47b3-89d3-a314efef79e2", "messages": [{"abxMessageId": 4551618356913732076, "abxMessageIdStr": "4551618356913732076", "abxPortalUrl": "https://portal.abnormalsecurity.com/home/threat-center/remediation-history/4551618356913732076", "subject": "Phishing Email", "fromAddress": "support@secure-reply.org", "fromName": "Secure Reply", "toAddresses": "example@company.com", "recipientAddress": "example@company.com", "receivedTime": "2025-01-15T17:42:59Z", "sentTime": "2025-01-15T17:42:45Z", "internetMessageId": "<5edfca1c.1c69fb81.4b055.8fd5@mx.google.com>", "autoRemediated": true, "postRemediated": false, "attackType": "Phishing", "attackStrategy": "Name Impersonation", "returnPath": "support@secure-reply.org", "replyToEmails": [], "ccEmails": [], "senderIpAddress": "100.101.102.103", "impersonatedParty": "None / Others", "attackVector": "Link", "attachmentNames": [], "urls": ["https://malicious-site.example.com/login"], "summaryInsights": ["Unusual Sender", "Suspicious Link"], "remediationTimestamp": "2025-01-15T17:43:10Z", "isRead": false, "attackedParty": "Employee"}], "recipientCount": 1}
```



#### Mark Case In Progress
Acknowledge an Abnormal Security case as currently being worked. Convenience action for `Post Case Action` with action=acknowledge_in_progress hard-coded.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case ID|The unique identifier of the Abnormal Case (Account Takeover / abuse-mailbox case) to act on. Cases are a distinct resource from threats and do not appear in the SIEM threat-log event body, so this field does not auto-fill from a threat event. Enter the case ID directly, or chain it from a prior List Cases / Get Case step.|True|String||



##### JSON Results
```json
{"activity_log_id": "act-markcaseinprogress-001", "status": "pending", "submitted_time": "2026-05-13T10:00:00Z"}
```



#### Submit Messages To D360
Submit messages to Abnormal's Detection 360 service for re-analysis. Convenience action for `Remediate Messages` with action=submit_to_d360 hard-coded.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Source|Source mailbox for the messages. Valid values: abnormal, quarantine.|True|String|abnormal|
|Messages JSON|JSON array of message objects to submit to Detection 360, from the JsonResult of a prior Search Messages action. Each object must include tenant_id, raw_message_id, mailbox_name, native_user_id, subject, sender, and received_time. A single message ID is not sufficient — to act on the message behind a single threat, use the Remediate Threat action instead.|True|String||
|Remediation Reason|Reason for remediation. Valid values: false_negative, unsolicited, other, groups_remediation, quarantine_release.|True|String|false_negative|
|Tenant IDs|Optional comma-separated tenant IDs.|False|String||



##### JSON Results
```json
{"activity_log_id": "act-submitmessagestod360-001", "status": "pending", "submitted_time": "2026-05-13T10:00:00Z"}
```



#### Remediate Messages
Take automated remediation action on email messages identified as threats. Returns an Activity Log ID that can be passed to Get Activity Status to verify the operation completed successfully.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Action|Remediation action to take. Valid values: delete, move_to_inbox, submit_to_d360.|True|String|delete|
|Source|Source of the messages. Valid values: abnormal, quarantine.|True|String|abnormal|
|Messages JSON|JSON array of message objects from the JsonResult of a prior Search Messages action. Each object must include: tenant_id (int), raw_message_id, mailbox_name, native_user_id, subject, sender, received_time (ISO 8601). A single message ID is not sufficient — to act on the message behind a single threat, use the Remediate Threat action instead. Example: [{"tenant_id": 123, "raw_message_id": "AAMkAGI2THVSAAA=", "mailbox_name": "user@company.com", "native_user_id": "user@company.com", "subject": "Phishing", "sender": "attacker@bad.com", "received_time": "2025-01-15T10:30:00Z"}]|True|String||
|Remediation Reason|Reason for remediation. Valid values: false_negative, unsolicited, other, groups_remediation, quarantine_release. Note: quarantine_release requires source=quarantine; groups_remediation is only valid with action=delete.|True|String|false_negative|
|Tenant IDs|Comma-separated list of tenant IDs to scope remediation. Leave empty to apply to all authorized tenants.|False|String||



##### JSON Results
```json
{"action_id": "action_abc123def456", "activity_log_id": "actlog_xyz789abc123", "status": "submitted"}
```



#### Submit Inquiry
Submit a false-positive or false-negative report to Abnormal Security's detection team. Use this when a SOAR analyst disagrees with an Abnormal verdict.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Report Type|The inquiry type. Valid values: false-positive, false-negative.|True|String|false-positive|
|Reporter|Identifier of the analyst submitting the inquiry (email or username).|True|String||
|Subject|Optional subject line of the message in question.|False|String||
|Sender Email|Optional sender email address.|False|String||
|Sender Display Name|Optional sender display name.|False|String||
|Recipient Email|Optional recipient email address.|False|String||
|Recipient Display Name|Optional recipient display name.|False|String||
|Received Time|Optional ISO 8601 timestamp the message was received (e.g. 2026-05-13T10:00:00Z).|False|String||
|Description|Optional analyst note explaining why the verdict is being challenged.|False|String||



##### JSON Results
```json
{"submitted": true, "inquiry_id": "inq-001", "received_time": "2026-05-13T10:00:00Z"}
```



#### Remediate Threat
Remediate an Abnormal Security threat. Convenience action for `Post Threat Action` with action=remediate hard-coded — easier to discover and use in playbooks.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threat ID|The unique identifier of the threat to act on. When the action is run with scope on a ThreatSignature entity, this resolves to the entity's identifier (the Abnormal threat_id).|True|String|[Event.event_extracted_event.abx_body.threat_id]|
|Message IDs|Comma-separated list of specific message IDs to act on within the threat. Leave empty to act on all messages.|False|String|[Event.event_extracted_event.abx_body.abx_message_id_str]|



##### JSON Results
```json
{"activity_log_id": "act-remediatethreat-001", "status": "pending", "submitted_time": "2026-05-13T10:00:00Z"}
```



#### Move Messages To Inbox
Restore messages back to their recipients' inboxes. Convenience action for `Remediate Messages` with action=move_to_inbox hard-coded.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Source|Source mailbox for the messages. Valid values: abnormal, quarantine.|True|String|abnormal|
|Messages JSON|JSON array of message objects to move back to inbox, from the JsonResult of a prior Search Messages action. Each object must include tenant_id, raw_message_id, mailbox_name, native_user_id, subject, sender, and received_time. A single message ID is not sufficient — to act on the message behind a single threat, use the Remediate Threat action instead.|True|String||
|Remediation Reason|Reason for remediation. Valid values: false_negative, unsolicited, other, groups_remediation, quarantine_release.|True|String|false_negative|
|Tenant IDs|Optional comma-separated tenant IDs.|False|String||



##### JSON Results
```json
{"activity_log_id": "act-movemessagestoinbox-001", "status": "pending", "submitted_time": "2026-05-13T10:00:00Z"}
```



#### List Activities
List all remediation activities visible to the API key, with optional tenant scoping. Useful for audit workflows — see every action submitted, not just one by ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Tenant IDs|Optional comma-separated tenant IDs to scope the query to.|False|String||
|Page Size|Number of activities to return per page.|False|String|100|
|Page Number|Page number to retrieve.|False|String|1|



##### JSON Results
```json
{"activities": [{"activity_log_id": "act-001", "action": "delete", "status": "success", "submitted_time": "2026-05-13T10:00:00Z", "completed_time": "2026-05-13T10:00:05Z"}], "pageNumber": 1, "pageSize": 100, "total": 1}
```



#### Unremediate Threat
Reverse a remediation on an Abnormal Security threat. Convenience action for `Post Threat Action` with action=unremediate hard-coded.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threat ID|The unique identifier of the threat to act on. When the action is run with scope on a ThreatSignature entity, this resolves to the entity's identifier (the Abnormal threat_id).|True|String|[Event.event_extracted_event.abx_body.threat_id]|
|Message IDs|Comma-separated list of specific message IDs to act on within the threat. Leave empty to act on all messages.|False|String|[Event.event_extracted_event.abx_body.abx_message_id_str]|



##### JSON Results
```json
{"activity_log_id": "act-unremediatethreat-001", "status": "pending", "submitted_time": "2026-05-13T10:00:00Z"}
```



#### Get Activity Status
Check the status of a remediation operation using the Activity Log ID returned by Remediate Messages. Poll this action until the status reaches a terminal state (success, partial_success, or error).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Activity Log ID|Numeric Activity Log ID returned by the Remediate Messages action.|True|String||
|Tenant IDs|Optional. Tenant scope is resolved from the API key, so this field is not required and is ignored by the status endpoint.|False|String||



##### JSON Results
```json
{"activity_log_id": "actlog_xyz789abc123", "status": "success", "message_statuses": [{"abxMessageId": "msg_abc123def456", "status": "success", "action": "delete", "completedAt": "2025-01-15T10:32:00Z"}]}
```



#### Ping
Test connectivity and authentication to the Abnormal Security API. Run this action after configuring the integration to verify the API URL and API key are valid before building playbooks.
Timeout - 600 Seconds









## Connectors
#### Abnormal Security Threats and Cases Connector
Polls Abnormal Security for new threats and cases and ingests them as SOAR alerts. Runs on a configurable schedule (recommended every 2 minutes) and uses time-based filtering to fetch only new events since the last run.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API URL|Base URL of the Abnormal Security API. US customers use https://api.abnormalplatform.com (default). EU customers use https://eu.rest.abnormalsecurity.com.|True|String|https://api.abnormalplatform.com|
|API Key|API key used to authenticate with the Abnormal Security API.|True|Password|*****|
|Verify SSL|If enabled, SSL certificates will be verified for API requests.|False|Boolean|true|
|Max Days Backwards|Maximum number of days back to fetch events on the first run (or if the saved timestamp is older than this value).|False|Int|1|
|Max Alerts Per Cycle|Maximum number of alerts (threats + cases combined) to process per connector execution cycle.|False|Int|50|
|Force From Date|Override the saved timestamp for this run only. ISO format: 2025-01-01T00:00:00Z. Leave as None to use the saved timestamp.|False|String|None|
|Proxy Server Address|The address of the proxy server to use.|False|String|None|
|Proxy Username|The proxy username to authenticate with.|False|String|None|
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




