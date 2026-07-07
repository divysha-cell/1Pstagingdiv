
# GoogleCloudIAM

Google Cloud Identity and Access Management (IAM) lets administrators authorize who can take action on specific resources, giving you full control and visibility to manage Google Cloud resources centrally. For enterprises with complex organizational structures, hundreds of workgroups, and many projects, IAM provides a unified view into security policy across your entire organization, with built-in auditing to ease compliance processes.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API root of the Google Cloud IAM instance.|False|String|https://iam.googleapis.com|
|Account Type|Type of the Google Cloud account. Located at the “type” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|String|service_account|
|Project ID|Project ID of the Google Cloud account. Located at the “project_id” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|String||
|Quota Project ID|ID of your Google Cloud project for Google Cloud API usage and billing. If no value is provided, the project ID defined in your Google Cloud service account is used. For this parameter to work, make sure to grant the “Service Usage Consumer” IAM role to your Google Cloud service account.|False|String||
|Private Key ID|Private Key ID of the Google Cloud account. Located at the “private_key_id” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|Password|*****|
|Private Key|Private Key of the Google Cloud account. Located at the “private_key” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|Password|*****|
|Client Email|Client Email of the Google Cloud account. Located at the “client_email” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|String||
|Client ID|Client ID of the Google Cloud account. Located at the “client_id” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|String||
|Auth URI|Auth URI of the Google Cloud account. Located at the “auth_uri” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|String|https://accounts.google.com/o/oauth2/auth|
|Token URI|Token URI of the Google Cloud account. Located at the “token_uri” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|String|https://oauth2.googleapis.com/token|
|Auth Provider X509 URL|Auth Provider X509 URL of the Google Cloud account. Located at the “auth_provider_x509_cert_url” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|String|https://www.googleapis.com/oauth2/v1/certs|
|Client X509 URL|Client X509 URL of the Google Cloud account. Located at the “client_x509_cert_url” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|String||
|Organization ID|ID of the organization that can be used with the Google Cloud IAM integration.|False|String||
|Service Account Json File Content|Optional: Instead of specifying private key id, private key and other parameters, specify here the full JSON content of the service account file. Other connection parameters will be ignored if this parameter is provided.|False|Password|*****|
|Workload Identity Email|A Service Account Client Email to replace the usage of "Service Account Json File Content", which will be used for Impersonation. Note that the SOAR Service Account must be granted the "Service Account Token Creator" IAM role on the User Service Account.|False|String||
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Google Cloud IAM service is valid.|False|Boolean|true|


#### Dependencies
| |
|-|
|google-3.0.0-py2.py3-none-any.whl|
|idna-3.7-py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|pyparsing-3.1.2-py3-none-any.whl|
|beautifulsoup4-4.12.3-py3-none-any.whl|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|google_api_python_client-2.142.0-py2.py3-none-any.whl|
|setuptools-73.0.1-py3-none-any.whl|
|six-1.16.0-py2.py3-none-any.whl|
|certifi-2024.7.4-py3-none-any.whl|
|TIPCommon-1.1.6.1-py2.py3-none-any.whl|
|google_api_core-2.19.1-py3-none-any.whl|
|pyasn1-0.6.0-py2.py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|google_auth-2.34.0-py2.py3-none-any.whl|
|soupsieve-2.6-py3-none-any.whl|
|google_cloud-0.34.0-py2.py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|googleapis_common_protos-1.63.2-py2.py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|proto_plus-1.24.0-py3-none-any.whl|
|protobuf-5.27.3-cp38-abi3-manylinux2014_x86_64.whl|
|pyasn1_modules-0.4.0-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|cachetools-5.5.0-py3-none-any.whl|


## Actions
#### Delete Service Account
Delete service account. Supported entities: Username, Deployment. Note: the supported formats for entities are IAM service account email and resource name.
Timeout - 600 Seconds



#### Get Service Account IAM Policy
Gets the access control policy for the service account. Supported entities: Username, Deployment. Note: the supported formats for entities are IAM service account email and resource name.
Timeout - 600 Seconds



##### JSON Results
```json
[[{"Entity":"XXXXXXXXXX@XXXXXX-XXXXXX-XXXXXXX.iam.gserviceaccount.com","EntityResult":{"version":1,"etag":"XXXXXXX","bindings":[{"role":"roles/iam.XXXXXXX","members":["user:XXXXXX@XXXXXX.XX"]}]}}]]
```



#### Delete Role
Delete a Google Cloud IAM Role.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project ID|Specify the name of the project, where you want to delete the role. If nothing is provided, the project will be extracted from integration configuration.|False|String||
|Role ID|Specify role id for newly created IAM role.|True|String||



##### JSON Results
```json
[{"name": "projects/XXXXXX-XXXXXX/roles/XXXXXXX","role_id":"XXXXXXX","title":"XXXXXX","description": "XXXXX XXXXXX","includedPermissions":["XXXXXXXXXXXX.XXXXXXXXX.XXXX"],"stage":"XX","etag":"XXXXXXXXXXXX"}]
```



#### List Roles
List Google Cloud IAM roles based on the specified search criteria. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project ID|Specify the name of the project, where you want to list the roles. If nothing is provided, the project will be extracted from integration configuration.|False|String||
|View|Specify which view should be used to return role information.|False|List|Basic|
|Max Rows To Return|Specify how many roles the action should return.|False|String|50|
|List Custom Roles Only?|If enabled, action will return only custom roles defined for the current project or orgranization.|False|Boolean|false|
|Show Deleted|If enabled, action will also return deleted roles.|False|Boolean|false|



##### JSON Results
```json
[{"roles":[{"name":"roles/XXXXXX.XXXXX","role_id":"XXXXXXX","title":"XXXXXXXXXXXXXXX","description":"XXXXXXXXXXXXXX","stage":"XXXX","etag":"XXXXX"},{"name":"roles/XXXXXXXXX.XXXXX","role_id":"XXXXXXX","title":"XXXXXXXXXXXXXXX","description":"XXXXXXXXXXXXXX","includedPermissions":["XXXXXXXXXXXXXX.XXXXXXXX.XXXXXXX","XXXXXXXXXXXXXX.XXXXXXXX.XXXXXXX","XXXXXXXXXXXXXX.XXXXXXXX.XXXXXXX","XXXXXXXXXXXXXX.XXXXXXXX.XXXXXXX","XXXXXXXXXXXXXX.XXXXXXXX.XXXXXXX","XXXXXXXXXXXXXX.XXXXXXXX.XXXXXXX"],"stage":"XXXX","etag":"XXXX"}]}]
```



#### Create Service Account
Create a Google Cloud IAM Service Account.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project ID|Specify the name of the project to create service accounts in. If nothing is provided, the project will be extracted from integration configuration.|False|String||
|Service Account ID|Specify service account id to create.|True|String||
|Service Account Display Name|Specify service account display name to create.|False|String||
|Service Account Description|Specify service account description to create.|False|String||



##### JSON Results
```json
[{"name": "XXXXXXXXX/XXXXXXX-XXXXXX-XXXXXXX/XXXXXXXXX/XXXXXXXX@XXXXXX-XXXXXX-XXXXX.XXXX.XXXX.XXX","projectId": "XXXXXX-XXXXX-XXXXX","uniqueId": "XXXXXXXXXXXXXX","email": "XXXXXXXX@XXXXXX-XXXXXX-XXXXXX.XXX.XXXXXXXXX.XXX","displayName": "XXXXXXX","etag": "XXXXXXXXX","oauth2ClientId": "XXXXXXXXXXXXXXXXXX"}]
```



#### Disable Service Account
Disable service account. Supported entities: Username, Deployment. Note: the supported formats for entities are IAM service account email and resource name.
Timeout - 600 Seconds



#### List Service Accounts
List service accounts available in Google Cloud IAM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project ID|Specify the name of the project to list service accounts in. If nothing is provided, the project will be extracted from integration configuration.|False|String||
|Service Account Display Name|Specify service account display name to return. Parameter accepts multiple values as a comma separated string.|False|String||
|Service Account Email|Specify service account email to return. Parameter accepts multiple values as a comma separated string.|False|String||
|Max Rows To Return|Specify how many service accounts the action should return.|False|String|50|



##### JSON Results
```json
[{"accounts":[{"name":"XXXXXXX/XXXXX-XXXXX-XXXXXX/XXXXXXXXX/XXXXXXX-XXXXXX-XXXXXXX-XXXXX@XXXXXX-XXXXXXX-XXXXXXX.XXX.XXXXXXXXXX.XXX","projectId":"XXXXXX-XXXXX-XXXXXX","uniqueId":"XXXXXXXXXXXXXXXXXX","email":"XXXXXX-XXXXXX-XXXXXX-XXXX@XXXXXX-XXXXXX-XXXX.XXX.XXXXXXXXXX.XXX","displayName":"XXXXXXX-XXXXX-XXXXXX-XXXX","etag":"XXXXXXXX","description":"XXXXXXX XXXXX XXXXX XXXXXXX XXXX XXXXX","oauth2ClientId":"XXXXXXXXXXXXXXXXXX"}]}]
```



#### Rotate Service Account Keys
Rotate user-managed keys associated with a service account. During the rotation all existing keys will be deleted and a new key will be created. Supported entities: Username, Deployment. Note: the supported formats for entities are IAM service account email and resource name.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Service Account|A comma-separated list of service accounts for which to rotate keys. This parameter works alongside entities. If provided, the action rotates keys for these specific accounts in addition to any service account entities identified in the action scope.|False|String||



##### JSON Results
```json
[{"Entity": "xxxx","EntityResult": {"name": "xxxx","validAfterTime": "xxxx","validBeforeTime": "xxxx","keyAlgorithm": "xxxx","keyOrigin": "xxxx","keyType": "xxxx"}}]
```



#### Create Role
Create a Google Cloud IAM Role.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project ID|Specify the name of the project, where you want to create the role. If nothing is provided, the project will be extracted from integration configuration.|False|String||
|Role ID|Specify role id for newly created IAM role.|True|String||
|Role Definition|Specify JSON policy document to use as the role definition.|True|String||



##### JSON Results
```json
[{"name": "projects/XXXXXX-XXXXXX/roles/XXXXXXX","role_id":"XXXXXXX","title":"XXXXXX","description":"XXXXX XXXXXX","includedPermissions": ["XXXXXXXXXXXX.XXXXXXXXX.XXXX"],"stage": "XX","etag": "XXXXXXXXXXXX"}]
```



#### Enrich Entities
Enrich Siemplify User entities with service accounts information from Google Cloud IAM. Supported entities: Username, Deployment. Note: the supported formats for entities are IAM service account email and resource name.
Timeout - 600 Seconds



##### JSON Results
```json
[[{"Entity": "XXXX-XXXX@XXXX-XXXX-XXXX.XXX.XXXXXXXXXXXX.XXX","EntityResult": {"name": "XXXXXXX/XXXXXX-XXXXX-XXXXXX/XXXXXXXXXXX/XX-XXXXXXX@XXXXXX-XXXXX-XXXXXX.XXX.XXXXXXXXX.XXX","projectId": "XXXXXX-XXXXXX-XXXXXX","uniqueId": "XXXXXXXXXXXXXXXXXXXXXX","email": "XXXXXX-XXXXXX@XXXXXX-XXXXXX-XXXXXX.XXX.XXXXXXXXXXXX.XXX","displayName": "XXXXX XXXXXX","etag": "XXXXXXXXXX=","oauth2ClientId": "XXXXXXXX","disabled": "true","version": "1","bindings": [{"role": "roles/owner","members": ["XXXX:XXXXXXX.XXXXXX@XXXXXXX.XX"]},{"role": "roles/viewer","members": ["XXXX:XXXX.XXXXXXX@XXXXXXX.XX"]}]}}]]
```



#### Enable Service Account
Enable service account. Supported entities: Username, Deployment. Note: the supported formats for entities are IAM service account email and resource name.
Timeout - 600 Seconds



#### Set Service Account IAM Policy
Sets the access control policy on the specified service account. Supported entities: Username, Deployment. Note: the supported formats for entities are IAM service account email and resource name.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy|Specify JSON policy document to set for service account.|True|String||



##### JSON Results
```json
[{"Entity":"XXXXXXXXXX@XXXXXX-XXXXXX-XXXXXXX.iam.gserviceaccount.com","EntityResult":{"version":1,"etag":"XXXXXXX","bindings":[{"role":"roles/iam.XXXXXXX","members":["user:XXXXXX@XXXXXX.XX"]}]}}]
```



#### Ping
Test connectivity to the Google Cloud IAM service with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









