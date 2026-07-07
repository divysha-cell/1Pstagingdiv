
# MicrosoftGraphSecurityTools

Expands on the MicrosoftGraphSecurity integration by providing additional alerting functionality for SOC, along with entity enrichment and remediation actions.
Additional documentation: https://github.com/snags141/SiemplifyIntegration_MicrosoftGraphSecurityTools

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Certificate Password|Optional, if certificate is password-protected, specify the password to open the certificate file.|False|Password|*****|
|Client ID|Client ID from Azure|True|String|clientIdhere|
|Secret ID|Secret ID from Azure|False|Password|*****|
|Tenant ID|Tenant ID from Azure here|True|String|tenantidhere|
|Certificate Path|If authentication based on certificates is  used instead of client secret, specify path to the certificate on Siemplify server|False|String|None|


#### Dependencies
| |
|-|
|PyJWT-2.10.1-py3-none-any.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|urllib3-2.5.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|cryptography-45.0.4-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|cffi-1.17.1-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|pycparser-2.22-py3-none-any.whl|
|typing_extensions-4.14.0-py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|pyopenssl-25.1.0-py3-none-any.whl|


## Actions
#### Delete Message
Delete a message in the specified user's mailbox, or delete a relationship of the message.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Message ID|ID of the message to delete|True|String|someb64=|
|User ID|User ID/userPrincipalName (email) of the user who's mailbox you want to delete a message from. Supports a CSV input to delete from several mailboxes|True|String|john.smith@mail.com|



##### JSON Results
```json
{"status_code": "204", "result": "success", "output_message": "Deletion request completed successfully"}
```



#### Get Message
Get Email Message from a user's inbox
https://docs.microsoft.com/en-us/graph/api/message-get?view=graph-rest-1.0&tabs=http
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User ID|User ID/userPrincipalName (email)|True|String|john.smith@email.com|
|Message ID|ID of the message to retrieve|True|String|AAMkADhMGAAA=|



##### JSON Results
```json
{"@odata.context": "https://graph.microsoft.com/v1.0/$metadata#users('7f180cbb-a5ae-457c-b7e8-6f5b42ba33e7')/messages/$entity", "@odata.etag": "W/\"CQAAABYAAAC4ofQHEIqCSbQPot83AFcbAAAnjjuZ\"", "id": "AAMkADhMGAAA=", "createdDateTime": "2018-09-09T03:15:05Z", "lastModifiedDateTime": "2018-09-09T03:15:08Z", "changeKey": "CQAAABYAAAC4ofQHEIqCSbQPot83AFcbAAAnjjuZ", "categories": [], "receivedDateTime": "2018-09-09T03:15:08Z", "sentDateTime": "2018-09-09T03:15:06Z", "hasAttachments": false, "internetMessageId": "<MWHPR6E1BE060@MWHPR1120.namprd22.prod.outlook.com>", "subject": "9/9/2018: concert", "bodyPreview": "The group represents Nevada.", "importance": "normal", "parentFolderId": "AAMkADcbAAAAAAEJAAA=", "conversationId": "AAQkADOUpag6yWs=", "isDeliveryReceiptRequested": false, "isReadReceiptRequested": false, "isRead": true, "isDraft": false, "webLink": "https://outlook.office365.com/owa/?ItemID=AAMkADMGAAA%3D&exvsurl=1&viewmodel=ReadMessageItem", "inferenceClassification": "focused", "body": {"contentType": "html", "content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n<meta content=\"text/html; charset=us-ascii\">\r\n</head>\r\n<body>\r\nThe group represents Nevada.\r\n</body>\r\n</html>\r\n"}, "sender": {"emailAddress": {"name": "Adele Vance", "address": "adelev@contoso.OnMicrosoft.com"}}, "from": {"emailAddress": {"name": "Adele Vance", "address": "adelev@contoso.OnMicrosoft.com"}}, "toRecipients": [{"emailAddress": {"name": "Alex Wilber", "address": "AlexW@contoso.OnMicrosoft.com"}}], "ccRecipients": [], "bccRecipients": [], "replyTo": [], "flag": {"flagStatus": "notFlagged"}}
```



#### List Attachments
Retrieve a list of attachment objects attached to a message.
https://docs.microsoft.com/en-us/graph/api/message-list-attachments?view=graph-rest-1.0&tabs=http
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User ID|Either email (userPrincipalName) or ID|True|String|john.smith@mail.com|
|Message ID|ID of message to retrieve attachment list from|False|String|None|



##### JSON Results
```json
[{"@odata.type": "#microsoft.graph.fileAttachment", "@odata.mediaContentType": "image/png", "id": "AAMkADY4OWJiOTY5LWZiODItNDNjMy05MjA4LTA2ZTNiMzNkZTg1NQBGAAAAAADi_cDVGMwvSY14bTcuE30PBwBq0FWx2eMAQJKh8wSyz13FAAAAAAEMAABq0FWx2eMAQJKh8wSyz13FAAHfMNGJAAABEgAQAE7nqquOvxZAnwi-XELc2aw=", "lastModifiedDateTime": "2020-11-04T13:57:31Z", "name": "banner.png", "contentType": "image/png", "size": 14061, "isInline": "False", "contentId": "206BF41F95785446BD7BC1721276F923@ausprd01.prod.outlook.com", "contentLocation": "None", "contentBytes": "verylongb64string=="}]
```



#### List Mail Rules
Get all the messageRule objects defined for the user's Inbox.
https://docs.microsoft.com/en-us/graph/api/mailfolder-list-messagerules?view=graph-rest-1.0&tabs=http
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User ID|User ID/userPrincipalName (email)|True|String|john.smith@mail.com|



##### JSON Results
```json
[{"id": "BQCBAcc7hg4=", "displayName": "IBM XForce", "sequence": 1, "isEnabled": "True", "hasError": "False", "isReadOnly": "False", "conditions": {"fromAddresses": [{"emailAddress": {"name": "no-reply@xforce.ibmcloud.com", "address": "no-reply@xforce.ibmcloud.com"}}]}, "actions": {"moveToFolder": "YXNmYWRmd2RzZmZzZmRzYWRmYXNkZmFzZGZhc2RmYXNmYXNmYWZhZ2hmZ2hydGJmZ3ZiZGZzdmZkYWRzZmE=", "stopProcessingRules": "True"}}, {"id": "CQAccc7hg8=", "displayName": "Siemplify", "sequence": 2, "isEnabled": "True", "hasError": "False", "isReadOnly": "False", "conditions": {"fromAddresses": [{"emailAddress": {"name": "user@siemplify.co", "address": "user@siemplify.co"}}]}, "actions": {"moveToFolder": "YXNkZiBhc2RmIGFzZGZhZGZhZGZhc2YgZGFzZnNmIGFoZGZnYXNkIGZnYXNmZGdhZ2RmaHNnZmhhIHNkZ2ZhaHMgZ2ZhaGZnc2YgZ2FzamhkZ2YgYWpzZ2QgZmhnYXNzaGRmZ2E=", "stopProcessingRules": "True"}}]
```



#### Delete Attachment
Delete an attachment from a user's mailbox.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User ID|User ID/userPrincipalName (email)|True|String|john.smith@mail.com|
|Message ID|ID of the message|True|String|someb64=|
|Attachment ID|ID of the attachment to delete.|True|String|someb64=|



##### JSON Results
```json
{"status_code": "204", "result": "success", "output_message": "Deletion request completed successfully"}
```



#### Get User MFA
Search for given user and return MFA stats. Queries a given User Email field including any valid email entities. JSON result will always return your User Email input first at index zero.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Create Insight|Create an insight for each email checked with MFA stats.|False|Boolean|false|
|User Email|Users email address to search for (userPrincipalName). Valid target entities (emails) will also be checked.|True|String|user@email.com|



##### JSON Results
```json
[{"id": "75as5323-a3b6-1234-f86b-30dc4bfb56e1", "userPrincipalName": "john.smith@email.com", "userDisplayName": "John Smith", "isRegistered": "True", "isEnabled": "False", "isCapable": "False", "isMfaRegistered": "True", "authMethods": ["mobilePhone", "appNotification", "appCode"]}, {"id": "d14f12cc-f123-1234-f3c3-a574926bad3c", "userPrincipalName": "Jack.Smith@email.com", "userDisplayName": "Jack Smith", "isRegistered": "True", "isEnabled": "False", "isCapable": "False", "isMfaRegistered": "True", "authMethods": ["mobilePhone", "appNotification", "appCode"]}]
```



#### List Messages
List the messages in a user's mailbox
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query Parameters|Should begin with '$' - See MS Graph docs for query-parameters. EG: $filter=subject eq 'test'|False|String|None|
|Select Filter|CSV list of fields to return, eg: sender,subject|False|String|None|
|User ID|User ID/userPrincipalName (email)|True|String|john.smith@mail.com|



##### JSON Results
```json
[{"@odata.etag": "W/\"CQAAABYAAADHcgC8Hl9tRZ/hc1wEUs1TAAAwR4Hg\"", "id": "AAMkAGUAAAwTW09AAA=", "subject": "You have late tasks!", "sender": {"emailAddress": {"name": "Microsoft Planner", "address": "noreply@Planner.Office365.com"}}}, {"@odata.etag": "W/\"CQAAABYAAADHcgC8Hl9tRZ/hc1wEUs1TAAAq4D1e\"", "id": "AAMkAGUAAAq5QKlAAA=", "subject": "You have late tasks!", "sender": {"emailAddress": {"name": "Microsoft Planner", "address": "noreply@Planner.Office365.com"}}}, {"@odata.etag": "W/\"CQAAABYAAADHcgC8Hl9tRZ/hc1wEUs1TAAAq4D0v\"", "id": "AAMkAGUAAAq5QKkAAA=", "subject": "Your Azure AD Identity Protection Weekly Digest", "sender": {"emailAddress": {"name": "Microsoft Azure", "address": "azure-noreply@microsoft.com"}}}, {"@odata.etag": "W/\"CQAAABYAAADHcgC8Hl9tRZ/hc1wEUs1TAAAq4DsN\"", "id": "AAMkAGUAAAq5QKjAAA=", "subject": "Use attached file", "sender": {"emailAddress": {"name": "Megan Bowen", "address": "MeganB@contoso.OnMicrosoft.com"}}}, {"@odata.etag": "W/\"CQAAABYAAADHcgC8Hl9tRZ/hc1wEUs1TAAAq4Dq9\"", "id": "AAMkAGUAAAq5QKiAAA=", "subject": "Original invitation", "sender": {"emailAddress": {"name": "Megan Bowen", "address": "MeganB@contoso.OnMicrosoft.com"}}}, {"@odata.etag": "W/\"CQAAABYAAADHcgC8Hl9tRZ/hc1wEUs1TAAAq4Dq1\"", "id": "AAMkAGUAAAq5QKhAAA=", "subject": "Koala image", "sender": {"emailAddress": {"name": "Megan Bowen", "address": "MeganB@contoso.OnMicrosoft.com"}}}, {"@odata.etag": "W/\"CQAAABYAAADHcgC8Hl9tRZ/hc1wEUs1TAAAq4Dqp\"", "id": "AAMkAGUAAAq5QKgAAA=", "subject": "Sales invoice template", "sender": {"emailAddress": {"name": "Megan Bowen", "address": "MeganB@contoso.OnMicrosoft.com"}}}, {"@odata.type": "#microsoft.graph.eventMessage", "@odata.etag": "W/\"DAAAABYAAADHcgC8Hl9tRZ/hc1wEUs1TAAAq4Dft\"", "id": "AAMkAGUAAAq5UMVAAA=", "subject": "Accepted: Review strategy for Q3", "sender": {"emailAddress": {"name": "Adele Vance", "address": "/O=EXCHANGELABS/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=A17A02BCF30C4937A87B14273385667C-ADELEV"}}}, {"@odata.type": "#microsoft.graph.eventMessage", "@odata.etag": "W/\"DAAAABYAAADHcgC8Hl9tRZ/hc1wEUs1TAAAq4DfF\"", "id": "AAMkAGUAAAq5UMUAAA=", "subject": "Accepted: Review strategy for Q3", "sender": {"emailAddress": {"name": "Adele Vance", "address": "/O=EXCHANGELABS/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=A17A02BCF30C4937A87B14273385667C-ADELEV"}}}, {"@odata.type": "#microsoft.graph.eventMessage", "@odata.etag": "W/\"CwAAABYAAADHcgC8Hl9tRZ/hc1wEUs1TAAAq4Dfa\"", "id": "AAMkAGUAAAq5T8tAAA=", "subject": "Review strategy for Q3", "sender": {"emailAddress": {"name": "Megan Bowen", "address": "MeganB@contoso.OnMicrosoft.com"}}}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds



##### JSON Results
```json
{}
```









## Connectors
#### MS SecureScore Alert
Allows for easy monitoring of Secure Score. Set a threshold and you will be alerted when the score drops below.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Specify the Secure Score threshold. If your Secure Score drops below this threshold, an alert will be raised.|False|Int|0|
|Tenant ID|Tenant ID  from Azure|True|String|x|
|Secret ID|Secret ID from Azure|True|Password|*****|
|Default Priority|Set the default priority (-1 to 100). Informative = -1, Low = 40, Medium = 60, High = 80, Critical = 100|True|Int|60|
|Client ID|Client ID from Azure|True|String|x|
|Certificate Path|If authentication based on certificates is used instead of client secret, specify path to the certificate on Siemplify server|False|String||
|Certificate Password|Optional, if certificate is password-protected, specify the password to open the certificate file.|False|Password|*****|


#### MS365 MFA Alert
Alert on negative changes to user MFA registration. Use the allowlist to prevent alerts for legacy service accounts that don't support MFA, etc.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Tenant ID|Tenant ID from Azure|True|String|x|
|Self Service Reset Alert|Create alert when a user has the ability to self-service reset their password/MFA.|False|Boolean|false|
|Secret ID|Secret ID from Azure|True|Password|*****|
|MFA Registration Alert|Create alert when a user is not registered for MFA. Recommended.|False|Boolean|true|
|Exclude Guests|Exclude guests/external users from alerts (emails containing #EXT#)|False|Boolean|false|
|Client ID|Client ID from Azure|True|String|x|
|Certificate Path|If authentication based on certificates is used instead of client secret, specify path to the certificate on Siemplify server|False|String||
|Certificate Password|Optional, if certificate is password-protected, specify the password to open the certificate file.|False|Password|*****|




