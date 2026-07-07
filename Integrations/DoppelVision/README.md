
# DoppelVision

Test Integration for DoppelVision Playbook

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Key|API key required to authenticate Doppel APIs|True|Password|*****|
|User API Key|User API key required to authenticate Doppel APIs|False|Password|*****|
|Organization Code|Organization code required to authenticate Doppel APIs for multi-tenant setup|False|String|None|


#### Dependencies
| |
|-|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|urllib3-2.5.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Update Alert
Updates a alert in the system with certain parameters.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert_ID|Unique identity for each specific alert in Doppel tenant|False|String|None|
|Entity|Entity to be alerted|False|String|https://dummyurl.com|
|Queue_State|Queue state value of the Alerts Values : "doppel_review","needs_confirmation","monitoring","taken_down","actioned", "archived"|True|List|actioned|
|Entity_State|Entity state of Alerts Values : "active", "down", "parked"|True|List|active|



##### JSON Results
```json
{}
```



#### Create Abuse Alert
Create an alert for the provided value to abuse box. Will fail if the alert value is invalid or is protected (e.g. google.com) in Doppel's system.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Entity|Entity to be Alerted|True|String|https://dummyabuseurl.com|



##### JSON Results
```json
{}
```



#### Create Alert
Create an alert for the provided entity. Will fail if entity is invalid or protected in Doppel's system.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Entity|Entity to be alerted.|True|String|https://dummyrul.com|



##### JSON Results
```json
{}
```



#### Get Alert
Retrieves the alert details by ID or entity
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Entity|Entity to be alerted.|False|String|https://dummyurl.com|
|Alert_ID|The unique ID of the created Alert on Doppel Tenant|False|String|TST-1|



##### JSON Results
```json
{}
```



#### Get Alerts
Fetches all alerts from Doppel Tenant at once.
Doesn't require any input parameters.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Search Key|Currently only supports search by url|False|String|None|
|Product|Product category the report belongs to.|False|List||
|Created Before|Filter alerts created before this date. '2024-01-05T13:45:30' -- Represents the 5th of January 2024, at 1:45:30 PM|False|String|None|
|Created After|Filter alerts created after this date. '2024-01-05T13:45:30' -- Represents the 5th of January 2024, at 1:45:30 PM|False|String|None|
|Sort Type|The field to sort the reports by. Defaults to date_sourced.|False|List||
|Sort Order|The order to sort the reports by. Defaults to desc.|False|List||
|Page|Page number for pagination; defaults to 0|False|String||
|Queue State|New queue status to update alert with (id required)|False|List||
|Tags|List of tags to filter alerts|False|String|None|



##### JSON Results
```json
{}
```



#### Ping
Ping features enable the integration users to test the connectivity and validate the Doppel credential(API Key) while configuring the Doppel integration.
Timeout - 600 Seconds



##### JSON Results
```json
{}
```









