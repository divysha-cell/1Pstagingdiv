
# AzureSecurityCenter

Azure Security Center is a unified infrastructure security management system that strengthens the security posture of your data centers, and provides advanced threat protection across your hybrid workloads in the cloud - whether they're in Azure or not - as well as on premises.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Client ID||True|String||
|Client Secret||True|Password|*****|
|Username||False|String||
|Password||False|Password|*****|
|Subscription ID||False|String||
|Tenant ID||True|String||
|Refresh Token||False|Password|*****|
|Verify SSL||False|Boolean|false|


#### Dependencies
| |
|-|
|typing_extensions-4.15.0-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|TIPCommon-2.2.12-py2.py3-none-any.whl|
|pyasn1-0.6.3-py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|httpx-0.28.1-py3-none-any.whl|
|anyio-4.13.0-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|google_auth_httplib2-0.3.0-py3-none-any.whl|
|google_api_core-2.30.3-py3-none-any.whl|
|idna-3.15-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|httplib2-0.31.2-py3-none-any.whl|
|google_auth-2.47.0-py3-none-any.whl|
|protobuf-7.35.0-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|googleapis_common_protos-1.75.0-py3-none-any.whl|
|urllib3-2.7.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|proto_plus-1.28.0-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|google_api_python_client-2.188.0-py3-none-any.whl|


## Actions
#### List Regulatory Standard Controls
List available controls related to standards in Microsoft Azure Security Center.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Subscription ID|Specify the ID of the subscription for which you want to query information. Note: if subscription ID is provided at the integration level and action level, priority will be given to action configuration.|False|String||
|Standard Names|Specify a comma-separated list of standard names for which you want to retrieve details. Example: Azure-CIS-1.1.0|True|String||
|State Filter|Specify the comma-separated list of states. Example: Failed, Skipped. Only standards with the matching state will be returned. For example, if you specify “Failed”, action will only return failed standards. Possible values: Passed, Failed, Unsupported, Skipped|False|String|Failed|
|Max Standards To Return|Specify how many controls to return per standard.|False|String|50|



##### JSON Results
```json
[{"results": [{"Name": "PCI-DSS-3.2.1", "Controls": [{"id": "/subscriptions/XXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXX/providers/Microsoft.Security/regulatoryComplianceStandards/PCI-DSS-3.2.1/regulatoryComplianceControls/1.2.1", "name": "1.2.1", "type": "Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls", "properties": {"description": "Restrict inbound and outbound traffic to that which is necessary for the cardholder data environment, and specifically deny all other traffic.", "state": "Failed", "passedAssessments": 112, "failedAssessments": 12, "skippedAssessments": 0}}]}]}]
```



#### Update Alert Status
Update status of the alert in Microsoft Azure Security Center.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Location|Specify the location of the alert. Example: centralus.|True|String||
|Status|Specify the status for the alert.|True|List|Resolve|
|Subscription ID|Specify the ID of the subscription for which you want to query information. Note: if subscription ID is provided at the integration level and action level, priority will be given to action configuration.|False|String||
|Alert ID|Specify an ID of the alert, where you want to update status.|True|String||



#### List Regulatory Standards
List available regulatory standards in Microsoft Azure Security Center
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Subscription ID|Specify the ID of the subscription for which you want to query information. Note: if subscription ID is provided at the integration level and action level, priority will be given to action configuration.|False|String||
|State Filter|Specify the comma-separated list of states. Example: Failed, Skipped. Only standards with the matching state will be returned. For example, if you specify “Failed”, action will only return failed standards. Possible values: Passed, Failed, Unsupported, Skipped|False|String|Failed|
|Max Standards To Return|Specify how many standards to return.|False|String|50|



##### JSON Results
```json
[{"value": [{"id": "/subscriptions/XXXXXXX-XXXX-XXXX-XXXX-XXXXXXX/providers/Microsoft.Security/regulatoryComplianceStandards/Azure-CIS-1.1.0", "name": "Azure-CIS-1.1.0", "type": "Microsoft.Security/regulatoryComplianceStandards", "properties": {"state": "Failed", "passedControls": 21, "failedControls": 3, "skippedControls": 0, "unsupportedControls": 87}}]}]
```



#### Get OAuth Authorization Code
Generate an OAuth authorization code in Azure Security Center. Please refer to the documentation portal for more information.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Redirect URL|Specify the redirect URL that was used when the app was created.|True|String|https://localhost|



#### Get OAuth Refresh Token
Generate the refresh token that is needed for the integration configuration. Authorization code can be generated using "Get OAuth Authorization Code". Please refer to the documentation portal for more information.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Redirect URL|Specify the redirect URL that was used when the app was created.|True|String|https://localhost|
|Authorization Code|Specify the authorization code from action "Get OAuth Authorization Code"|True|String||



#### Ping
Test connectivity to Azure Security Center with parameters provided at the integration configuration page on Marketplace tab.
Timeout - 600 Seconds






## Jobs

#### Refresh Token Renewal Job
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Integration Environments|False|String||
|Connector Names|False|String||



## Connectors
#### Azure Security Center - Security Alerts Connector
Deprecation Notice! This connector is planned to be deprecated on 30th March 2027. Visit documentation for more information. Pull security alerts from Azure Security Center. Note: whitelist works with alertType field.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|Client ID|Client ID of the Microsoft Azure application. |True|String||
|Client Secret|Client Secret of the Microsoft Azure application.|True|Password|*****|
|Username|Username of the Microsoft Azure account.|False|String||
|Password|Password of the Microsoft Azure account.|False|Password|*****|
|Subscription ID|Subscription ID of the Microsoft Azure application.|True|String||
|Tenant ID|Tenant ID of the Microsoft Azure application.|True|String||
|Refresh Token|Refresh token for the OAuth authorization.|False|Password|*****|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Max Alerts To Fetch|How many alerts to process per one connector iteration.|False|Int|50|
|Lowest Severity To Fetch|Lowest severity that will be used to fetch Alert. Possible values: Low, Medium, High|True|String|Low|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Azure Security Center server is valid.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




