
# Hibob

Hibob integration facilitates the centralized management and synchronization of the company's employees information stored in the HR system called Hibob.
Bob is a cloud-based human resources (HR) management and benefits administration platform for HR teams, CEOs, and accountants.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Token|API Token|True|Password|*****|


#### Dependencies
| |
|-|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|urllib3-2.5.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Send Invitation
Sending an invitation to a new employee in order to invite them to log in the Hibob system for the first time or reinvite the user after he was disabled
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Employee's Email|The email of the employee that you want to send the invitation in order to start using Hibob system.|True|String|email@gmail.com|
|Welcome Wizard Name|The wizard name found in Hibob (Setting-> Flows), for example: "Welcome!". Please note: this is case sensitive!|True|String|Welcome!|



##### JSON Results
```json
{"exists": "True", "invitationWasSent": "False", "wizardName": "Welcome!", "wizardId": "954554"}
```



#### Search User
Search if a specific user exists in Hibob
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Employee's Email|The employee's email to check if it exists|True|String|email@gmail.com|



##### JSON Results
```json
{"fullName": "Amy Miles", "creationDate": "2020-08-18", "displayName": "Amy Miles", "payroll": {"additionalPensionContribution": null, "nin": null, "timeSinceLastSalaryChange": {"humanize": "5 years, 5 months and 10 days", "sortFactor": 1960, "periodISO": "P5Y5M10D"}, "salary": {"monthlyPayment": {"currency": "USD", "value": 3333.3333333333335}, "payPeriod": "Annual", "yearlyPayment": {"currency": "USD", "value": 40000}, "payment": {"currency": "USD", "value": 40000}, "activeEffectiveDate": "2015-03-20", "payFrequency": "Every two weeks"}, "taxCode": null, "employment": {"fte": 100, "type": null, "flsaCode": null, "contract": "Full time", "salaryPayType": null, "weeklyHours": 45, "workingPattern": {"raw": null}, "activeEffectiveDate": "2015-03-20", "siteWorkingPattern": {"hoursPerDay": 9, "days": {"wednesday": true, "sunday": false, "tuesday": true, "saturday": false, "monday": true, "friday": true, "thursday": true}, "workingPatternType": "partial_week"}}}, "address": {"city": "New York", "line2": null, "country": "United States", "line1": "1335 Grove Street", "fullAddress": "1335 Grove Street  New York  11757 NY United States", "zipCode": "11757", "usaState": "NY", "activeEffectiveDate": "2015-03-20", "postCode": null}, "state": "uninvited", "personal": {"shortBirthDate": "11-25", "communication": {"skypeUsername": null, "slackUsername": null}, "pronouns": null, "honorific": "Ms", "nationality": ["American"], "age": 28, "birthDate": "1991-11-25"}, "creationDateTime": "2020-08-18T10:02:42.44441", "work": {"shortStartDate": "03-20", "startDate": "2015-03-20", "manager": "2378379584279150891", "workPhone": null, "reportsToIdInCompany": 1, "durationOfEmployment": {"humanize": "5 years, 5 months and 11 days", "sortFactor": 1961, "periodISO": "P5Y5M11D"}, "employeeIdInCompany": 39, "reportsTo": {"displayName": "Zoe Clark", "email": "zoe.clark_200519@samplebob.com", "surname": "Clark", "firstName": "Zoe", "id": "2378379584279150891"}, "workMobile": null, "siteId": 708868, "department": "Product", "title": "Designer", "site": "New York (Demo)", "activeEffectiveDate": "2015-03-20", "secondLevelManager": "2378379548686287126", "yearsOfService": 5.417}, "internal": {"periodSinceTermination": null, "yearsSinceTermination": null, "terminationReason": null, "probationEndDate": null, "terminationDate": null, "status": "Active", "terminationType": null, "notice": null, "lifecycleStatus": "employed"}, "secondName": null, "avatarUrl": "https://cdn.filestackcontent.com/nxUwWkpZS1Scg9EjqA7K?policy=eyJoYW5kbGUiOiJueFV3V2twWlMxU2NnOUVqcUE3SyIsImV4cGlyeSI6NDYzNTkxODcwNH0=&signature=52ba8596c28ea66305882d6a6aa583487476207d72bf4499dcfc865d3bfa4e74", "emergency": {"city": null, "address": null, "mobilePhone": null, "country": null, "relation": null, "secondName": null, "email": null, "surname": null, "phone": null, "firstName": null, "postCode": null}, "eeo": {"ethnicity": null, "jobCategory": null}, "about": {"foodPreferences": ["vegan"], "socialData": {"linkedin": null, "twitter": null, "facebook": null}, "hobbies": ["yoga", "cooking", "film"], "superpowers": ["excel"], "about": "The most important thing is to enjoy your life - to be happy - it's all that matters.", "avatar": "https://cdn.filestackcontent.com/nxUwWkpZS1Scg9EjqA7K?policy=eyJoYW5kbGUiOiJueFV3V2twWlMxU2NnOUVqcUE3SyIsImV4cGlyeSI6NDYzNTkxODcwNH0=&signature=52ba8596c28ea66305882d6a6aa583487476207d72bf4499dcfc865d3bfa4e74"}, "companyId": 200519, "email": "amy.miles_200519@samplebob.com", "surname": "Miles", "home": {"familyStatus": "Single", "mobilePhone": "914-963-9202", "privateEmail": "AMiles@dayrep.com", "legalGender": "Female", "privatePhone": null, "numberOfKids": 0, "spouse": {"shortBirthDate": null, "gender": null, "birthDate": null, "surname": null, "firstName": null}}, "identification": {"ssn": "084-52-6155", "ssnSerialNumber": "***-**-6155"}, "financial": {"iban": null, "swift": null, "routingNumber": null, "bankName": "Chase", "rightToWorkExpiryDate": null, "passportNumber": null, "identificationNumber": null, "accountnumber": null, "bankAddress": null, "bankAccountType": null, "accountType": null, "sortcode": null, "accountName": null}, "firstName": "Amy", "id": "2378379585948483884"}
```



#### Revoke Access
Disabling a given employee in Hibob based on his email address
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Employee's Email|The email of the employee you want to disable the access to Hibob|True|String|email@gmail.com|



##### JSON Results
```json
{}
```



#### Enrich Entities
Enrich entities with Hibob properties
Timeout - 600 Seconds



##### JSON Results
```json
{"fullName": "Amy Miles", "creationDate": "2020-08-18", "displayName": "Amy Miles", "payroll": {"additionalPensionContribution": null, "nin": null, "timeSinceLastSalaryChange": {"humanize": "5 years, 5 months and 10 days", "sortFactor": 1960, "periodISO": "P5Y5M10D"}, "salary": {"monthlyPayment": {"currency": "USD", "value": 3333.3333333333335}, "payPeriod": "Annual", "yearlyPayment": {"currency": "USD", "value": 40000}, "payment": {"currency": "USD", "value": 40000}, "activeEffectiveDate": "2015-03-20", "payFrequency": "Every two weeks"}, "taxCode": null, "employment": {"fte": 100, "type": null, "flsaCode": null, "contract": "Full time", "salaryPayType": null, "weeklyHours": 45, "workingPattern": {"raw": null}, "activeEffectiveDate": "2015-03-20", "siteWorkingPattern": {"hoursPerDay": 9, "days": {"wednesday": true, "sunday": false, "tuesday": true, "saturday": false, "monday": true, "friday": true, "thursday": true}, "workingPatternType": "partial_week"}}}, "address": {"city": "New York", "line2": null, "country": "United States", "line1": "1335 Grove Street", "fullAddress": "1335 Grove Street  New York  11757 NY United States", "zipCode": "11757", "usaState": "NY", "activeEffectiveDate": "2015-03-20", "postCode": null}, "state": "uninvited", "personal": {"shortBirthDate": "11-25", "communication": {"skypeUsername": null, "slackUsername": null}, "pronouns": null, "honorific": "Ms", "nationality": ["American"], "age": 28, "birthDate": "1991-11-25"}, "creationDateTime": "2020-08-18T10:02:42.44441", "work": {"shortStartDate": "03-20", "startDate": "2015-03-20", "manager": "2378379584279150891", "workPhone": null, "reportsToIdInCompany": 1, "durationOfEmployment": {"humanize": "5 years, 5 months and 11 days", "sortFactor": 1961, "periodISO": "P5Y5M11D"}, "employeeIdInCompany": 39, "reportsTo": {"displayName": "Zoe Clark", "email": "zoe.clark_200519@samplebob.com", "surname": "Clark", "firstName": "Zoe", "id": "2378379584279150891"}, "workMobile": null, "siteId": 708868, "department": "Product", "title": "Designer", "site": "New York (Demo)", "activeEffectiveDate": "2015-03-20", "secondLevelManager": "2378379548686287126", "yearsOfService": 5.417}, "internal": {"periodSinceTermination": null, "yearsSinceTermination": null, "terminationReason": null, "probationEndDate": null, "terminationDate": null, "status": "Active", "terminationType": null, "notice": null, "lifecycleStatus": "employed"}, "secondName": null, "avatarUrl": "https://cdn.filestackcontent.com/nxUwWkpZS1Scg9EjqA7K?policy=eyJoYW5kbGUiOiJueFV3V2twWlMxU2NnOUVqcUE3SyIsImV4cGlyeSI6NDYzNTkxODcwNH0=&signature=52ba8596c28ea66305882d6a6aa583487476207d72bf4499dcfc865d3bfa4e74", "emergency": {"city": null, "address": null, "mobilePhone": null, "country": null, "relation": null, "secondName": null, "email": null, "surname": null, "phone": null, "firstName": null, "postCode": null}, "eeo": {"ethnicity": null, "jobCategory": null}, "about": {"foodPreferences": ["vegan"], "socialData": {"linkedin": null, "twitter": null, "facebook": null}, "hobbies": ["yoga", "cooking", "film"], "superpowers": ["excel"], "about": "The most important thing is to enjoy your life - to be happy - it's all that matters.", "avatar": "https://cdn.filestackcontent.com/nxUwWkpZS1Scg9EjqA7K?policy=eyJoYW5kbGUiOiJueFV3V2twWlMxU2NnOUVqcUE3SyIsImV4cGlyeSI6NDYzNTkxODcwNH0=&signature=52ba8596c28ea66305882d6a6aa583487476207d72bf4499dcfc865d3bfa4e74"}, "companyId": 200519, "email": "amy.miles_200519@samplebob.com", "surname": "Miles", "home": {"familyStatus": "Single", "mobilePhone": "914-963-9202", "privateEmail": "AMiles@dayrep.com", "legalGender": "Female", "privatePhone": null, "numberOfKids": 0, "spouse": {"shortBirthDate": null, "gender": null, "birthDate": null, "surname": null, "firstName": null}}, "identification": {"ssn": "084-52-6155", "ssnSerialNumber": "***-**-6155"}, "financial": {"iban": null, "swift": null, "routingNumber": null, "bankName": "Chase", "rightToWorkExpiryDate": null, "passportNumber": null, "identificationNumber": null, "accountnumber": null, "bankAddress": null, "bankAccountType": null, "accountType": null, "sortcode": null, "accountName": null}, "firstName": "Amy", "id": "2378379585948483884"}
```



