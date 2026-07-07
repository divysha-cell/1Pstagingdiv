
# CBLiveResponse

The VMware Carbon Black Endpoint Standard Live Response feature allows security operators to collect information and take action on remote endpoints with Carbon Black agents in real time.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|IP_OR_HOST|https://defense-<environment>.conferdeploy.net/|
|Organization Key||True|String||
|Carbon Black Cloud API ID||True|String||
|Carbon Black Cloud API Secret Key||True|Password|*****|
|Live Response API ID||False|String||
|Live Response API Secret Key||False|Password|*****|
|Use Live Response V6 API||False|Boolean|false|


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
#### Execute File
Execute file on a host running VMware CB Cloud Agent based on the Siemplify Host or IP entity. Note: The File name can be provided either as a Siemplify File entity (artifact) or as an action input parameter. If the File name is passed to action both as an entity and input parameter - action will be executed on the input parameter. File name is case insensitive. File name will be appended to Remote Directory Path to get the resulting file paths that CB Cloud API accepts. File Name also can be specified as a "full path" having both path and a file name, or having file name and file path as separate parameters
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Name|Specify the file name to execute. File name is case insensitive. File Name can be specified as a "full path" having both path and a file name, in that case Remote Directory Path parameter will not be used.|False|String||
|Remote Directory Path|Specify the remote directory path for the file to execute. Example: C:\TMP\|False|String||
|Output Log File on Remote Host|Specify the output log file action should save the redirected output to. Example: C:\TMP\cmdoutput.log|False|String||
|Command Arguments to Pass to File|Specify the command arguments to pass for executing the file. Example, here we specify "/C whoami" to execute whoami command with cmd: C:\Windows\system32\cmd.exe /C whoami|False|String||
|Wait for the Result|If enabled, action will wait for the command to complete.|False|Boolean|false|
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|



##### JSON Results
```json
[{"Entity": "api_v6", "EntityResult": [{"status": "COMPLETE", "values": [], "process_details": {"pid": "xxx", "return_code": 0}, "id": "xx", "name": "create process", "filename": "filename_v6", "result_code": 0, "result_type": "WinHresult", "result_desc": "", "sub_keys": [], "files": [], "input": {"wait": true, "name": "create process", "output_file": "C:\\\\TMP\\\\cmdoutput.log", "object": "C:\\\\Windows\\\\system32\\\\cmd.exe /C whoami"}, "create_time": "2021-08-10T10:03:13Z", "finish_time": "2021-08-10T10:03:14Z", "processes": [], "step": "Command Check", "reason": "Command with id xx ready with no result.", "is_success": false}]}, {"Entity": "api_v3", "EntityResult": [{"obj": {"wait": false, "name": "create process", "output_file": "C://TMP//xxxx.log", "object": "C:\\\\Windows\\\\system32\\\\xxxx.exe /C whoami"}, "id": "xx", "name": "create process", "filename": "filename_v3", "username": null, "creation_time": 1628256284, "completion_time": 1628256284, "result_code": 0, "result_type": "WinHresult", "result_desc": "", "status": "complete", "pid": "40xxx", "return_code": -1, "files": [], "processes": [], "step": "Command Check", "reason": "Command with id xx ready with no result.", "is_success": false}]}]
```



#### List Files in Cloud Storage
List files in the VMware Carbon Black Cloud file storage for an existing live response session based on the Siemplify Host or IP entity.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Rows to Return|Specify how many rows action should return.|False|String|50|
|Start from Row|Specify from which row action should start to return data.|False|String|0|
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|



##### JSON Results
```json
[{"Entity": "CB-xxxx", "EntityResult": [{"id": "64fbbff0-7143-4101-bc1d-xxxxx", "size": 188, "file_name": "file.txt", "size_uploaded": 0, "upload_url": "null", "step": "Get Files from Cloud Storage", "reason": "No files found in Cloud Storage", "is_success": false}]}]
```



