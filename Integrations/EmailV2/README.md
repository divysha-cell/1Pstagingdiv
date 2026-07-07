
# EmailV2

Email integration over smtp and imap protocols

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Sender's address|None|True|String|user@mail.com|
|Sender's Display Name|None|True|String||
|SMTP Server Address|None|False|IP_OR_HOST|Not yet configured|
|SMTP Port|None|False|String|Not yet configured|
|IMAP Server Address|None|False|IP_OR_HOST|Not yet configured|
|IMAP Port|None|False|String|Not yet configured|
|Username|None|True|String|user@mail.com|
|Password|None|True|Password|*****|
|SMTP USE SSL|None|False|Boolean||
|IMAP USE SSL|None|False|Boolean||
|SMTP Use Authentication|None|False|Boolean||


#### Dependencies
| |
|-|
|red-black-tree-mod-1.20.tar.gz|
|typing_extensions-4.15.0-py3-none-any.whl|
|msoffcrypto_tool-5.4.2-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|pyasn1-0.6.3-py3-none-any.whl|
|lark-1.1.9-py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|html2text-2024.2.26.tar.gz|
|pycparser-3.0-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|anyio-4.13.0-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|beautifulsoup4-4.12.3-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|extract_msg-0.52.0-py3-none-any.whl|
|win_inet_pton-1.1.0-py2.py3-none-any.whl|
|google_auth_httplib2-0.3.0-py3-none-any.whl|
|proto_plus-1.27.1-py3-none-any.whl|
|emaildata-0.3.4-py3-none-any.whl|
|ebcdic-1.1.1-py2.py3-none-any.whl|
|IMAPClient-3.0.1-py2.py3-none-any.whl|
|six-1.16.0-py2.py3-none-any.whl|
|icalendar-6.0.1-py3-none-any.whl|
|pyopenssl-25.3.0-py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|enum34-1.1.10-py3-none-any.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|httplib2-0.31.2-py3-none-any.whl|
|requests_toolbelt-1.0.0-py2.py3-none-any.whl|
|google_api_core-2.30.0-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|tzlocal-5.2-py3-none-any.whl|
|colorclass-2.2.2-py2.py3-none-any.whl|
|TIPCommon-2.3.8-py3-none-any.whl|
|google_auth-2.47.0-py3-none-any.whl|
|soupsieve-2.6-py3-none-any.whl|
|setuptools-80.9.0-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|compressed_rtf-1.0.6.tar.gz|
|easygui-0.98.3-py2.py3-none-any.whl|
|protobuf-6.33.6-cp39-abi3-manylinux2014_x86_64.whl|
|cryptography-46.0.5-cp311-abi3-manylinux_2_34_x86_64.whl|
|idna-3.11-py3-none-any.whl|
|olefile-0.47-py2.py3-none-any.whl|
|certifi-2026.2.25-py3-none-any.whl|
|tzdata-2024.2-py2.py3-none-any.whl|
|PySocks-1.7.1-py3-none-any.whl|
|charset_normalizer-3.4.6-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|oletools-0.60.2-py2.py3-none-any.whl|
|pcodedmp-1.2.6-py2.py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|RTFDE-0.1.2-py3-none-any.whl|
|cachetools-5.5.0-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|google_api_python_client-2.188.0-py3-none-any.whl|
|googleapis_common_protos-1.73.0-py3-none-any.whl|


## Actions
#### Save Email Attachments To Case
Save email attachments from email stored in monitored mailbox to the Case Wall. Requires: IMAP configuration
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Folder Name|Mailbox folder to search email in. Parameter should also accept comma separated list of folders to check the user response in multiple folders.|True|String|Inbox|
|Message ID|Message id to find an email to download attachments from.|False|String||
|Attachment To Save|If parameter is not specified - save all email attachments to the case wall. If parameter specified - save only matching attachment to the case wall.|False|String||



##### JSON Results
```json
{"emails":[{"name": "aaa@aaa.com_1574937477000", "message_id": "<CAHNaB8eum4Tc=fj4U-n42zJNf6hgN6jop+KqG+WC3eGret_ZmA@mail.gmail.com>", "email_uid": 14, "subject": "Test 35", "StartTime": 1574937477000, "EndTime": 1574937477000, "Environment": "Undefined", "body": "Test with attachment", "html_body": "<div>Test with attachment</div>", "text_body": "Test with attachment", "device_product": "Mail", "vendor": "Mail", "event_type": "Mailbox Alert", "from": "uuu@uuu.com", "to": "hhh@hhh.com", "managerReceiptTime": 1574937477000, "original_message": "", "reply_to": "", "answer": "", "url_1": "https://siemplify.co", "url_2": "github.com", "file_1_name": "Test email as MSG.zip", "file_1_md5": "fc0118857de51b68c6c38c71566d9a5c", "file_2_name": "small_jpg.jpg", "file_2_md5": "2c39ce6536da5891e3766005438d3b47", "extra_data_field": "ttt"}, {"name": "aaa@aaa.com_1574937477000", "message_id": "<CAHNaB8eum4Tc=fj4U-n42zJNf6hgN6jop+KqG+WC3eGret_ZmA@mail.gmail.com>", "email_uid": 14, "subject": "Test 35", "StartTime": 1574937477000, "EndTime": 1574937477000, "Environment": "Undefined", "body": "Test with attachment", "html_body": "<div>Test with attachment</div>", "text_body": "Test with attachment", "device_product": "Mail", "vendor": "Mail", "event_type": "Mailbox Alert", "from": "uuu@uuu.com", "to": "hhh@hhh.com", "managerReceiptTime": 1574937477000, "original_message": "", "reply_to": "", "answer": "", "url_1": "https://siemplify.co", "url_2": "github.com", "file_1_name": "Test email as MSG.zip", "file_1_md5": "fc0118857de51b68c6c38c71566d9a5c", "file_2_name": "small_jpg.jpg", "file_2_md5": "2c39ce6536da5891e3766005438d3b47", "extra_data_field": "ttt"}]}
```



#### Forward Email
Forward email including previous messages. Message_id of the email to forward needs to be provided as an action input parameter.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Folder Name|Mailbox folder to search email in. Parameter should also accept comma separated list of folders. Note that you can set mail-specific folders, for example "[Gmail]/All Mail"  to search in all of the folders of Gmail mailbox. Additionally, folder name should match exactly the IMAP folder. If folder contains spaces, folder must be wrapped in double quotes.|True|String|Inbox|
|Message ID of email to forward|message_id value of the email to forward.|True|String||
|Recipients|Arbitrary comma separated list of email addresses for the email recipients.|True|String||
|CC|Arbitrary comma separated list of email addresses to be put in the CC field of email.|False|String||
|BCC|BCC email address. Multiple addresses can be separated by commas.|False|String||
|Subject|The email subject part.|True|String||
|Content|The email body part, if Email HTML Template is set, action should support definition of body of the email with provided HTML template.|False|EmailContent||
|Return message id for the forwarded email|If selected, action returns the message id for the sent email in JSON technical result.|False|Boolean||
|Attachments Paths|Comma separated list of attachments file paths stored on the server for addition to the email.|False|String||



##### JSON Results
```json
{"date": "2019-11-18 08:02:57.984000+00:00", "message_id": "<157406417676.181148.9624253160139989862@C3431448806>", "recipients": "aaa@aaa.com, bbb@bbb.com"}
```



#### Wait for Email from User
Wait for user's response based on an email sent via Send Email action. Note: This is a Siemplify async action, if required, please adjust the async timeout for action (polling timeout) and global action timeout as needed. Action input parameter “Wait stage timeout (minutes)“ cant be larger than global timeout. Note: Please make sure to set IDE timeout as well, as the IDE timeout will override the action’s timeout if the IDE timeout will be shorter. Requires: IMAP configuration
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Email Message_id|Message_id of the email, which current action would be waiting for. If message has been sent using Send Email action, please select SendEmail.JSONResult.message_id field as a placeholder.|True|String||
|Email Date|Send timestamp of the email, which current action would be waiting for. If message has been sent using Send Email action, please select SendEmail.JSONResult.email_date field as a placeholder.|True|String||
|Email Recipients|Comma-separated list of recipient emails, response from which current action would be waiting for. If message has been sent using Send Email action, please select Select SendEmail.JSONResult.recipients field as a placeholder.|True|String||
|Wait stage timeout (minutes)|How long in minutes to wait for the user’s reply before marking it timed out.|True|String|1440|
|Wait for all recipients to reply?|Parameter can be used to define if there are multiple recipients - should the Action wait for responses from all of recipients until timeout, or Action should wait for first reply to proceed.|False|Boolean|True|
|Wait stage exclude pattern|Regular expression to exclude specific replies from the wait stage. Works with body part of email. Example is, to exclude automatic Out-Of-Office emails to be considered as recipient reply, and instead wait for actual user reply|False|String||
|Folder to check for reply|Parameter can be used to specify mailbox email folder (mailbox that was used to send the email with question) to search for the user reply in this folder. Parameter should also accept comma separated list of folders to check the user response in multiple folders. Parameter is case sensitive.|False|String|Inbox|
|Fetch Response Attachments|If selected, if recipient replies with attachment – fetch recipient response and add it as attachment for the action result.|False|Boolean|False|



