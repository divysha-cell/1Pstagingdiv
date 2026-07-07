
# AbuseIPDB

Leverage the AbuseIPDB threat intelligence API with this integration.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Key||True|Password|*****|
|Verify SSL||False|Boolean|true|


#### Dependencies
| |
|-|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|urllib3-2.5.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Check IP Reputation
Checks the reputation of all address entities associated with an alert. Includes pre-formatted insight creation. Excludes internal entities by default.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Exclude Internal Addresses|If true, excludes any address entities that you've marked as internal, saving your API allowance on wasted IP checks against your own infrastructure.|False|Boolean|true|
|Suspicious Threshold|An abuse confidence score equal to, or above this threshold will mark the entity as supicious. Set to 0 to disable.|True|String|100|
|Create Insight|Create an insight for each IP|False|Boolean|true|
|Max Age in Days|Max report age to check|True|String|90|



##### JSON Results
```json
[{"Entity": "1.1.1.1", "EntityResult": {"ipAddress": "1.1.1.1", "isPublic": false, "ipVersion": 4, "isWhitelisted": null, "abuseConfidenceScore": 0, "countryCode": null, "usageType": "Reserved", "isp": "Private IP AddressLAN", "domain": null, "hostnames": [], "totalReports": 0, "numDistinctUsers": 0, "lastReportedAt": null}}, {"Entity": "1.1.1.1", "EntityResult": {"ipAddress": "1.1.1.1", "isPublic": true, "ipVersion": 4, "isWhitelisted": false, "abuseConfidenceScore": 0, "countryCode": "US", "usageType": "Data Center/Web Hosting/Transit", "isp": "DigitalOcean LLC", "domain": "digitalocean.com", "hostnames": [], "totalReports": 0, "numDistinctUsers": 0, "lastReportedAt": null}}]
```



#### Ping

Timeout - 600 Seconds



##### JSON Results
```json
{}
```









