
# Group-IB-DRP

This integration connects the Group-IB Digital Risk Protection portal to Google SecOps SOAR. It imports DRP violation events into SecOps as structured cases, surfaces URLs as actionable entities, and enables analysts to approve or reject violations directly from SecOps playbooks — without leaving the SOAR platform. In case of any queries, please reach out to integration@group-ib.com.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Verify SSL|Verify the server's SSL certificate.|False|Boolean|true|
|API URL||True|String|https://drp.group-ib.com/client_api|
|API login||False|Email|None|
|API key||False|Password|*****|


#### Dependencies
| |
|-|
|typing_extensions-4.15.0-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|pyasn1-0.6.3-py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|pycparser-3.0-py3-none-any.whl|
|proto_plus-1.27.2-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|anyio-4.13.0-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|google_auth-2.49.2-py3-none-any.whl|
|validators-0.35.0-py3-none-any.whl|
|protobuf-7.34.1-py3-none-any.whl|
|google_api_core-2.30.3-py3-none-any.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|httplib2-0.31.2-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|requests-2.33.1-py3-none-any.whl|
|googleapis_common_protos-1.74.0-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|EnvironmentCommon-1.0.3-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|cryptography-46.0.7-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|TIPCommon-2.0.6-py2.py3-none-any.whl|
|google_api_python_client-2.194.0-py3-none-any.whl|
|ciaops-1.0.1-py3-none-any.whl|
|google_auth_httplib2-0.3.1-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|


## Actions
#### URL-Approve

Timeout - 600 Seconds



##### JSON Results
```json
{}
```



#### URL-Reject

Timeout - 600 Seconds



##### JSON Results
```json
{}
```



#### Get Violation Details

Timeout - 600 Seconds



##### JSON Results
```json
{}
```



#### Ping

Timeout - 600 Seconds



##### JSON Results
```json
{}
```






## Jobs

#### DRP Deduplication Job


|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Case Type|True|String|Violations|
|Max Cases To Process|True|Int|2000|
|Lookback Days|True|Int|1|
|Dry Run|False|Boolean|true|
|Close Root Cause|True|String|Duplicate|
|Close Reason|True|String|Maintenance|
|Merge Mode|True|String|close|
|Carry Over To Primary|False|Boolean|false|
|Chronicle Instance Path|False|String||



## Connectors
#### DRP Violations Connector
DRP Violations Connector

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API login| your DRP email  |True|Email|example@email.me|
|API key|your DRP API token |True|Password|*****|
|API URL|DRP URL|True|String|https://drp.group-ib.com/client_api/|
|Verify SSL|Verify the server's SSL certificate.|False|Boolean|true|
| Case name  |Violation URL |True|String|Violation URL |
|Case severity|Severity|True|String|Medium|
|Case type  |Type|True|String|Violations|
|Start date |leave blank (defaults to 1 day back) |False|String||
|Brand IDs|Filtering by company brands|False|String||
|Approve States|1 - Not required; 2 - Rejected; 3 - Under review; 4 - approved|False|String||
|Subtypes|1 - counterfeit; 2 - piracy; 3 - partner_policy_compliance; 4 - trademark; 5 - malware; 6 - phishing; 7 - fraud; 8 - no_violation|False|String||
|Section|1 - Web; 2 - Mobile apps; 3 - Marketplace; 4 - Social networks; 5 - Advertising; 6 - Instant messengers|False|String||


#### DRP Violations Review Connector
DRP Violations Review Connector

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API login|DRP username|True|Email|your@email.com |
|API key|your API token |True|Password|*****|
|API URL|DRP URL|True|String|https://drp.group-ib.com/client_api/|
|Verify SSL|Verify the server's SSL certificate.|False|Boolean|true|
|Case name |Name|True|String|Violation URL - review required |
|Case type|type|True|String|Violations Under Review|
|Case severity |Severity|True|String|Medium|
|Start date |leave blank - auto takes -1 day|False|String||


#### DRP Typosquatting Connector
DRP Typosquatting Connector

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case name|Default — label shown on cases  |True|String|Typosquatting Domain |
|Case type|type|True|String|Typosquatting    |
|API login| Email used for DRP portal login |True|Email|your@email.com   |
|API key|API token from DRP profile   |True|Password|*****|
|API URL|DRP URL|True|String|https://drp.group-ib.com/client_api/|
|Verify SSL|Verify the server's SSL certificate.|False|Boolean|true|
|Case severity|Options: Informative / Low / Medium / High / Critical |True|String|Medium|
|Start date|Blank = start from 1 day ago. Set YYYY-MM-DD only for a historical backfill |False|String||




