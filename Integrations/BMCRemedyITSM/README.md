
# BMCRemedyITSM

BMC Remedy ITSM is industry-leading, service management that transforms the best-practice ITSM principles you've come to appreciate from Remedy to provide unprecedented ROI on your choice of cloud.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https://{IP}:{port}|
|Username||True|String||
|Password||True|Password|*****|
|Verify SSL||False|Boolean|true|


#### Dependencies
| |
|-|
|typing_extensions-4.15.0-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|TIPCommon-2.2.1-py2.py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|pyasn1-0.6.3-py3-none-any.whl|
|google_api_python_client-2.196.0-py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|pycparser-3.0-py3-none-any.whl|
|google_auth-2.53.0-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|anyio-4.13.0-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|protobuf-7.34.1-py3-none-any.whl|
|google_api_core-2.30.3-py3-none-any.whl|
|idna-3.15-py3-none-any.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|httplib2-0.31.2-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|google_auth_httplib2-0.4.0-py3-none-any.whl|
|googleapis_common_protos-1.75.0-py3-none-any.whl|
|urllib3-2.7.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|proto_plus-1.28.0-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|cryptography-48.0.0-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|h11-0.16.0-py3-none-any.whl|


## Actions
#### Wait For Incident Fields Update
Wait for incident fields update in BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident ID|Specify the ID of the incident that needs to be updated.|True|String||
|Status|Specify what is the expected status for the incident.|False|List|Select One|
|Fields To Check|Specify a JSON object containing all of the needed fields and values. Note: this parameter has priority over "Status" field.|False|String|{"field":"value"}|
|Fail If Timeout|If enabled, action will be failed, if not all of the fields were updated.|False|Boolean|true|



##### JSON Results
```json
{"Request ID": "INC00xxxxxxxxxx|INC00xxxxxxxxxx", "Submitter": "Test", "Submit Date": "2022-01-06T12:58:51.000+0000", "Assignee Login ID": "Mxxx", "Last Modified By": "Remedy Application Service", "Last Modified Date": "2022-01-06T12:58:51.000+0000", "Status": "Assigned", "Status-History": {"New": {"user": "Test", "timestamp": "2022-01-06T12:58:51.000+0000"}, "Assigned": {"user": "Test", "timestamp": "2022-01-06T12:58:51.000+0000"}}, "Assignee Groups": "1000000xxx;1000000xxx;'Allen';", "InstanceId": "AGGAA5V0G207EARF074Dxxxxxxxxxx", "Vendor Assignee Groups": null, "Vendor Assignee Groups_parent": null, "Assignee Groups_parent": "", "Product Categorization Tier 1": null, "Product Categorization Tier 2": null, "Product Categorization Tier 3": null, "Department": "Customer Service", "Site Group": "United States", "Region": "Americas", "Product Name": null, "Manufacturer": null, "Product Model/Version": null, "Site": "Headquarters, Building 1.31", "SRAttachment": null, "Created_By": null, "MaxRetries": null, "z1D_Command": null, "AccessMode": null, "z1D_WorklogDetails": null, "z1D_Char02": null, "z1D_FormName": null, "AppInstanceServer": null, "SRInstanceID": "NA", "zTmpEventGUID": null, "AppInterfaceForm": null, "Entry ID": "INC00xxxxxxxxxx", "z1D_Activity_Type": null, "z1D_Summary": null, "z1D_Details": null, "z1D_Secure_Log": null, "z1D_View_Access": null, "z2AF_Act_Attachment_1": null, "Protocol": null, "AppLogin": null, "AppPassword": null, "PortNumber": null, "SRMS Registry Instance ID": null, "SRMSAOIGuid": null, "SRID": null, "TemplateID": null, "z1D_CommunicationSource": null, "z1D_ActivityDate_tab": null, "Last _Assigned_Date": null, "z1D_AssociationDescription": null, "Component_ID": null, "mc_ueid": null, "cell_name": null, "policy_name": null, "status_incident": null, "status_reason2": null, "root_component_id_list": null, "root_incident_id_list": null, "Impact_OR_Root": null, "bOrphanedRoot": null, "use_case": null, "ClientLocale": null, "ServiceCI": null, "HPD_CI": null, "ServiceCI_ReconID": null, "HPD_CI_ReconID": null, "z1D_CI_FormName": null, "Previous_ServiceCI_ReconID": null, "Previous_HPD_CI_ReconID": null, "z1D_SR_Instanceid": null, "Direct Contact Corporate ID": null, "KMSGUID": null, "HPD_CI_FormName": null, "z1D_InterfaceAction": null, "z1D_WorkInfoSubmitter": null, "Direct Contact Login ID": null, "Customer Login ID": "Allen", "AttachmentSourceFormName": null, "AttachmentSourceGUID": null, "z1D_ConfirmGroup": null, "z1D_CreatedFromBackEndSynchWI": null, "InfrastructureEventType": "null", "policy_type": null, "Chat Session ID": null, "Modified Chat Session ID": null, "Auto Open Session": null, "TimeOfEvent": null, "FirstWIPDate": null, "LastWIPDate": null, "Broker Vendor Name": null, "Description": "Try One", "Company": "Calbro Services", "Country": "United States", "State Province": "New York", "City": "New York", "Organization": "Information Technology", "Assigned Support Organization": "IT Support", "Last Name": "Allbrook", "First Name": "Allen", "Middle Initial": null, "Contact Client Type": "Office-Based Employee", "VIP": "No", "Contact Sensitivity": "Standard", "Desk Location": null, "Mail Station": null, "Street": "1114 Eighth Avenue, 31st Floor", "Zip/Postal Code": "10xxx", "Internet E-mail": "test@example.com", "Corporate ID": null, "Phone Number": "1 212 xxx-xxxx (11)", "z1D Char01": null, "Categorization Tier 1": null, "Categorization Tier 2": null, "Categorization Tier 3": null, "z1D Char02": null, "Site ID": "STE_SOxxxxxxxxx", "z1D Action": null, "Assigned Group ID": "SGP00xxxxxxxxxx", "Person ID": "PPL00xxxxxxxxxx", "Contact Company": "Calbro Services", "Service Type": "User Service Restoration", "Status_Reason": null, "Detailed Decription": null, "Resolution": null, "Incident Number": "INC00xxxxxxxxxx", "Urgency": "1-Critical", "Impact": "1-Extensive/Widespread", "Priority": "Critical", "Priority Weight": 29, "Reported Source": "Direct Input", "Assigned Group": "Service Desk", "Assignee": "Mary Mann", "Assigned Support Company": "Calbro Services", "Assigned Group Shift Name": null, "Assigned Group Shift ID": null, "Owner Support Organization": "IT Support", "Number of Attachments": null, "Vendor Name": null, "Owner Group": "Service Desk", "Owner Support Company": "Calbro Services", "Owner Group ID": "SGP00xxxxxxxxxx", "Reported Date": "2022-01-06T12:58:51.000+0000", "Responded Date": "2022-01-06T12:58:51.000+0000", "Last Acknowledged Date": null, "Last Resolved Date": null, "Closed Date": null, "Vendor Ticket Number": null, "z1D Permission Group ID": null, "z1D Permission Group List": null, "Resolution Category": null, "Direct Contact Internet E-mail": null, "Vendor Organization": null, "Vendor Group": null, "Vendor Group ID": null, "Total Transfers": 1, "Resolution Method": null, "Resolution Category Tier 2": null, "Resolution Category Tier 3": null, "Closure Product Category Tier1": null, "Closure Product Category Tier2": null, "Closure Product Category Tier3": null, "Closure Product Name": null, "Closure Product Model/Version": null, "Closure Manufacturer": null, "Estimated Resolution Date": null, "Required Resolution DateTime": null, "Direct Contact Company": null, "Direct Contact Last Name": null, "Direct Contact First Name": null, "Direct Contact Middle Initial": null, "Direct Contact Phone Number": null, "Direct Contact Organization": null, "Direct Contact Department": null, "Direct Contact Region": null, "Direct Contact Site Group": null, "Direct Contact Site": null, "Direct Contact Person ID": null, "Direct Contact Street": null, "Direct Contact Country": null, "Direct Contact State/Province": null, "Direct Contact City": null, "Direct Contact Zip/Postal Code": null, "Direct Contact Time Zone": null, "Direct Contact Desk Location": null, "Direct Contact Mail Station": null, "Direct Contact Location Details": null, "Direct Contact Site ID": null, "Direct Contact Country Code": null, "Direct Contact Area Code": null, "Direct Contact Local Number": null, "Direct Contact Extension": null}
```



#### Delete Incident
Delete an incident in BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident ID|Specify the id of the incident that needs to be deleted.|True|String||



#### Get Incident Details
Get detailed information about the incidents from BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident IDs|Specify the ids of incidents for which you want to return details.|True|String||
|Fields To Return|Specify what fields to return. If invalid fields are provided, action will fail. If nothing is provided, action will return all fields.|False|String||
|Fetch Work Notes|If enabled, action will return work notes related to the incident.|False|Boolean|true|
|Max Work Notes To Return|Specify how many Work Notes to return. If nothing is provided, action will return 50 Work Notes.|False|String|50|



##### JSON Results
```json
[{"Work Log ID": "WLG00000xxxxxx", "Submitter": "Admin", "Submit Date": "2022-01-06T10:42:43.000+0000", "Assigned To": null, "Last Modified By": "Admin", "Last Modified Date": "2022-01-06T10:42:43.000+0000", "Status": "Enabled", "Short Description": ".", "Status History": null, "Assignee Groups": "", "Worknotes": [{"Submitter": "Admin", "Detailed Description": "asdasd", "Work Log Type": "Working Log", "Work Log Submit Date": "2022-01-06T11:21:56.000+0000"}, {"Submitter": "Demo", "Detailed Description": "Work Log Entry from Bob.", "Work Log Type": "Customer Communication", "Work Log Submit Date": "2008-11-07T00:30:41.000+0000"}]}]
```



#### Delete Record
Delete a record in BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Record Type|Specify the type of the record that needs to be deleted.|True|String||
|Record ID|Specify the id of the record that needs to be deleted.|True|String||



#### Get Record Details
Get detailed information about the record from BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Record Type|Specify the type of the record for which you want to retrieve details.|True|String||
|Record IDs|Specify the ids of records for which you want to return details.|True|String||
|Fields To Return|Specify what fields to return. If invalid fields are provided, action will fail. If nothing is provided, action will return all fields.|False|String||



##### JSON Results
```json
[{"Request ID": "CRQ_CAL_100xxxx", "Assignee Groups": "1000xxxxx;", "Vendor Assignee Groups": "1000xxxxx;", "VENDOR_ASSIGNEE_GROUPS_PARENT": "", "ASSIGNEE_GROUPS_PARENT": "", "RootRequestID": " ", "RootRequestName": " ", "Product Categorization Tier 1": "Hardware", "Product Categorization Tier 2": "Component", "Product Categorization Tier 3": "Memory", "Department": "Customer Service", "Site Group": " ", "Region": " ", "LookupKeyword": "MAINCHANGE", "Product Name": null, "Manufacturer": " ", "Product Model/Version": " ", "Escalated?": "No", "Site": "Headquarters, Building 1.32", "Last Modified Date": "2008-11-07T05:25:45.000+0000", "Create-Date": "2008-11-07T05:25:45.000+0000", "FORMNAME": "View CHG:Infrastructure Change", "appInstanceId": "AG00123F73Cxxxxxxxx", "ConsolidatedStatus": "Completed", "ConsolidatedStatusReason": null, "TicketType": "Change", "Abstract_KDB": " ", "LastModifiedBy_Request": "Remedy Application Service", "Submitter_Request": "Remedy Application Service", "EntryID": "CRQ00xxxxxxxx", "Service": null, "CI": " ", "ServiceCI_ReconID": null, "ServiceCI_Class": null, "z1D_ConfirmGroup": null, "Description": "Increase RAM on network file server.", "Company": "Calbro Services", "Assignee Organization": " ", "Last Name": "Baxter", "First Name": "Bob", "Internet Email": " ", "Phone Number Business": " ", "Categorization Tier 1": "Request", "Categorization Tier 2": "Hardware", "Categorization Tier 3": "Add", "Assignee Group ID": "SGP000xxxxxxx", "Requester_Company": " ", "Urgency": "3-Medium", "Impact": "4-Minor/Localized", "Priority": "Medium", "Priority Weight": null, "Assignee Group": "Frontoffice Support", "Assignee": "Ian Plyment", "ID": "CRQ_CAL_100xxxxx", "Investigation Justification": " ", "Vendor Phone": " ", "Assignee Company": "Calbro Services", "Requestor ID": "Bob", "Requester_Group_Name": " ", "Requester_Organization": " ", "Vendor Name": " ", "Manager Group ID": "SGP0000xxxxxxx", "Vendor Responded On": null, "Vendor Ticket Number": " ", "GA Date/Time": null, "View Access": null, "Investigation Driver": null, "Manager Company": "Calbro Services", "Manager Organization": " ", "Manager Group": " ", "Manager": " ", "Manager Login ID": "Mary", "Assignee Login ID": "Ian", "PreRelease Date/Time": null, "Vendor Contact": " ", "Workaround Determined On": null, "Reported to Vendor": null, "Patch Last Build ID": " ", "Corrective Model/Version": " ", "Infrastructure Chg Initiated": null, "Category": null, "Reproduceable Flag": null, "Assign To Vendor": null, "Known Error Created": null, "Searchable": null, "Target Resolution Date": null, "Corrective Action Determined": null, "Requester Group ID": "SGP000xxxxxxxx", "Implementer Company": "Calbro Services", "Implementer Organization": " ", "Implementer Goup": " ", "Implementer": " ", "Implementer Login ID": "Francie", "Implementer Group ID": "SGP00xxxxxxxx", "Request Status": "10", "Publish Date": null, "Expiry Date": null, "Archive Date": null}, {"Request ID": "CRQ_CAL_100xxxxx", "Assignee Groups": "10000xxxxx;", "Vendor Assignee Groups": "10000xxxxx;", "VENDOR_ASSIGNEE_GROUPS_PARENT": "", "ASSIGNEE_GROUPS_PARENT": "", "RootRequestID": " ", "RootRequestName": " ", "Product Categorization Tier 1": null, "Product Categorization Tier 2": null, "Product Categorization Tier 3": null, "Department": "Customer Service", "Site Group": " ", "Region": " ", "LookupKeyword": "MAINCHANGE", "Product Name": null, "Manufacturer": " ", "Product Model/Version": " ", "Escalated?": "No", "Site": "Amsterdam Support Center", "Last Modified Date": "2008-11-07T05:25:46.000+0000", "Create-Date": "2008-11-07T05:25:46.000+0000", "FORMNAME": "View CHG:Infrastructure Change", "appInstanceId": "AG00123F73xxxxxxxxxxxx", "ConsolidatedStatus": "Closed", "ConsolidatedStatusReason": null, "TicketType": "Change", "Abstract_KDB": " ", "LastModifiedBy_Request": "Remedy Application Service", "Submitter_Request": "Remedy Application Service", "EntryID": "CRQ000xxxxxxxxx", "Service": null, "CI": " ", "ServiceCI_ReconID": null, "ServiceCI_Class": null, "z1D_ConfirmGroup": null, "Description": "Setup new user with basic system permissions.", "Company": "Calbro Services", "Assignee Organization": " ", "Last Name": "Mann", "First Name": "Mary", "Internet Email": " ", "Phone Number Business": " ", "Categorization Tier 1": "Request", "Categorization Tier 2": "Account", "Categorization Tier 3": "Create", "Assignee Group ID": "SGP000xxxxxxx", "Requester_Company": " ", "Urgency": "3-Medium", "Impact": "2-Significant/Large", "Priority": "Medium", "Priority Weight": null, "Assignee Group": "Frontoffice Support", "Assignee": "Ian Plyment", "ID": "CRQ_CAL_100xxxxx", "Investigation Justification": " ", "Vendor Phone": " ", "Assignee Company": "Calbro Services", "Requestor ID": "Mary", "Requester_Group_Name": " ", "Requester_Organization": " ", "Vendor Name": " ", "Manager Group ID": "SGP000xxxxxxxx", "Vendor Responded On": null, "Vendor Ticket Number": " ", "GA Date/Time": null, "View Access": null, "Investigation Driver": null, "Manager Company": "Calbro Services", "Manager Organization": " ", "Manager Group": " ", "Manager": " ", "Manager Login ID": "Mary", "Assignee Login ID": "Ian", "PreRelease Date/Time": null, "Vendor Contact": " ", "Workaround Determined On": null, "Reported to Vendor": null, "Patch Last Build ID": " ", "Corrective Model/Version": " ", "Infrastructure Chg Initiated": null, "Category": null, "Reproduceable Flag": null, "Assign To Vendor": null, "Known Error Created": null, "Searchable": null, "Target Resolution Date": null, "Corrective Action Determined": null, "Requester Group ID": "SGP000xxxxxxx", "Implementer Company": "Calbro Services", "Implementer Organization": " ", "Implementer Goup": " ", "Implementer": " ", "Implementer Login ID": "Ian", "Implementer Group ID": "SGP000xxxxxxx", "Request Status": "11", "Publish Date": null, "Expiry Date": null, "Archive Date": null}]
```



#### Update Incident
Update an incident in BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident ID|Specify the id of the  incident that needs to be updated.|True|String||
|Status|Specify the status for the incident. Note: if status is "Pending" or "Resolved", then you also need to provide "Status Reason" value.|False|List|Select One|
|Status Reason|Specify the status reason for the incident.|False|String||
|Impact|Specify the impact for the incident.|False|List|Select One|
|Urgency|Specify the urgency for the incident.|False|List|Select One|
|Description|Specify the description of the incident|False|String||
|Incident Type|Specify the incident type for the incident.|False|List|Select One|
|Assigned Group|Specify the assigned group for the incident|False|String||
|Assignee|Specify the assignee for the incident|False|String||
|Resolution|Specify the resolution for the incident.|False|String||
|Resolution Category Tier 1|Specify the resolution category tier 1 for the incident.|False|String||
|Resolution Category Tier 2|Specify the resolution category tier 2 for the incident.|False|String||
|Resolution Category Tier 3|Specify the resolution category tier 3 for the incident.|False|String||
|Resolution Product Category Tier 1|Specify the resolution category tier 1 for the incident.|False|String||
|Resolution Product Category Tier 2|Specify the resolution category tier 2 for the incident.|False|String||
|Resolution Product Category Tier 3|Specify the resolution category tier 3 for the incident.|False|String||
|Reported Source|Specify the reported source.|False|List|Select One|
|Custom Fields|Specify a JSON object containing all of the needed fields and  values that need to be updated. Note: this parameter will overwrite other provided parameters.|False|String||



#### Add Work Note To Incident
Add a work note to incidents in BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident ID|Specify the id of the incident to which you want to add a work note.|True|String||
|Work Note Text|Specify the text for the work note.|True|String||



#### Create Record
Create a record in BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Record Type|Specify the type of the record that needs to be created.|True|String||
|Record Payload|Specify a JSON object containing all of the needed fields and  values.|True|String|{"field": "value"}|



##### JSON Results
```json
{"Work Log ID": "WLG000xxxxxxx", "Submitter": "User", "Submit Date": "2022-04-27T08:41:10.000+0000", "Assigned To": null, "Last Modified By": "User", "Last Modified Date": "2022-04-27T08:41:10.000+0000", "Status": "Enabled", "Short Description": ".", "Status History": null, "Assignee Groups": "100000xxxx;"}
```



#### Create Incident
Create an incident in BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Status|Specify the status for the incident.|False|List|Select One|
|Impact|Specify the impact for the incident.|False|List|Select One|
|Urgency|Specify the urgency for the incident.|False|List|Select One|
|Description|Specify the description of the incident|False|String||
|Company|Specify the company for the incident|False|String||
|Customer|Specify the customer for the incident. Note: Customer needs to be provide in the format "{Last Name} {First Name}". Example: Allbrook Allen.|False|String||
|Template Name|Specify the name of the template for the incident. Note: action will try to find the ID of the template in the background. For better precision you can provide the template ID directly via Custom Fields.|False|String||
|Incident Type|Specify the incident type for the incident.|False|List|Select One|
|Assigned Group|Specify the assigned group for the incident|False|String||
|Assignee|Specify the assignee for the incident|False|String||
|Resolution|Specify the resolution for the incident.|False|String||
|Resolution Category Tier 1|Specify the resolution category tier 1 for the incident.|False|String||
|Resolution Category Tier 2|Specify the resolution category tier 2 for the incident.|False|String||
|Resolution Category Tier 3|Specify the resolution category tier 3 for the incident.|False|String||
|Resolution Product Category Tier 1|Specify the resolution category tier 1 for the incident.|False|String||
|Resolution Product Category Tier 2|Specify the resolution category tier 2 for the incident.|False|String||
|Resolution Product Category Tier 3|Specify the resolution category tier 3 for the incident.|False|String||
|Reported Source|Specify the reported source|False|List|Select One|
|Custom Fields|Specify a JSON object containing all of the needed fields and  values that need to be used during the creation. Note: this parameter will overwrite other provided parameters.|False|String||



