
# AWSIAMAccessAnalyzer

AWS IAM Access Analyzer is built on Zelkova, which translates IAM policies into equivalent logical statements, and runs a suite of general-purpose and specialized logical solvers (satisfiability modulo theories) against the problem. Access Analyzer applies Zelkova repeatedly to a policy with increasingly specific queries to characterize classes of behaviors the policy allows, based on the content of the policy. To learn more about satisfiability modulo theories, see Satisfiability Modulo Theories. Access Analyzer does not examine access logs to determine whether an external entity accessed a resource within your zone of trust. It generates a finding when a resource-based policy allows access to a resource, even if the resource was not accessed by the external entity. Access Analyzer also does not consider the state of any external accounts when making its determination. That is, if it indicates that account 11112222333 can access your S3 bucket, it knows nothing about the state of users, roles, service control policies (SCP), and other relevant configurations in that account. This is for customer privacy – Access Analyzer doesn't consider who owns the other account. It is also for security – if the account is not owned by the Access Analyzer customer, it is still important to know that an external entity could gain access to their resources even if there are currently no principals in the account that could access the resources. Access Analyzer considers only certain IAM condition keys that external users cannot directly influence, or that are otherwise impactful to authorization. Access Analyzer does not currently report findings from AWS service principals or internal service accounts. In rare cases where Access Analyzer isn't able to fully determine whether a policy statement grants access to an external entity, it errs on the side of declaring a false positive finding. Access Analyzer is designed to provide a comprehensive view of the resource sharing in your account, and strives to minimize false negatives.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|AWS Access Key ID||True|String||
|AWS Secret Key||True|Password|*****|
|AWS Default Region||True|String||
|Analyzer Name||True|String||


#### Dependencies
| |
|-|
|six-1.17.0-py2.py3-none-any.whl|
|pyopenssl-26.2.0-py3-none-any.whl|
|typing_extensions-4.15.0-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|pycparser-3.0-py3-none-any.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|idna-3.15-py3-none-any.whl|
|botocore-1.35.11-py3-none-any.whl|
|jmespath-1.1.0-py3-none-any.whl|
|s3transfer-0.10.4-py3-none-any.whl|
|urllib3-2.7.0-py3-none-any.whl|
|requests-2.34.2-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|cryptography-48.0.0-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|boto3-1.35.11-py3-none-any.whl|


## Actions
#### Archive Finding
Archive finding in AWS IAM Access Analyzer
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Finding ID|Specify ID of the finding that you want to archive.|True|String||



#### Scan Resources
Scan resources using AWS IAM Access Analyzer.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Resource ARNs|Specify a comma-separated list of resource ARNs that need to be scanned.|True|String||



##### JSON Results
```json
[{"resources": [{"analyzedAt": 1606289201000, "isPublic": "True", "resourceArn": "arn:aws:s3:::accessanalyzerXXX", "resourceOwnerAccount": "XXXXXXXXXXX", "resourceType": "AWS::S3::Bucket"}]}]
```



#### Ping
Test connectivity to AWS IAM Access Analyzer with parameters provided at the integration configuration page on Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### AWS IAM Access Analyzer - Findings Connector
Pull findings from AWS IAM Access Analyzer. Note: Whitelist works on resource types.Example: AWS::S3::Bucket.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|AWS Access Key ID|AWS Access Key ID to use in integration.|True|String||
|AWS Secret Key|AWS Secret Key to use in integration.|True|Password|*****|
|AWS Default Region|AWS default region to use in integration, for example us-west-2.|True|String||
|Analyzer Name|Name of the analyzer that should be used in the integration.|True|String||
|Alert Severity|Severity of the Siemplify Alerts created from this connector. Possible values: Critical, High, Medium , Low, Informational.|False|String|Medium|
|Max Findings To Fetch|How many findings to process per one connector iteration.|False|Int|50|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve findings from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the AWS IAM Access Analyzer server is valid.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