#### Get User Image
Get the image base64 and URL for a specific employee
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Employee's Email|The employee's email you want to upload a photo.|True|String|email@gmail.com|



##### JSON Results
```json
{"exists": "True", "imageBase64": "aHR0cHM6Ly9jZG4uZmlsZXN0YWNrY29udGVudC5jb20vWWE0dHhkWjRReUtjd0NCUkE2MUs/cG9saWN5PWV5Sm9ZVzVrYkdVaU9pSlpZVFIwZUdSYU5GRjVTMk4zUTBKU1FUWXhTeUlzSW1WNGNHbHllU0k2TkRZek5Ua3hPRGN3TkgwPSZzaWduYXR1cmU9ODhjM2ZhYTliN2RkMTE0ZWM2MmQwM2I2Y2I2OTFmNjM5ZWM0ODYxM2JlZGYyOGQwZjRlZDg3MTI5MmY0YjA1Mw==", "imageUrl": "https://cdn.filestackcontent.com/Ya4txdZ4QyKcwCBRA61K?policy=eyJoYW5kbGUiOiJZYTR0eGRaNFF5S2N3Q0JSQTYxSyIsImV4cGlyeSI6NDYzNTkxODcwNH0=&signature=88c3faa9b7dd114ec62d03b6cb691f639ec48613bedf28d0f4ed871292f4b053"}
```



#### Upload User Image
Uploading an image (URL image) to a specific employee
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Employee's Email|The email of the employee that you want to upload an image to.|True|String|email@gmail.com|
|Url Image|The employee URL image|True|String|https://|



##### JSON Results
```json
{}
```



#### Ping
Testing the connectivity with Hibob 
Timeout - 600 Seconds



##### JSON Results
```json
{}
```









