
# GoogleAlertCenter

Real-time security alerts and insights that help you protect your organization from the latest threats, including phishing, malware, and other suspicious activity.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Service Account JSON Secret|Specify the full JSON content of the service account file to be used in the integration.|True|Password|*****|
|Impersonation Email Address|Email address that has access to the alert center.|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Google Alert Center server is valid.|False|Boolean|true|


#### Dependencies
| |
|-|
|certifi-2026.4.22-py3-none-any.whl|
|pyasn1-0.6.3-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|protobuf-5.29.6-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|google_api_core-2.19.2-py3-none-any.whl|
|cachetools-5.5.2-py3-none-any.whl|
|googleapis_common_protos-1.65.0-py2.py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|idna-3.15-py3-none-any.whl|
|google_api_python_client-2.144.0-py2.py3-none-any.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|httplib2-0.31.2-py3-none-any.whl|
|google_auth-2.34.0-py2.py3-none-any.whl|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|google_auth_httplib2-0.4.0-py3-none-any.whl|
|urllib3-2.7.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|proto_plus-1.28.0-py3-none-any.whl|
|requests-2.34.2-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|


## Actions
#### Delete Alert
Delete an alert in Google Alert Center. Note: it takes 30 days for the alert to fully disappear in Google Alert Center, before that they can still be recovered.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify the id of the alert that needs to be deleted.|True|String||



#### Ping
Test connectivity to the Google Alert Center with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### Google Alert Center - Alerts Connector
Pull information about alerts from Google Alert Center. Note: whitelist filter works with "type" parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|Service Account JSON Secret|JSON that contains the secret of service account keys.|True|Password|*****|
|Impersonation Email Address|Email address that has access to the alert center.|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Google Alert Center server is valid.|False|Boolean|true|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Max Alerts To Fetch|How many alerts to process per one connector iteration. Default: 100.|False|Int|100|
|Lowest Severity To Fetch|Lowest severity that needs to be used to fetch alerts. Possible values: Informational, Low, Medium, High. If nothing is specified, the connector will ingest alerts with all severities.|False|String||
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




