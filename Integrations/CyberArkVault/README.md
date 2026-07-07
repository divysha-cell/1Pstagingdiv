
# CyberArkVault

Secure, Rotate and Control Access to Privileged Account Credentials

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root||True|String|https://{Base URL}:{Port}|
|Password Vault Api Root||True|String|https://{Base URL}:{Port}|
|Username||True|String||
|Password||True|Password|*****|
|Application ID||True|String||
|Use SSL||False|Boolean||


#### Dependencies
| |
|-|
|certifi-2026.4.22-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|idna-3.15-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|urllib3-2.7.0-py3-none-any.whl|


## Actions
#### Disable User
Update user attribute - disable user
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User Name|Full user name as exist in the CyberArkVault|True|String|None|



#### Enable User
Update user attribute - enable user
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User Name|Full user name as exist in the CyberArkVault|True|String|None|



#### Get Group Details
Get group details
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Group Name|Full group name as exist in the CyberArkVault|True|String|None|



#### Get User Details
Get user details
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User Name|Full user name as exist in the CyberArkVault|True|String|None|



#### Ping
Test Connectivity
Timeout - 600 Seconds









