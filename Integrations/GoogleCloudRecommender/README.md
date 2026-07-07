
# GoogleCloudRecommender

Google Cloud Recommender is a service that provides recommendations and insights for using resources on Google Cloud. These recommendations and insights are per-product or per-service, and are generated based on heuristic methods, machine learning, and current resource usage. Currently integration supports insights only from google.iam.policy.Recommender recommender.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API root of the Google Recommender service.|True|String|https://recommender.googleapis.com/v1/|
|Resource Manager API Root|API root of the Google Cloud Resource Manager service.|True|String|https://cloudresourcemanager.googleapis.com/v3/|
|Organization ID|ID of the organization that can be used with the Cloud Recommender integration.|False|String||
|Project ID|ID of the project that should be used in the integration. Takes priority over Organization ID, if both are provided.|False|String||
|Quota Project ID|ID of your Google Cloud project for Google Cloud API usage and billing. If no value is provided, the project ID defined in your Google Cloud service account is used. For this parameter to work, make sure to grant the “Service Usage Consumer” IAM role to your Google Cloud service account.|False|String||
|Workload Identity Email|A Service Account Client Email to replace the usage of "User's Service Account", which will be used for Impersonation. Note that the SOAR Service Account must be granted the "Service Account Token Creator" IAM role on the User Service Account.|False|String||
|User Service Account|Service account of the Google Recommender service. A full content of the service account JSON file should be provided. This or "Workload Identity Email" must be provided.|False|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Google Recommender service is valid.|False|Boolean|true|


#### Dependencies
| |
|-|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|beautifulsoup4-4.12.3-py3-none-any.whl|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|google_api_python_client-2.142.0-py2.py3-none-any.whl|
|certifi-2024.7.4-py3-none-any.whl|
|TIPCommon-1.1.6.1-py2.py3-none-any.whl|
|google_api_core-2.19.1-py3-none-any.whl|
|pyasn1-0.6.0-py2.py3-none-any.whl|
|pyparsing-3.1.4-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|google_auth-2.34.0-py2.py3-none-any.whl|
|soupsieve-2.6-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|idna-3.8-py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|googleapis_common_protos-1.63.2-py2.py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|proto_plus-1.24.0-py3-none-any.whl|
|protobuf-5.27.3-cp38-abi3-manylinux2014_x86_64.whl|
|pyasn1_modules-0.4.0-py3-none-any.whl|
|cachetools-5.5.0-py3-none-any.whl|


## Actions
#### List Recommendations
List available recommendations in the Google Cloud Recommender service. Note 1: This action doesn’t run on Chronicle SOAR entities. Note 2: Currently action returns insights only from google.iam.policy.Recommender recommender.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Recommendation Filter|Specify the filter to fetch the recommendations for. Parameter expects a string of a format "<projects or organizations>/<project or organization name or id>" or "//cloudresourcemanager.googleapis.com/<projects or organizations>/<project or organization name or id>" for which to fetch the recommendations for. If nothing is provided - action will take the project id from the service account configured.|False|String||
|Recommendation Location|Specify the GCP location to fetch recommendations for.|True|String|global|
|Recommendation State|Specify the recommendation state to return.|False|List|Not Specified|
|Recommendation Priority|Specify the recommender priority to return, multiple values can be specified as a comma separated string.|False|String||
|Recommender Subtype|Specify the recommender subtype to return.|False|List|Not Specified|
|Max Records To Return|Specify how many records to return. If nothing is provided, action will return 50 records.|False|String|50|



##### JSON Results
```json
[{"name": "name", "description": "This role has not been used during the observation window.", "lastRefreshTime": "2023-07-27T07:00:00Z", "primaryImpact": {"category": "SECURITY", "securityProjection": {"details": {"revokedIamPermissionsCount": 68}}}, "content": {"operationGroups": [{"operations": [{"action": "remove", "resourceType": "cloudresourcemanager.googleapis.com/Project", "resource": "//cloudresourcemanager.googleapis.com/projects", "path": "/iamPolicy/bindings/*/members/*", "pathFilters": {"/iamPolicy/bindings/*/condition/expression": "", "/iamPolicy/bindings/*/members/*": "serviceAccount:test-333", "/iamPolicy/bindings/*/role": "roles/monitoring.admin"}}]}], "overview": {"resource": "//cloudresourcemanager.googleapis.com/", "member": "serviceAccount:test-333", "removedRole": "roles/monitoring.admin", "minimumObservationPeriodInDays": "0"}}, "stateInfo": {"state": "ACTIVE"}, "etag": "", "recommenderSubtype": "REMOVE_ROLE", "associatedInsights": [{"insight": "projects/i/locations/global/insightTypes/"}], "priority": "P4"}, {"name": "name", "description": "This role has not been used during the observation window.", "lastRefreshTime": "2023-07-27T07:00:00Z", "primaryImpact": {"category": "SECURITY", "securityProjection": {"details": {"revokedIamPermissionsCount": 5}}}, "content": {"operationGroups": [{"operations": [{"action": "remove", "resourceType": "cloudresourcemanager.googleapis.com/Project", "resource": "//cloudresourcemanager.googleapis.com/projects/8", "path": "/iamPolicy/bindings/*/members/*", "pathFilters": {"/iamPolicy/bindings/*/condition/expression": "", "/iamPolicy/bindings/*/members/*": "user:demo@demo.com", "/iamPolicy/bindings/*/role": "roles/chroniclesm.admin"}}]}], "overview": {"resource": "//cloudresourcemanager.googleapis.com/projects", "member": "user:demo@demo.com", "removedRole": "roles/chroniclesm.admin", "minimumObservationPeriodInDays": "0"}}, "stateInfo": {"state": "ACTIVE"}, "etag": "", "recommenderSubtype": "REMOVE_ROLE", "associatedInsights": [{"insight": "projects"}], "priority": "P4"}]
```



#### Get Recommendation
Get specific recommendation from the Google Cloud Recommender service. Note 1: This action doesn’t run on Chronicle SOAR entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Recommendation Name|Specify the recommendation name to return. Action accepts multiple values as a comma separated string. Example of expected input: projects/projectname/locations/global/recommenders/google.iam.policy.Recommender/recommendations/0f262740-bf4a-4c3d-9573-0da3345cf3f7|True|String||



##### JSON Results
```json
[{"name": "name", "description": "This role has not been used during the observation window.", "lastRefreshTime": "2023-07-28T07:00:00Z", "primaryImpact": {"category": "SECURITY", "securityProjection": {"details": {"revokedIamPermissionsCount": 68}}}, "content": {"operationGroups": [{"operations": [{"action": "remove", "resourceType": "cloudresourcemanager.googleapis.com/Project", "resource": "//cloudresourcemanager.googleapis.com/projects/xxxxxxx", "path": "/iamPolicy/bindings/*/members/*", "pathFilters": {"/iamPolicy/bindings/*/condition/expression": "", "/iamPolicy/bindings/*/members/*": "serviceAccount:test@-test-project.iam.gserviceaccount.com", "/iamPolicy/bindings/*/role": "roles/monitoring.admin"}}]}], "overview": {"resource": "//cloudresourcemanager.googleapis.com/projects/xxxxxx", "member": "serviceAccount:test-@-test-project.iam.gserviceaccount.com", "removedRole": "roles/monitoring.admin", "minimumObservationPeriodInDays": "0"}}, "stateInfo": {"state": "ACTIVE"}, "etag": "", "recommenderSubtype": "REMOVE_ROLE", "associatedInsights": [{"insight": "projects/xxxxxx/locations/global/insightTypes/google.iam.policy.Insight/insights/"}], "priority": "P4"}]
```



#### Update Recommendation
Update recommendation in the Google Cloud Recommender service. Note 1: This action doesn’t run on Chronicle SOAR entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Recommendation Name|Specify the recommendation name to update. Action accepts multiple values as a comma separated string. Example of expected input: projects/projectname/locations/global/recommenders/google.iam.policy.Recommender/recommendations/0f262740-bf4a-4c3d-9573-0da3345cf3f7|True|String||
|Recommendation State|Specify the state for the recommendation to change to.|False|List|Not Specified|
|Recommendation Result|Specify the result for the recommendation to change to.|False|List|Not Specified|



##### JSON Results
```json
[{"name": "name", "description": "This role has not been used during the observation window.", "lastRefreshTime": "2023-07-28T07:00:00Z", "primaryImpact": {"category": "SECURITY", "securityProjection": {"details": {"revokedIamPermissionsCount": 68}}}, "content": {"operationGroups": [{"operations": [{"action": "remove", "resourceType": "cloudresourcemanager.googleapis.com/Project", "resource": "//cloudresourcemanager.googleapis.com/projects/xxxxxxx", "path": "/iamPolicy/bindings/*/members/*", "pathFilters": {"/iamPolicy/bindings/*/condition/expression": "", "/iamPolicy/bindings/*/members/*": "serviceAccount:test@-test-project.iam.gserviceaccount.com", "/iamPolicy/bindings/*/role": "roles/monitoring.admin"}}]}], "overview": {"resource": "//cloudresourcemanager.googleapis.com/projects/xxxxxx", "member": "serviceAccount:test-@-test-project.iam.gserviceaccount.com", "removedRole": "roles/monitoring.admin", "minimumObservationPeriodInDays": "0"}}, "stateInfo": {"state": "ACTIVE"}, "etag": "", "recommenderSubtype": "REMOVE_ROLE", "associatedInsights": [{"insight": "projects/xxxxxx/locations/global/insightTypes/google.iam.policy.Insight/insights/"}], "priority": "P4"}]
```



#### Apply IAM Recommendations
Apply IAM Recommendations based on provided input. Action works only with google.iam.policy.Recommender recommendations.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|IAM Recommendations JSON|Specify the JSON of the recommendation to apply to. JSON can be provided as a placeholder from “List Recommendations” or “Get Recommendation” actions.|True|String||



##### JSON Results
```json
{"applied_recommendations": [{"name": "projects/432593839568/locations/global/recommenders/google.iam.policy.Recommender/recommendations/217d3019-bae5-4a52-9968-787fdd546a53", "description": "Replace the current role with a smaller role to cover the permissions needed.", "lastRefreshTime": "2023-07-28T07:00:00Z", "primaryImpact": {"category": "SECURITY", "securityProjection": {"details": {"revokedIamPermissionsCount": 610}}}, "content": {"operationGroups": [{"operations": [{"action": "add", "resourceType": "cloudresourcemanager.googleapis.com/Project", "resource": "//cloudresourcemanager.googleapis.com/projects/432593839568", "path": "/iamPolicy/bindings/*/members/-", "value": "user:xxx@domain.com", "pathFilters": {"/iamPolicy/bindings/*/condition/expression": "", "/iamPolicy/bindings/*/role": "roles/compute.instanceAdmin"}}, {"action": "remove", "resourceType": "cloudresourcemanager.googleapis.com/Project", "resource": "//cloudresourcemanager.googleapis.com/projects/432593839568", "path": "/iamPolicy/bindings/*/members/*", "pathFilters": {"/iamPolicy/bindings/*/condition/expression": "", "/iamPolicy/bindings/*/members/*": "user:xxx@domain.com", "/iamPolicy/bindings/*/role": "roles/compute.admin"}}]}], "overview": {"resource": "//cloudresourcemanager.googleapis.com/projects/432593839568", "member": "user:xxx@domain.com", "removedRole": "roles/compute.admin", "addedRoles": ["roles/compute.instanceAdmin"], "minimumObservationPeriodInDays": "0"}}, "stateInfo": {"state": "SUCCEEDED", "stateMetadata": {"applied_by": "bulk_apply_by_automated_script-2023-08-11"}}, "etag": "\"892d57ee41baa03e\"", "recommenderSubtype": "REPLACE_ROLE", "associatedInsights": [{"insight": "projects/432593839568/locations/global/insightTypes/google.iam.policy.Insight/insights/c184ecb2-421e-4e31-9fb6-99676def157e"}], "priority": "P4"}, {"name": "projects/432593839568/locations/global/recommenders/google.iam.policy.Recommender/recommendations/1ecb46c3-9f3e-4dfc-bc87-fecbe2d2ac43", "description": "Replace the current role with a smaller role to cover the permissions needed.", "lastRefreshTime": "2023-07-28T07:00:00Z", "primaryImpact": {"category": "SECURITY", "securityProjection": {"details": {"revokedIamPermissionsCount": 19}}}, "content": {"operationGroups": [{"operations": [{"action": "add", "resourceType": "cloudresourcemanager.googleapis.com/Project", "resource": "//cloudresourcemanager.googleapis.com/projects/432593839568", "path": "/iamPolicy/bindings/*/members/-", "value": "user:yyy@domain.com", "pathFilters": {"/iamPolicy/bindings/*/condition/expression": "", "/iamPolicy/bindings/*/role": "roles/storage.objectAdmin"}}, {"action": "remove", "resourceType": "cloudresourcemanager.googleapis.com/Project", "resource": "//cloudresourcemanager.googleapis.com/projects/432593839568", "path": "/iamPolicy/bindings/*/members/*", "pathFilters": {"/iamPolicy/bindings/*/condition/expression": "", "/iamPolicy/bindings/*/members/*": "user:yyy@domain.com", "/iamPolicy/bindings/*/role": "roles/storage.admin"}}]}], "overview": {"resource": "//cloudresourcemanager.googleapis.com/projects/432593839568", "member": "user:yyy@domain.com", "removedRole": "roles/storage.admin", "addedRoles": ["roles/storage.objectAdmin"], "minimumObservationPeriodInDays": "0"}}, "stateInfo": {"state": "SUCCEEDED", "stateMetadata": {"applied_by": "bulk_apply_by_automated_script-2023-08-11"}}, "etag": "\"af7635ffeb512998\"", "recommenderSubtype": "REPLACE_ROLE", "associatedInsights": [{"insight": "projects/432593839568/locations/global/insightTypes/google.iam.policy.Insight/insights/bdaf418b-99a3-4676-b24c-e850114795c9"}], "priority": "P4"}], "failed_recommendations": []}
```



#### Ping
Test connectivity to the Google Recommender service with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









