
# Alexa

The Alexa Web Information Service (AWIS) offers a platform for creating innovative Web solutions and services based on Alexa's vast information about web sites.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Access key id||True|String||
|Secret access key||True|Password|*****|


#### Dependencies
| |
|-|
|defusedxml-0.7.1-py2.py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|idna-3.15-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|certifi-2026.5.20-py3-none-any.whl|
|urllib3-2.7.0-py3-none-any.whl|


## Actions
#### Get URL Rank
Query Alexa for URL rank information
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Rank. e.g. 5|True|String||



##### JSON Results
```json
[{"EntityResult": {"TrafficData": [{"text": "          ", "DataUrl": [{"text": "domain.com", "type": "canonical"}], "Rank": [{"text": "5"}]}], "text": "        ", "Request": [{"text": "          ", "Arguments": [{"text": "            ", "Argument": [{"text": "              ", "Name": [{"text": "url"}], "Value": [{"text": "domain.com"}]}, {"text": "              ", "Name": [{"text": "responsegroup"}], "Value": [{"text": "Rank"}]}]}]}]}, "Entity": "domain.com"}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds









