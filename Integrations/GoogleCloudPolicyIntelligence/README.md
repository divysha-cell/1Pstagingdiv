
# GoogleCloudPolicyIntelligence

Google Cloud Policy Intelligence is a service that helps you understand and manage your Google Cloud IAM policies. Policy Intelligence provides a comprehensive view of your policies, including their configuration, relationships, and usage. This information can be used to improve your security posture, optimize your costs, and make better decisions about your cloud resources.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project ID|ID of the project that should be used in Google Cloud Policy Intelligence integration.|False|String||
|API Root|API root of the Google Cloud Policy Intelligence instance.|True|String|https://policyanalyzer.googleapis.com|
|User Service Account|Service account of the Google Cloud Policy Intelligence instance. A full content of the service account JSON file should be provided.|False|Password|*****|
|Quota Project ID|ID of your Google Cloud project for Google Cloud API usage and billing. If no value is provided, the project ID defined in your Google Cloud service account is used. For this parameter to work, make sure to grant the "Service Usage Consumer" IAM role to your Google Cloud service account.|False|String||
|Workload Identity Email|A Service Account Client Email to replace the usage of "User's Service Account", which will be used for Impersonation. Note that the SOAR Service Account must be granted the "Service Account Token Creator" IAM role on the User Service Account.|False|String||
|Location ID|ID of the location that should be used in Google Cloud Policy Intelligence integration. Defaults to ‘global’.|False|String|global|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Google Cloud Policy Intelligence server is valid.|False|Boolean|true|


#### Dependencies
| |
|-|
|charset_normalizer-3.3.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|idna-3.7-py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|pyparsing-3.1.2-py3-none-any.whl|
|beautifulsoup4-4.12.3-py3-none-any.whl|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|google_api_python_client-2.142.0-py2.py3-none-any.whl|
|certifi-2024.7.4-py3-none-any.whl|
|TIPCommon-1.1.6.1-py2.py3-none-any.whl|
|google_api_core-2.19.1-py3-none-any.whl|
|pyasn1-0.6.0-py2.py3-none-any.whl|
|filelock-3.15.4-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|google_auth-2.34.0-py2.py3-none-any.whl|
|tldextract-5.1.2-py3-none-any.whl|
|soupsieve-2.6-py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|googleapis_common_protos-1.63.2-py2.py3-none-any.whl|
|regex-2024.7.24-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|requests_file-2.1.0-py2.py3-none-any.whl|
|proto_plus-1.24.0-py3-none-any.whl|
|protobuf-5.27.3-cp38-abi3-manylinux2014_x86_64.whl|
|pyasn1_modules-0.4.0-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|cachetools-5.5.0-py3-none-any.whl|


## Actions
#### Search Service Account Activity
Search activity related to service accounts in Google Cloud Policy Intelligence.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project ID|Specify the name of the project, where you want to search service account activities. If nothing is provided, the project will be extracted from integration configuration.|False|String||
|Service Account Resource Name|Specify a comma-separated list of service accounts for which you want to fetch activity.|True|String||
|Max Activities To Return|Specify how many activities to return. Maximum: 1000.|True|String|50|



##### JSON Results
```json
[{"Entity": "//iam.googleapis.com/projects/chronicle-demo-env/serviceAccounts/cdir-scc-service-account@chronicle-demo-env.iam.gserviceaccount.com", "EntityResult": [{"fullResourceName": "//iam.googleapis.com/projects/chronicle-demo-env/serviceAccounts/cdir-scc-service-account@chronicle-demo-env.iam.gserviceaccount.com", "activityType": "serviceAccountLastAuthentication", "observationPeriod": {"startTime": "2023-05-23T07:00:00Z", "endTime": "2023-08-20T07:00:00Z"}, "activity": {"lastAuthenticatedTime": "2023-08-20T07:00:00Z", "serviceAccount": {"serviceAccountId": "100969641053678159314", "projectNumber": "105111850896", "fullResourceName": "//iam.googleapis.com/projects/chronicle-demo-env/serviceAccounts/cdir-scc-service-account@chronicle-demo-env.iam.gserviceaccount.com"}}}]}]
```



#### Ping
Test connectivity to the Google Cloud Policy Intelligence with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









