
# SymantecBlueCoatProxySG

Symantec delivers its high-performance, proxy-based, Edge Secure Web Gateway (SWG) solution where you need it: on high-performance hardware, as a virtual appliance, or in your private cloud infrastructure. Symantec's industry-leading proxy protects organizations across the web, social media, applications, and mobile networks

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|SSH Root|SSH root of the Blue Coat ProxySG instance.|True|String|{ip address}:22|
|Username|Username of the Blue Coat ProxySG SSH account.|True|String||
|Password|Password of the Blue Coat ProxySG account.|True|Password|*****|


#### Dependencies
| |
|-|
|paramiko-3.1.0-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|cryptography-47.0.0-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|pycparser-3.0-py3-none-any.whl|
|bcrypt-5.0.0-cp39-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.6.3-py3-none-any.whl|
|TIPCommon-1.0.11.1-py2.py3-none-any.whl|
|requests-2.33.1-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|pynacl-1.6.2-cp38-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|


## Actions
#### Block Entities
Block entities using Symantec Blue Coat ProxySG. Supported entities: IP Address.
Timeout - 600 Seconds



##### JSON Results
```json
[{"Entity": "172.30.xxx.xxx", "EntityResult": {"raw_output": "block 172.30.xxx.xxx   ok 172.30.xxx.xxx - Blue Coat SG-VA Series#(config client)", "status": "success"}}, {"Entity": "1.1.x.x", "EntityResult": {"raw_output": "block 1.1.x.x   ok 172.30.xxx.xxx - Blue Coat SG-VA Series#(config client)", "status": "success"}}, {"Entity": "test", "EntityResult": {"raw_output": "block test % test: invalid address 172.30.xxx.xxx - Blue Coat SG-VA Series#(config client)", "status": "failure"}}]
```



#### Enrich Entities
Enrich entities using information from Symantec Blue Coat ProxySG. Supported entities: Hostname, IP Address, URL.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Create Insight|If enabled, action will create an insight containing all of the retrieved information about the entity.|False|Boolean|true|



##### JSON Results
```json
[{"Entity": "172.30.xxx.xx", "EntityResult": {"raw_output": "172.30.xxx.xxx - Blue Coat SG-VA Series>test geolocation...", "Country": "Ambiguous - Special Use"}}, {"Entity": "https://google.com", "EntityResult": {"raw_output": "172.30.xxx.xxx - Blue Coat SG-VA Series>test threat-risk...", "risk level": "1", "% categories": {"Policy": "none", "IWF": "none", "Proventia": "unavailable", "Blue Coat": "Search Engines/Portals", "Local": "test"}, "category groups": {"Blue Coat": "Business Related; Information Related"}}}, {"Entity": "twitter.com", "EntityResult": {"raw_output": "172.30.xxx.xxx - Blue Coat SG-VA Series>test dns twitter.com...", "DNS Response data": "", "Official Host Name": "twitter.com", "Resolved Addresses": ["104.244.xx.xx", "104.244.xx.xx"], "Cache TTL": "971, cache MISS", "DNS Resolver Response": "Success"}}]
```



#### Ping
Test connectivity to the Symantec Blue Coat ProxySG with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









