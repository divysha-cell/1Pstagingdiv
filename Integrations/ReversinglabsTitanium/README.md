
# ReversinglabsTitanium

Reversinglabs Titanium - Malware Analysis Solution.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|None|True|String|https://ticloud01.reversinglabs.com|
|Username|None|True|String||
|Password|None|True|Password|*****|


#### Dependencies
| |
|-|
|hashID-3.1.4-py2.py3-none-any.whl|


## Actions
#### Get Malware Details
Query Reversinglabs Titanium for hash information
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"rl": {"malware_presence": {"status": "KNOWN", "scanner_count": 41, "scanner_percent": 0.0, "scanner_match": 0, "query_hash": {"sha1": "81fe8bfe87576c3ecb22426f8e57847382917000"}, "first_seen": "2013-03-17T15:10:55", "threat_level": 0, "trust_factor": 0, "last_seen": "2019-05-18T19:48:34"}}}, "Entity": "81fe8bfe87576c3ecb22426f8e57847382917000"}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds









