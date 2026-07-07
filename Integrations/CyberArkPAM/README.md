
# CyberArkPAM

CyberArk's Privileged Access Manager is a full life-cycle solution for managing the most privileged accounts and SSH Keys in the enterprise. It enables organizations to secure, provision, manage, control and monitor all activities associated with all types of privileged identities.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|Specify the API root url.|True|String|https://x.x.x.x:port|
|Username|Specify the username to use to connect with.|True|String||
|Password|Specify the password to use to connect with.|True|Password|*****|
|Verify SSL|If enabled, the certificate configured for the API root is validated.|False|Boolean|false|
|CA Certificate|Specify the CA certificate to use to validate the secure connection to the API root. Parameter accepts the CA certificate in a form of base64 encoded string.|False|String||
|Client Certificate|Optional if configured for CyberArk PAM, specify the CyberArk client certificate to use to establish connection to the API root. Certificate should be provided in the .p12 format, parameter expects certificate as base64 encoded string.|False|String||
|Client Certificate Passphrase|Optionally, if the client certificate is requiring a passphrase, specify it for this parameter.|False|Password|*****|


#### Dependencies
| |
|-|
|idna-3.7-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|cffi-1.16.0-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|certifi-2024.7.4-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|requests_toolbelt-1.0.0-py2.py3-none-any.whl|
|pycparser-2.22-py3-none-any.whl|
|cryptography-43.0.0-cp39-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|chardet-5.2.0-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|pyOpenSSL-24.2.1-py3-none-any.whl|


## Actions
#### List Accounts
List accounts available in the CyberArk PAM based on provided criteria. Note: This action doesn’t run on Chronicle SOAR entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Search Query|Specify the search query to use in action.|False|String||
|Search operator|Specify the search operator action should use to search based on the provided search query.|False|List|contains|
|Max Records To Return|Specify how many records to return. If nothing is provided, action will return 50 records (API default).|False|String|50|
|Records Offset|Specify the offset the action should use to return the values.|False|String|0|
|Filter Query|Specify the filter query action should use. Filter can be based on safeName or modificationTime parameters.|False|String||
|Saved Filter|Specify the saved filter query action should use. Takes priority over the Filter Query parameter.|False|String||



##### JSON Results
```json
[{"categoryModificationTime": "1667915248", "platformId": "", "safeName": "XXXXX", "id": "12_23", "name": "xxxx", "userName": "xxxx", "secretType": "password", "secretManagement_automaticManagementEnabled": "True", "secretManagement_lastModifiedTime": "1667918145", "createdTime": "1667915248"}]
```



#### Get Account Password Value
Get account password value from CyberArk PAM. Note: Both password and SSH Key can be retrieved with this action.  Note 2: This action doesn’t run on Chronicle SOAR entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Account|Specify the account id to retrieve the password value for. Note that you can get the account id from the List Accounts action.|True|String||
|Reason|Specify the reason that account password value is accessed.|True|String|Retrieved automatically by Chronicle SOAR.|
|Ticketing System Name|Specify the name of the ticketing system.|False|String||
|Ticket ID|Specify the ticketing system ticket id.|False|String||
|Version|Specify the account password value version to retrieve.|False|String||



##### JSON Results
```json
{"content": "\"XXXX\""}
```



#### Ping
Test connectivity to the CyberArk PAM installation with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









