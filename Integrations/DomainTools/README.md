
# DomainTools

DomainTools turns threat data into threat intelligence. Assess risk of domains and augment malware intel with domain data. In case of any queries, please reach out to memberservices@domaintools.com

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Username||True|String||
|ApiToken||True|String||
|Verify SSL||False|Boolean|true|


#### Dependencies
| |
|-|
|pyyaml-6.0.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|typing_extensions-4.15.0-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|httpcore-1.0.9-py3-none-any.whl|
|shellingham-1.5.4-py2.py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|google_auth_httplib2-0.3.0-py3-none-any.whl|
|proto_plus-1.27.1-py3-none-any.whl|
|anyio-4.12.1-py3-none-any.whl|
|pyasn1-0.6.2-py3-none-any.whl|
|typer-0.21.2-py3-none-any.whl|
|mdurl-0.1.2-py3-none-any.whl|
|pyopenssl-25.3.0-py3-none-any.whl|
|pycparser-2.23-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|cryptography-46.0.3-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|click-8.3.1-py3-none-any.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|httplib2-0.31.2-py3-none-any.whl|
|requests_toolbelt-1.0.0-py2.py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|annotated_doc-0.0.4-py3-none-any.whl|
|google_auth-2.47.0-py3-none-any.whl|
|EnvironmentCommon-1.0.3-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|TIPCommon-2.3.0-py3-none-any.whl|
|protobuf-6.33.5-py3-none-any.whl|
|charset_normalizer-3.4.4-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|domaintools_api-2.7.2-py2.py3-none-any.whl|
|googleapis_common_protos-1.72.0-py3-none-any.whl|
|idna-3.11-py3-none-any.whl|
|markdown_it_py-4.0.0-py3-none-any.whl|
|rich-14.3.2-py3-none-any.whl|
|pygments-2.19.2-py3-none-any.whl|
|google_api_core-2.29.0-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|google_api_python_client-2.188.0-py3-none-any.whl|
|certifi-2026.1.4-py3-none-any.whl|


## Actions
#### Get WhoIs History
Enrich external domain entity with DomainTools threat Intelligence data and return CSV output
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Domain|The domain to get the whois history result.|False|String||



##### JSON Results
```json
[{"Entity": "HTTP://MARKOSSOLOMON.COM/F1Q7QX.PHP", "EntityResult": {"record_count": 5, "history": [{"date": "2021-12-09", "is_private": 0, "whois": {"registrant": "Privacy service provided by Withheld for Privacy ehf", "registration": {"created": "2013-12-06", "expires": "2022-12-06", "updated": "2021-12-06", "registrar": "NameCheap, Inc.", "statuses": ["clientTransferProhibited"]}, "name_servers": ["DNS101.REGISTRAR-SERVERS.COM", "DNS102.REGISTRAR-SERVERS.COM"], "server": "whois.namecheap.com", "record": "Domain name: markossolomon.com\nRegistry Domain ID: 1838126490_DOMAIN_COM-VRSN\nRegistrar WHOIS Server: whois.namecheap.com\nRegistrar URL: http://www.namecheap.com\nUpdated Date: 2020-11-06T07:28:40.08Z\nCreation Date: 2013-12-06T02:41:09.00Z\nRegistrar Registration Expiration Date: 2021-12-06T02:41:09.00Z\nRegistrar: NAMECHEAP INC\nRegistrar IANA ID: 1068\nRegistrar Abuse Contact Email: abuse@namecheap.com\nRegistrar Abuse Contact Phone: +1.9854014545\nReseller: NAMECHEAP INC\nDomain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited\nRegistry Registrant ID: \nRegistrant Name: Redacted for Privacy\nRegistrant Organization: Privacy service provided by Withheld for Privacy ehf\nRegistrant Street: Kalkofnsvegur 2 \nRegistrant City: Reykjavik\nRegistrant State/Province: Capital Region\nRegistrant Postal Code: 101\nRegistrant Country: IS\nRegistrant Phone: +354.4212434\nRegistrant Phone Ext: \nRegistrant Fax: \nRegistrant Fax Ext: \nRegistrant Email: 7b5590c2745f4a12afdd41c2056051b3.protect@withheldforprivacy.com\nRegistry Admin ID: \nAdmin Name: Redacted for Privacy\nAdmin Organization: Privacy service provided by Withheld for Privacy ehf\nAdmin Street: Kalkofnsvegur 2 \nAdmin City: Reykjavik\nAdmin State/Province: Capital Region\nAdmin Postal Code: 101\nAdmin Country: IS\nAdmin Phone: +354.4212434\nAdmin Phone Ext: \nAdmin Fax: \nAdmin Fax Ext: \nAdmin Email: 7b5590c2745f4a12afdd41c2056051b3.protect@withheldforprivacy.com\nRegistry Tech ID: \nTech Name: Redacted for Privacy\nTech Organization: Privacy service provided by Withheld for Privacy ehf\nTech Street: Kalkofnsvegur 2 \nTech City: Reykjavik\nTech State/Province: Capital Region\nTech Postal Code: 101\nTech Country: IS\nTech Phone: +354.4212434\nTech Phone Ext: \nTech Fax: \nTech Fax Ext: \nTech Email: 7b5590c2745f4a12afdd41c2056051b3.protect@withheldforprivacy.com\nName Server: dns101.registrar-servers.com\nName Server: dns102.registrar-servers.com\nDNSSEC: unsigned\nURL of the ICANN WHOIS Data Problem Reporting System: http://wdprs.internic.net/\nFor more information on Whois status codes, please visit https://icann.org/epp\n"}}, {"date": "2021-11-21", "is_private": 0, "whois": {"registrant": "Privacy service provided by Withheld for Privacy ehf", "registration": {"created": "2013-12-06", "expires": "2021-12-06", "updated": "2020-11-06", "registrar": "NameCheap, Inc.", "statuses": ["clientTransferProhibited"]}, "name_servers": ["FAILED-WHOIS-VERIFICATION.NAMECHEAP.COM", "VERIFY-CONTACT-DETAILS.NAMECHEAP.COM"], "server": "whois.namecheap.com", "record": "Domain name: markossolomon.com\nRegistry Domain ID: 1838126490_DOMAIN_COM-VRSN\nRegistrar WHOIS Server: whois.namecheap.com\nRegistrar URL: http://www.namecheap.com\nUpdated Date: 2020-11-06T07:28:40.08Z\nCreation Date: 2013-12-06T02:41:09.00Z\nRegistrar Registration Expiration Date: 2021-12-06T02:41:09.00Z\nRegistrar: NAMECHEAP INC\nRegistrar IANA ID: 1068\nRegistrar Abuse Contact Email: abuse@namecheap.com\nRegistrar Abuse Contact Phone: +1.9854014545\nReseller: NAMECHEAP INC\nDomain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited\nRegistry Registrant ID: \nRegistrant Name: Redacted for Privacy\nRegistrant Organization: Privacy service provided by Withheld for Privacy ehf\nRegistrant Street: Kalkofnsvegur 2 \nRegistrant City: Reykjavik\nRegistrant State/Province: Capital Region\nRegistrant Postal Code: 101\nRegistrant Country: IS\nRegistrant Phone: +354.4212434\nRegistrant Phone Ext: \nRegistrant Fax: \nRegistrant Fax Ext: \nRegistrant Email: 54ffbeb072a84cc0b1f7bdd318594fb0.protect@withheldforprivacy.com\nRegistry Admin ID: \nAdmin Name: Redacted for Privacy\nAdmin Organization: Privacy service provided by Withheld for Privacy ehf\nAdmin Street: Kalkofnsvegur 2 \nAdmin City: Reykjavik\nAdmin State/Province: Capital Region\nAdmin Postal Code: 101\nAdmin Country: IS\nAdmin Phone: +354.4212434\nAdmin Phone Ext: \nAdmin Fax: \nAdmin Fax Ext: \nAdmin Email: 54ffbeb072a84cc0b1f7bdd318594fb0.protect@withheldforprivacy.com\nRegistry Tech ID: \nTech Name: Redacted for Privacy\nTech Organization: Privacy service provided by Withheld for Privacy ehf\nTech Street: Kalkofnsvegur 2 \nTech City: Reykjavik\nTech State/Province: Capital Region\nTech Postal Code: 101\nTech Country: IS\nTech Phone: +354.4212434\nTech Phone Ext: \nTech Fax: \nTech Fax Ext: \nTech Email: 54ffbeb072a84cc0b1f7bdd318594fb0.protect@withheldforprivacy.com\nName Server: verify-contact-details.namecheap.com\nName Server: failed-whois-verification.namecheap.com\nDNSSEC: unsigned\nURL of the ICANN WHOIS Data Problem Reporting System: http://wdprs.internic.net/\nFor more information on Whois status codes, please visit https://icann.org/epp\n"}}, {"date": "2021-10-19", "is_private": 0, "whois": {"registrant": "Privacy service provided by Withheld for Privacy ehf", "registration": {"created": "2013-12-06", "expires": "2021-12-06", "updated": "2020-11-06", "registrar": "NameCheap, Inc.", "statuses": ["clientTransferProhibited"]}, "name_servers": ["FAILED-WHOIS-VERIFICATION.NAMECHEAP.COM", "VERIFY-CONTACT-DETAILS.NAMECHEAP.COM"], "server": "whois.namecheap.com", "record": "Domain name: markossolomon.com\nRegistry Domain ID: 1838126490_DOMAIN_COM-VRSN\nRegistrar WHOIS Server: whois.namecheap.com\nRegistrar URL: http://www.namecheap.com\nUpdated Date: 2020-11-06T07:28:40.08Z\nCreation Date: 2013-12-06T02:41:09.00Z\nRegistrar Registration Expiration Date: 2021-12-06T02:41:09.00Z\nRegistrar: NAMECHEAP INC\nRegistrar IANA ID: 1068\nRegistrar Abuse Contact Email: abuse@namecheap.com\nRegistrar Abuse Contact Phone: +1.6613102107\nReseller: NAMECHEAP INC\nDomain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited\nRegistry Registrant ID: \nRegistrant Name: Withheld for Privacy Purposes\nRegistrant Organization: Privacy service provided by Withheld for Privacy ehf\nRegistrant Street: Kalkofnsvegur 2 \nRegistrant City: Reykjavik\nRegistrant State/Province: Capital Region\nRegistrant Postal Code: 101\nRegistrant Country: IS\nRegistrant Phone: +354.4212434\nRegistrant Phone Ext: \nRegistrant Fax: \nRegistrant Fax Ext: \nRegistrant Email: c9ad5a410f8d417e8cce17434be948e4.protect@withheldforprivacy.com\nRegistry Admin ID: \nAdmin Name: Withheld for Privacy Purposes\nAdmin Organization: Privacy service provided by Withheld for Privacy ehf\nAdmin Street: Kalkofnsvegur 2 \nAdmin City: Reykjavik\nAdmin State/Province: Capital Region\nAdmin Postal Code: 101\nAdmin Country: IS\nAdmin Phone: +354.4212434\nAdmin Phone Ext: \nAdmin Fax: \nAdmin Fax Ext: \nAdmin Email: c9ad5a410f8d417e8cce17434be948e4.protect@withheldforprivacy.com\nRegistry Tech ID: \nTech Name: Withheld for Privacy Purposes\nTech Organization: Privacy service provided by Withheld for Privacy ehf\nTech Street: Kalkofnsvegur 2 \nTech City: Reykjavik\nTech State/Province: Capital Region\nTech Postal Code: 101\nTech Country: IS\nTech Phone: +354.4212434\nTech Phone Ext: \nTech Fax: \nTech Fax Ext: \nTech Email: c9ad5a410f8d417e8cce17434be948e4.protect@withheldforprivacy.com\nName Server: verify-contact-details.namecheap.com\nName Server: failed-whois-verification.namecheap.com\nDNSSEC: unsigned\nURL of the ICANN WHOIS Data Problem Reporting System: http://wdprs.internic.net/\nFor more information on Whois status codes, please visit https://icann.org/epp\n"}}, {"date": "2021-07-23", "is_private": 0, "whois": {"registrant": "Privacy service provided by Withheld for Privacy ehf", "registration": {"created": "2013-12-06", "expires": "2021-12-06", "updated": "2020-11-06", "registrar": "NameCheap, Inc.", "statuses": ["clientTransferProhibited"]}, "name_servers": ["FAILED-WHOIS-VERIFICATION.NAMECHEAP.COM", "VERIFY-CONTACT-DETAILS.NAMECHEAP.COM"], "server": "whois.namecheap.com", "record": "Domain name: markossolomon.com\nRegistry Domain ID: 1838126490_DOMAIN_COM-VRSN\nRegistrar WHOIS Server: whois.namecheap.com\nRegistrar URL: http://www.namecheap.com\nUpdated Date: 2020-11-06T07:28:40.08Z\nCreation Date: 2013-12-06T02:41:09.00Z\nRegistrar Registration Expiration Date: 2021-12-06T02:41:09.00Z\nRegistrar: NAMECHEAP INC\nRegistrar IANA ID: 1068\nRegistrar Abuse Contact Email: abuse@namecheap.com\nRegistrar Abuse Contact Phone: +1.6613102107\nReseller: NAMECHEAP INC\nDomain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited\nRegistry Registrant ID: \nRegistrant Name: Withheld for Privacy Purposes\nRegistrant Organization: Privacy service provided by Withheld for Privacy ehf\nRegistrant Street: Kalkofnsvegur 2 \nRegistrant City: Reykjavik\nRegistrant State/Province: Capital Region\nRegistrant Postal Code: 101\nRegistrant Country: IS\nRegistrant Phone: +354.4212434\nRegistrant Phone Ext: \nRegistrant Fax: \nRegistrant Fax Ext: \nRegistrant Email: c9ad5a410f8d417e8cce17434be948e4.protect@withheldforprivacy.com\nRegistry Admin ID: \nAdmin Name: Withheld for Privacy Purposes\nAdmin Organization: Privacy service provided by Withheld for Privacy ehf\nAdmin Street: Kalkofnsvegur 2 \nAdmin City: Reykjavik\nAdmin State/Province: Capital Region\nAdmin Postal Code: 101\nAdmin Country: IS\nAdmin Phone: +354.4212434\nAdmin Phone Ext: \nAdmin Fax: \nAdmin Fax Ext: \nAdmin Email: c9ad5a410f8d417e8cce17434be948e4.protect@withheldforprivacy.com\nRegistry Tech ID: \nTech Name: Withheld for Privacy Purposes\nTech Organization: Privacy service provided by Withheld for Privacy ehf\nTech Street: Kalkofnsvegur 2 \nTech City: Reykjavik\nTech State/Province: Capital Region\nTech Postal Code: 101\nTech Country: IS\nTech Phone: +354.4212434\nTech Phone Ext: \nTech Fax: \nTech Fax Ext: \nTech Email: c9ad5a410f8d417e8cce17434be948e4.protect@withheldforprivacy.com\nName Server: verify-contact-details.namecheap.com\nName Server: failed-whois-verification.namecheap.com\nDNSSEC: unsigned\nURL of the ICANN WHOIS Data Problem Reporting System: http://wdprs.internic.net/\nFor more information on Whois status codes, please visit https://icann.org/epp\n"}}, {"date": "2021-06-17", "is_private": 0, "whois": {"registrant": "Privacy service provided by Withheld for Privacy ehf", "registration": {"created": "2013-12-06", "expires": "2021-12-06", "updated": "2020-11-06", "registrar": "NameCheap, Inc.", "statuses": ["clientTransferProhibited"]}, "name_servers": ["FAILED-WHOIS-VERIFICATION.NAMECHEAP.COM", "VERIFY-CONTACT-DETAILS.NAMECHEAP.COM"], "server": "whois.namecheap.com", "record": "Domain name: markossolomon.com\nRegistry Domain ID: 1838126490_DOMAIN_COM-VRSN\nRegistrar WHOIS Server: whois.namecheap.com\nRegistrar URL: http://www.namecheap.com\nUpdated Date: 2020-11-06T07:28:40.08Z\nCreation Date: 2013-12-06T02:41:09.00Z\nRegistrar Registration Expiration Date: 2021-12-06T02:41:09.00Z\nRegistrar: NAMECHEAP INC\nRegistrar IANA ID: 1068\nRegistrar Abuse Contact Email: abuse@namecheap.com\nRegistrar Abuse Contact Phone: +1.6613102107\nReseller: NAMECHEAP INC\nDomain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited\nRegistry Registrant ID: \nRegistrant Name: Withheld for Privacy Purposes\nRegistrant Organization: Privacy service provided by Withheld for Privacy ehf\nRegistrant Street: Kalkofnsvegur 2 \nRegistrant City: Reykjavik\nRegistrant State/Province: Capital Region\nRegistrant Postal Code: 101\nRegistrant Country: IS\nRegistrant Phone: +354.4212434\nRegistrant Phone Ext: \nRegistrant Fax: \nRegistrant Fax Ext: \nRegistrant Email: c9ad5a410f8d417e8cce17434be948e4.protect@withheldforprivacy.com\nRegistry Admin ID: \nAdmin Name: Withheld for Privacy Purposes\nAdmin Organization: Privacy service provided by Withheld for Privacy ehf\nAdmin Street: Kalkofnsvegur 2 \nAdmin City: Reykjavik\nAdmin State/Province: Capital Region\nAdmin Postal Code: 101\nAdmin Country: IS\nAdmin Phone: +354.4212434\nAdmin Phone Ext: \nAdmin Fax: \nAdmin Fax Ext: \nAdmin Email: c9ad5a410f8d417e8cce17434be948e4.protect@withheldforprivacy.com\nRegistry Tech ID: \nTech Name: Withheld for Privacy Purposes\nTech Organization: Privacy service provided by Withheld for Privacy ehf\nTech Street: Kalkofnsvegur 2 \nTech City: Reykjavik\nTech State/Province: Capital Region\nTech Postal Code: 101\nTech Country: IS\nTech Phone: +354.4212434\nTech Phone Ext: \nTech Fax: \nTech Fax Ext: \nTech Email: c9ad5a410f8d417e8cce17434be948e4.protect@withheldforprivacy.com\nName Server: verify-contact-details.namecheap.com\nName Server: failed-whois-verification.namecheap.com\nDNSSEC: unsigned\nURL of the ICANN WHOIS Data Problem Reporting System: http://wdprs.internic.net/\nFor more information on Whois status codes, please visit https://icann.org/epp\n"}}], "has_found": true}}]
```



#### Investigate Domain
Enrich external domain entity with DomainTools Iris Investigate and return CSV output
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Domain|The domain to investigate.|False|String||



##### JSON Results
```json
[{"Entity": "HTTP://MARKOSSOLOMON.COM/F1Q7QX.PHP", "EntityResult": {"name": "markossolomon.com", "last_enriched": "2026-02-19", "analytics": {"overall_risk_score": 23, "proximity_risk_score": 23, "malware_risk_score": "", "phishing_risk_score": "", "spam_risk_score": "", "threat_profile_risk_score": {"risk_score": "", "threats": "", "evidence": ""}, "website_response_code": 349, "google_adsense": [{"value": {"value": "", "count": 0}}], "google_analytics": [{"value": {"value": "", "count": 0}}], "ga4": [], "gtm_codes": [], "fb_codes": [], "hotjar_codes": [], "baidu_codes": [], "yandex_codes": [], "matomo_codes": [], "statcounter_project_codes": [], "statcounter_security_codes": [], "popularity_rank": "None", "tags": []}, "identity": {"registrant_name": "Redacted for Privacy", "registrant_org": "Privacy service provided by Withheld for Privacy ehf", "registrar": {"value": "NAMECHEAP INC", "count": 31147790}, "soa_email": [{"value": "hostmaster@markossolomon.com", "count": 1}], "ssl_email": [], "email_domains": ["namecheap.com", "withheldforprivacy.com"], "additional_whois_emails": [{"value": "abuse@namecheap.com", "count": 64168972}], "registrant_contact": {"country": {"value": "is", "count": 37734014}, "email": [{"value": "7b5590c2745f4a12afdd41c2056051b3.protect@withheldforprivacy.com", "count": 1}], "name": {"value": "Redacted for Privacy", "count": 31000866}, "phone": {"value": "3544212434", "count": 25222042}, "street": {"value": "Kalkofnsvegur 2", "count": 36834400}, "city": {"value": "Reykjavik", "count": 36980069}, "state": {"value": "Capital Region", "count": 49680190}, "postal": {"value": "101", "count": 36931305}, "org": {"value": "Privacy service provided by Withheld for Privacy ehf", "count": 48005278}}, "admin_contact": {"country": {"value": "is", "count": 37734014}, "email": [{"value": "7b5590c2745f4a12afdd41c2056051b3.protect@withheldforprivacy.com", "count": 1}], "name": {"value": "Redacted for Privacy", "count": 31000866}, "phone": {"value": "3544212434", "count": 25222042}, "street": {"value": "Kalkofnsvegur 2", "count": 36834400}, "city": {"value": "Reykjavik", "count": 36980069}, "state": {"value": "Capital Region", "count": 49680190}, "postal": {"value": "101", "count": 36931305}, "org": {"value": "Privacy service provided by Withheld for Privacy ehf", "count": 48005278}}, "technical_contact": {"country": {"value": "is", "count": 37734014}, "email": [{"value": "7b5590c2745f4a12afdd41c2056051b3.protect@withheldforprivacy.com", "count": 1}], "name": {"value": "Redacted for Privacy", "count": 31000866}, "phone": {"value": "3544212434", "count": 25222042}, "street": {"value": "Kalkofnsvegur 2", "count": 36834400}, "city": {"value": "Reykjavik", "count": 36980069}, "state": {"value": "Capital Region", "count": 49680190}, "postal": {"value": "101", "count": 36931305}, "org": {"value": "Privacy service provided by Withheld for Privacy ehf", "count": 48005278}}, "billing_contact": {"country": {"value": "", "count": 0}, "email": [], "name": {"value": "", "count": 0}, "phone": {"value": "", "count": 0}, "street": {"value": "", "count": 0}, "city": {"value": "", "count": 0}, "state": {"value": "", "count": 0}, "postal": {"value": "", "count": 0}, "org": {"value": "", "count": 0}}}, "registration": {"registrar_status": ["clienttransferprohibited"], "domain_status": false, "create_date": "2013-12-06", "expiration_date": "2022-12-06"}, "hosting": {"ip_addresses": [{"address": {"value": "99.83.154.118", "count": 8702028}, "asn": [{"value": 16509, "count": 171896407}], "country_code": {"value": "us", "count": 190010201}, "isp": {"value": "Amazon.com Inc.", "count": 82746846}}], "ip_country_code": "us", "mx_servers": [], "spf_info": [], "name_servers": [{"host": {"value": "dns101.registrar-servers.com", "count": 31005633}, "domain": {"value": "registrar-servers.com", "count": 47697498}, "ip": [{"value": "13.248.239.149", "count": 8992397}]}, {"host": {"value": "dns102.registrar-servers.com", "count": 30985073}, "domain": {"value": "registrar-servers.com", "count": 47697498}, "ip": [{"value": "76.223.108.9", "count": 8991773}]}, {"host": {"value": "dns1.registrar-servers.com", "count": 23915549}, "domain": {"value": "registrar-servers.com", "count": 47697498}, "ip": [{"value": "156.154.132.200", "count": 26165120}]}, {"host": {"value": "dns2.registrar-servers.com", "count": 23905522}, "domain": {"value": "registrar-servers.com", "count": 47697498}, "ip": [{"value": "156.154.133.200", "count": 26174394}]}], "ssl_certificates": [], "redirects_to": {"value": "", "count": 0}, "redirect_domain": {"value": "", "count": 0}}, "website_title": "", "first_seen": "2013-12-06T00:00:00Z", "server_type": ""}}]
```



#### Get Domain Rdap
Enrich external domain entity with DomainTools threat Intelligence data and return CSV output
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Domain|The domain to get the parsed domain RDAP result.|False|String||



##### JSON Results
```json
[{"Entity": "HTTP://MARKOSSOLOMON.COM/F1Q7QX.PHP", "EntityResult": {"domain": "domaintools.com", "handle": "1697312_DOMAIN_COM-VRSN", "domain_statuses": ["client transfer prohibited"], "creation_date": "1998-08-02T04:00:00+00:00", "last_changed_date": "2020-01-09T23:06:29+00:00", "expiration_date": "2027-08-01T04:00:00+00:00", "registrar": {"name": "ENOM, INC.", "iana_id": "48", "contacts": [{"name": "", "org": "", "email": "ABUSE@ENOM.COM", "phone": "tel:+1.4259744689", "street": "", "city": "", "postal": "", "region": "", "country": "", "roles": ["abuse"]}]}, "contacts": [{"name": "Domain Administrator", "org": "DomainTools, LLC", "email": "memberservices@domaintools.com", "phone": "tel:+1.2068389035", "street": "2101 4th Ave Suite 1720", "city": "Seattle", "postal": "98121", "region": "WA", "country": "US", "roles": ["registrant"]}], "dnssec": {"signed": false}, "nameservers": ["DNS1.P04.NSONE.NET", "DNS2.P04.NSONE.NET", "DNS3.P04.NSONE.NET", "DNS4.P04.NSONE.NET"], "conformance": [], "emails": ["abuse@enom.com", "memberservices@domaintools.com"], "email_domains": ["domaintools.com", "enom.com"], "has_found": true}}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds









