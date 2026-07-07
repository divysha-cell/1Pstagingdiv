
# MicrosoftGraphSecurity

Microsoft Graph Security provide integrating with Intelligent Security Graph providers that enable your app to retrieve alerts and update alert lifecycle properties

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Client ID|None|True|String||
|Secret ID|None|False|Password|*****|
|Certificate Path|None|False|String||
|Certificate Password|None|False|Password|*****|
|Tenant|None|True|String||
|Use V2 API|If enabled, integration will use V2 API endpoints inside actions.|False|Boolean|false|
|Verify SSL|None|False|Boolean|false|


#### Dependencies
| |
|-|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|cryptography-43.0.1-cp39-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|anyio-4.6.2.post1-py3-none-any.whl|
|httpcore-1.0.6-py3-none-any.whl|
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
|TIPCommon-2.0.3-py2.py3-none-any.whl|
|pyOpenSSL-24.2.1-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|pycryptodome-3.21.0-cp36-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|certifi-2024.8.30-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|google_auth-2.36.0-py2.py3-none-any.whl|
|cachetools-5.5.0-py3-none-any.whl|


## Actions
#### List Alerts
Get all alerts
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter Key|Specify the key that needs to be used to filter alerts. Note: "Title" option is not supported in the V2 API.|False|List|Not Specified|
|Filter Logic|Specify what filter logic should be applied. Filtering logic is working based on the value  provided in the “Filter Key” parameter.|False|List|Not Specified|
|Filter Value|Specify what value should be used in the filter. If “Equal“ is selected, action will try to find the exact match among results and if “Contains“ is selected, action will try to find results that contain that substring. If nothing is provided in this parameter, the filter will not be applied. Filtering logic is working based on the value  provided in the “Filter Key” parameter.|False|String|None|
|Max Records To Return|Specify how many records to return. If nothing is provided, action will return 50 records.|False|String|50|



##### JSON Results
```json
[{"category": "category-value", "azureTenantId": "azureTenantId-value", "assignedTo": "assignedTo-value", "activityGroupName": "activityGroupName-value", "closedDateTime": "datetime-value", "azureSubscriptionId": "azureSubscriptionId-value"}]
```



#### Update Alert
Update an editable alert property
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|The ID of the alert to update.|True|String||
|Assigned To|Name of the analyst the alert is assigned to for triage, investigation, or remediation.|False|String||
|Closed Date Time|Time at which the alert was closed. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: '2014-01-01T00:00:00Z'. Note: this parameter is not supported in the V2 version of API.|False|String||
|Comments|Analyst comments on the alert (for customer alert management), separated by comma. This method can update the comments field with the following values only: Closed in IPC, Closed in MCAS. Note: in V2 version of API this parameter works as a string and a single comment will be added to the Alert.|False|String||
|Feedback|Analyst feedback on the alert. Possible values are: unknown, truePositive, falsePositive, benignPositive. Note: in V2 version of API this parameter is mapped to "classification" and has the following possible values: unknown, falsePositive, truePositive, informationalExpectedActivity, unknownFutureValue.|False|String||
|Status|Alert lifecycle status (stage). Possible values are: unknown, newAlert, inProgress, resolved.|False|String||
|Tags|User-definable labels that can be applied to an alert. Separated by comma. Note: this parameter is not supported in the V2 version of API.|False|String||



#### List Incidents
List security incidents from Microsoft Graph based on provided criteria.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter Key|Specify the key that needs to be used to filter incidents.|False|List|Not Specified|
|Filter Logic|Specify what filter logic should be applied. Filtering logic is working based on the value  provided in the “Filter Key” parameter.|False|List|Not Specified|
|Filter Value|Specify what value should be used in the filter. If “Equal“ is selected, action will try to find the exact match among results and if “Contains“ is selected, action will try to find results that contain that substring. If nothing is provided in this parameter, the filter will not be applied. Filtering logic is working based on the value  provided in the “Filter Key“ parameter.|False|String|None|
|Max Records To Return|Specify how many records to return. If nothing is provided, action will return 50 records.|False|String|50|



##### JSON Results
```json
[{"id": "251409", "tenantId": "d48f52", "status": "active", "incidentWebUrl": "https://sav.com", "redirectIncidentId": null, "displayName": "Example Name", "createdDateTime": "2023-10-03T16:06:52.4266667Z", "lastUpdateDateTime": "2024-11-12T16:11:21.8233333Z", "assignedTo": null, "classification": "unknown", "determination": "unknown", "severity": "high", "customTags": [], "systemTags": [], "description": null, "lastModifiedBy": "Automation", "resolvingComment": null, "summary": null, "comments": []}]
```



#### Add Alert Comment
Add a comment to the alert in Microsoft Graph.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify the ID of the alert that needs to be updated.|True|String||
|Comment|Specify the comment for the alert.|True|String||



#### Kill User Session
The action invalidates all the refresh tokens issued to applications for a user, by resetting the signInSessionsValidFromDateTime user property to the current date-time.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|userPrincipalName | ID|The user's username used during sign in or the user Unique ID provided by Azure AD|True|String||



#### Get Alert
Retrieve the properties and relationships of an alert by ID
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Alert ID|True|String||



##### JSON Results
```json
{"feedback": "@odata.type: microsoft.graph.alertFeedback", "recommendedActions": ["String"], "networkConnections": [{"applicationName": "String", "natDestinationPort": "String", "destinationAddress": "String", "localDnsName": "String", "natDestinationAddress": "String", "destinationUrl": "String", "natSourceAddress": "String", "sourceAddress": "String", "direction": "@odata.type: microsoft.graph.connectionDirection", "domainRegisteredDateTime": "String (timestamp)", "status": "@odata.type: microsoft.graph.connectionStatus", "destinationDomain": "String", "destinationPort": "String", "sourcePort": "String", "protocol": "@odata.type: microsoft.graph.securityNetworkProtocol", "natSourcePort": "String", "riskScore": "String", "urlParameters": "String"}], "cloudAppStates": [{"destinationServiceIp": "String", "riskScore": "String", "destinationServiceName": "String"}], "detectionIds": ["String"], "id": "String (identifier)", "category": "String", "fileStates": [{"path": "String", "riskScore": "String", "name": "String", "fileHash": {"hashType": "@odata.type: microsoft.graph.fileHashType", "hashValue": "String"}}], "severity": "@odata.type: microsoft.graph.alertSeverity", "title": "String", "sourceMaterials": ["String"], "comments": ["String"], "assignedTo": "String", "eventDateTime": "String (timestamp)", "activityGroupName": "String", "status": "@odata.type: microsoft.graph.alertStatus", "description": "String", "tags": ["String"], "confidence": 1024, "vendorInformation": {"providerVersion": "String", "vendor": "String", "subProvider": "String", "provider": "String"}, "userStates": [{"emailRole": "@odata.type: microsoft.graph.emailRole", "logonId": "String", "domainName": "String", "onPremisesSecurityIdentifier": "String", "userPrincipalName": "String", "userAccountType": "@odata.type: microsoft.graph.userAccountSecurityType", "logonIp": "String", "logonDateTime": "String (timestamp)", "logonType": "@odata.type: microsoft.graph.logonType", "logonLocation": "String", "aadUserId": "String", "accountName": "String", "riskScore": "String", "isVpn": "true"}], "malwareStates": [{"category": "String", "wasRunning": "true", "name": "String", "family": "String", "severity": "String"}], "processes": [{"processId": 1024, "integrityLevel": "@odata.type: microsoft.graph.processIntegrityLevel", "name": "String", "fileHash": {"hashType": "@odata.type: microsoft.graph.fileHashType", "hashValue": "String"}, "parentProcessId": 1024, "createdDateTime": "String (timestamp)", "commandLine": "String", "parentProcessName": "String", "accountName": "String", "isElevated": "true", "path": "String", "parentProcessCreatedDateTime": "String (timestamp)"}], "azureTenantId": "String", "triggers": [{"type": "String", "name": "String", "value": "String"}], "createdDateTime": "String (timestamp)", "vulnerabilityStates": [{"cve": "String", "severity": "String", "wasRunning": "true"}], "hostStates": [{"isAzureAadRegistered": "true", "riskScore": "String", "fqdn": "String", "isHybridAzureDomainJoined": "true", "netBiosName": "String", "publicIpAddress": "String", "isAzureAadJoined": "true", "os": "String", "privateIpAddress": "String"}], "lastModifiedDateTime": "String (timestamp)", "registryKeyStates": [{"processId": 1024, "oldKey": "String", "oldValueName": "String", "valueType": "@odata.type: microsoft.graph.registryValueType", "oldValueData": "String", "hive": "@odata.type: microsoft.graph.registryHive", "valueData": "String", "key": "String", "valueName": "String", "operation": "@odata.type: microsoft.graph.registryOperation"}], "closedDateTime": "String (timestamp)", "azureSubscriptionId": "String"}
```



#### Get Incident
Get details of a security incident by an incident ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident ID|Specify the ID of the incident.|True|String||



##### JSON Results
```json
{"@odata.context": "https://abc.com", "id": "251409", "tenantId": "dagre", "status": "active", "incidentWebUrl": "https://abc.com", "redirectIncidentId": null, "displayName": "Example Name", "createdDateTime": "2023-10-03T16:06:52.4266667Z", "lastUpdateDateTime": "2024-11-13T16:17:36.5266667Z", "assignedTo": null, "classification": "unknown", "determination": "unknown", "severity": "high", "customTags": [], "systemTags": [], "description": null, "lastModifiedBy": "Automation", "resolvingComment": null, "summary": null, "comments": []}
```



#### Get Administrator Consent
Run the action and browse to the received url TO grant the permissions your app needs at the Azure portal
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Redirect URL|Use the redirect url you registered to request an authorization.|True|String||



#### Ping
Test Connectivity
Timeout - 600 Seconds









## Connectors
#### Microsoft Graph Security Connector
Deprecation Notice! This connector is planned to be deprecated on 30th March 2027. Visit documentation for more information. Microsoft Graph security Alerts Connector ingests alerts published in Microsoft Graph Security as Google Security Operations SOAR alerts. The connector periodically connects to the Microsoft Graph security endpoint and pulls a list of incidents generated for a specific time period.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the Environment Field Name field.|False|String|.*|
|Client ID|Client (Application) ID that was added for the app registration in Azure Active Directory for this integration.|True|String||
|Client Secret|Secret that was entered for Azure AD app registration.|False|Password|*****|
|Certificate Path|If authentication based on certificates is used instead of client secret, specify path to the certificate on Siemplify server.|False|String||
|Certificate Password|Optional, if certificate is password-protected, specify the password to open the certificate file.|False|Password|*****|
|Azure Active Directory ID|Azure Active Directory Tenant ID|True|String||
|Use V2 API|If enabled, connector will use V2 API endpoints. Note: the structure of the alerts and events will change. Additionally, parameter "Fetch Alerts only from" will require different values to be provided.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the server is valid.|False|Boolean|false|
|Offset Time In Hours|Fetch alerts from X hours backwards.|True|Int|120|
|Fetch Alerts only from|A comma-separated list of providers to pull alerts from Microsoft Graph. If you set the 'Fetch Alerts only from' parameter to Office 365 Security and Compliance, the connector doesn't support multiple values in the Alert Statuses to fetch or Alert Severities to fetch parameters. If 'Use V2 API' is enabled, then this parameter will work with 'serviceSource' property of the alert.|False|String||
|Alert Statuses to fetch|Specify statuses of the alerts that should be fetched by the Siemplify server. Values should be comma separated.|True|String|unknown, newAlert, inProgress, resolved|
|Alert Severities to fetch|Specify severities of the alerts that should be fetched by the Siemplify server. Values should be comma separated.|True|String|high, medium, low, informational, unknown|
|Max Alerts Per Cycle|How many alerts should be processed during one connector run.|True|Int|50|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|


#### Microsoft Graph Office 365 Security and Compliance Connector
Deprecation Notice! This connector is planned to be deprecated on 30th March 2027. Visit documentation for more information. Ingest Office 365 Security and Compliance alerts using Graph API

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the Environment Field Name field.|False|String|.*|
|Client ID|Client (Application) ID that was added for the app registration in Azure Active Directory for this integration.|True|String||
|Client Secret|Secret that was entered for Azure AD app registration.|False|Password|*****|
|Certificate Path|If authentication based on certificates is used instead of client secret, specify path to the certificate on Siemplify server.|False|String||
|Certificate Password|Optional, if certificate is password-protected, specify the password to open the certificate file.|False|Password|*****|
|Azure Active Directory ID|Azure Active Directory Tenant ID|True|String||
|Use V2 API|If enabled, connector will use V2 API endpoints. Note: the structure of the alerts and events will change.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the server is valid.|False|Boolean|true|
|Offset Time In Hours|Fetch alerts from X hours backwards.|True|Int|120|
|Alert Statuses to fetch|Specify statuses of the alerts that should be fetched by the Siemplify server. Values should be comma separated.|False|String|Dismissed, Active, Investigating, Resolved|
|Alert Severities to fetch|Specify severities of the alerts that should be fetched by the Siemplify server. Values should be comma separated.|False|String|high, medium, low, informational, unknown|
|Max Alerts Per Cycle|How many alerts should be processed during one connector run.|True|Int|50|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




