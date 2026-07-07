
# Luminar IOCs and Leaked Credentials

Cognyte is a global leader in security analytics software that empowers governments and enterprises with Actionable Intelligence for a safer world. Our open software fuses, analyzes and visualizes disparate data sets at scale to help security organizations find the needles in the haystacks. Over 1,000 government and enterprise customers in more than 100 countries rely on Cognyte’s solutions to accelerate security investigations and connect the dots to successfully identify, neutralize, and prevent threats to national security, business continuity and cyber security.

Luminar is an asset-based cybersecurity intelligence platform that empowers enterprise organizations to build and maintain a proactive threat intelligence operation that enables to anticipate and mitigate cyber threats, reduce risk and enhance security resilience. Luminar enables security teams to define a customized, dynamic monitoring plan to uncover malicious activity in its earliest stages on all layers of the Web.

“Luminar IOCs and Leaked Credentials” App allows integration of intelligence-based IOC data and customer-related leaked records identified by Luminar.


Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Luminar Base URL|Please enter valid Luminar Base URL|True|String|https://demo.cyberluminar.com|
|Luminar API Account ID|Please enter valid Luminar API Account ID|True|Password|*****|
|Luminar API Client ID|Please enter valid Luminar API Client ID|True|Password|*****|
|Luminar API Client Secret|Please enter valid Luminar API Client Secret|True|Password|*****|


#### Dependencies
| |
|-|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|urllib3-2.5.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Ping

Timeout - 600 Seconds



##### JSON Results
```json
{}
```






## Jobs

#### Luminar IOC and Leaked Credentials Job


|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Siemplify Username|True|String||
|Siemplify Password|True|Password|*****|



## Connectors
#### Luminar IOCs and Leaked Credentials  Connector


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Luminar API Account ID|Please enter valid Luminar API Account ID|True|Password|*****|
|Luminar API Client ID|Please enter valid Luminar API Client ID|True|Password|*****|
|Luminar API Client Secret|Please enter valid Luminar API Client Secret|True|Password|*****|
|Luminar Base URL|Please enter valid Luminar Base URL|True|String|https://demo.cyberluminar.com|
|Proxy Password|Please enter valid proxy server Password|False|Password|*****|
|Proxy Port|Please enter valid Proxy port|False|Int||
|Proxy Server Address|Please enter valid proxy server details|False|String||
|Proxy Username |Please enter valid Proxy Username |False|String||
|Verify SSL |Please select SSL |False|Boolean|false|