#### Delete File
Delete a file from a host running VMware CB Cloud Agent based on the Siemplify Host or IP entity. Note: The File name can be provided either as a Siemplify File entity (artifact) or as an action input parameter. If the File name is passed to action both as an entity and input parameter - action will be executed on the input parameter. File name is case insensitive. File name will be appended to Remote Directory Path to get the resulting file paths that CB Cloud API accepts. File Name also can be specified as a "full path" having both path and a file name, or having file name and file path as separate parameters
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Remote Directory Path|Specify the remote directory path to file to delete. Example: C:\TMP\|False|String||
|File Name|Specify the file name to delete. File name is case insensitive. File Name can be specified as a "full path" having both path and a file name, in that case Remote Directory Path parameter will not be used.|False|String||
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|



##### JSON Results
```json
[{"Entity": "api_v6", "EntityResult": [{"status": "COMPLETE", "values": [], "id": 3, "name": "delete file", "filename": "filename_v6", "result_code": 0, "result_type": "WinHresult", "result_desc": "", "sub_keys": [], "files": [], "input": {"name": "delete file", "object": "file path"}, "create_time": "2021-08-10T06:53:30Z", "finish_time": "2021-08-10T06:53:30Z", "processes": [], "step": "Session Check", "reason": "Max retry for Session Check reached.", "is_success": false}]}, {"Entity": "api_v3", "EntityResult": [{"obj": {"name": "delete file", "object": "file path"}, "id": 4, "name": "delete file", "filename": "filename_v3", "username": "None", "creation_time": 1628578584, "completion_time": 1628578585, "result_code": 0, "result_type": "WinHresult", "result_desc": "", "status": "complete", "files": [], "processes": [], "step": "Session Check", "reason": "Max retry for Session Check reached.", "is_success": false}]}]
```



#### Create Memdump
Create memdump on a host running VMware CB Cloud Agent based on the Siemplify Host or IP entity. Note: The File name for the memdump to create can be provided either as a Siemplify File entity (artifact) or as an action input parameter. If the File name is passed to action both as an entity and input parameter - action will be executed on the input parameter. File name is case insensitive. File name will be appended to Remote Directory Path to get the resulting file paths that CB Cloud API accepts. Additionally, note that VMware CB API does not provide an error message if an unvalid Remote Directory Path is provided for the created memory dump.  File Name also can be specified as a "full path" having both path and a file name, or having file name and file path as separate parameters
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Name|Specify the file name for memdump creation. File name is case insensitive. File Name can be specified as a "full path" having both path and a file name, in that case Remote Directory Path parameter will not be used.|False|String||
|Remote Directory Path|Specify the directory file path to store the memdump. Example: C:\TMP\|False|String||
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|



##### JSON Results
```json
[{"Entity": "api_v3", "EntityResult": [{"compressing": false, "complete": true, "dumping": false, "obj": {"name": "memdump", "object": "C://TMP//file.txt"}, "id": "xx", "name": "memdump", "filepath": "filepath_v3", "username": null, "creation_time": 1628503879, "completion_time": 1628503956369, "result_code": 0, "result_type": "WinHresult", "result_desc": "", "status": "complete", "return_code": 0, "percentdone": 0, "files": [], "processes": [], "step": "Command Check", "reason": "Command with id xx ready with no result.", "is_success": false}]}, {"Entity": "api_v6", "EntityResult": [{"status": "COMPLETE", "values": [], "mem_dump": {"compressing": false, "complete": true, "dumping": false, "return_code": 0, "percentdone": 0}, "id": "xx", "name": "memdump", "filepath": "filepath_v6", "result_code": 0, "result_type": "WinHresult", "result_desc": "", "sub_keys": [], "files": [], "input": {"name": "memdump", "object": "C://TMP//asd1793.txt"}, "create_time": "2021-08-09T09:50:54Z", "finish_time": "+53575-03-13T11:56:26Z", "processes": [], "step": "Command Check", "reason": "Command with id xx ready with no result.", "is_success": false}]}]
```



#### List Files
List files on a host running VMware CB Cloud Agent based on the Siemplify Host or IP entity.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Remote Directory Path|Specify the target directory path action should list. Example: C:\TMP\ or /tmp/|True|String||
|Max Rows to Return|Specify how many rows action should return.|False|String|50|
|Start from Row|Specify from which row action should start to return data.|False|String|0|
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|



##### JSON Results
```json
[{"Entity": "api_v6", "EntityResult": {"status": "COMPLETE", "values": [], "id": "xxxxxx", "name": "directory list", "result_code": 0, "result_type": "WinHresult", "result_desc": "", "sub_keys": [], "files": [{"size": 0, "attributes": ["DIRECTORY"], "filename": "xxxx", "alternate_name": "", "create_time": "2021-06-24T05:50:40Z", "last_access_time": "2021-07-26T17:42:40Z", "last_write_time": "2021-07-23T14:19:32Z"}, {"size": 0, "attributes": ["DIRECTORY"], "filename": "xxxx", "alternate_name": "", "create_time": "2021-06-24T05:50:40Z", "last_access_time": "2021-07-26T17:42:40Z", "last_write_time": "2021-07-23T14:19:32Z"}, {"size": 767, "attributes": ["ARCHIVE"], "filename": "xxxxxxx", "alternate_name": "IMAGE(~1.PNG", "create_time": "2021-07-23T12:26:59Z", "last_access_time": "2021-07-23T12:26:59Z", "last_write_time": "2021-07-23T12:26:59Z"}, {"size": 61186, "attributes": ["ARCHIVE"], "filename": "xxxxxxxx", "alternate_name": "", "create_time": "2021-07-23T13:13:39Z", "last_access_time": "2021-07-23T13:13:39Z", "last_write_time": "2021-07-23T13:13:39Z"}, {"size": 19190, "attributes": ["ARCHIVE"], "filename": "xxxxxxx", "alternate_name": "", "create_time": "2021-07-23T13:20:13Z", "last_access_time": "2021-07-23T13:20:13Z", "last_write_time": "2021-07-23T13:20:13Z"}, {"size": 94025, "attributes": ["ARCHIVE"], "filename": "xxxxxxx", "alternate_name": "", "create_time": "2021-07-23T13:31:29Z", "last_access_time": "2021-07-23T13:31:29Z", "last_write_time": "2021-07-23T13:31:29Z"}, {"size": 99251, "attributes": ["ARCHIVE"], "filename": "xxxxxx", "alternate_name": "", "create_time": "2021-07-23T14:19:32Z", "last_access_time": "2021-07-23T14:19:32Z", "last_write_time": "2021-07-23T14:19:32Z"}, {"size": 133082, "attributes": ["ARCHIVE"], "filename": "xxxxxxx", "alternate_name": "VANUHI~1.PNG", "create_time": "2021-07-23T13:01:48Z", "last_access_time": "2021-07-23T13:01:48Z", "last_write_time": "2021-07-23T13:01:48Z"}], "input": {"name": "directory list", "object": "folder name"}, "create_time": "2021-07-26T17:55:16Z", "finish_time": "2021-07-26T17:55:17Z", "is_success": false, "step": "Get Device", "reason": "Unable to get device for CB-xxxxx. Error is No devices found for entity CB-xxxxx. Skipping."}}, {"Entity": "api_v3", "EntityResult": {"obj": {"name": "directory list", "object": "C:\\\\TMP\\\\"}, "id": "xx", "name": "directory list", "username": null, "creation_time": 1628598855, "completion_time": 1628598855, "result_code": 0, "result_type": "WinHresult", "result_desc": "", "status": "complete", "files": [{"size": 21, "attributes": ["ARCHIVE"], "create_time": 1628578270, "last_access_time": 1628589793, "last_write_time": 1628589793, "filename": "cmdoutput.log", "alternate_name": "CMDOUT~1.LOG"}, {"size": 21, "attributes": ["ARCHIVE"], "create_time": 1628582293, "last_access_time": 1628582293, "last_write_time": 1628582293, "filename": "cmdoutput1.log", "alternate_name": "CMDOUT~2.LOG"}, {"size": 10, "attributes": ["ARCHIVE"], "create_time": 1628529239, "last_access_time": 1628529239, "last_write_time": 1628529239, "filename": "txt.txt", "alternate_name": ""}, {"size": 953860096, "attributes": ["ARCHIVE"], "create_time": 1628527762, "last_access_time": 1628527893, "last_write_time": 1628527893, "filename": "file.txt", "alternate_name": ""}, {"size": 14, "attributes": ["ARCHIVE"], "create_time": 1627623623, "last_access_time": 1627623623, "last_write_time": 1627623623, "filename": "kughb", "alternate_name": ""}, {"size": 228723, "attributes": ["ARCHIVE"], "create_time": 1627045764, "last_access_time": 1627045764, "last_write_time": 1627045764, "filename": "test.png", "alternate_name": "test.PNG"}], "step": "Get Device", "reason": "Unable to get device for CB-xxxxx. Error is No devices found for entity CB-xxxxx. Skipping."}}]
```



#### Put File
Put a file on a host running VMware CB Cloud Agent based on the Siemplify Host or IP entity. Note: The File name can be provided either as a Siemplify File entity (artifact) or as an action input parameter. If the File name is passed to action both as an entity and input parameter - action will be executed on the input parameter. File name is case insensitive. File name will be appended to both Source Directory Path and Destination Directory Path to get the resulting file paths that CB Cloud API accepts. File Name also can be specified as a "full path" having both path and a file name, or having file name and file path as separate parameters
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Name|Specify the file name to upload. File name is case insensitive. File Name can be specified as a "full path" having both path and a file name, in that case Source Directory Path parameter will not be used.|False|String||
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|
|Source Directory Path|Specify the source directory path action should take to get the file to upload. Example: /tmp/|False|String||
|Destination Directory Path|Specify the target directory path action should upload the file to. Example: C:\TMP\|True|String||



##### JSON Results
```json
[{"Entity": "api_v3", "EntityResult": [{"obj": {"file_id": "file id", "name": "put file", "object": "file path", "chunkNumber": 0}, "id": 23, "name": "put file", "filename": "filename_v3", "absolute_file_path": "filepath_v3", "username": "None", "creation_time": 1628580883, "completion_time": 1628580883, "result_code": 0, "result_type": "WinHresult", "result_desc": "", "status": "complete", "file_id": "file id", "files": [], "processes": [], "step": "Session Check", "reason": "Max retry for Session Check reached.", "is_success": false}]}, {"Entity": "api_v6", "EntityResult": [{"status": "COMPLETE", "values": [], "id": 33, "name": "put file", "result_code": 0, "result_type": "WinHresult", "result_desc": "", "sub_keys": [], "files": [], "input": {"chunkNumber": 0, "file_id": "file id", "name": "put file", "object": "file path"}, "create_time": "2021-08-10T07:49:04Z", "filename": "filename_v6", "absolute_file_path": "filepath_v6", "finish_time": "2021-08-10T07:49:04Z", "processes": [], "step": "Session Check", "reason": "Max retry for Session Check reached.", "is_success": false}]}]
```



#### Kill Process
Kill process on a host based on the Siemplify Host or IP entity. Note: The Process name can be provided either as a Siemplify entity (artifact) or as an action input parameter. If the Process name is passed to action both as an entity (process) and input parameter - action will be executed on the input parameter.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Process Name|Process name to search PID for.|False|String||
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|



##### JSON Results
```json
[{"Entity": "api_v6", "EntityResult": {"status": "COMPLETE", "values": [], "id": 47, "name": "kill", "result_code": 0, "result_type": "WinHresult", "result_desc": "", "sub_keys": [], "files": [], "input": {"name": "kill", "object": 2636}, "create_time": "2021-08-03T10:01:05Z", "finish_time": "2021-08-03T10:01:05Z", "processes": [], "is_success": false, "step": "Get Device", "reason": "Unable to get device for WWW.IRCNET.ORG. Error is No devices found for entity WWW.IXXXXT.ORG. Skipping."}}, {"Entity": "api_v3", "EntityResult": {"obj": {"name": "kill", "object": 940}, "id": 25, "name": "kill", "username": null, "creation_time": 1628600079, "completion_time": 1628600079, "result_code": 0, "result_type": "WinHresult", "result_desc": "", "status": "complete", "is_success": false, "step": "Get Device", "reason": "Unable to get device for WWW.IRCNET.ORG. Error is No devices found for entity WWW.IXXXXT.ORG. Skipping."}}]
```



#### Download File
Download a file from a host running VMware CB Cloud Agent based on the Siemplify Host or IP entity. Note: The File name can be provided either as a Siemplify File entity (artifact) or as an action input parameter. If the File name is passed to action both as an entity and input parameter - action will be executed on the input parameter. File name is case insensitive. File name will be appended to both Local Directory Path and Remote Directory Path to get the resulting file paths that CB Cloud API accepts. If action is executed against multiple Host or IP entities, to not overwrite the file downloaded from multiple entities, the downloaded file name is appended with Hostname or IP address, example format: hostname_filename. File Name also can be specified as a "full path" having both path and a file name, or having file name and file path as separate parameters
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Name|Specify the file name to download. File name is case insensitive. File Name can be specified as a "full path" having both path and a file name, in that case Remote Directory Path parameter will not be used.|False|String||
|Remote Directory Path|Specify the remote directory path action should take to download the file. Example: C:\TMP\|False|String||
|Local Directory Path|Specify the local directory path action should save the file to. Example: /tmp/|True|String||
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|



##### JSON Results
```json
[{"Entity": "api_v3", "EntityResult": [{"obj": {"name": "get file", "object": "C:\\\\TMP\\\\/file.txt"}, "id": "xxx", "name": "get file", "username": null, "creation_time": 1628600630, "completion_time": 1628600631, "result_code": 0, "result_type": "WinHresult", "result_desc": "", "status": "complete", "file_id": "ea36c75c-c0e1-4551-89e5-xxxxx", "offset": 0, "count": 0, "files": [], "processes": [], "step": "Session Check", "reason": "Max retry for Session Check reached.", "is_success": false, "absolute_file_path": "filepath_v3"}]}, {"Entity": "api_v6", "EntityResult": [{"file": "test.txt", "status": "COMPLETE", "values": [], "file_details": {"offset": 0, "count": 0, "file_id": "ca0b62cc-0445-4dce-b4b1-xxxxxxx"}, "id": "xxxxx", "name": "get file", "result_code": 0, "result_type": "WinHresult", "result_desc": "", "sub_keys": [], "files": [], "input": {"name": "get file", "object": "C:\\\\TMP\\\\/file.txt"}, "create_time": "2021-08-03T11:37:23Z", "finish_time": "2021-08-03T11:37:24Z", "processes": [], "step": "Session Check", "reason": "Max retry for Session Check reached.", "is_success": false, "absolute_file_path": "filepath_v6"}]}]
```



#### List Processes
List processes running on endpoint based on the provided Siemplify Host or IP entity.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Process Name|Process name to search for on the host.|False|String||
|How Many Records To Return|How many records per entity action should return.|False|String|25|
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|



##### JSON Results
```json
[{"Entity": "PC-01", "EntityResult": [{"pid": 672, "create_time": 132463818959144, "path": "c:\\windows\\system32\\test.exe", "command_line": "C:\\Windows\\system32\\test.exe", "sid": "S-1-5-18", "username": "NT AUTHORITY\\SYSTEM", "parent": 536, "parent_create_time": 132463818958027601, "is_success": false, "step": "Get Device", "reason": "Unable to get device for PC-01. Error is No devices found for entity PC-01. Skipping."}]}]
```



#### Delete File from Cloud Storage
Delete a file from the VMware Carbon Black Cloud file storage for an existing live response session based on the Siemplify Host or IP entity. Note: This action is not supported in Carbon Black Live Response API v3, API v6 should be used to run this action. The File name can be provided either as a Siemplify File entity (artifact) or as an action input parameter. If the File name is passed to action both as an entity and input parameter - action will be executed on the input parameter. File name is case insensitive.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Name|Specify the file name to delete. File name is case insensitive.|False|String||
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|



##### JSON Results
```json
[{"Entity": "CB-xxxx", "EntityResult": [{"file_name": "file.txt", "step": "Delete Files from Cloud Storage", "reason": "No files with file name file.txt found in Cloud Storage for session 1111:111111", "is_success": false}]}]
```



#### Ping
Test connectivity to the VMware Carbon Black Endpoint Standard Live Response with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









