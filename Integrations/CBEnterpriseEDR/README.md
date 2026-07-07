
# CBEnterpriseEDR

The VMware Carbon Black Enterprise EDR is an advanced threat hunting and incident response solution delivering continuous visibility for top security operations centers (SOCs) and incident response (IR) teams. Enterprise EDR is delivered through the VMware Carbon Black Cloud, a next-generation endpoint protection platform that consolidates security in the cloud using a single agent, console and dataset.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String||
|Organization Key||True|String||
|API ID||True|Password|*****|
|API Secret Key||True|Password|*****|
|Verify SSL||False|Boolean||


#### Dependencies
| |
|-|
|six-1.17.0-py2.py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|arrow-1.3.0-py3-none-any.whl|
|types_python_dateutil-2.9.0.20260408-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.6.3-py3-none-any.whl|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|


## Actions
#### Enrich Hash
Enrich Siemplify File hash entity based on the information from the VMware Carbon Black Enterprise EDR. Note: Action accepts file hashes only in SHA256 format!
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"original_filename": "java.exe", "charset_id": 1200, "last_seen_device_id": 3350748, "product_version": "8.0.2320.9", "first_seen_device_timestamp": "2020-04-06T14:20:51.537912Z", "last_seen_device_name": "DOMAIN\\TEST", "file_description": "OpenJDK Platform binary", "file_size": 207800, "private_build": null, "first_seen_device_name": "QA\\VM-2K12-HK-010", "md5": "afede6f64ed8878bc0cac57e1831a3bc", "last_seen_device_timestamp": "2020-05-29T22:49:53.706984Z", "num_devices": 3, "first_seen_device_id": 3350748, "copyright": "Copyright \u00c2\u00a9 2019", "file_available": true, "special_build": null, "file_version": "8.0.2320.9", "trademark": null, "product_description": null, "comments": null, "available_file_size": 207800, "lang_id": null, "company_name": "example.com Inc.", "internal_name": "java", "os_type": "WINDOWS", "sha256": "e24dd278cec867486b68418c9066ffa9bd4f394dac3ba94125d58415f677f0f4", "product_name": "OpenJDK Platform 8", "architecture": ["amd64"]}, "Entity": "e24dd278cec867486b68418c9066ffa9bd4f394dac3ba94125d58415f677f0f4"}]
```



#### Process Search
Search information about process activity on the host with CB sensor based on the provided search parameters. The action accepts Host Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|Query to execute in process search. For example, process_name:svchost.exe - to search based by process name, process_hash:9520a99e77d6196d0d09833146424113 - to search based by process hash.|False|String||
|Time Frame|Specify a time frame in hours for which to fetch alerts.|False|String|4|
|Record limit|Specify how many records can be returned by the action.|True|String|20|
|Sort By|Specify a parameter for sorting the data.|False|String||
|Sort Order|Sort order.|False|List|ASC|



##### JSON Results
```json
[{"EntityResult": [{"process_name": "c:\\programfiles(x86)\\microsoft\\edgeupdate\\microsoftedgeupdate.exe", "event_type": "netconn", "parent_guid": "7DESJ9GN-00640ad8-0000034c-00000000-1d9e11032b31276", "device_group_id": 0, "alert_id": ["f1e1fc04-f3bb-f3c5-6b78-db5d02fc1e26"], "legacy": true, "observation_description": "Theapplication\"<share><linkhash=\"bef9dbed290af17cf3f30cc43fc0a94cdadc540f171c25df1363b2e852d0a042\">c:\\programfiles(x86)\\microsoft\\edgeupdate\\microsoftedgeupdate.exe</link></share>\"attemptedtoestablisha<accent>TCP/443</accent>connectionto<share><accent>13.67.191.143</accent></share><accent>:443</accent>(<share><accent>msedge.api.cdp.microsoft.com</accent></share>,locatedinDesMoinesIA,UnitedStates)from<share><accent>172.31.16.82</accent></share><accent>:50445</accent>.Thedevicewasoffthecorporatenetworkusingthepublicaddress<accent>54.197.24.139</accent>(<accent>SSQ-Win-TGT-EP.ec2.internal</accent>,locatedinAshburnVA,UnitedStates).Theoperationwas<accent>blockedbyCarbonBlack</accent>.", "netconn_port": 443, "netconn_protocol": "PROTO_TCP", "ingress_time": 1702031379043, "netconn_location": "DesMoines,Iowa,UnitedStates", "observation_type": "CB_ANALYTICS", "event_description": "Theapplication\"<share><linkhash=\"bef9dbed290af17cf3f30cc43fc0a94cdadc540f171c25df1363b2e852d0a042\">c:\\programfiles(x86)\\microsoft\\edgeupdate\\microsoftedgeupdate.exe</link></share>\"attemptedtoestablisha<accent>TCP/443</accent>connectionto<share><accent>13.67.191.143</accent></share><accent>:443</accent>(<share><accent>msedge.api.cdp.microsoft.com</accent></share>,locatedinDesMoinesIA,UnitedStates)from<share><accent>172.31.16.82</accent></share><accent>:50445</accent>.Thedevicewasoffthecorporatenetworkusingthepublicaddress<accent>54.197.24.139</accent>(<accent>SSQ-Win-TGT-EP.ec2.internal</accent>,locatedinAshburnVA,UnitedStates).Theoperationwas<accent>blockedbyCarbonBlack</accent>.", "parent_pid": 844, "event_id": "a98cc1d495b411ee9a8ac1cbb967113b", "enriched_event_type": ["NETWORK"], "enriched": true, "netconn_local_ipv4": -1407250350, "process_guid": "7DESJ9GN-00640ad8-00001218-00000000-1da29c13e132fd6", "process_pid": [4632], "process_hash": ["8661fbb97161096be503cd295aa46409", "bef9dbed290af17cf3f30cc43fc0a94cdadc540f171c25df1363b2e852d0a042"], "alert_category": ["THREAT"], "device_timestamp": "2023-12-08T10:28:11.064Z", "netconn_ipv4": 222543759, "netconn_inbound": false, "process_username": ["NTAUTHORITY\\SYSTEM"], "device_policy_id": 6525, "device_id": 6556376, "sensor_action": ["BLOCK", "DENY"], "org_id": "7DESJ9GN", "device_name": "ssq-win-tgt-ep", "backend_timestamp": "2023-12-08T10:30:54.961Z", "observation_id": "a98cc1d495b411ee9a8ac1cbb967113b:f1e1fc04-f3bb-f3c5-6b78-db5d02fc1e26"}], "Entity": "SSQ-Win-TGT-EP"}]
```



#### Get Events Associated With Process by Process Guid
Get events associated with specific processes based on the information from the VMware Carbon Black Enterprise EDR. This action can get more detailed results on specific process activity than “Process Search” action. Note for the action to work, Siemplify process artifact passed to action should be a process guid type.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Process GUID|Specify a process guid to search events for.|True|String||
|Search Criteria|Specify a search criteria for the request. Currently, only “event_type” values are accepted as the search criteria, for example, netconn. Multiple values are accepted as a comma separated string.|False|String||
|Query|Query to execute in process search.For example, “netconn_action:ACTION_CONNECTION_CREATE OR netconn_action:ACTION_CONNECTION_ESTABLISHED”|True|String||
|Time Frame|Specify a time frame in hours for which to fetch events.|False|String|4|
|Record limit|Specify how many records can be returned by the action.|True|String|20|
|Sort By|Specify a parameter for sorting the data.|False|String||
|Sort Order|Sort order.|False|List|ASC|



##### JSON Results
```json
[{"EntityResult": [{"event_type": "netconn", "ttp": ["NETWORK_ACCESS"], "netconn_remote_ipv4": -1407222337, "legacy": true, "created_timestamp": "2020-06-03T12:30:13.167Z", "netconn_protocol": "PROTO_UDP", "event_guid": "301y4vXtS2OnGSfgDE4piA", "netconn_domain": "MANTICOREWIN764", "event_description": "The application \"<share><link hash=\"c7db4ae8175c33a47baa3ddfa089fad17bc8e362f21e835d78ab22c9231fe370\">C:\\Windows\\system32\\svchost.exe -k NetworkService</link></share>\" established a <accent>UDP/51888</accent> connection to <share><accent>172.31.125.191</accent></share><accent>:51888</accent> (<share><accent>MANTICOREWIN764</accent></share>) from <share><accent>172.31.126.60</accent></share><accent>:5355</accent>. The device was off the corporate network using the public address <accent>64.69.75.131</accent> (<accent>MANTICOREWIN864.qaam.local</accent>, located in Canada). The operation was successful.", "enriched_event_type": "NETWORK", "enriched": true, "netconn_local_ipv4": -1407222212, "process_guid": "7DESJ9GN-002efb20-000003ec-00000000-1d5fb6d63ba535c", "process_pid": 1004, "netconn_inbound": false, "netconn_remote_port": 51888, "netconn_action": "ACTION_CONNECTION_ESTABLISHED", "event_hash": "7948efa8f7e4f4bfc26d0267f3ea4ba7", "netconn_local_port": 5355, "event_timestamp": "2020-06-03T12:06:38.233Z", "backend_timestamp": "2020-06-03T12:08:22.470Z", "legacy_description": "The application \"<share><link hash=\"c7db4ae8175c33a47baa3ddfa089fad17bc8e362f21e835d78ab22c9231fe370\">C:\\Windows\\system32\\svchost.exe -k NetworkService</link></share>\" established a <accent>UDP/51888</accent> connection to <share><accent>172.31.125.191</accent></share><accent>:51888</accent> (<share><accent>MANTICOREWIN764</accent></share>) from <share><accent>172.31.126.60</accent></share><accent>:5355</accent>. The device was off the corporate network using the public address <accent>64.69.75.131</accent> (<accent>MANTICOREWIN864.qaam.local</accent>, located in Canada). The operation was successful."}], "Entity": "7DESJ9GN-002efb20-000003ec-00000000-1d5fb6d63ba535c"}]
```



#### Ping
Test connectivity to the VMware Carbon Black Enterprise EDR with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









