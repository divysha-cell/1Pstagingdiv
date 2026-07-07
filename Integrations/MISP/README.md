
# MISP

MISP is an open source software solution for collecting, storing, distributing and sharing cyber security indicators and threat about cyber security incidents

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root||True|String|https://{IP}|
|Api Key||True|Password|*****|
|Use SSL||False|Boolean|False|
|CA Certificate File - parsed into Base64 String||False|String||


#### Dependencies
| |
|-|
|six-1.17.0-py2.py3-none-any.whl|
|typing_extensions-4.15.0-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|pyasn1-0.6.3-py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|pycparser-3.0-py3-none-any.whl|
|TIPCommon-2.3.9-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|anyio-4.13.0-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|tzdata-2026.2-py2.py3-none-any.whl|
|requests_file-3.0.1-py2.py3-none-any.whl|
|google_auth_httplib2-0.3.0-py3-none-any.whl|
|pyopenssl-25.3.0-py3-none-any.whl|
|google_api_core-2.30.3-py3-none-any.whl|
|idna-3.15-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|httplib2-0.31.2-py3-none-any.whl|
|requests_toolbelt-1.0.0-py2.py3-none-any.whl|
|tldextract-5.1.2-py3-none-any.whl|
|google_auth-2.47.0-py3-none-any.whl|
|protobuf-7.35.0-py3-none-any.whl|
|filelock-3.29.0-py3-none-any.whl|
|googleapis_common_protos-1.75.0-py3-none-any.whl|
|urllib3-2.7.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|cryptography-46.0.7-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|proto_plus-1.28.0-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|arrow-1.4.0-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|google_api_python_client-2.188.0-py3-none-any.whl|


## Actions
#### Create IP-Port Misp Object
Create a IP-Port Object in MISP. Requires one of: Dst-port, Src-port, Domain, HOSTNAME, IP-Src, IP-Dst to be provided or “Use Entities“ parameter set to true.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event ID|Specify the ID or UUID of the event to which you want to add IP-Port objects.|True|String||
|Dst-port|Specify the destination port, which you want to add to the event.|False|String||
|Src-port|Specify the source port, which you want to add to the event.|False|String||
|Domain|Specify the domain, which you want to add to the event.|False|String||
|HOSTNAME|Specify the hostname, which you want to add to the event.|False|String||
|IP-Src|Specify the source IP, which you want to add to the event.|False|String||
|IP-Dst|Specify the destination IP, which you want to add to the event.|False|String||
|Use Entities|If enabled, action will use entities in order to create objects. Supported entities: IP Address. “Use Entities“ has priority over other parameters.|False|Boolean|false|
|IP Type|Specify what attribute type should be used with IP entities.|False|List|Source IP|



##### JSON Results
```json
{"Object": {"id": "7xx", "name": "url", "meta-category": "network", "description": "url object describes an url along with its normalized field (like extracted using faup parsing library) and its metadata.", "template_uuid": "60efb77b-40b5-4c46-871b-ed1ed999fce5", "template_version": "8", "event_id": "1", "uuid": "751de0b1-df9a-4154-81fc-bbc0591a1a57", "timestamp": "1595935488", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "first_seen": null, "last_seen": null, "Attribute": [{"id": "2xx", "event_id": "1xx", "object_id": "7xx", "object_relation": "url", "category": "Network activity", "type": "url", "value1": "www.domain.cxx", "value2": "", "to_ids": false, "uuid": "c9bd6348-548e-4dfb-b5f8-xxxxxx", "timestamp": "1595935488", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "www.domain.com"}, {"id": "2xx", "event_id": "1xx", "object_id": "7xx", "object_relation": "port", "category": "Network activity", "type": "port", "value1": "3xx", "value2": "", "to_ids": false, "uuid": "01e9367e-ae63-49d4-ba8f-xxxxxx", "timestamp": "1595935488", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "3xx"}, {"id": "2xx", "event_id": "1xx", "object_id": "7xx", "object_relation": "ip", "category": "Network activity", "type": "ip-dst", "value1": "1.1.1.xx", "value2": "", "to_ids": false, "uuid": "291d75d4-4bda-49ff-8823-xxxxxx", "timestamp": "1595935488", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "1.1.1.xx"}, {"id": "2xx", "event_id": "1xx", "object_id": "7xx", "object_relation": "text", "category": "Other", "type": "text", "value1": "Test", "value2": "", "to_ids": false, "uuid": "177322b9-eda1-462c-9b95-xxxxxx", "timestamp": "1595935488", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "Test"}]}}
```



#### Get Event Details
Retrieve details about events in MISP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event ID|Specify a comma-separated list of IDs or UUIDs of the events for which you want retrieve details.|True|String||
|Return Attributes Info|If enabled, action will create a case wall table for all of the attributes that are a part of the event.|False|Boolean|True|



##### JSON Results
```json
[{"Entity": "2", "EntityResult": {"id": "2", "orgc_id": "1", "org_id": "1", "date": "2020-07-29", "threat_level_id": "4", "info": "EventSiemplify", "published": false, "uuid": "0039bd4c-2869-4123-8f47-39ebdf61a2cb", "attribute_count": "43", "analysis": "0", "timestamp": "1601381871", "distribution": "1", "proposal_email_lock": false, "locked": false, "publish_timestamp": "1596533581", "sharing_group_id": "0", "disable_correlation": false, "extends_uuid": "", "event_creator_email": "admin@admin.test", "Org": {"id": "1", "name": "ORGNAME", "uuid": "09b0dde1-2934-4310-a107-74b6f534f041", "local": true}, "Orgc": {"id": "1", "name": "ORGNAME", "uuid": "09b0dde1-2934-4310-a107-74b6f534f041", "local": true}, "Attribute": [{"id": "176", "type": "md5", "category": "Payload delivery", "to_ids": false, "uuid": "cf3146de-b459-4e29-9484-7a3e6e99079c", "event_id": "2", "distribution": "5", "timestamp": "1601379800", "comment": "Test Comment 4", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "0", "object_relation": null, "first_seen": null, "last_seen": null, "value": "44d88612fea8a8f36de82e1278abb02f", "Galaxy": [], "ShadowAttribute": []}, {"id": "177", "type": "md5", "category": "Artifacts dropped", "to_ids": false, "uuid": "68cdc07e-2704-4e7c-954c-b159c8a9989d", "event_id": "2", "distribution": "5", "timestamp": "1601380041", "comment": "Test Comment 5", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "0", "object_relation": null, "first_seen": null, "last_seen": null, "value": "44d88612fea8a8f36de82e1278abb02f", "Galaxy": [], "ShadowAttribute": []}, {"id": "178", "type": "text", "category": "Internal reference", "to_ids": false, "uuid": "92ddb824-e34e-47bc-a466-ae9ed4137fd2", "event_id": "2", "distribution": "0", "timestamp": "1601381228", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "0", "object_relation": null, "first_seen": null, "last_seen": null, "value": "HOST-01", "Galaxy": [], "ShadowAttribute": []}, {"id": "179", "type": "comment", "category": "Other", "to_ids": false, "uuid": "78821299-8126-4685-9bf3-fc7b9e0c4a80", "event_id": "2", "distribution": "0", "timestamp": "1601381793", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "0", "object_relation": null, "first_seen": null, "last_seen": null, "value": "host-01", "Galaxy": [], "ShadowAttribute": []}, {"id": "180", "type": "hostname", "category": "Network activity", "to_ids": false, "uuid": "b3c0a4b7-8d39-410e-91fc-1cb7acffb2b6", "event_id": "2", "distribution": "5", "timestamp": "1601381871", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "0", "object_relation": null, "first_seen": null, "last_seen": null, "value": "host01.com", "Galaxy": [], "ShadowAttribute": []}], "ShadowAttribute": [], "RelatedEvent": [{"Event": {"id": "11", "date": "2020-09-25", "threat_level_id": "2", "info": "TestEvent", "published": false, "uuid": "502c843e-f5a4-46e6-8c2d-bf673a5dbb8b", "analysis": "0", "timestamp": "1601379586", "distribution": "1", "org_id": "1", "orgc_id": "1", "Org": {"id": "1", "name": "ORGNAME", "uuid": "09b0dde1-2934-4310-a107-74b6f534f041"}, "Orgc": {"id": "1", "name": "ORGNAME", "uuid": "09b0dde1-2934-4310-a107-74b6f534f041"}}}, {"Event": {"id": "4", "date": "2020-08-04", "threat_level_id": "4", "info": "PlaybookEvent", "published": false, "uuid": "6776f2de-14d1-4437-8425-1d44b32ba3f5", "analysis": "0", "timestamp": "1601378210", "distribution": "1", "org_id": "1", "orgc_id": "1", "Org": {"id": "1", "name": "ORGNAME", "uuid": "09b0dde1-2934-4310-a107-74b6f534f041"}, "Orgc": {"id": "1", "name": "ORGNAME", "uuid": "09b0dde1-2934-4310-a107-74b6f534f041"}}}], "Galaxy": [], "Object": [{"id": "29", "name": "ip-port", "meta-category": "network", "description": "An IP address (or domain or hostname) and a port seen as a tuple (or as a triple) in a specific time frame.", "template_uuid": "9f8cea74-16fe-4968-a2b4-026676949ac6", "template_version": "8", "event_id": "2", "uuid": "4452bdea-1e46-422d-839e-9f6047825f33", "timestamp": "1599456087", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "first_seen": null, "last_seen": null, "ObjectReference": [], "Attribute": [{"id": "108", "type": "port", "category": "Network activity", "to_ids": false, "uuid": "09c05001-1618-40b6-9199-d18a0a01cee4", "event_id": "2", "distribution": "5", "timestamp": "1596201964", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "29", "object_relation": "dst-port", "first_seen": null, "last_seen": null, "value": "80", "Galaxy": [], "ShadowAttribute": [], "Sighting": [{"id": "1", "attribute_id": "108", "event_id": "2", "org_id": "1", "date_sighting": "1596192047", "uuid": "71fa65a5-2a7c-496f-8740-cd192eed1094", "source": "", "type": "0", "Organisation": {"id": "1", "uuid": "09b0dde1-2934-4310-a107-74b6f534f041", "name": "ORGNAME"}, "attribute_uuid": "09c05001-1618-40b6-9199-d18a0a01cee4"}]}, {"id": "109", "type": "port", "category": "Network activity", "to_ids": false, "uuid": "a242e066-3513-4883-8dfd-ecbbdbdc805b", "event_id": "2", "distribution": "5", "timestamp": "1596180025", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "29", "object_relation": "src-port", "first_seen": null, "last_seen": null, "value": "22", "Galaxy": [], "ShadowAttribute": []}, {"id": "111", "type": "ip-src", "category": "Network activity", "to_ids": false, "uuid": "82bf1db6-dde9-4565-b97e-7218692d775d", "event_id": "2", "distribution": "5", "timestamp": "1599456087", "comment": "Comment 2020-09-07", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "29", "object_relation": "ip-src", "first_seen": null, "last_seen": null, "value": "192.168.1.13", "Galaxy": [], "ShadowAttribute": [], "Tag": [{"id": "1", "name": "MarkoTest", "colour": "#b81d1d", "exportable": true, "user_id": "0", "hide_tag": false, "numerical_value": null, "local": 0}]}, {"id": "112", "type": "ip-dst", "category": "Network activity", "to_ids": false, "uuid": "1a95c4d3-5581-4fbd-b4fb-2d0ff6e1334f", "event_id": "2", "distribution": "5", "timestamp": "1596187642", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "29", "object_relation": "ip-dst", "first_seen": null, "last_seen": null, "value": "192.168.1.31", "Galaxy": [], "ShadowAttribute": [], "Tag": [{"id": "1", "name": "MarkoTest", "colour": "#b81d1d", "exportable": true, "user_id": "0", "hide_tag": false, "numerical_value": null, "local": 0}]}]}, {"id": "30", "name": "ip-port", "meta-category": "network", "description": "An IP address (or domain or hostname) and a port seen as a tuple (or as a triple) in a specific time frame.", "template_uuid": "9f8cea74-16fe-4968-a2b4-026676949ac6", "template_version": "8", "event_id": "2", "uuid": "604ea442-0a89-49d0-a63a-bdf003ac2739", "timestamp": "1599456099", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "first_seen": null, "last_seen": null, "ObjectReference": [], "Attribute": [{"id": "113", "type": "port", "category": "Network activity", "to_ids": false, "uuid": "cb759022-dc6b-41f5-a310-44a1d5d3e459", "event_id": "2", "distribution": "5", "timestamp": "1596182567", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "30", "object_relation": "dst-port", "first_seen": null, "last_seen": null, "value": "80", "Galaxy": [], "ShadowAttribute": []}, {"id": "114", "type": "port", "category": "Network activity", "to_ids": false, "uuid": "f4d0db8b-63fa-4bdf-ba66-c449d0f1a12c", "event_id": "2", "distribution": "5", "timestamp": "1596182567", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "30", "object_relation": "src-port", "first_seen": null, "last_seen": null, "value": "22", "Galaxy": [], "ShadowAttribute": []}, {"id": "115", "type": "domain", "category": "Network activity", "to_ids": false, "uuid": "319412db-70c0-4325-896e-120210cfbfe2", "event_id": "2", "distribution": "5", "timestamp": "1596182567", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "30", "object_relation": "domain", "first_seen": null, "last_seen": null, "value": "example.com", "Galaxy": [], "ShadowAttribute": []}, {"id": "116", "type": "ip-src", "category": "Network activity", "to_ids": false, "uuid": "ad119b31-d767-4f84-b3e4-0082cb126808", "event_id": "2", "distribution": "5", "timestamp": "1599456099", "comment": "Comment 2020-07-31", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "30", "object_relation": "ip-src", "first_seen": null, "last_seen": null, "value": "192.168.1.13", "Galaxy": [], "ShadowAttribute": [], "Tag": [{"id": "2", "name": "TestTag", "colour": "#41d947", "exportable": true, "user_id": "0", "hide_tag": false, "numerical_value": null, "local": 0}, {"id": "1", "name": "MarkoTest", "colour": "#b81d1d", "exportable": true, "user_id": "0", "hide_tag": false, "numerical_value": null, "local": 0}]}, {"id": "117", "type": "ip-dst", "category": "Network activity", "to_ids": false, "uuid": "3a6488cf-f2fd-4a35-b714-a8607c8e66b5", "event_id": "2", "distribution": "5", "timestamp": "1596182567", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "30", "object_relation": "ip-dst", "first_seen": null, "last_seen": null, "value": "192.168.1.31", "Galaxy": [], "ShadowAttribute": []}]}, {"id": "32", "name": "file", "meta-category": "file", "description": "File object describing a file with meta-information", "template_uuid": "688c46fb-5edb-40a3-8273-1af7923e2215", "template_version": "20", "event_id": "2", "uuid": "5dd4ce51-8e78-4c37-9a25-42f1120a9be5", "timestamp": "1596526764", "distribution": "1", "sharing_group_id": "0", "comment": "", "deleted": false, "first_seen": null, "last_seen": null, "ObjectReference": [], "Attribute": [{"id": "125", "type": "malware-sample", "category": "External analysis", "to_ids": true, "uuid": "0148f12a-c2e7-4b3e-ad63-147874ad5e1f", "event_id": "2", "distribution": "1", "timestamp": "1596526764", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "32", "object_relation": "malware-sample", "first_seen": null, "last_seen": null, "value": "gofile.txt|88829123c4dcf998da77ce31b7631d38", "Galaxy": [], "data": "UEsDBBQACQAIAOw8BFFyWAVN/AEAAPkDAAAgABwAODg4MjkxMjNjNGRjZjk5OGRhNzdjZTMxYjc2MzFkMzhVVAkAA6sQKV+rEClfdXgLAAEEIQAAAAQhAAAA5lxTDiIM0YDeXm5cEprdgpBHk4mG4KVcCCbRJWH+pOf1M+5g/xN9LdWE4QyMnyoBTJeciMUWqAyy/sPBFLHfR3xyNFrIpTjdI5IoXvi60ecV2Gdyb/pwcW6Yi+OAUEf/Gmzq2tY3dA5WlIPki43TwcRMJYsKT526m+jryJeStUqSgFRrHsBZf4qAwDgVoE7gjmYxaUfIbPgnSOMDx412JmcDN9QOGOCvlmM7eQqYmYgE2jVhK63AcokA2xvn6DYAaP56/Bc8UiJz/Bfw7Iw/0eDKt5cy31XPvzfQ/rexrOLjL4iLyWeYDU9ryB3hSNWJWqiZ0RjovwT+j744dQM5dQk4mo0pxcNWDO24LHWVEKY0Kn2+czEFBf/6YQ12tBtBB+xSv+gtNKsL6VGU3VFxX6kG6ttH8GMaL90UWwxLMMcE9D9FSTMQEREMotov6aKOwCSsLxvjQpXy3w7OZ1ATVtHUmwGhqfjdtC423jmZWXcxoNLWERPu6Axl117ZBqmCRnhOXDUm4QM03oDvHlpqMeIyC9jkcsLKm371UN1nxW1P6up4qiAZfORAVBs2h6Sk1Ojn3Ijz+c8ZHW2YkT27WDMDiPnYBCr3QiRJaVLQCLf2MWBW+UeyiuEXShzxKbAUfuWecyjK751d4oMVt89F99+qLgJ/7DxyqZIK91BLBwhyWAVN/AEAAPkDAABQSwMECgAJAAAA7DwEUUbwvtYWAAAACgAAAC0AHAA4ODgyOTEyM2M0ZGNmOTk4ZGE3N2NlMzFiNzYzMWQzOC5maWxlbmFtZS50eHRVVAkAA6sQKV+rEClfdXgLAAEEIQAAAAQhAAAA1u1Qp/9kTGuwuOutN9xQTkXoC/A/y1BLBwhG8L7WFgAAAAoAAABQSwECHgMUAAkACADsPARRclgFTfwBAAD5AwAAIAAYAAAAAAABAAAApIEAAAAAODg4MjkxMjNjNGRjZjk5OGRhNzdjZTMxYjc2MzFkMzhVVAUAA6sQKV91eAsAAQQhAAAABCEAAABQSwECHgMKAAkAAADsPARRRvC+1hYAAAAKAAAALQAYAAAAAAABAAAApIFmAgAAODg4MjkxMjNjNGRjZjk5OGRhNzdjZTMxYjc2MzFkMzguZmlsZW5hbWUudHh0VVQFAAOrEClfdXgLAAEEIQAAAAQhAAAAUEsFBgAAAAACAAIA2QAAAPMCAAAAAA==", "ShadowAttribute": []}, {"id": "127", "type": "md5", "category": "External analysis", "to_ids": true, "uuid": "0f497551-a65c-40ba-b270-3e6753f73225", "event_id": "2", "distribution": "1", "timestamp": "1596526764", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "32", "object_relation": "md5", "first_seen": null, "last_seen": null, "value": "88829123c4dcf998da77ce31b7631d38", "Galaxy": [], "ShadowAttribute": []}, {"id": "128", "type": "sha1", "category": "External analysis", "to_ids": true, "uuid": "a4acaf9a-eb91-43d8-beab-507886254eb7", "event_id": "2", "distribution": "1", "timestamp": "1596526764", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "32", "object_relation": "sha1", "first_seen": null, "last_seen": null, "value": "01b0a48159ab6a5d53bb6b012da33b3a9587d77d", "Galaxy": [], "ShadowAttribute": []}, {"id": "129", "type": "sha256", "category": "External analysis", "to_ids": true, "uuid": "48afa872-af00-4a3e-a08a-219a6065052b", "event_id": "2", "distribution": "1", "timestamp": "1596526764", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "32", "object_relation": "sha256", "first_seen": null, "last_seen": null, "value": "f41650f178955587ce86fc6fb0f0ba75525724c06eb40a15ec60059aa2814c42", "Galaxy": [], "ShadowAttribute": []}, {"id": "130", "type": "size-in-bytes", "category": "Other", "to_ids": false, "uuid": "798f0bf4-2867-4c78-b294-e6509bb67e8b", "event_id": "2", "distribution": "1", "timestamp": "1596526764", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": true, "object_id": "32", "object_relation": "size-in-bytes", "first_seen": null, "last_seen": null, "value": "1017", "Galaxy": [], "ShadowAttribute": []}]}, {"id": "33", "name": "file", "meta-category": "file", "description": "File object describing a file with meta-information", "template_uuid": "688c46fb-5edb-40a3-8273-1af7923e2215", "template_version": "20", "event_id": "2", "uuid": "3bc16806-4bdb-4c07-9dae-7d0e9d65dc7f", "timestamp": "1596533585", "distribution": "1", "sharing_group_id": "0", "comment": "", "deleted": false, "first_seen": null, "last_seen": null, "ObjectReference": [], "Attribute": [{"id": "131", "type": "malware-sample", "category": "External analysis", "to_ids": false, "uuid": "d92dedbf-6196-4f6d-ad7e-0eb7851c4dc9", "event_id": "2", "distribution": "1", "timestamp": "1596533585", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "33", "object_relation": "malware-sample", "first_seen": null, "last_seen": null, "value": "newfile.txt|64f6d511795fdc1a10b01e6e1a9904bc", "Galaxy": [], "data": "UEsDBBQACQAIAHVCBFFSq+uIzAAAAOcAAAAgABwANjRmNmQ1MTE3OTVmZGMxYTEwYjAxZTZlMWE5OTA0YmNVVAkAAx0aKV8dGilfdXgLAAEEIQAAAAQhAAAAXDjYmJiUAHim/bqC+waB4W4sTGzZGLjalqtVn/sbJIIAiJNxnm40egDtA9MW3jnXc4MlD9ilJF1F/wxyUGmJvNodgYVYEmVJxf/BjaV/ahdEEG6TYfdP1LrdCjnFQAyKplpwfMsnqiORNB6biqa0W7EsEqhelYprsR744hpG3HWaYaD5zYARhOGgMk6/jbI9zDvU9DZkS3Z0b+ZPlH0O76NvDSlBv6LmfZJbsitiCXIUyG/vmLRQw+FJINBL5kP8BJ6wutIsexUnmoDmUEsHCFKr64jMAAAA5wAAAFBLAwQKAAkAAAB1QgRRtqT8TxcAAAALAAAALQAcADY0ZjZkNTExNzk1ZmRjMWExMGIwMWU2ZTFhOTkwNGJjLmZpbGVuYW1lLnR4dFVUCQADHRopXx0aKV91eAsAAQQhAAAABCEAAACkHncHRj6v1bfbOC06eWPEX3vwCCTXMlBLBwi2pPxPFwAAAAsAAABQSwECHgMUAAkACAB1QgRRUqvriMwAAADnAAAAIAAYAAAAAAABAAAApIEAAAAANjRmNmQ1MTE3OTVmZGMxYTEwYjAxZTZlMWE5OTA0YmNVVAUAAx0aKV91eAsAAQQhAAAABCEAAABQSwECHgMKAAkAAAB1QgRRtqT8TxcAAAALAAAALQAYAAAAAAABAAAApIE2AQAANjRmNmQ1MTE3OTVmZGMxYTEwYjAxZTZlMWE5OTA0YmMuZmlsZW5hbWUudHh0VVQFAAMdGilfdXgLAAEEIQAAAAQhAAAAUEsFBgAAAAACAAIA2QAAAMQBAAAAAA==", "ShadowAttribute": []}, {"id": "132", "type": "filename", "category": "External analysis", "to_ids": false, "uuid": "3db0663d-88d2-4487-98ad-fd9d8e745342", "event_id": "2", "distribution": "1", "timestamp": "1596529181", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "33", "object_relation": "filename", "first_seen": null, "last_seen": null, "value": "newfile.txt", "Galaxy": [], "ShadowAttribute": [], "Sighting": [{"id": "3", "attribute_id": "132", "event_id": "2", "org_id": "1", "date_sighting": "1596533571", "uuid": "f4c84ac2-d282-4327-a580-9dad569e8277", "source": "", "type": "1", "Organisation": {"id": "1", "uuid": "09b0dde1-2934-4310-a107-74b6f534f041", "name": "ORGNAME"}, "attribute_uuid": "09c05001-1618-40b6-9199-d18a0a01cee4"}]}, {"id": "133", "type": "md5", "category": "External analysis", "to_ids": true, "uuid": "102a46f7-6872-488a-a394-d6e6a8032a1c", "event_id": "2", "distribution": "1", "timestamp": "1596529181", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "33", "object_relation": "md5", "first_seen": null, "last_seen": null, "value": "64f6d511795fdc1a10b01e6e1a9904bc", "Galaxy": [], "ShadowAttribute": []}, {"id": "134", "type": "sha1", "category": "External analysis", "to_ids": true, "uuid": "b1da95c0-9a7a-4069-81e2-41fdc5956efd", "event_id": "2", "distribution": "1", "timestamp": "1596529181", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "33", "object_relation": "sha1", "first_seen": null, "last_seen": null, "value": "5a04a28ad2f702bd46fa1a73ac5de524dbe22009", "Galaxy": [], "ShadowAttribute": []}, {"id": "135", "type": "sha256", "category": "External analysis", "to_ids": true, "uuid": "ac8d92ea-3c84-4ac1-a762-a17c9242314c", "event_id": "2", "distribution": "1", "timestamp": "1596529181", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "33", "object_relation": "sha256", "first_seen": null, "last_seen": null, "value": "aee84449d28d9f22baad6702c782074e2beaf5fe245fd7bd2284cb75a44efe65", "Galaxy": [], "ShadowAttribute": []}, {"id": "136", "type": "size-in-bytes", "category": "Other", "to_ids": false, "uuid": "2946bc8e-cc35-43e7-a569-ed47ef0297ed", "event_id": "2", "distribution": "1", "timestamp": "1596529181", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": true, "object_id": "33", "object_relation": "size-in-bytes", "first_seen": null, "last_seen": null, "value": "231", "Galaxy": [], "ShadowAttribute": []}]}, {"id": "34", "name": "file", "meta-category": "file", "description": "File object describing a file with meta-information", "template_uuid": "688c46fb-5edb-40a3-8273-1af7923e2215", "template_version": "20", "event_id": "2", "uuid": "78ba1bc6-1a04-49cb-95be-30edfc907c41", "timestamp": "1596533573", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "first_seen": null, "last_seen": null, "ObjectReference": [], "Attribute": [{"id": "138", "type": "filename", "category": "Payload delivery", "to_ids": false, "uuid": "4a85a395-bc31-4c80-9335-4c3b6c9ce4ab", "event_id": "2", "distribution": "5", "timestamp": "1596533573", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "34", "object_relation": "filename", "first_seen": null, "last_seen": null, "value": "Sample.txt", "Galaxy": [], "ShadowAttribute": []}]}, {"id": "35", "name": "ip-port", "meta-category": "network", "description": "An IP address (or domain or hostname) and a port seen as a tuple (or as a triple) in a specific time frame.", "template_uuid": "9f8cea74-16fe-4968-a2b4-026676949ac6", "template_version": "8", "event_id": "2", "uuid": "eca280d8-a709-4653-9e45-4bdb4258518d", "timestamp": "1596533574", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "first_seen": null, "last_seen": null, "ObjectReference": [], "Attribute": [{"id": "139", "type": "port", "category": "Network activity", "to_ids": false, "uuid": "3478ad9c-cea5-41b5-b8a2-1eab110a5226", "event_id": "2", "distribution": "5", "timestamp": "1596533574", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "35", "object_relation": "dst-port", "first_seen": null, "last_seen": null, "value": "99", "Galaxy": [], "ShadowAttribute": []}, {"id": "140", "type": "port", "category": "Network activity", "to_ids": false, "uuid": "a72fa84a-439e-4712-83d8-e5198a53aeaf", "event_id": "2", "distribution": "5", "timestamp": "1596533574", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "35", "object_relation": "src-port", "first_seen": null, "last_seen": null, "value": "11", "Galaxy": [], "ShadowAttribute": []}, {"id": "141", "type": "ip-src", "category": "Network activity", "to_ids": false, "uuid": "17b3496f-363b-4b92-9f12-89a3f8a2419a", "event_id": "2", "distribution": "5", "timestamp": "1596533574", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "35", "object_relation": "ip-src", "first_seen": null, "last_seen": null, "value": "4.3.2.1", "Galaxy": [], "ShadowAttribute": []}, {"id": "142", "type": "ip-dst", "category": "Network activity", "to_ids": false, "uuid": "ec68fc4b-3e5f-4126-8bd9-02f3902e5891", "event_id": "2", "distribution": "5", "timestamp": "1596533574", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "35", "object_relation": "ip-dst", "first_seen": null, "last_seen": null, "value": "1.2.3.4", "Galaxy": [], "ShadowAttribute": []}]}, {"id": "36", "name": "url", "meta-category": "network", "description": "url object describes an url along with its normalized field (like extracted using faup parsing library) and its metadata.", "template_uuid": "60efb77b-40b5-4c46-871b-ed1ed999fce5", "template_version": "8", "event_id": "2", "uuid": "36b4fbc9-e3b0-4a1b-ab2b-67a5c21215ff", "timestamp": "1596533575", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "first_seen": null, "last_seen": null, "ObjectReference": [], "Attribute": [{"id": "143", "type": "url", "category": "Network activity", "to_ids": false, "uuid": "f57f6ce8-235e-47ec-a2cd-1a89ad47a6e5", "event_id": "2", "distribution": "5", "timestamp": "1596533575", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "36", "object_relation": "url", "first_seen": null, "last_seen": null, "value": "https://stackoverflow.com/questions/51553395/find-docker-file-path-according-to-container-id", "Galaxy": [], "ShadowAttribute": []}, {"id": "144", "type": "port", "category": "Network activity", "to_ids": false, "uuid": "7a297866-c7ae-4fc2-9aee-2103846e769c", "event_id": "2", "distribution": "5", "timestamp": "1596533575", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "36", "object_relation": "port", "first_seen": null, "last_seen": null, "value": "89", "Galaxy": [], "ShadowAttribute": []}, {"id": "145", "type": "ip-dst", "category": "Network activity", "to_ids": false, "uuid": "bf923622-38e2-4ef6-a53a-2446b0d61cf9", "event_id": "2", "distribution": "5", "timestamp": "1596533575", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "36", "object_relation": "ip", "first_seen": null, "last_seen": null, "value": "5.6.7.8", "Galaxy": [], "ShadowAttribute": []}]}, {"id": "37", "name": "network-connection", "meta-category": "network", "description": "A local or remote network connection.", "template_uuid": "af16764b-f8e5-4603-9de1-de34d272f80b", "template_version": "3", "event_id": "2", "uuid": "63fd1a61-d387-45a7-ba09-e6a5c8da8c82", "timestamp": "1596533576", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "first_seen": null, "last_seen": null, "ObjectReference": [], "Attribute": [{"id": "146", "type": "port", "category": "Network activity", "to_ids": false, "uuid": "dc17a79b-18e1-437b-8cfa-37cc723af449", "event_id": "2", "distribution": "5", "timestamp": "1596533576", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "37", "object_relation": "dst-port", "first_seen": null, "last_seen": null, "value": "22", "Galaxy": [], "ShadowAttribute": []}, {"id": "147", "type": "port", "category": "Network activity", "to_ids": false, "uuid": "38e5b17b-62cd-4320-8bcd-6a4259c14507", "event_id": "2", "distribution": "5", "timestamp": "1596533576", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "37", "object_relation": "src-port", "first_seen": null, "last_seen": null, "value": "80", "Galaxy": [], "ShadowAttribute": []}, {"id": "148", "type": "ip-dst", "category": "Network activity", "to_ids": false, "uuid": "42f4ece5-aa54-41ea-b1bd-db6dfa92beae", "event_id": "2", "distribution": "5", "timestamp": "1596533576", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "37", "object_relation": "ip-dst", "first_seen": null, "last_seen": null, "value": "6.7.8.9", "Galaxy": [], "ShadowAttribute": []}, {"id": "149", "type": "ip-src", "category": "Network activity", "to_ids": false, "uuid": "1811fc7e-16c3-433f-89f6-fc65c63f7341", "event_id": "2", "distribution": "5", "timestamp": "1596533576", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "37", "object_relation": "ip-src", "first_seen": null, "last_seen": null, "value": "9.8.7.6", "Galaxy": [], "ShadowAttribute": []}]}, {"id": "38", "name": "file", "meta-category": "file", "description": "File object describing a file with meta-information", "template_uuid": "688c46fb-5edb-40a3-8273-1af7923e2215", "template_version": "20", "event_id": "2", "uuid": "56104c1c-6271-45c0-afa6-d1dbef4c3f12", "timestamp": "1596534283", "distribution": "1", "sharing_group_id": "0", "comment": "", "deleted": false, "first_seen": null, "last_seen": null, "ObjectReference": [], "Attribute": [{"id": "150", "type": "malware-sample", "category": "External analysis", "to_ids": true, "uuid": "df329478-e4d0-4fe4-ab18-a8b4d3516ca8", "event_id": "2", "distribution": "1", "timestamp": "1596534283", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "38", "object_relation": "malware-sample", "first_seen": null, "last_seen": null, "value": "trythis.txt|7d0fd30df681b6b7665cd6129f160856", "Galaxy": [], "data": "UEsDBBQACQAIAJZNBFHitCAHTAAAAEYAAAAgABwAN2QwZmQzMGRmNjgxYjZiNzY2NWNkNjEyOWYxNjA4NTZVVAkAAwsuKV8LLilfdXgLAAEEIQAAAAQhAAAApgBWDjabX/v1nMmJSs5I5paTXaFd6+QxSAjO1HJxUPCTW8GG1RSitx+029ENjGCPAdGwPWWGwOlCpdLyzMnvXL0zAtlbjiD/J3s6WlBLBwjitCAHTAAAAEYAAABQSwMECgAJAAAAlk0EUYm3kSkXAAAACwAAAC0AHAA3ZDBmZDMwZGY2ODFiNmI3NjY1Y2Q2MTI5ZjE2MDg1Ni5maWxlbmFtZS50eHRVVAkAAwsuKV8LLilfdXgLAAEEIQAAAAQhAAAAyEz5GkE8gi5CHOPI6nyWh00dZQH0JKlQSwcIibeRKRcAAAALAAAAUEsBAh4DFAAJAAgAlk0EUeK0IAdMAAAARgAAACAAGAAAAAAAAQAAAKSBAAAAADdkMGZkMzBkZjY4MWI2Yjc2NjVjZDYxMjlmMTYwODU2VVQFAAMLLilfdXgLAAEEIQAAAAQhAAAAUEsBAh4DCgAJAAAAlk0EUYm3kSkXAAAACwAAAC0AGAAAAAAAAQAAAKSBtgAAADdkMGZkMzBkZjY4MWI2Yjc2NjVjZDYxMjlmMTYwODU2LmZpbGVuYW1lLnR4dFVUBQADCy4pX3V4CwABBCEAAAAEIQAAAFBLBQYAAAAAAgACANkAAABEAQAAAAA=", "ShadowAttribute": []}, {"id": "151", "type": "filename", "category": "External analysis", "to_ids": false, "uuid": "09b81948-1217-478a-87ce-4c39d04c6754", "event_id": "2", "distribution": "1", "timestamp": "1596534283", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "38", "object_relation": "filename", "first_seen": null, "last_seen": null, "value": "trythis.txt", "Galaxy": [], "ShadowAttribute": []}, {"id": "152", "type": "md5", "category": "External analysis", "to_ids": true, "uuid": "116a50eb-f7f4-4a41-8f89-ad6856c207ea", "event_id": "2", "distribution": "1", "timestamp": "1596534283", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "38", "object_relation": "md5", "first_seen": null, "last_seen": null, "value": "7d0fd30df681b6b7665cd6129f160856", "Galaxy": [], "ShadowAttribute": []}, {"id": "153", "type": "sha1", "category": "External analysis", "to_ids": true, "uuid": "6fb4cf1a-0599-428e-85e7-55d5228fcccf", "event_id": "2", "distribution": "1", "timestamp": "1596534283", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "38", "object_relation": "sha1", "first_seen": null, "last_seen": null, "value": "024407b65e79f9d0818871876a0a5648ddd55071", "Galaxy": [], "ShadowAttribute": []}, {"id": "154", "type": "sha256", "category": "External analysis", "to_ids": true, "uuid": "7b3bf01e-5b98-4db3-af8b-52b0c5f9d6d5", "event_id": "2", "distribution": "1", "timestamp": "1596534283", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "38", "object_relation": "sha256", "first_seen": null, "last_seen": null, "value": "7b15a02069bd5d24bd20019d45c1a408315a443004f594d9e5f7dd00dca461a7", "Galaxy": [], "ShadowAttribute": []}, {"id": "155", "type": "size-in-bytes", "category": "Other", "to_ids": false, "uuid": "320c791d-5e7d-4d39-a420-d3689bf3abd7", "event_id": "2", "distribution": "1", "timestamp": "1596534283", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": true, "object_id": "38", "object_relation": "size-in-bytes", "first_seen": null, "last_seen": null, "value": "70", "Galaxy": [], "ShadowAttribute": []}]}], "Tag": [{"id": "3", "name": "\u05dc\u05e4\u05d9\u05db\u05da", "colour": "#7b38e8", "exportable": true, "user_id": "0", "hide_tag": false, "numerical_value": null, "local": 0}, {"id": "2", "name": "TestTag", "colour": "#41d947", "exportable": true, "user_id": "0", "hide_tag": false, "numerical_value": null, "local": 0}]}}]
```



#### Create File Misp Object
Create a File Object in MISP. Requires one of: FILENAME, MD5, SHA1, SHA256, SSDEEP to be provided or “Use Entities“ parameter set to true.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event ID|Specify the ID or UUID of the event for which you want to add file objects.|True|String||
|FILENAME|Specify the name of the file, which you want to add to the event.|False|String||
|MD5|Specify the md5 of the file, which you want to add to the event.|False|String||
|SHA1|Specify the sha1 of the file, which you want to add to the event.|False|String||
|SHA256|Specify the sha256 of the file, which you want to add to the event.|False|String||
|SSDEEP|Specify the ssdeep of the file, which you want to add to the event. Format: size:hash:hash|False|String||
|Use Entities|If enabled, action will use entities in order to create objects. Supported entities: File name and hash. “Use Entities“ has priority over other parameters.|False|Boolean|false|



##### JSON Results
```json
{"Object": {"id": "XXX", "name": "file", "meta-category": "file", "description": "File object describing a file with info", "template_uuid": "XXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXX", "template_version": "XX", "event_id": "XX", "uuid": "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX", "timestamp": "1595435541", "distribution": "info", "sharing_group_id": "XX", "comment": "", "deleted": false, "first_seen": null, "last_seen": null, "Attribute": [{"id": "XXX", "event_id": "XX", "object_id": "XX", "object_relation": "filename", "category": "Category type", "type": "filename", "value1": "test.file", "value2": "", "to_ids": false, "uuid": "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX", "timestamp": "1594935541", "distribution": "info", "sharing_group_id": "XX", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "test.file"}]}}
```



#### List Event Objects
Retrieve information about available objects in MISP event.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event ID|Specify a comma-separated list of IDs and UUIDs of the events, for which you want to retrieve details.|True|String||
|Max Objects to Return|Specify how many objects to return.|False|String|50|



##### JSON Results
```json
[{"Object": {"id": "1", "name": "ftm-Associate", "meta-category": "followthemoney", "description": "Non-family association between two people", "template_uuid": "6119ecb3-dedd-44b6-b88f-174585b0b1bf", "template_version": "1", "event_id": "1", "uuid": "2a3e260f-d3b2-4164-b2b1-2f6f5b559970", "timestamp": "1594632232", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "first_seen": null, "last_seen": null, "ObjectReference": [], "Attribute": [{"id": "2", "type": "port", "category": "Network activity", "to_ids": false, "uuid": "8d39ecef-0e0c-47ff-8d6e-9b2dc555d89e", "event_id": "1", "distribution": "5", "timestamp": "1594632775", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "1", "object_relation": "dst-port", "first_seen": null, "last_seen": null, "value": "80", "Galaxy": [], "ShadowAttribute": []}, {"id": "3", "type": "ip-dst", "category": "Network activity", "to_ids": false, "uuid": "885ccc66-de8a-47b4-a926-a62fb5053dc9", "event_id": "1", "distribution": "5", "timestamp": "1594627709", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "1", "object_relation": "ip-dst", "first_seen": null, "last_seen": null, "value": "2.2.2.2", "Galaxy": [], "ShadowAttribute": []}]}}]
```



#### Set IDS Flag for an Attribute
Set IDS flag for attributes in MISP
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Attribute Name|Specify a comma-separated list of attribute identifiers for which you want to set an IDS flag. Note: If both “Attribute Name“ and “Attribute UUID“ are specified, action will work with “Attribute UUID“ values.|False|String||
|Event ID|Specify the ID or UUID of the event, where to seach for attributes. This parameter is required, if “Attribute Search“ is set to “Provided Event“.|False|String||
|Category|Specify a comma-separated list of categories. If specified, action will only set IDS flag for attributes that have matching category. If nothing is specified, action will ignore categories in attributes. Possible values: External Analysis, Payload Delivery, Artifacts Dropped, Payload Installation.|False|String||
|Type|Specify a comma-separated list of attribute types. If specified, action will only set IDS flag for attributes that have matching attribute type. If nothing is specified, action will ignore types in attributes. Example values: md5, sha1, ip-src, ip-dst|False|String||
|Attribute Search|Specify, where action should search for attributes. If “Provided Event“ is selected, action will only search for attributes or attribute UUIDs in event with ID/UUID provided in “Event ID“ parameter. If “All Events“, action will search for attributes among all events and set IDS flag for all attributes that match our criteria.|False|List|Provided Event|
|Attribute UUID|Specify a comma-separated list of attribute UUIDs for which you want to set an IDS flag. Note: If both “Attribute Name“ and “Attribute UUID“ are specified, action will work with “Attribute UUID“ values.|False|String||



#### Publish Event
The action allows the user to publish an event. Publishing an event shares it to the sharing group selected, making it visible to all members.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event ID|Specify the ID or UUID of the event that you want to publish.|True|String||



##### JSON Results
```json
{"orgc_id": "228", "ShadowAttribute": [], "id": "55555", "threat_level_id": "3", "uuid": "55555555-5555-5555-5555-55555555555", "Object": [], "Tag": [{"hide_tag": false, "user_id": "0", "name": "misp-galaxy:threat-actor=\"Turla Group\"", "colour": "#0088cc", "numerical_value": null, "exportable": true, "local": 0, "id": "2"}, {"hide_tag": false, "user_id": "0", "name": "Lampion", "colour": "#c40ab2", "numerical_value": null, "exportable": true, "local": 0, "id": "2606"}], "Orgc": {"uuid": "55555555-5555-5555-5555-55555555555", "local": false, "id": "228", "name": "CERT-RLP_1185"}, "Org": {"uuid": "55555555-5555-5555-5555-55555555555", "local": true, "id": "1", "name": "CyberInt-Proxy"}, "RelatedEvent": [{"Event": {"info": "Some info", "orgc_id": "228", "uuid": "55555555-5555-5555-5555-55555555555", "timestamp": "1578633609", "Orgc": {"uuid": "55555555-5555-5555-5555-55555555555", "id": "228", "name": "CERT-RLP_1185"}, "org_id": "1", "analysis": "2", "published": true, "date": "2020-01-10", "Org": {"uuid": "55555555-5555-5555-5555-55555555555", "id": "1", "name": "CyberInt-Proxy"}, "distribution": "3", "id": "58630", "threat_level_id": "3"}}, {"Event": {"info": "Some info", "orgc_id": "228", "uuid": "55555555-5555-5555-5555-55555555555", "timestamp": "1578547207", "Orgc": {"uuid": "55555555-5555-5555-5555-55555555555", "id": "228", "name": "CERT-RLP_1185"}, "org_id": "1", "analysis": "2", "published": true, "date": "2020-01-09", "Org": {"uuid": "55555555-5555-5555-5555-55555555555", "id": "1", "name": "CyberInt-Proxy"}, "distribution": "3", "id": "58618", "threat_level_id": "3"}}], "sharing_group_id": "0", "timestamp": "1578987213", "date": "2020-01-11", "disable_correlation": false, "info": "Some info", "locked": true, "publish_timestamp": "1578987213", "Attribute": [{"category": "Network activity", "comment": "", "Tag": [{"hide_tag": false, "user_id": "0", "name": "test", "colour": "#cedfba", "numerical_value": null, "exportable": true, "local": 0, "id": "5555"}], "uuid": "55555555-5555-5555-5555-55555555555", "event_id": "55555", "timestamp": "1578986154", "to_ids": true, "deleted": false, "object_id": "0", "sharing_group_id": "0", "ShadowAttribute": [], "value": "111.111.111.11", "disable_correlation": false, "distribution": "5", "object_relation": null, "type": "ip-src", "id": "555555", "Galaxy": []}, {"category": "Network activity", "comment": "", "uuid": "55555555-5555-5555-5555-55555555555", "event_id": "55555", "timestamp": "1578720007", "to_ids": true, "deleted": false, "object_id": "0", "sharing_group_id": "0", "ShadowAttribute": [], "value": "555.555.5.555", "disable_correlation": false, "distribution": "5", "object_relation": null, "type": "ip-src", "id": "555555", "Galaxy": []}], "attribute_count": "8", "org_id": "1", "analysis": "2", "extends_uuid": "", "published": true, "distribution": "3", "proposal_email_lock": false, "Galaxy": [{"GalaxyCluster": [{"description": "Some description", "galaxy_id": "33", "uuid": "55555555-5555-5555-5555-55555555555", "value": "Turla Group", "local": false, "source": "MISP Project", "tag_name": "misp-galaxy:threat-actor=\"Turla Group\"", "version": "110", "meta": {"cfr-suspected-victims": ["France", "Romania", "Kazakhstan", "Poland", "Tajikistan", "Russia", "United States", "Saudi Arabia", "Germany", "India", "Belarus", "Netherlands", "Iran", "Uzbekistan", "Iraq"], "country": ["RU"], "refs": ["http://www.example.com/some_file.pdf"], "cfr-target-category": ["Government", "Military"], "cfr-type-of-incident": ["Espionage"], "synonyms": ["Turla", "Snake", "Venomous Bear", "Group 88", "Waterbug", "WRAITH", "Turla Team", "Uroburos", "Pfinet", "TAG_0530", "KRYPTON", "Hippo Team", "Pacifier APT", "Popeye"], "attribution-confidence": ["50"], "cfr-suspected-state-sponsor": ["Russian Federation"]}, "tag_id": "2", "authors": ["Name Name", "Name2 Name2", "Name3 Name2", "Name4 Name4", "Various"], "type": "threat-actor", "id": "17422", "collection_uuid": "55555555-5555-5555-5555-55555555555"}], "description": "Some description", "namespace": "misp", "uuid": "55555555-5555-5555-5555-55555555555", "version": "3", "icon": "user-secret", "type": "threat-actor", "id": "33", "name": "Threat Actor"}]}
```



#### Delete an Attribute
Delete attributes in MISP. Supported hashes: MD5, SHA1, SHA224, SHA256, SHA384, SHA512, SSDeep.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Attribute Name|Specify a comma-separated list of attribute identifiers that you want to delete. Note: If both “Attribute Name“ and “Attribute UUID“ are specified, action will work with “Attribute UUID“ values.|False|String||
|Event ID|Specify the ID or UUID of the event, where to search for attributes. This parameter is required, if “Attribute Search“ is set to “Provided Event“ or Object UUID is provided.|False|String||
|Category|Specify a comma-separated list of categories. If specified, action will only delete attributes that have matching category. If nothing is specified, action will ignore categories in attributes. Possible values: External Analysis, Payload Delivery, Artifacts Dropped, Payload Installation.|False|String||
|Type|Specify a comma-separated list of attribute types. If specified, action will only delete attributes that have matching attribute type. If nothing is specified, action will ignore types in attributes. Example values: md5, sha1, ip-src, ip-dst|False|String||
|Object UUID|Specify the uuid of the object that contains the desired attribute|False|String||
|Attribute UUID|Specify a comma-separated list of attribute UUIDs that you want to delete. Note: If both “Attribute Name“ and “Attribute UUID“ are specified, action will work with “Attribute UUID“ values.|False|String||
|Attribute Search|Specify, where action should search for attributes. If “Provided Event“ is selected, action will only search for attributes or attribute UUIDs in event with ID/UUID provided in “Event ID“ parameter. If “All Events“, action will search for attributes among all events and delete all attributes that match our criteria.|False|List|Provided Event|



##### JSON Results
```json
[{"message": "Attribute deleted."}]
```



#### Create network-connection Misp Object
Create a network-connection Object in MISP. Requires one of: Dst-port, Src-port, IP-Src, IP-Dst to be provided or “Use Entities“ parameter set to true.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event ID|Specify the ID or UUID of the event to which you want to add network-connection objects.|True|String||
|Dst-port|Specify the destination port, which you want to add to the event.|False|String||
|Src-port|Specify the source port, which you want to add to the event.|False|String||
|Hostname-src|Specify the source hostname, which you want to add to the event.|False|String||
|Hostname-dst|Specify the source destination, which you want to add to the event.|False|String||
|IP-Src|Specify the source IP, which you want to add to the event.|False|String||
|IP-Dst|Specify the destination IP, which you want to add to the event.|False|String||
|Layer3-protocol|Specify the related layer 3 protocol, which you want to add to the event.|False|String||
|Layer4-protocol|Specify the related layer 4 protocol, which you want to add to the event.|False|String||
|Layer7-protocol|Specify the related layer 7 protocol, which you want to add to the event.|False|String||
|Use Entities|If enabled, action will use entities in order to create objects. Supported entities: IP Address. “Use Entities“ has priority over other parameters.|False|Boolean|false|
|IP Type|Specify what attribute type should be used with IP entities.|False|List|Source IP|



##### JSON Results
```json
{"Object": {"id": "1xx", "name": "network-connection", "meta-category": "network", "description": "A local or remote network connection.", "template_uuid": "af16764b-f8e5-4603-9de1-xxxxxx", "template_version": "3", "event_id": "1xx", "uuid": "9619eeeb-a09c-4b1a-94df-xxxxxx", "timestamp": "1595937853", "distribution": "5", "sharing_group_id": "xx", "comment": "", "deleted": false, "first_seen": null, "last_seen": null, "Attribute": [{"id": "3xx", "event_id": "1xx", "object_id": "1xx", "object_relation": "dst-port", "category": "Network activity", "type": "port", "value1": "80xx", "value2": "", "to_ids": false, "uuid": "e7d32f1f-9e65-4553-8659-9a9ae1ca8389", "timestamp": "1595937853", "distribution": "5", "sharing_group_id": "xx", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "80xx"}, {"id": "3xx", "event_id": "1xx", "object_id": "1xx", "object_relation": "src-port", "category": "Network activity", "type": "port", "value1": "84xx", "value2": "", "to_ids": false, "uuid": "974c09f9-209b-4ca2-8792-xxxxxx", "timestamp": "1595937853", "distribution": "5", "sharing_group_id": "xx", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "84xx"}, {"id": "3xx", "event_id": "1xx", "object_id": "1xx", "object_relation": "hostname-dst", "category": "Network activity", "type": "hostname", "value1": "domain.co", "value2": "", "to_ids": false, "uuid": "9bc973cf-4c99-4934-8505-xxxxxx", "timestamp": "1595937853", "distribution": "5", "sharing_group_id": "xx", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "domain.co"}, {"id": "4xx", "event_id": "1xx", "object_id": "1xx", "object_relation": "hostname-src", "category": "Network activity", "type": "hostname", "value1": "domain.com", "value2": "", "to_ids": false, "uuid": "338657a0-4d14-4392-b606-xxxxxx", "timestamp": "1595937853", "distribution": "5", "sharing_group_id": "xx", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "domain.com"}, {"id": "4xx", "event_id": "1xx", "object_id": "1xx", "object_relation": "ip-dst", "category": "Network activity", "type": "ip-dst", "value1": "2.2.2.xx", "value2": "", "to_ids": false, "uuid": "c128d6ae-0ec4-463b-a0cd-xxxxxx", "timestamp": "1595937853", "distribution": "5", "sharing_group_id": "xx", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "2.2.2.xx"}, {"id": "4xx", "event_id": "1xx", "object_id": "1xx", "object_relation": "ip-src", "category": "Network activity", "type": "ip-src", "value1": "1.1.1.xx", "value2": "", "to_ids": false, "uuid": "3c5a90b9-209b-46d8-a9e9-xxxxxx", "timestamp": "1595937853", "distribution": "5", "sharing_group_id": "xx", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "1.1.1.xx"}, {"id": "4xx", "event_id": "1xx", "object_id": "1xx", "object_relation": "layer3-protocol", "category": "Other", "type": "text", "value1": "Ixxx", "value2": "", "to_ids": false, "uuid": "609944d0-4db9-4ad8-99eb-xxxxxx", "timestamp": "1595937853", "distribution": "5", "sharing_group_id": "xx", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "Ixxx"}, {"id": "4xx", "event_id": "1xx", "object_id": "1xx", "object_relation": "layer4-protocol", "category": "Other", "type": "text", "value1": "Uxx", "value2": "", "to_ids": false, "uuid": "8b7ad826-92fd-43b4-b94b-xxxxxx", "timestamp": "1595937853", "distribution": "5", "sharing_group_id": "xx", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "Uxx"}, {"id": "4xx", "event_id": "1xx", "object_id": "1xx", "object_relation": "layer7-protocol", "category": "Other", "type": "text", "value1": "xxx", "value2": "", "to_ids": false, "uuid": "7de49873-35a8-4fe2-8dd1-xxxxxx", "timestamp": "1595937853", "distribution": "5", "sharing_group_id": "xx", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "xxx"}]}}
```



#### Add Tag to an Event
Add tags to event in MISP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event ID|Specify the ID or UUID of the event, for which you want to add tags.|True|String||
|Tag Name|Specify a comma-separated list of tags that you want to add to events.|True|String||



##### JSON Results
```json
[{"saved": true, "success": "Tag(s) added.", "check_publish": true}]
```



#### Upload File
Upload a file to a MISP event.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event ID|Specify the ID or UUID of the event to which you want to upload this file.|True|String||
|File Path|Specify a comma-separated list of absolute filepaths of the files that you want to upload to MISP.|True|String||
|Category|Specify the category for the uploaded file. Possible values: External Analysis, Payload Delivery, Artifacts Dropped, Payload Installation.|False|String||
|Distribution|Specify the distribution for the uploaded file. Possible values: 0 - Organisation, 1 - Community, 2 - Connected, 3 - All. You can either provide a number or a string.|False|String|Community|
|For Intrusion Detection System|If enabled, uploaded file will be used for intrusion detection systems.|False|Boolean|False|
|Comment|Specify additional comments related to the uploaded file.|False|String||



##### JSON Results
```json
{"id": "XXX", "orgc_id": "1", "org_id": "1", "date": "2020-12-25", "threat_level_id": "3", "info": "information...", "published": false, "uuid": "567XXXXX-XXXXX-XXXXX-XXXXXd39", "attribute_count": "24", "analysis": "0", "timestamp": "1609149632", "distribution": "0", "proposal_email_lock": false, "locked": false, "publish_timestamp": "0", "sharing_group_id": "0", "disable_correlation": false, "extends_uuid": "", "event_creator_email": "admin@admin.test", "Org": {"id": "1", "name": "ORGNAME", "uuid": "09b0XXXXXX-XXXXX-XXXXXXXX-XX41", "local": true}, "Orgc": {"id": "1", "name": "ORGNAME", "uuid": "09b0XXXXXX-XXXXX-XXXXXXXX-XX41", "local": true}, "Attribute": [], "ShadowAttribute": [], "RelatedEvent": [{"Event": {"id": "XX", "date": "2020-12-25", "threat_level_id": "3", "info": "information...", "published": false, "uuid": "XXXXX-XXXXX-XXXXX-XXXXXX", "analysis": "0", "timestamp": "1609146844", "distribution": "0", "org_id": "1", "orgc_id": "1", "Org": {"id": "1", "name": "ORGNAME", "uuid": "09b0XXXXXX-XXXXX-XXXXXXXX-XX41"}, "Orgc": {"id": "1", "name": "ORGNAME", "uuid": "09b0XXXXXX-XXXXX-XXXXXXXX-XX41"}}}], "Galaxy": [], "Object": [{"id": "XXX", "name": "file", "meta-category": "file", "description": "File object describing a file with meta-information", "template_uuid": "XXXXXXX-XXXXXXX-XXXXXX-XXXXX", "template_version": "20", "event_id": "XXX", "uuid": "XXXXXX-XXXX-XXXX-XXXXXXXX", "timestamp": "1609149360", "distribution": "1", "sharing_group_id": "0", "comment": "", "deleted": false, "first_seen": null, "last_seen": null, "ObjectReference": [], "Attribute": [{"id": "XXX", "type": "malware-sample", "category": "Payload installation", "to_ids": true, "uuid": "88XXXXXX-XXXXXX-XXXXXX-XXXXd", "event_id": "XXX", "distribution": "1", "timestamp": "1609349360", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "XXX", "object_relation": "malware-sample", "first_seen": null, "last_seen": null, "value": "test_file.png|38XXXXXXXXXXXXXXXXXXXXXXXXXXXX9", "Galaxy": [], "data": "UEsDBBQACQAIAABioB......A2QAAAPsnAAAAAA==", "ShadowAttribute": []}, {"id": "XXX", "type": "filename", "category": "Payload installation", "to_ids": false, "uuid": "5eXXX-XXXXX-XXXXXX-XXXXXXa", "event_id": "XXX", "distribution": "1", "timestamp": "1609149360", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "XXXX", "object_relation": "filename", "first_seen": null, "last_seen": null, "value": "test_file.png", "Galaxy": [], "ShadowAttribute": []}, {"id": "XXX", "type": "md5", "category": "Payload installation", "to_ids": true, "uuid": "XXXXXX-XXXXXX-XXXXXX-XXXXXX", "event_id": "XXX", "distribution": "1", "timestamp": "1609149360", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "XX", "object_relation": "md5", "first_seen": null, "last_seen": null, "value": "XXXXXXXXXXXXXXXXXXXXXXXX", "Galaxy": [], "ShadowAttribute": []}, {"id": "XXX", "type": "sha1", "category": "Payload installation", "to_ids": true, "uuid": "XXXXXX-XXXX-XXXX-XXX-XXXXXXX", "event_id": "XXX", "distribution": "1", "timestamp": "1609149360", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "XX", "object_relation": "sha1", "first_seen": null, "last_seen": null, "value": "XXXXXXXXXXXXXXXXXXXXXXXXXXXXX", "Galaxy": [], "ShadowAttribute": []}, {"id": "XXX", "type": "shaXXX", "category": "Payload installation", "to_ids": true, "uuid": "XXXXXXXX-XXXXXXX-XXXXXXX-XXXXX", "event_id": "XXX", "distribution": "1", "timestamp": "1609149360", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": false, "object_id": "XXX", "object_relation": "shaXXX", "first_seen": null, "last_seen": null, "value": "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX", "Galaxy": [], "ShadowAttribute": []}, {"id": "XXX", "type": "size-in-bytes", "category": "Other", "to_ids": false, "uuid": "XXXXXX-XXXXXX-XXXXXX-XXXXXX", "event_id": "XXX", "distribution": "1", "timestamp": "1609149360", "comment": "", "sharing_group_id": "0", "deleted": false, "disable_correlation": true, "object_id": "XX", "object_relation": "size-in-bytes", "first_seen": null, "last_seen": null, "value": "106367", "Galaxy": [], "ShadowAttribute": []}]}]}
```



#### Unpublish Event
The action allows the user to unpublish an event. Unpublishing an event prevents it from being visible to the shared groups.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event ID|Specify the ID or UUID of the event that you want to unpublish.|True|String||



##### JSON Results
```json
{"orgc_id": "228", "ShadowAttribute": [], "id": "55555", "threat_level_id": "3", "uuid": "55555555-5555-5555-5555-55555555555", "Object": [], "Tag": [{"hide_tag": false, "user_id": "0", "name": "misp-galaxy:threat-actor=\"Turla Group\"", "colour": "#0088cc", "numerical_value": null, "exportable": true, "local": 0, "id": "2"}, {"hide_tag": false, "user_id": "0", "name": "Lampion", "colour": "#c40ab2", "numerical_value": null, "exportable": true, "local": 0, "id": "2606"}], "Orgc": {"uuid": "55555555-5555-5555-5555-55555555555", "local": false, "id": "228", "name": "CERT-RLP_1185"}, "Org": {"uuid": "55555555-5555-5555-5555-55555555555", "local": true, "id": "1", "name": "CyberInt-Proxy"}, "RelatedEvent": [{"Event": {"info": "Some info", "orgc_id": "228", "uuid": "55555555-5555-5555-5555-55555555555", "timestamp": "1578633609", "Orgc": {"uuid": "55555555-5555-5555-5555-55555555555", "id": "228", "name": "CERT-RLP_1185"}, "org_id": "1", "analysis": "2", "published": false, "date": "2020-01-10", "Org": {"uuid": "55555555-5555-5555-5555-55555555555", "id": "1", "name": "CyberInt-Proxy"}, "distribution": "3", "id": "58630", "threat_level_id": "3"}}, {"Event": {"info": "Some info", "orgc_id": "228", "uuid": "55555555-5555-5555-5555-55555555555", "timestamp": "1578547207", "Orgc": {"uuid": "55555555-5555-5555-5555-55555555555", "id": "228", "name": "CERT-RLP_1185"}, "org_id": "1", "analysis": "2", "published": false, "date": "2020-01-09", "Org": {"uuid": "55555555-5555-5555-5555-55555555555", "id": "1", "name": "CyberInt-Proxy"}, "distribution": "3", "id": "58618", "threat_level_id": "3"}}], "sharing_group_id": "0", "timestamp": "1578987213", "date": "2020-01-11", "disable_correlation": false, "info": "Some info", "locked": true, "publish_timestamp": "1578987213", "Attribute": [{"category": "Network activity", "comment": "", "Tag": [{"hide_tag": false, "user_id": "0", "name": "test", "colour": "#cedfba", "numerical_value": null, "exportable": true, "local": 0, "id": "5555"}], "uuid": "55555555-5555-5555-5555-55555555555", "event_id": "55555", "timestamp": "1578986154", "to_ids": true, "deleted": false, "object_id": "0", "sharing_group_id": "0", "ShadowAttribute": [], "value": "111.111.111.11", "disable_correlation": false, "distribution": "5", "object_relation": null, "type": "ip-src", "id": "555555", "Galaxy": []}, {"category": "Network activity", "comment": "", "uuid": "55555555-5555-5555-5555-55555555555", "event_id": "55555", "timestamp": "1578720007", "to_ids": true, "deleted": false, "object_id": "0", "sharing_group_id": "0", "ShadowAttribute": [], "value": "555.555.5.555", "disable_correlation": false, "distribution": "5", "object_relation": null, "type": "ip-src", "id": "555555", "Galaxy": []}], "attribute_count": "8", "org_id": "1", "analysis": "2", "extends_uuid": "", "published": false, "distribution": "3", "proposal_email_lock": false, "Galaxy": [{"GalaxyCluster": [{"description": "Some description", "galaxy_id": "33", "uuid": "55555555-5555-5555-5555-55555555555", "value": "Turla Group", "local": false, "source": "MISP Project", "tag_name": "misp-galaxy:threat-actor=\"Turla Group\"", "version": "110", "meta": {"cfr-suspected-victims": ["France", "Romania", "Kazakhstan", "Poland", "Tajikistan", "Russia", "United States", "Saudi Arabia", "Germany", "India", "Belarus", "Netherlands", "Iran", "Uzbekistan", "Iraq"], "country": ["RU"], "refs": ["http://www.example.com/some_file.pdf"], "cfr-target-category": ["Government", "Military"], "cfr-type-of-incident": ["Espionage"], "synonyms": ["Turla", "Snake", "Venomous Bear", "Group 88", "Waterbug", "WRAITH", "Turla Team", "Uroburos", "Pfinet", "TAG_0530", "KRYPTON", "Hippo Team", "Pacifier APT", "Popeye"], "attribution-confidence": ["50"], "cfr-suspected-state-sponsor": ["Russian Federation"]}, "tag_id": "2", "authors": ["Name Name", "Name2 Name2", "Name3 Name2", "Name4 Name4", "Various"], "type": "threat-actor", "id": "17422", "collection_uuid": "55555555-5555-5555-5555-55555555555"}], "description": "Some description", "namespace": "misp", "uuid": "55555555-5555-5555-5555-55555555555", "version": "3", "icon": "user-secret", "type": "threat-actor", "id": "33", "name": "Threat Actor"}]}
```



#### Add Attribute
Add attributes based on entities to the event in MISP. Supported hashes: MD5, SHA1, SHA224, SHA256, SHA384, SHA512, SSDeep.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event ID|TheSpecify the ID or UUID of the event, for which you want to add attributes.|True|String||
|Category|Specify the category for attributes. Possible values: Targeting data, Payload delivery, Artifacts dropped, Payload installation, Persistence mechanism, Network activity, Attribution, External analysis, Social network.|False|String||
|Distribution|Specify the distribution of the attribute. Possible values: 0 - Organisation, 1 - Community, 2 - Connected, 3 - All, 5 - Inherit. You can either provide a number or a string.|False|String|Community|
|For Intrusion Detection System|If enabled, attribute will be labeled as eligible to create an IDS signature out of it.|False|Boolean|false|
|Comment|Specify comment related to attribute.|False|String||
|Fallback IP Type|Specify what should be the fallback attribute type for the IP address entity.|False|List|Source Address|
|Fallback Email Type|Specify what should be the fallback attribute type for the email address entity.|False|List|Source Email Address|
|Extract Domain|If enabled, action will extract domain out of URL entity.|False|Boolean|true|



##### JSON Results
```json
[{"Attribute": {"id": "xxxx", "event_id": "xx", "object_id": "xx", "object_relation": null, "category": "External analysis", "type": "domain", "value1": "xxxxx.com", "value2": "", "to_ids": true, "uuid": "76b41f31-abe9-40a5-9de6-xxxx", "timestamp": "1610724106", "distribution": "1", "sharing_group_id": "xx", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "xxxxx.com"}}, {"Attribute": {"id": "xxxx", "event_id": "xx", "object_id": "xx", "object_relation": null, "category": "External analysis", "type": "md5", "value1": "f925daf782826be42d26fdd3xxxx", "value2": "", "to_ids": true, "uuid": "844923b9-81cf-4e37-b3d6-xxxxx", "timestamp": "1610724106", "distribution": "1", "sharing_group_id": "xx", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "f925daf782826be42d26fxxxx"}}]
```



#### Download File
Download files related to event in MISP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event ID|Specify the ID or UUID of the event from which you want to download files|False|String||
|Download Folder Path|Specify the absolute path to the folder, which should store files. If nothing is specified, action will create an attachment instead. Note: JSON result is only available, when you provide proper value for this parameter.|False|String||
|Overwrite|If enabled, action will overwrite existing files.|False|Boolean|false|



##### JSON Results
```json
{"absolute_paths": ["/etc/file1.txt", "/etc/file2.txt"]}
```



#### Create Event
Create a new event in MISP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event Name|Specify the name for the new event.|True|String||
|Distribution|Specify the distribution of the event. Possible values: 0 - Organisation, 1 - Community, 2 - Connected, 3 - All. You can either provide a number or a string.|False|String|Community|
|Threat Level|Specify the threat level of the event. Possible values: 1 - High, 2 - Medium, 3 - Low, 4 - Undefined. You can either provide a number or a string.|False|String|High|
|Analysis|Specify the analysis of the event. Possible values: 0 - Initial, 1 - Ongoing, 2 - Completed. You can either provide a number or a string.|False|String|Initial|
|Publish|If enabled, action will publish the event to the community.|False|Boolean|false|
|Comment|Specify additional comments related to the event.|False|String||



##### JSON Results
```json
{"id": "XXX", "orgc_id": "1", "org_id": "1", "date": "2020-12-21", "threat_level_id": "1", "info": "qweqwe", "published": false, "uuid": "e8c5c0adXXXXXXXXXXXXXXXXXXXd62c06ee", "attribute_count": "0", "analysis": "1", "timestamp": "1608536549", "distribution": "0", "proposal_email_lock": false, "locked": false, "publish_timestamp": "0", "sharing_group_id": "0", "disable_correlation": false, "extends_uuid": "", "event_creator_email": "admin@admin.test", "Org": {"id": "1", "name": "ORGNAME", "uuid": "09b0dde1-2934XXXXXXXXXXXXXX6f534f041", "local": true}, "Orgc": {"id": "1", "name": "ORGNAME", "uuid": "09b0dde1-2934XXXXXXXXXXXXXX6f534f041", "local": true}}
```



#### Remove Tag from an Event
Remove tags from event in MISP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event ID|Specify the ID or UUID of the event, from which you want to remove tags.|True|String||
|Tag Name|Specify a comma-separated list of tags that you want to remove from events.|True|String||



##### JSON Results
```json
[{"saved": true, "success": "Tag removed.", "check_publish": true}]
```



#### Delete an Event
Delete event in MISP
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event ID|Specify the ID or UUID of the event that you want to delete.|True|String||



##### JSON Results
```json
[{"name": "Event deleted.", "message": "Event deleted.", "url": "/events/delete/4"}]
```



#### Get Related Events
Retrieve information about events that are related to entities in MISP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Events Limit|Specify max amount of events to fetch. If not specified, all events will be fetched.|False|String||
|Mark As Suspicious|If enabled, action will mark entity as suspicious, if there is at least one related event to it.|False|Boolean|true|



##### JSON Results
```json
[{"Entity": "103.129.xx.xx", "EntityResult": [{"Event ID": "1xx", "UUID": "c357571f-1f73-4cd5-8fa7-xxxx", "Org": "ORGNAME", "Date": "2021-01-18", "Threat Level": "Low", "Analysis": "Initial", "Distribution": "This community only", "Published": false, "Event Name": "event name"}, {"Event ID": "1xx", "UUID": "c357571f-1f73-4cd5-8fa7-xxxx", "Org": "ORGNAME", "Date": "2021-01-18", "Threat Level": "Low", "Analysis": "Initial", "Distribution": "This community only", "Published": false, "Event Name": "event name"}, {"Event ID": "1xx", "UUID": "a25a1f7b-2c51-4aab-8043-xxxx", "Org": "ORGNAME", "Date": "2021-01-18", "Threat Level": "Undefined", "Analysis": "Initial", "Distribution": "This community only", "Published": false, "Event Name": "testtest"}]}]
```



#### Add Tag to an Attribute
Add tags to attributes in MISP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Attribute Name|Specify a comma-separated list of attribute identifiers to which you want to add tags. Note: If both “Attribute Name“ and “Attribute UUID“ are specified, action will work with “Attribute UUID“ values.|False|String||
|Event ID|Specify the ID or UUID of the event, where to search for attributes. This parameter is required, if “Attribute Search“ is set to “Provided Event“ or Object UUID is provided.|False|String||
|Tag Name|Specify a comma-separated list of tags that you want to add to attributes.|True|String||
|Category|Specify a comma-separated list of categories. If specified, action will only add tags to attributes that have matching category. If nothing is specified, action will ignore categories in attributes. Possible values: External Analysis, Payload Delivery, Artifacts Dropped, Payload Installation.|False|String||
|Type|Specify a comma-separated list of attribute types. If specified, action will only add tags to attributes that have matching attribute type. If nothing is specified, action will ignore types in attributes. Example values: md5, sha1, ip-src, ip-dst|False|String||
|Object UUID|Specify the uuid of the object that contains the desired attribute.|False|String||
|Attribute UUID|Specify a comma-separated list of attribute UUIDs to which you want to add new tags. Note: If both “Attribute Name“ and “Attribute UUID“ are specified, action will work with “Attribute UUID“ values.|False|String||
|Attribute Search|Specify, where action should search for attributes. If “Provided Event“ is selected, action will only search for attributes or attribute UUIDs in event with ID/UUID provided in “Event ID“ parameter. If “All Events“, action will search for attributes among all events and add sighting for all attributes that match our criteria.|False|List|Provided Event|



##### JSON Results
```json
[{"name": "Global tag unique___test(7) successfully attached to Attribute(9).", "message": "Global tag unique___test(7) successfully attached to Attribute(9).", "url": "/tags/attachTagToObject"}]
```



#### Unset IDS Flag for an Attribute
Unset IDS flag for attributes in MISP
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Attribute Name|Specify a comma-separated list of attribute identifiers for which you want to unset an IDS flag. Note: If both “Attribute Name“ and “Attribute UUID“ are specified, action will work with “Attribute UUID“ values.|False|String||
|Event ID|Specify the ID or UUID of the event, where to seach for attributes. This parameter is required, if “Attribute Search“ is set to “Provided Event“.|False|String||
|Category|Specify a comma-separated list of categories. If specified, action will only unset IDS flag for attributes that have matching category. If nothing is specified, action will ignore categories in attributes. Possible values: External Analysis, Payload Delivery, Artifacts Dropped, Payload Installation.|False|String||
|Type|Specify a comma-separated list of attribute types. If specified, action will only unset IDS flag for attributes that have matching attribute type. If nothing is specified, action will ignore types in attributes. Example values: md5, sha1, ip-src, ip-dst|False|String||
|Attribute Search|Specify, where action should search for attributes. If “Provided Event“ is selected, action will only search for attributes or attribute UUIDs in event with ID/UUID provided in “Event ID“ parameter. If “All Events“, action will search for attributes among all events and unset IDS flag for all attributes that match our criteria.|False|List|Provided Event|
|Attribute UUID|Specify a comma-separated list of attribute UUIDs for which you want to unset an IDS flag. Note: If both “Attribute Name“ and “Attribute UUID“ are specified, action will work with “Attribute UUID“ values.|False|String||



#### Create Url Misp Object
Create a URL Object in MISP. Requires “URL” to be provided or “Use Entities“ parameter set to true.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event ID|Specify the ID or UUID of the event to which you want to add URL objects.|True|String||
|URL|Specify the URL, which you want to add to the event.|False|String||
|Port|Specify the port, which you want to add to the event.|False|String||
|First seen|Specify, when the URL was first seen. Format: 2020-12-22T13:07:32Z|False|String||
|Last seen|Specify, when the URL was last seen. Format: 2020-12-22T13:07:32Z|False|String||
|Domain|Specify the domain, which you want to add to the event.|False|String||
|Text|Specify the additional text, which you want to add to the event.|False|String||
|IP|Specify the IP, which you want to add to the event.|False|String||
|Host|Specify the Host, which you want to add to the event.|False|String||
|Use Entities|If enabled, action will use entities in order to create objects. Supported entities: URL. “Use Entities“ has priority over other parameters.|False|Boolean|false|



##### JSON Results
```json
[{"Object": {"id": "7", "name": "url", "meta-category": "network", "description": "url object describes an url along with its normalized field (like extracted using faup parsing library) and its metadata.", "template_uuid": "60efb77b-40b5-4c46-871b-ed1ed999fce5", "template_version": "8", "event_id": "1", "uuid": "751de0b1-df9a-4154-81fc-bbc0591a1a57", "timestamp": "1595935488", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "first_seen": null, "last_seen": null, "Attribute": [{"id": "24", "event_id": "1", "object_id": "7", "object_relation": "url", "category": "Network activity", "type": "url", "value1": "www.google.com", "value2": "", "to_ids": false, "uuid": "c9bd6348-548e-4dfb-b5f8-978dcf5e7d96", "timestamp": "1595935488", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "www.google.com"}, {"id": "25", "event_id": "1", "object_id": "7", "object_relation": "port", "category": "Network activity", "type": "port", "value1": "35", "value2": "", "to_ids": false, "uuid": "01e9367e-ae63-49d4-ba8f-c539b45a6ee1", "timestamp": "1595935488", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "35"}, {"id": "26", "event_id": "1", "object_id": "7", "object_relation": "ip", "category": "Network activity", "type": "ip-dst", "value1": "1.1.1.7", "value2": "", "to_ids": false, "uuid": "291d75d4-4bda-49ff-8823-26251ca209c2", "timestamp": "1595935488", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "1.1.1.7"}, {"id": "27", "event_id": "1", "object_id": "7", "object_relation": "text", "category": "Other", "type": "text", "value1": "Test", "value2": "", "to_ids": false, "uuid": "177322b9-eda1-462c-9b95-7d3c58a821bb", "timestamp": "1595935488", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "Test"}]}}]
```



#### Enrich Entities
Enrich entities based on the attributes in MISP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Number of attributes to return|Specify how many attributes to return for entities.|True|String|10|
|Filtering condition|Specify the filtering condition for the action. If “Last“ is selected, action will use the oldest attribute for enrichment, if “First“ is selected, action will use the newest attribute for enrichment.|True|List|LAST|
|Create Insights|If enabled, action will generate an insight for every entity that was fully processed.|False|Boolean|true|
|Threat Level Threshold|Specify what should be the threshold for the threat level of the event, where the entity was found. If related event exceeds or matches threshold, entity will be marked as suspicious.|False|List|Low|



##### JSON Results
```json
[{"EntityResult": [{"Event": {"orgc_id": "xx", "ShadowAttribute": [], "id": "xx", "threat_level_id": "xx", "event_creator_email": "john_doe@example.com", "uuid": "5c5bff1b-a414-4a83-8755-035f0a0xxxx", "Object": [], "Orgc": {"uuid": "5c5ac66e-3884-4031-afd7-46f5bb9xxxx", "name": "ORGNAME", "id": "xx"}, "Org": {"uuid": "5c5ac66e-3884-4031-afd7-46f5bb9xxxx", "name": "ORGNAME", "id": "xx"}, "RelatedEvent": [], "sharing_group_id": "0", "timestamp": "1549533154", "date": "2019-02-07", "disable_correlation": "False", "info": "Test event", "locked": "False", "publish_timestamp": "1549533214", "Attribute": [{"category": "Network activity", "comment": "", "uuid": "5c5bffe2-9298-4098-ae31-035d0a00xxxx", "deleted": "False", "timestamp": "1549533154", "to_ids": "False", "distribution": "3", "object_id": "xx", "event_id": "xx", "ShadowAttribute": [], "sharing_group_id": "0", "value": "1.1.xx.xx", "disable_correlation": "False", "object_relation": "None", "type": "ip-src", "id": "xx", "Galaxy": []}], "attribute_count": "1", "org_id": "xx", "analysis": "2", "extends_uuid": "", "published": "True", "distribution": "3", "proposal_email_lock": "False", "Galaxy": []}}], "Entity": "1.1.xx.xx"}]
```



#### Remove Tag from an Attribute
Remove tags from attributes in MISP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Attribute Name|Specify a comma-separated list of attribute identifiers from which you want to remove tags. Note: If both “Attribute Name“ and “Attribute UUID“ are specified, action will work with “Attribute UUID“ values.|False|String||
|Event ID|Specify the ID or UUID of the event, where to search for attributes. This parameter is required, if “Attribute Search“ is set to “Provided Event“ or Object UUID is provided.|False|String||
|Tag Name|Specify a comma-separated list of tags that you want to remove from attributes.|True|String||
|Category|Specify a comma-separated list of categories. If specified, action will only remove tags from attributes that have matching category. If nothing is specified, action will ignore categories in attributes. Possible values: External Analysis, Payload Delivery, Artifacts Dropped, Payload Installation.|False|String||
|Type|Specify a comma-separated list of attribute types. If specified, action will only remove tags from attributes that have matching attribute type. If nothing is specified, action will ignore types in attributes. Example values: md5, sha1, ip-src, ip-dst|False|String||
|Object UUID|Specify the UUID of the object that contains the desired attribute.|False|String||
|Attribute UUID|Specify a comma-separated list of attribute UUIDs from which you want to remove new tags. Note: If both “Attribute Name“ and “Attribute UUID“ are specified, action will work with “Attribute UUID“ values.|False|String||
|Attribute Search|Specify, where action should search for attributes. If “Provided Event“ is selected, action will only search for attributes or attribute UUIDs in event with ID/UUID provided in “Event ID“ parameter. If “All Events“, action will search for attributes among all events and remove tags from all attributes that match our criteria.|False|List|Provided Event|



##### JSON Results
```json
[{"name": "Tag unique___test(7) successfully removed from Attribute(9).", "message": "Tag unique___test(7) successfully removed from Attribute(9).", "url": "/tags/removeTagFromObject"}]
```



#### Add Sighting to an Attribute
Add a sighting to attributes in MISP
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Attribute Name|Specify a comma-separated list of attribute identifiers to which you want to add a new sighting. Note: If both “Attribute Name“ and “Attribute UUID“ are specified, action will work with “Attribute UUID“ values.|False|String||
|Event ID|Specify the ID or UUID of the event, where to search for attributes. This parameter is required, if “Attribute Search“ is set to “Provided Event“.|False|String||
|Category|Specify a comma-separated list of categories. If specified, action will only add sightings to attributes that have matching category. If nothing is specified, action will ignore categories in attributes. Possible values: External Analysis, Payload Delivery, Artifacts Dropped, Payload Installation.|False|String||
|Type|Specify a comma-separated list of attribute types. If specified, action will only add sightings to attributes that have matching attribute type. If nothing is specified, action will ignore types in attributes. Example values: md5, sha1, ip-src, ip-dst|False|String||
|Sightings Type|Specify the type of the Sighting.|True|List|Sighting|
|Source|Specify the source for the sighting. Example: SIEM, SOAR, Siemplify.|False|String||
|Date Time|Specify the date time for the sighting. Format: 2020-02-10 11:00:00.|False|String||
|Object UUID|Specify the uuid of the object that contains the desired attribute|False|String||
|Attribute Search|Specify, where action should search for attributes. If “Provided Event“ is selected, action will only search for attributes or attribute UUIDs in event with ID/UUID provided in “Event ID“ parameter. If “All Events“, action will search for attributes among all events and add sighting for all attributes that match our criteria. |False|List|Provided Event|
|Attribute UUID|Specify a comma-separated list of attribute UUIDs to which you want to add a new sighting. Note: If both “Attribute Name“ and “Attribute UUID“ are specified, action will work with “Attribute UUID“ values. |False|String||



##### JSON Results
```json
[{"Sighting": {"uuid": "12345678-3448-3453-a414-12345678af", "event_id": "XXX", "org_id": "XXX", "source": "Test", "attribute_id": "XXX", "date_sighting": "1588354243", "type": "XXX", "id": "XXX"}}]
```



#### Create Virustotal-Report Object
Create a Virustotal-Report Object in MISP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event ID|Specify the ID or UUID of the event to which you want to add URL objects.|True|String||
|Permalink|Specify the link to the VirusTotal report, which you want to add to the event.|True|String||
|Comment|Specify the comment, which you want to add to the event.|False|String||
|Detection Ratio|Specify the detection ration, which you want to add to the event.|False|String||
|Community Score|Specify the community score, which you want to add to the event.|False|String||
|First Submission|Specify first submission of the event. Format: 2020-12-22T13:07:32Z|False|String||
|Last Submission|Specify last submission of the event. Format: 2020-12-22T13:07:32Z|False|String||



##### JSON Results
```json
{"Object": {"id": "12", "name": "virustotal-report", "meta-category": "misc", "description": "VirusTotal report", "template_uuid": "XXXXXXXXX-e04f-4c34-a2fb-XXXXXXXXX", "template_version": "3", "event_id": "1", "uuid": "XXXXXXXXX-6638-4789-8636-XXXXXXXXX", "timestamp": "1595938006", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "first_seen": null, "last_seen": null, "Attribute": [{"id": "1", "event_id": "1", "object_id": "1", "object_relation": "permalink", "category": "External analysis", "type": "link", "value1": "https://www.virustotal.com/url/__urlsha256__/analysis/XXXXXX/", "value2": "", "to_ids": false, "uuid": "XXXXXXX-2c4d-4198-a8fe-XXXXXXX", "timestamp": "1595938006", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "https://www.virustotal.com/url/__urlsha256__/analysis/XXXXXXX/"}, {"id": "47", "event_id": "1", "object_id": "12", "object_relation": "comment", "category": "External analysis", "type": "text", "value1": "test", "value2": "", "to_ids": false, "uuid": "XXXXXXXX-2993-4975-956b-XXXXXXXX", "timestamp": "1595938006", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "test"}, {"id": "48", "event_id": "1", "object_id": "1", "object_relation": "first-submission", "category": "Other", "type": "datetime", "value1": "0000-00-00T08:08:29.000000+0000", "value2": "", "to_ids": false, "uuid": "XXXXXXX-0ba8-4caf-8a1e-XXXXXXX", "timestamp": "1595938006", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "000-00-00T08:08:29.000000+0000"}, {"id": "49", "event_id": "1", "object_id": "12", "object_relation": "last-submission", "category": "Other", "type": "datetime", "value1": "2014-01-23T09:03:02.000000+0000", "value2": "", "to_ids": false, "uuid": "XXXXXXX-f25c-436a-811d-XXXXXXX", "timestamp": "1595938006", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "2014-01-23T09:03:02.000000+0000"}, {"id": "1", "event_id": "1", "object_id": "1", "object_relation": "detection-ratio", "category": "External analysis", "type": "text", "value1": "1/5", "value2": "", "to_ids": false, "uuid": "XXXXXXX-c8e0-422a-b086-XXXXXXX", "timestamp": "1595938006", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "1/5"}, {"id": "1", "event_id": "1", "object_id": "1", "object_relation": "community-score", "category": "External analysis", "type": "text", "value1": "3", "value2": "", "to_ids": false, "uuid": "XXXXXXX-4109-4eb2-a200-XXXXXXX", "timestamp": "0000038006", "distribution": "5", "sharing_group_id": "0", "comment": "", "deleted": false, "disable_correlation": false, "first_seen": null, "last_seen": null, "value": "1"}]}}
```



#### List Sightings of an Attribute
List available sightings for attributes in MISP
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Attribute Name|Specify a comma-separated list of attribute identifiers for which you want to list sightings. Note: If both “Attribute Name“ and “Attribute UUID“ are specified, action will work with “Attribute UUID“ values.|False|String||
|Event ID|Specify the ID or UUID of the event, where to seach for attributes. This parameter is required, if “Attribute Search“ is set to “Provided Event“.|False|String||
|Category|Specify a comma-separated list of categories. If specified, action will only list sightings for attributes that have matching category. If nothing is specified, action will ignore categories in attributes. Possible values: External Analysis, Payload Delivery, Artifacts Dropped, Payload Installation.|False|String||
|Type|Specify a comma-separated list of attribute types. If specified, action will only list sightings for attributes that have matching attribute type. If nothing is specified, action will ignore types in attributes. Example values: md5, sha1, ip-src, ip-dst|False|String||
|Attribute Search|Specify, where action should search for attributes. If “Provided Event“ is selected, action will only search for attributes or attribute UUIDs in event with ID/UUID provided in “Event ID“ parameter. If “All Events“, action will search for attributes among all events and list sightings for all attributes that match our criteria.|False|List|Provided Event|
|Attribute UUID|Specify a comma-separated list of attribute UUIDs for which you want to list sightings. Note: If both “Attribute Name“ and “Attribute UUID“ are specified, action will work with “Attribute UUID“ values.|False|String||



##### JSON Results
```json
[{"Organisation": {"name": "TESTORG"}, "Sighting": {"uuid": "12345678-3448-4fe7-a414-41940a00xxxx", "event_id": "xx", "org_id": "xx", "source": "Test", "attribute_id": "1xx", "date_sighting": "1584354243", "type": "0", "id": "xx"}}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds









## Connectors
#### MISP - Attributes Connector
Pull attributes from MISP.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|
|CA Certificate File - parsed into Base64 String|CA Certificate File - parsed into Base64 String|False|String||
|API Root|API Root for MISP account.|True|String||
|API Key|API Key of the MISP account.|True|Password|*****|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve attributes from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Max Attributes Per Cycle|How many attributes to process per one connector iteration.|True|Int|50|
|Lowest Threat Level To Fetch|Lowest severity that will be used to fetch alerts. Possible values: 1-4.|True|String|1|
|Attribute Type Filter|Filter attributes by their type, comma separated. If provided, only attributes with whitelisted type will be processed.|False|String||
|Category Filter|Filter attributes by their category, comma separated. If provided, only attributes with whitelisted category will be processed.|False|String||
|Galaxy Filter|Filter attributes by their parent event's galaxy, comma separated. If provided, only attributes that belong to an event with a whitelisted galaxy will be processed.|False|String||
|Verify SSL|If enabled, verify the SSL certificate for the connection to the CheckPoint Cloud Guard server is valid.|False|Boolean|false|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||




