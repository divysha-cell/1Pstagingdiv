
# Zerofox

ZeroFox is the leading Threat Intelligence and Digital Risk Protection platform, helping you secure your digital world.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Verify SSL|If selected, the integration validates the SSL certificate when connecting to Zerofox. Selected by default.|False|Boolean|true|
|API Root|The API root of the Zerofox instance.|True|String||
|API Token|The Zerofox API token.|True|Password|*****|


#### Dependencies
| |
|-|
|charset_normalizer-3.4.1-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|urllib3-2.3.0-py3-none-any.whl|
|googleapis_common_protos-1.69.2-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|proto_plus-1.26.1-py3-none-any.whl|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|google_api_python_client-2.166.0-py2.py3-none-any.whl|
|cachetools-5.5.2-py3-none-any.whl|
|pycryptodome-3.22.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|idna-3.10-py3-none-any.whl|
|h11-0.14.0-py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|httpcore-1.0.7-py3-none-any.whl|
|protobuf-6.30.2-cp39-abi3-manylinux2014_x86_64.whl|
|google_auth-2.38.0-py2.py3-none-any.whl|
|pyparsing-3.2.3-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|anyio-4.9.0-py3-none-any.whl|
|google_api_core-2.24.2-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|typing_extensions-4.13.0-py3-none-any.whl|
|TIPCommon-2.2.0-py2.py3-none-any.whl|
|certifi-2025.1.31-py3-none-any.whl|


## Actions
#### Request Takedown
Use the Request Takedown action to request takedown in Zerofox.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|ID of the Zerofox Alert.|True|String||



#### Close Alert
Use the Close Alert action to close alert in Zerofox.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|ID of the Zerofox Alert.|True|String||



#### Add Note To Alert
Use the Add Note To Alert action to add a note to alert in Zerofox.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|ID of the Zerofox Alert.|True|String||
|Note|Note for the alert.|True|String||



#### Add Evidence To Alert
Use the Add Evidence To Alert action to add evidence to alert in Zerofox.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|ID of the Zerofox Alert.|True|String||
|Filepath|Absolute file path for the evidence that needs to be submitted to the alert.|True|String||



#### Ping
Use the Ping action to test the connectivity to Zerofox.
Timeout - 600 Seconds