##### JSON Results
```json
{"Request ID": "00000xxxxxxxxxx", "Submitter": "Test", "Create Date": "2022-01-14T14:43:17.000+0000", "Assigned To": null, "Last Modified By": "Test", "Modified Date": "2022-01-14T14:43:17.000+0000", "Status": "Assigned", "Short Description": ".", "Status History": {"New": {"user": "Test", "timestamp": "2022-01-14T14:43:17.000+0000"}, "Assigned": {"user": "Test", "timestamp": "2022-01-14T14:43:17.000+0000"}}, "Assignee Groups": null, "InstanceId": "AGGAA5V0G207EARFP5KFxxxxxxxxxx", "Vendor Assignee Groups": null, "Vendor Assignee Groups_parent": null, "Assignee Groups_parent": null, "Product Categorization Tier 1": null, "Product Categorization Tier 2": null, "Product Categorization Tier 3": null, "Department": null, "Site Group": null, "Region": "ABC", "CI Name": null, "Schema Name": null, "Lookup Keyword": null, "Product Name": null, "Manufacturer": null, "Product Model/Version": null, "Site": "ABC", "Created_By": null, "Person Instance ID": "IDGAA5V0G207EARFI9AFxxxxxxxxxx", "MaxRetries": null, "z1D_Command": null, "AccessMode": null, "z1D_WorklogDetails": null, "z1D_Char02": null, "AppInstanceServer": null, "SRInstanceID": null, "zTmpEventGUID": null, "AppInterfaceForm": null, "z1D_Activity_Type": null, "z1D_Details": null, "z1D_Secure_Log": null, "z1D_View_Access": null, "Protocol": null, "AppLogin": null, "AppPassword": null, "PortNumber": null, "z1D_SupportGroupID": null, "Unknown User": null, "SRMS Registry Instance ID": null, "SRMSAOIGuid": null, "SRID": null, "TemplateID": null, "DataTags": null, "z1D_CommunicationSource": null, "z1D_ActivityDate_tab": null, "Created_From_flag": null, "Flag_Create_Request": null, "Component_ID": null, "mc_ueid": null, "cell_name": null, "z1D_CIUASupportCompany": null, "z1D_CIUASupportOrg": null, "z1D_CIUAAssignGroup": null, "z1D_UAAssignmentMethod": null, "Unavailability_Priority": null, "policy_name": null, "status_incident": null, "status_reason2": null, "root_component_id_list": null, "root_incident_id_list": null, "Impact_OR_Root": null, "bOrphanedRoot": null, "OptionForClosingIncident": null, "first_name2": null, "last_name2": null, "Login_ID": "incABC", "Global_OR_Custom_Mapping": null, "use_case": null, "BiiARS_01": null, "BiiARS_02": null, "BiiARS_03": null, "BiiARS_04": null, "BiiARS_05": null, "Assignee Login ID": null, "TemplateID2": null, "ClientLocale": null, "ServiceCI": null, "HPD_CI": null, "ServiceCI_ReconID": null, "HPD_CI_ReconID": null, "z1D_CI_FormName": null, "z1D_SRMInteger": null, "z1D_Direct Contact Person ID": null, "Direct Contact Corporate ID": null, "KMSGUID": null, "HPD_CI_FormName": null, "z1D_Phone_Number": null, "z1D_CC_Business": null, "z1D_Area_Business": null, "z1D_Local_Business": null, "z1D_Extension_Business": null, "z1D_DC_Phone_Number": null, "z1D_DC_CountryCode": null, "z1D_DC_AreaCode": null, "z1D_DC_LocalNumber": null, "z1D_DC_Extension": null, "z1D_Internet_Email": null, "z1D_DC_Internet_Email": null, "HPD_TemplateName": null, "Contact Login Id": null, "Direct Contact LoginID": null, "z1D_ConfirmGroup": null, "z1D_CreatedFromBackEndSynchWI": null, "z1D_PersonInfo": null, "z1D_Person_Match_Found": null, "InfrastructureEventType": "null", "policy_type": null, "Chat Session ID": null, "Modified Chat Session ID": null, "Auto Open Session": null, "Broker Vendor Name": null, "ApplyTemplate": null, "Person ID": "PPL00xxxxxxxxxx", "DatasetId": "0", "ReconciliationIdentity": "0", "Description": "testing", "Company": "Invention, Inc.", "State Province": null, "Organization": null, "Assigned Support Organization": null, "Last_Name": "ABCinc", "First_Name": "incABC", "Middle Initial": null, "Client Type": "Office-Based Employee", "VIP": "No", "Client Sensitivity": "Standard", "CC Business": "359xx", "Area Business": "553323xxx", "Local Business": "123xxx", "Extension Business": "12xxx", "Desk Location": null, "Mail Station": null, "Street": null, "Zip/Postal Code": null, "Internet E-mail": null, "Corporate ID": null, "Phone_Number": "359 553323xxx xxxxxx (12xxx)", "z1D Char01": null, "Categorization Tier 1": null, "Categorization Tier 2": null, "Categorization Tier 3": null, "Site ID": "STE00xxxxxxxxxx", "z1D_Action": null, "Assigned Group ID": null, "Contact_Company": "Invention, Inc.", "Service_Type": "User Service Restoration", "Default City": "SF", "Default Country": "Bulgaria", "Status_Reason": null, "Detailed_Decription": null, "Resolution": null, "Incident Number": "INC00xxxxxxxxxx", "Urgency": "3-Medium", "Impact": "1-Extensive/Widespread", "Priority": "High", "Priority Weight": null, "Reported Source": "Direct Input", "Assigned Group": "ABC", "Assignee": null, "Assigned Support Company": null, "Assigned Group Shift Name": null, "Vendor Name": null, "Unavailability Type": null, "Incident_Entry_ID": null, "Time Zone": null, "Reported Date": null, "Vendor Ticket Number": null, "Generic Categorization Tier 1": null, "z1D Permission Group ID": null, "z1D Permission Group List": null, "Resolution Category Tier 1": null, "Direct Contact Internet E-mail": null, "Vendor Organization": null, "Vendor Group": null, "Vendor Group ID": null, "Resolution Method": null, "Resolution Category Tier 2": null, "Resolution Category Tier 3": null, "Closure Product Category Tier1": null, "Closure Product Category Tier2": null, "Closure Product Category Tier3": null, "Closure Product Name": null, "Closure Product Model/Version": null, "Closure Manufacturer": null, "Required Resolution DateTime": null, "Direct Contact Company": null, "Direct Contact Last Name": null, "Direct Contact First Name": null, "Direct Contact Middle Initial": null, "Direct Contact Phone Number": null, "Direct Contact Organization": null, "Direct Contact Department": null, "Direct Contact Region": null, "Direct Contact Site Group": null, "Direct Contact Site": null, "z2AF_Act_Attachment_1": null, "Direct Contact Street": null, "Direct Contact Country": null, "Direct Contact State/Province": null, "Direct Contact City": null, "Direct Contact Zip/Postal Code": null, "Direct Contact Time Zone": null, "Direct Contact Desk Location": null, "Direct Contact Mail Station": null, "Direct Contact Location Details": null, "Direct Contact Site ID": null, "Direct Contact Country Code": null, "Direct Contact Area Code": null, "Direct Contact Local Number": null, "Direct Contact Extension": null}
```



#### Wait For Record Fields Update
Wait for record fields update in BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Record Type|Specify the type of the record for which you are waiting an update.|True|String||
|Record ID|Specify the ID of the record that needs to be updated.|True|String||
|Fields To Check|Specify a JSON object containing all of the needed fields and values.|True|String|{"field":"value"}|
|Fail If Timeout|If enabled, action will be failed, if not all of the fields were updated.|False|Boolean|true|



##### JSON Results
```json
{"Request ID": "00000xxxxxxxxxx", "Submitter": "Test", "Create Date": "2022-01-14T14:43:17.000+0000", "Assigned To": null, "Last Modified By": "Test", "Modified Date": "2022-01-14T14:43:17.000+0000", "Status": "Assigned", "Short Description": ".", "Status History": {"New": {"user": "Test", "timestamp": "2022-01-14T14:43:17.000+0000"}, "Assigned": {"user": "Test", "timestamp": "2022-01-14T14:43:17.000+0000"}}, "Assignee Groups": null, "InstanceId": "AGGAA5V0G207EARFP5KFxxxxxxxxxx", "Vendor Assignee Groups": null, "Vendor Assignee Groups_parent": null, "Assignee Groups_parent": null, "Product Categorization Tier 1": null, "Product Categorization Tier 2": null, "Product Categorization Tier 3": null, "Department": null, "Site Group": null, "Region": "ABC", "CI Name": null, "Schema Name": null, "Lookup Keyword": null, "Product Name": null, "Manufacturer": null, "Product Model/Version": null, "Site": "ABC", "Created_By": null, "Person Instance ID": "IDGAA5V0G207EARFI9AFxxxxxxxxxx", "MaxRetries": null, "z1D_Command": null, "AccessMode": null, "z1D_WorklogDetails": null, "z1D_Char02": null, "AppInstanceServer": null, "SRInstanceID": null, "zTmpEventGUID": null, "AppInterfaceForm": null, "z1D_Activity_Type": null, "z1D_Details": null, "z1D_Secure_Log": null, "z1D_View_Access": null, "Protocol": null, "AppLogin": null, "AppPassword": null, "PortNumber": null, "z1D_SupportGroupID": null, "Unknown User": null, "SRMS Registry Instance ID": null, "SRMSAOIGuid": null, "SRID": null, "TemplateID": null, "DataTags": null, "z1D_CommunicationSource": null, "z1D_ActivityDate_tab": null, "Created_From_flag": null, "Flag_Create_Request": null, "Component_ID": null, "mc_ueid": null, "cell_name": null, "z1D_CIUASupportCompany": null, "z1D_CIUASupportOrg": null, "z1D_CIUAAssignGroup": null, "z1D_UAAssignmentMethod": null, "Unavailability_Priority": null, "policy_name": null, "status_incident": null, "status_reason2": null, "root_component_id_list": null, "root_incident_id_list": null, "Impact_OR_Root": null, "bOrphanedRoot": null, "OptionForClosingIncident": null, "first_name2": null, "last_name2": null, "Login_ID": "incABC", "Global_OR_Custom_Mapping": null, "use_case": null, "BiiARS_01": null, "BiiARS_02": null, "BiiARS_03": null, "BiiARS_04": null, "BiiARS_05": null, "Assignee Login ID": null, "TemplateID2": null, "ClientLocale": null, "ServiceCI": null, "HPD_CI": null, "ServiceCI_ReconID": null, "HPD_CI_ReconID": null, "z1D_CI_FormName": null, "z1D_SRMInteger": null, "z1D_Direct Contact Person ID": null, "Direct Contact Corporate ID": null, "KMSGUID": null, "HPD_CI_FormName": null, "z1D_Phone_Number": null, "z1D_CC_Business": null, "z1D_Area_Business": null, "z1D_Local_Business": null, "z1D_Extension_Business": null, "z1D_DC_Phone_Number": null, "z1D_DC_CountryCode": null, "z1D_DC_AreaCode": null, "z1D_DC_LocalNumber": null, "z1D_DC_Extension": null, "z1D_Internet_Email": null, "z1D_DC_Internet_Email": null, "HPD_TemplateName": null, "Contact Login Id": null, "Direct Contact LoginID": null, "z1D_ConfirmGroup": null, "z1D_CreatedFromBackEndSynchWI": null, "z1D_PersonInfo": null, "z1D_Person_Match_Found": null, "InfrastructureEventType": "null", "policy_type": null, "Chat Session ID": null, "Modified Chat Session ID": null, "Auto Open Session": null, "Broker Vendor Name": null, "ApplyTemplate": null, "Person ID": "PPL00xxxxxxxxxx", "DatasetId": "0", "ReconciliationIdentity": "0", "Description": "testing", "Company": "Invention, Inc.", "State Province": null, "Organization": null, "Assigned Support Organization": null, "Last_Name": "ABCinc", "First_Name": "incABC", "Middle Initial": null, "Client Type": "Office-Based Employee", "VIP": "No", "Client Sensitivity": "Standard", "CC Business": "359xx", "Area Business": "553323xxx", "Local Business": "123xxx", "Extension Business": "12xxx", "Desk Location": null, "Mail Station": null, "Street": null, "Zip/Postal Code": null, "Internet E-mail": null, "Corporate ID": null, "Phone_Number": "359 553323xxx xxxxxx (12xxx)", "z1D Char01": null, "Categorization Tier 1": null, "Categorization Tier 2": null, "Categorization Tier 3": null, "Site ID": "STE00xxxxxxxxxx", "z1D_Action": null, "Assigned Group ID": null, "Contact_Company": "Invention, Inc.", "Service_Type": "User Service Restoration", "Default City": "SF", "Default Country": "Bulgaria", "Status_Reason": null, "Detailed_Decription": null, "Resolution": null, "Incident Number": "INC00xxxxxxxxxx", "Urgency": "3-Medium", "Impact": "1-Extensive/Widespread", "Priority": "High", "Priority Weight": null, "Reported Source": "Direct Input", "Assigned Group": "ABC", "Assignee": null, "Assigned Support Company": null, "Assigned Group Shift Name": null, "Vendor Name": null, "Unavailability Type": null, "Incident_Entry_ID": null, "Time Zone": null, "Reported Date": null, "Vendor Ticket Number": null, "Generic Categorization Tier 1": null, "z1D Permission Group ID": null, "z1D Permission Group List": null, "Resolution Category Tier 1": null, "Direct Contact Internet E-mail": null, "Vendor Organization": null, "Vendor Group": null, "Vendor Group ID": null, "Resolution Method": null, "Resolution Category Tier 2": null, "Resolution Category Tier 3": null, "Closure Product Category Tier1": null, "Closure Product Category Tier2": null, "Closure Product Category Tier3": null, "Closure Product Name": null, "Closure Product Model/Version": null, "Closure Manufacturer": null, "Required Resolution DateTime": null, "Direct Contact Company": null, "Direct Contact Last Name": null, "Direct Contact First Name": null, "Direct Contact Middle Initial": null, "Direct Contact Phone Number": null, "Direct Contact Organization": null, "Direct Contact Department": null, "Direct Contact Region": null, "Direct Contact Site Group": null, "Direct Contact Site": null, "z2AF_Act_Attachment_1": null, "Direct Contact Street": null, "Direct Contact Country": null, "Direct Contact State/Province": null, "Direct Contact City": null, "Direct Contact Zip/Postal Code": null, "Direct Contact Time Zone": null, "Direct Contact Desk Location": null, "Direct Contact Mail Station": null, "Direct Contact Location Details": null, "Direct Contact Site ID": null, "Direct Contact Country Code": null, "Direct Contact Area Code": null, "Direct Contact Local Number": null, "Direct Contact Extension": null}
```



#### Update Record
Update a record in BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Record Type|Specify the type of the record that needs to be updated.|True|String||
|Record ID|Specify the id of the  record that needs to be updated.|True|String||
|Record Payload|Specify a JSON object containing all of the needed fields and values that need to be updated.|True|String|{"field": "value"}|



#### Ping
Test connectivity to the BMC Remedy ITSM with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds






## Jobs

#### Sync Closed Incidents By Tag
This job will synchronize BMC Remedy ITSM incidents that were created within Siemplify Case playbook and Siemplify cases. Note: in BMC Remedy ITSM statuses "Cancelled", "Closed" and "Resolved" are treated as closed. Additionally, in order for the job to work, it's required for the case to have 2 tags. First tag should be "BMC Remedy ITSM" and the second should be with the prefix "BMC Remedy ITSM:{Incident ID}". Job can only close incidents that are assigned in BMC Remedy ITSM.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Incident Table|True|String|HPD:IncidentInterface|
|API Root|True|String|https://{IP}:{port}|
|Username|True|String||
|Password|True|Password|*****|
|Environment|False|String||
|Max Hours Backwards|False|String|24|
|Verify SSL|False|Boolean|true|