##### JSON Results
```json
{"Responses": [{"recipient": "aaa@aaa.com", "content": "It's approved, John!"}, {"recipient": "xxx@xxx.com", "content": "I approve going forward on this"}]}
```



#### Send Email
Send email message. Requires: SMTP configuration
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Recipients|Arbitrary comma separated list of email addresses for the email recipients|True|String||
|CC|Arbitrary comma separated list of email addresses to be put in the CC field of email|False|String||
|BCC|BCC email address. Multiple addresses can be separated by commas|False|String||
|Subject|The email subject part|True|String||
|Content|The email body part, if Email HTML Template is set, action should support definition of body of the email with provided HTML template.|True|EmailContent||
|Return message id for the sent email|If selected, action returns the message id for the sent email in JSON technical result. This message id when can be used for the 'Wait for Email from user' action to process user response|False|Boolean||
|Attachments Paths|Comma separated list of attachments file paths stored on the server for addition to the email.|False|String||



##### JSON Results
```json
{"date": "2019-11-18 08:02:57.984000+00:00", "message_id": "<157406417676.181148.9624253160139989862@C3431448806>", "recipients": "aaa@aaa.com, bbb@bbb.com"}
```



#### Delete Email
Delete one or multiple email from the mailbox that matches search criteria. Delete can be done for the first email that matched the search criteria, or it can be done for all matching emails. Requires: IMAP configuration
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Folder Name|Mailbox folder to search email in. Parameter should also accept comma separated list of folders to check the user response in multiple folders.|True|String|Inbox|
|Message IDs|Filter condition, specify emails with which email ids to find. Should accept comma separated list of message ids to search for. If message id is provided, subject, sender, recipient and time filters are ignored.|False|String||
|Subject Filter|Filter condition, specify subject to search for emails.|False|String||
|Sender Filter|Filter condition, specify who should be the sender of needed emails|False|String||
|Recipient Filter|Filter condition, specify who should be the recipient of needed emails|False|String||
|Days Back|Filter condition, specify in what time frame in days should action look for emails to delete. Note - Action works in days granularity only. 0 means it will search for mails from today.|False|String||
|Delete All Matching Emails|Filter condition, specify if action should delete all matched by criteria emails from the mailbox or delete only first match.|False|Boolean|False|



##### JSON Results
```json
{"emails":[{"name": "aaa@aaa.com_1574937477000", "message_id": "<CAHNaB8eum4Tc=fj4U-n42zJNf6hgN6jop+KqG+WC3eGret_ZmA@mail.gmail.com>", "email_uid": 14, "subject": "Test 35", "StartTime": 1574937477000, "EndTime": 1574937477000, "Environment": "Undefined", "body": "Test with attachment", "html_body": "<div>Test with attachment</div>", "text_body": "Test with attachment", "device_product": "Mail", "vendor": "Mail", "event_type": "Mailbox Alert", "from": "uuu@uuu.com", "to": "hhh@hhh.com", "managerReceiptTime": 1574937477000, "original_message": "", "reply_to": "", "answer": "", "url_1": "https://siemplify.co", "url_2": "github.com", "file_1_name": "Test email as MSG.zip", "file_1_md5": "fc0118857de51b68c6c38c71566d9a5c", "file_2_name": "small_jpg.jpg", "file_2_md5": "2c39ce6536da5891e3766005438d3b47", "extra_data_field": "ttt"}, {"name": "aaa@aaa.com_1574937477000", "message_id": "<CAHNaB8eum4Tc=fj4U-n42zJNf6hgN6jop+KqG+WC3eGret_ZmA@mail.gmail.com>", "email_uid": 14, "subject": "Test 35", "StartTime": 1574937477000, "EndTime": 1574937477000, "Environment": "Undefined", "body": "Test with attachment", "html_body": "<div>Test with attachment</div>", "text_body": "Test with attachment", "device_product": "Mail", "vendor": "Mail", "event_type": "Mailbox Alert", "from": "uuu@uuu.com", "to": "hhh@hhh.com", "managerReceiptTime": 1574937477000, "original_message": "", "reply_to": "", "answer": "", "url_1": "https://siemplify.co", "url_2": "github.com", "file_1_name": "Test email as MSG.zip", "file_1_md5": "fc0118857de51b68c6c38c71566d9a5c", "file_2_name": "small_jpg.jpg", "file_2_md5": "2c39ce6536da5891e3766005438d3b47", "extra_data_field": "ttt"}]}
```



#### Send Thread Reply
Send a message as a reply to the email thread.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Message ID|Specify the ID of the message to which you want to send a reply.|True|String||
|Folder Name|Specify a comma-separated list of mailbox folders in which action should search for email. Note: you can set mail-specific folders, for example, "[Gmail]/All Mail" to search in all of the folders of Gmail mailbox. Additionally, folder name should match exactly the IMAP folder. If folder contains spaces, folder must be wrapped in double quotes.|True|String|Inbox|
|Content|Specify the content of the reply.|True|EmailContent||
|Attachment Paths|Specify a comma separated list of attachments file paths stored on the server for addition to the email.|False|String||
|Reply All|If enabled, action will send a reply to all recipients related to the original email. Note: this parameter has priority over "Reply To" parameter.|False|Boolean|true|
|Reply To|Specify a comma-separated list of emails to which you want to send this reply. If nothing is provided and "Reply All" is disabled, action will only send a reply to the sender of the email. If "Reply All" is enabled, action will ignore this parameter.|False|String||



##### JSON Results
```json
{"message_id":"<162556278608.14165.480701790xxxxxxxxxx@siemplify>","recipients":"test@example.com"}
```



#### DownloadEmailAttachments
Download email attachments from email to specific file path on Siemplify server. Requires: IMAP configuration
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Folder Name|Mailbox folder to search email in. Parameter should also accept comma separated list of folders to check the user response in multiple folders|True|String|Inbox|
|Download Path|File path on the server where to download the email attachments|True|String||
|Message IDs|Filter condition, specify emails with which email ids to find. Should accept comma separated multiple message ids. If message id is provided, subject filter is ignored|False|String||
|Subject Filter|Filter condition to search emails by specific subject|False|String||



#### Move Email To Folder
Searches for emails in the source folder, then moves emails matching the search criteria to the target folder. Requires: IMAP configuration
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Source Folder Name|Mailbox folder to search email in. Parameter should also accept comma separated list of folders to check the user response in multiple folders.|True|String|Inbox|
|Destination Folder Name|Destination folder to move emails to|True|String||
|Message IDs|Filter condition, specify emails with which email ids to find. Should accept comma separated multiple message ids. If message id is provided, subject filter is ignored.|False|String||
|Subject Filter|Filter condition, specify what subject to search for emails|False|String||
|Only Unread|Filter condition, specify if search should look only for unread emails|False|Boolean|False|



#### Search Email
Search email messages. Requires: IMAP configuration
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Folder Name|Mailbox folder to search email in. Parameter should also accept comma separated list of folders to check the user response in multiple folders.|True|String|Inbox|
|Subject Filter|Filter condition, specify what subject to search for emails|False|String||
|Sender Filter|Filter condition, specify who should be the sender of needed emails|False|String||
|Recipient Filter|Filter condition, specify who should be the recipient of needed emails|False|String||
|Time frame (minutes)|Filter condition, specify in what time frame in minutes should search look for emails|True|String|60|
|Only Unread|Filter condition, specify if search should look only for unread emails|False|Boolean|False|
|Max Emails To Return|Return max X emails as an action result.|True|String|100|



##### JSON Results
```json
{"emails":[{"name": "aaa@aaa.com_1574937477000", "message_id": "<CAHNaB8eum4Tc=fj4U-n42zJNf6hgN6jop+KqG+WC3eGret_ZmA@mail.gmail.com>", "email_uid": 14, "subject": "Test 35", "StartTime": 1574937477000, "EndTime": 1574937477000, "Environment": "Undefined", "body": "Test with attachment", "html_body": "<div>Test with attachment</div>", "text_body": "Test with attachment", "device_product": "Mail", "vendor": "Mail", "event_type": "Mailbox Alert", "from": "uuu@uuu.com", "to": "hhh@hhh.com", "managerReceiptTime": 1574937477000, "original_message": "", "reply_to": "", "answer": "", "url_1": "https://siemplify.co", "url_2": "github.com", "file_1_name": "Test email as MSG.zip", "file_1_md5": "fc0118857de51b68c6c38c71566d9a5c", "file_2_name": "small_jpg.jpg", "file_2_md5": "2c39ce6536da5891e3766005438d3b47", "extra_data_field": "ttt"}, {"name": "aaa@aaa.com_1574937477000", "message_id": "<CAHNaB8eum4Tc=fj4U-n42zJNf6hgN6jop+KqG+WC3eGret_ZmA@mail.gmail.com>", "email_uid": 14, "subject": "Test 35", "StartTime": 1574937477000, "EndTime": 1574937477000, "Environment": "Undefined", "body": "Test with attachment", "html_body": "<div>Test with attachment</div>", "text_body": "Test with attachment", "device_product": "Mail", "vendor": "Mail", "event_type": "Mailbox Alert", "from": "uuu@uuu.com", "to": "hhh@hhh.com", "managerReceiptTime": 1574937477000, "original_message": "", "reply_to": "", "answer": "", "url_1": "https://siemplify.co", "url_2": "github.com", "file_1_name": "Test email as MSG.zip", "file_1_md5": "fc0118857de51b68c6c38c71566d9a5c", "file_2_name": "small_jpg.jpg", "file_2_md5": "2c39ce6536da5891e3766005438d3b47", "extra_data_field": "ttt"}]}
```



#### Ping
Test Connectivity. Requires: IMAP or SMTP configuration
Timeout - 600 Seconds









## Connectors
#### Generic IMAP Email Connector


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|IMAP Server Address|e.g. imap.gmail.com|True|String||
|IMAP Port|Imap port. e.g. 993|True|Int||
|Username|IMAP Username|True|String||
|Password|IMAP Password|True|Password|*****|
|Folder to check for emails|Parameter can be used to specify email folder on the mailbox to search for the emails. Parameter should also accept comma separated list of folders to check the user response in multiple folders. Parameter is case sensitive.|True|String|Inbox|
|Server Time Zone|The timezone configured in the server, examples (1. UTC, 2. Asia/Jerusalem)|False|String|UTC|
|Environment Field Name|If defined - connector will extract the environment from the specified event field. You can manipulate the field data using the Regex pattern field to extract specific string. In case the the extracted environment field and Siemplify environment name are not equal - you can map them in the map.json that is auto-generated on the first run, inside the <run-folder>.<run-folder> = C:\Siemplify_Server\Scripting\SiemplifyConnectorExecution<Connector_Folder>|False|Int||
|Environment Regex Pattern|If defined - the connector will implement the specific RegEx pattern on the data from "envirnment field" to extract specific string. For example - extract domain from sender's address: "(?<=@)(\S+$)"|False|String||
|IMAP USE SSL|Indicates whether to use ssl on connection or not.|False|Boolean|true|
|Unread Emails Only|If checked, pull only unread mails|False|Boolean|true|
|Mark Emails as Read|If checked, mark mails as read after pulling them|False|Boolean|true|
|Attach Original EML|If checked, attach the original message as eml file.|False|Boolean|false|
|Offset Time In Days|Max number of days to fetch mails since. e.g. 3|True|String|5|
|Max Emails Per Cycle|Max count of mails to pull in one cycle|True|String|10|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|
|Additional headers to extract from emails|Specify additional headers to search and extract from processed emails. Found headers will be added to the email’s Siemplify event. Parameter accepts multiple values as a comma separated string, provided values can be set as an exact match or as a regex, for example, Received:, (Test).*|False|String||
|Exclusion Subject Regex|Exclude emails for which subject matches specified. For example '([N|n]ewsletter)|([O|o]ut of office)' finds all emails containing 'Newsletter' or 'Out of office' keywords.|False|String||
|Exclusion Body Regex|Exclude emails for which body matches specified regex. For example '([N|n]ewsletter)|([O|o]ut of office)' finds all emails containing 'Newsletter' or 'Out of office' keywords.|False|String||
|Original Received Mail Prefix|Prefix to add to the extracted keys (to, from,subject,…) from the original email received in the monitored mailbox.|False|String|orig|
|Attached Mail File Prefix|Prefix to add to the extracted keys (to, from,subject,…) from the attached mail file received with the email in the monitored mailbox.|False|String|attach|
|Create a Separate Siemplify Alert per Attached Mail File?|if enabled, connector will create multiple alerts, 1 alert per attached mail file. This behavior can be useful when processing email with multiple mail files attached and Siemplify event mapping set to create entities from attached mail file.|False|Boolean|false|


##### Allowlist
| |
|-|
|subject: (?<=Subject: ).*|
|to: (?m)(?<=^To: ).*|




