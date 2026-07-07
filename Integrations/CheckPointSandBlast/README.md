
# CheckPointSandBlast

Protect your organization from zero-day cyber attacks with SandBlast Network, the marketâ€™s leading advanced network threat prevention solution. Increase productivity while creating a secure environment with innovative technologies like threat emulation, threat extraction and artificial intelligence.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https://<service_address>/tecloud/api/<version>/file|
|API Key||True|Password|*****|
|Verify SSL||False|Boolean||


#### Dependencies
| |
|-|
|certifi-2026.4.22-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.6.3-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|


## Actions
#### Query
Get threat reputation information about FILEHASH entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Mark entity as suspicious if severity is equal or above the given threshold.|True|String|0|



##### JSON Results
```json
[{"Entity": "8a2f57269b2f47b4e8f2e122e424754b", "EntityResult": {"status": {"code": 1006, "label": "PARTIALLY_FOUND", "message": "The request cannot be fully answered at this time."}, "md5": "8a2f57269b2f47b4e8f2e122e424754b", "file_type": "", "file_name": "untitled.doc", "features": ["te", "av"], "te": {"trust": 0, "images": [{"report": {"verdict": "unknown"}, "status": "not_found", "id": "e50e99f3-5963-4573-af9e-e3f4750b55e2", "revision": 1}, {"report": {"verdict": "unknown"}, "status": "not_found", "id": "5e5de275-a103-4f67-b55b-47532918fa59", "revision": 1}], "score": -2147483648, "status": {"code": 1004, "label": "NOT_FOUND", "message": "Could not find the requested file. Please upload it."}}, "av": {"malware_info": {"signature_name": "", "malware_family": 0, "malware_type": 0, "severity": 0, "confidence": 0}, "status": {"code": 1001, "label": "FOUND", "message": "The request has been fully answered."}}}}]
```



#### Upload File
Upload files for analysis
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Path|The full path of the file to upload. For multiple, use comma separated values.|True|String||
|Enable Threat Emulation feature|If enabled, threat emulation feature will be enabled for the upload. By default, if no features are selected, threat emulation will be used.|False|Boolean||
|Enable AntiVirus feature|If enabled, antivirus feature will be enabled for the upload. By default, if no features are selected, threat emulation will be used.|False|Boolean||
|Enable Threat Extraction feature|If enabled, threat extraction feature will be enabled for the upload. By default, if no features are selected, threat emulation will be used.|False|Boolean||



##### JSON Results
```json
[{"Entity": "/tmp/test.txt", "EntityResult": {"status": {"code": 1002, "label": "UPLOAD_SUCCESS", "message": "The file was uploaded successfully."}, "sha1": "6caf005c3183d9b5b8dfa5b60f24eb1ebbfab876", "md5": "c12c504bbe0f7be6ca87d4933c43fac1", "sha256": "e757f729d149e047705ad6adfbcdd28b0ad28899385712ee0a58261bcb03ac36", "file_type": "", "file_name": "2020092414.log", "features": ["te"], "te": {"trust": 0, "images": [{"report": {"verdict": "unknown"}, "status": "not_found", "id": "e50e99f3-5963-4573-af9e-e3f4750b55e2", "revision": 1}, {"report": {"verdict": "unknown"}, "status": "not_found", "id": "5e5de275-a103-4f67-b55b-47532918fa59", "revision": 1}], "score": -2147483648, "status": {"code": 1002, "label": "UPLOAD_SUCCESS", "message": "The file was uploaded successfully."}}}}]
```



#### Ping
Test connectivity to the Check Point SandBlast with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









