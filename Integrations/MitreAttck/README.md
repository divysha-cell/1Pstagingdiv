
# MitreAttck

MITRE ATT&CK™ is a globally-accessible knowledge base of adversary tactics and techniques based on real-world observations. The ATT&CK knowledge base is used as a foundation for the development of specific threat models and methodologies in the private sector, in government, and in the cybersecurity product and service community.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|None|True|IP_OR_HOST|https://raw.githubusercontent.com/mitre/cti/master/enterprise-attack/enterprise-attack.json|
|Verify SSL|None|False|Boolean|True|


#### Dependencies
| |
|-|
|urllib3-2.2.1-py3-none-any.whl|
|idna-3.7-py3-none-any.whl|
|typing_extensions-4.15.0-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|pyasn1-0.6.3-py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|certifi-2024.2.2-py3-none-any.whl|
|pycparser-3.0-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|anyio-4.13.0-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|google_auth_httplib2-0.3.0-py3-none-any.whl|
|proto_plus-1.27.1-py3-none-any.whl|
|pyopenssl-25.3.0-py3-none-any.whl|
|PyJWT-2.9.0-py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|filelock-3.15.4-py3-none-any.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|httplib2-0.31.2-py3-none-any.whl|
|requests_toolbelt-1.0.0-py2.py3-none-any.whl|
|google_api_core-2.30.0-py3-none-any.whl|
|tldextract-5.1.2-py3-none-any.whl|
|TIPCommon-2.3.8-py3-none-any.whl|
|google_auth-2.47.0-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|requests_file-2.1.0-py2.py3-none-any.whl|
|protobuf-6.33.6-cp39-abi3-manylinux2014_x86_64.whl|
|cryptography-46.0.5-cp311-abi3-manylinux_2_34_x86_64.whl|
|cachetools-5.5.0-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|google_api_python_client-2.188.0-py3-none-any.whl|
|googleapis_common_protos-1.73.0-py3-none-any.whl|


## Actions
#### Get Technique Details
Retrieve detailed information about MITRE attack technique
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Technique Identifier|Specify the comma-separated list of identifiers that will be used to find the detailed information about techniques. Example: identifier_1,identifier_2|True|String||
|Identifier Type|Specify what identifier type to use. Possible values: Name (Example: Access Token Manipulation) ID (Example: attack-pattern--478aa214-2ca7-4ec0-9978-18798e514790) External ID (Example: T1050)|True|List|ID|
|Create Insights|If enabled, action will create a separate insight for every processed technique|False|Boolean|false|



##### JSON Results
```json
[{"created_by_ref":"identity--c78cb6e5-0c4b-4611-8297-d1xxxxxxxxxx","external_references":[{"url":"https://attack.mitre.org/techniques/Txxxx","external_id":"Txxxx","source_name":"mitre-attack"},{"url":"http://www.netsec.colostate.edu/~zhang/DetectingEncryptedBotnetTraffic.pdf","source_name":"Zhang 2013","description":"Zhang, H., Papadopoulos, C., & Massey, D. (2013, April). Detecting encrypted botnet traffic. Retrieved August 19, 2015."},{"url":"https://en.wikipedia.org/wiki/List_of_file_signatures","source_name":"Wikipedia File Header Signatures","description":"Wikipedia. (2016, March 31). List of file signatures. Retrieved April 22, 2016."}],"created":"2017-05-31T21:30:30.26Z","x_mitre_platforms":["Linux","macOS","Windows"],"type":"attack-pattern","description":"Data is encrypted before being exfiltrated in order to hide the information that is being exfiltrated from detection or to make the exfiltration less conspicuous upon inspection by a defender. The encryption is performed by a utility, programming library, or custom algorithm on the data itself and is considered separate from any encryption performed by the command and control or file transfer protocol. Common file archive formats that can encrypt files are RAR and zip.\n\nOther exfiltration techniques likely apply as well to transfer the information out of the network, such as [Exfiltration Over Command and Control Channel](https://attack.mitre.org/techniques/Txxxx) and [Exfiltration Over Alternative Protocol](https://attack.mitre.org/techniques/Txxxx)","kill_chain_phases":[{"phase_name":"exfiltration","kill_chain_name":"mitre-attack"}],"modified":"2018-10-17T00:14:20.652Z","id":"attack-pattern--d54416bd-0803-41ca-870a-cexxxxxxxxxx","object_marking_refs":["marking-definition--fa42a846-8d90-4e51-bc29-71xxxxxxxxxx"],"x_mitre_network_requirements":false,"x_mitre_version":"1.0","x_mitre_data_sources":["File monitoring","Process monitoring","Process command-line parameters","Binary file metadata"],"x_mitre_detection":"Encryption software and encrypted files can be detected in many ways. Common utilities that may be present on the system or brought in by an adversary may be detectable through process monitoring and monitoring for command-line arguments for known encryption utilities. This may yield a significant amount of benign events, depending on how systems in the environment are typically used. Often the encryption key is stated within command-line invocation of the software. \n\nA process that loads the Windows DLL crypt32.dll may be used to perform encryption, decryption, or verification of file signatures. \n\nNetwork traffic may also be analyzed for entropy to determine if encrypted data is being transmitted. (Citation: Zhang 2013) If the communications channel is unencrypted, encrypted files of known file types can be detected in transit during exfiltration with a network intrusion detection or data loss prevention system analyzing file headers. (Citation: Wikipedia File Header Signatures)","name":"Data Encrypted"}, {"x_mitre_detection":"While users may customize their <code>~/.bashrc</code> and <code>~/.bash_profile</code> files , there are only certain types of commands that typically appear in these files. Monitor for abnormal commands such as execution of unknown programs, opening network sockets, or reaching out across the network when user profiles are loaded during the login process.","created_by_ref":"identity--c78cb6e5-0c4b-4611-8297-d1xxxxxxxxxx","description":"Adversaries may establish persistence by executing malicious content triggered by a user’s shell. <code>~/.bash_profile</code> and <code>~/.bashrc</code> are shell scripts that contain shell commands. These files are executed in a user's context when a new shell opens or when a user logs in so that their environment is set correctly.\n\n<code>~/.bash_profile</code> is executed for login shells and <code>~/.bashrc</code> is executed for interactive non-login shells. This means that when a user logs in (via username and password) to the console (either locally or remotely via something like SSH), the <code>~/.bash_profile</code> script is executed before the initial command prompt is returned to the user. After that, every time a new shell is opened, the <code>~/.bashrc</code> script is executed. This allows users more fine-grained control over when they want certain commands executed. These shell scripts are meant to be written to by the local user to configure their own environment.\n\nThe macOS Terminal.app is a little different in that it runs a login shell by default each time a new terminal window is opened, thus calling <code>~/.bash_profile</code> each time instead of <code>~/.bashrc</code>.\n\nAdversaries may abuse these shell scripts by inserting arbitrary shell commands that may be used to execute other binaries to gain persistence. Every time the user logs in or opens a new shell, the modified ~/.bash_profile and/or ~/.bashrc scripts will be executed.(Citation: amnesia malware)","created":"2020-01-24T14:13:45.936Z","x_mitre_data_sources":["Process use of network","Process command-line parameters","Process monitoring","File monitoring"],"x_mitre_is_subtechnique":true,"x_mitre_permissions_required":["User","Administrator"],"kill_chain_phases":[{"phase_name":"privilege-escalation","kill_chain_name":"mitre-attack"},{"phase_name":"persistence","kill_chain_name":"mitre-attack"}],"modified":"2020-03-24T16:28:04.990Z","name":".bash_profile and .bashrc","x_mitre_platforms":["Linux","macOS"],"object_marking_refs":["marking-definition--fa42a846-8d90-4e51-bc29-71xxxxxxxxxx"],"x_mitre_version":"1.0","type":"attack-pattern","id":"attack-pattern--b63a34e8-0a61-4c97-a23b-bfxxxxxxxxxx","external_references":[{"url":"https://attack.mitre.org/techniques/Txxxx/xxx","external_id":"Txxxx.xxx","source_name":"mitre-attack"},{"url":"https://researchcenter.paloaltonetworks.com/2017/04/unit42-new-iotlinux-malware-targets-dvrs-forms-botnet/","source_name":"amnesia malware","description":"Claud Xiao, Cong Zheng, Yanhui Jia. (2017, April 6). New IoT/Linux Malware Targets DVRs, Forms Botnet. Retrieved February 19, 2018."}]}]
```



#### Get Techniques Mitigations
Retrieve information about mitigations that are associated with MITRE attack techniques.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Technique ID|Specify the identifier that will be used to find the mitigations related to attack technique. Comma-separated values.|True|String||
|Identifier Type|Specify what identifier type to use. Possible values: Attack Name (Example: Access Token Manipulation) Attack ID (Example: attack-pattern--478aa214-2ca7-4ec0-9978-18798e514790) External Attack ID (Example: T1050)|True|List|Attack ID|
|Max Mitigations to Return|Specify how many mitigations to return.|False|String|20|



##### JSON Results
```json
[{"Entity": "course-of-action--4f170666-7edb-4489-85c2-9affa28a72e0", "EntityResult": {"mitigations": [{"created_by_ref":"identity--c78cb6e5-0c4b-4611-8297-d1b8b55e40b5","description":"Identify unnecessary system utilities, third-party tools, or potentially malicious software that may be used to encrypt files, and audit and/or block them by using whitelisting (Citation: Beechey 2010) tools, like AppLocker, (Citation: Windows Commands JPCERT) (Citation: NSA MS AppLocker) or Software Restriction Policies (Citation: Corio 2008) where appropriate. (Citation: TechNet Applocker vs SRP)","created":"2018-10-17T00:14:20.652Z","x_mitre_deprecated":true,"modified":"2019-07-24T14:26:14.411Z","object_marking_refs":["marking-definition--fa42a846-8d90-4e51-bc29-71d5b4802168"],"external_references":[{"url":"https://attack.mitre.org/mitigations/T1022","source_name":"mitre-attack","external_id":"T1022"},{"url":"http://www.sans.org/reading-room/whitepapers/application/application-whitelisting-panacea-propaganda-33599","source_name":"Beechey 2010","description":"Beechey, J. (2010, December). Application Whitelisting: Panacea or Propaganda?. Retrieved November 18, 2014."},{"url":"http://blog.jpcert.or.jp/2016/01/windows-commands-abused-by-attackers.html","source_name":"Windows Commands JPCERT","description":"Tomonaga, S. (2016, January 26). Windows Commands Abused by Attackers. Retrieved February 2, 2016."},{"url":"https://www.iad.gov/iad/library/ia-guidance/tech-briefs/application-whitelisting-using-microsoft-applocker.cfm","source_name":"NSA MS AppLocker","description":"NSA Information Assurance Directorate. (2014, August). Application Whitelisting Using Microsoft AppLocker. Retrieved March 31, 2016."},{"url":"http://technet.microsoft.com/en-us/magazine/2008.06.srp.aspx","source_name":"Corio 2008","description":"Corio, C., & Sayana, D. P. (2008, June). Application Lockdown with Software Restriction Policies. Retrieved November 18, 2014."},{"url":"https://technet.microsoft.com/en-us/library/ee791851.aspx","source_name":"TechNet Applocker vs SRP","description":"Microsoft. (2012, June 27). Using Software Restriction Policies and AppLocker Policies. Retrieved April 7, 2016."}],"x_mitre_version":"1.0","type":"course-of-action","id":"course-of-action--2a8de25c-f743-4348-b101-3ee33ab5871b","name":"Data Encrypted Mitigation"}]}}]
```



#### Get Associated Intrusions
Retrieve information about intrusions that are associated with MITRE attack technique.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Technique ID|Specify the identifier that will be used to find the associated intrusions.|True|String||
|Identifier Type|Specify what identifier type to use. Possible values: Attack Name (Example: Access Token Manipulation) Attack ID (Example: attack-pattern--478aa214-2ca7-4ec0-9978-18798e514790) External Attack ID (Example: T1050)|True|List|Attack ID|
|Max Intrusions to Return|Specify how many intrusions to return.|False|String|20|



##### JSON Results
```json
[{"created_by_ref":"identity--c78cb6e5-0c4b-4611-8297-d1b8b55e40b5","description":"[APT32](https://attack.mitre.org/groups/G0050) is a threat group that has been active since at least 2014. The group has targeted multiple private sector industries as well as with foreign governments, dissidents, and journalists with a strong focus on Southeast Asian countries like Vietnam, the Philippines, Laos, and Cambodia. They have extensively used strategic web compromises to compromise victims. The group is believed to be Vietnam-based. (Citation: FireEye APT32 May 2017) (Citation: Volexity OceanLotus Nov 2017) (Citation: ESET OceanLotus)","created":"2017-12-14T16:46:06.044Z","x_mitre_contributors":["Romain Dumont, ESET"],"modified":"2019-07-17T13:11:37.402Z","name":"APT32","object_marking_refs":["marking-definition--fa42a846-8d90-4e51-bc29-71d5b4802168"],"x_mitre_version":"2.0","aliases":["APT32","SeaLotus","OceanLotus","APT-C-00"],"type":"intrusion-set","id":"intrusion-set--247cb30b-955f-42eb-97a5-a89fef69341e","external_references":[{"url":"https://attack.mitre.org/groups/G0050","source_name":"mitre-attack","external_id":"G0050"},{"source_name":"APT32","description":"(Citation: FireEye APT32 May 2017) (Citation: Volexity OceanLotus Nov 2017)(Citation: Cybereason Oceanlotus May 2017)"},{"source_name":"SeaLotus","description":"(Citation: Cybereason Oceanlotus May 2017)"},{"source_name":"OceanLotus","description":"(Citation: FireEye APT32 May 2017) (Citation: Volexity OceanLotus Nov 2017)(Citation: Cybereason Oceanlotus May 2017)"},{"source_name":"APT-C-00","description":"(Citation: ESET OceanLotus)(Citation: Cybereason Oceanlotus May 2017)"},{"url":"https://www.fireeye.com/blog/threat-research/2017/05/cyber-espionage-apt32.html","source_name":"FireEye APT32 May 2017","description":"Carr, N.. (2017, May 14). Cyber Espionage is Alive and Well: APT32 and the Threat to Global Corporations. Retrieved June 18, 2017."},{"url":"https://www.volexity.com/blog/2017/11/06/oceanlotus-blossoms-mass-digital-surveillance-and-exploitation-of-asean-nations-the-media-human-rights-and-civil-society/","source_name":"Volexity OceanLotus Nov 2017","description":"Lassalle, D., et al. (2017, November 6). OceanLotus Blossoms: Mass Digital Surveillance and Attacks Targeting ASEAN, Asian Nations, the Media, Human Rights Groups, and Civil Society. Retrieved November 6, 2017."},{"url":"https://www.welivesecurity.com/2018/03/13/oceanlotus-ships-new-backdoor/","source_name":"ESET OceanLotus","description":"Foltýn, T. (2018, March 13). OceanLotus ships new backdoor using old tricks. Retrieved May 22, 2018."},{"url":"https://www.cybereason.com/blog/operation-cobalt-kitty-apt","source_name":"Cybereason Oceanlotus May 2017","description":"Dahan, A. (2017, May 24). OPERATION COBALT KITTY: A LARGE-SCALE APT IN ASIA CARRIED OUT BY THE OCEANLOTUS GROUP. Retrieved November 5, 2018."}]},{"created_by_ref":"identity--c78cb6e5-0c4b-4611-8297-d1b8b55e40b5","name":"BRONZE BUTLER","created":"2018-01-16T16:13:52.465Z","description":"[BRONZE BUTLER](https://attack.mitre.org/groups/G0060) is a cyber espionage group with likely Chinese origins that has been active since at least 2008. The group primarily targets Japanese organizations, particularly those in government, biotechnology, electronics manufacturing, and industrial chemistry. (Citation: Trend Micro Daserf Nov 2017) (Citation: Secureworks BRONZE BUTLER Oct 2017)","modified":"2019-03-22T19:57:36.804Z","object_marking_refs":["marking-definition--fa42a846-8d90-4e51-bc29-71d5b4802168"],"external_references":[{"url":"https://attack.mitre.org/groups/G0060","source_name":"mitre-attack","external_id":"G0060"},{"source_name":"BRONZE BUTLER","description":"(Citation: Trend Micro Daserf Nov 2017)"},{"source_name":"REDBALDKNIGHT","description":"(Citation: Trend Micro Daserf Nov 2017)"},{"source_name":"Tick","description":"(Citation: Trend Micro Daserf Nov 2017) (Citation: Symantec Tick Apr 2016)"},{"url":"http://blog.trendmicro.com/trendlabs-security-intelligence/redbaldknight-bronze-butler-daserf-backdoor-now-using-steganography/","source_name":"Trend Micro Daserf Nov 2017","description":"Chen, J. and Hsieh, M. (2017, November 7). REDBALDKNIGHT/BRONZE BUTLER's Daserf Backdoor Now Using Steganography. Retrieved December 27, 2017."},{"url":"https://www.secureworks.com/research/bronze-butler-targets-japanese-businesses","source_name":"Secureworks BRONZE BUTLER Oct 2017","description":"Counter Threat Unit Research Team. (2017, October 12). BRONZE BUTLER Targets Japanese Enterprises. Retrieved January 4, 2018."},{"url":"https://www.symantec.com/connect/blogs/tick-cyberespionage-group-zeros-japan","source_name":"Symantec Tick Apr 2016","description":"DiMaggio, J. (2016, April 28). Tick cyberespionage group zeros in on Japan. Retrieved July 16, 2018."}],"x_mitre_version":"1.0","type":"intrusion-set","id":"intrusion-set--93f52415-0fe4-4d3d-896c-fc9b8e88ab90","aliases":["BRONZE BUTLER","REDBALDKNIGHT","Tick"]},{"created_by_ref":"identity--c78cb6e5-0c4b-4611-8297-d1b8b55e40b5","name":"CopyKittens","created":"2018-01-16T16:13:52.465Z","description":"[CopyKittens](https://attack.mitre.org/groups/G0052) is an Iranian cyber espionage group that has been operating since at least 2013. It has targeted countries including Israel, Saudi Arabia, Turkey, the U.S., Jordan, and Germany. The group is responsible for the campaign known as Operation Wilted Tulip. (Citation: ClearSky CopyKittens March 2017) (Citation: ClearSky Wilted Tulip July 2017) (Citation: CopyKittens Nov 2015)","modified":"2019-05-03T16:42:19.026Z","object_marking_refs":["marking-definition--fa42a846-8d90-4e51-bc29-71d5b4802168"],"external_references":[{"url":"https://attack.mitre.org/groups/G0052","source_name":"mitre-attack","external_id":"G0052"},{"source_name":"CopyKittens","description":"(Citation: ClearSky CopyKittens March 2017) (Citation: ClearSky Wilted Tulip July 2017) (Citation: CopyKittens Nov 2015)"},{"url":"http://www.clearskysec.com/copykitten-jpost/","source_name":"ClearSky CopyKittens March 2017","description":"ClearSky Cyber Security. (2017, March 30). Jerusalem Post and other Israeli websites compromised by Iranian threat agent CopyKitten. Retrieved August 21, 2017."},{"url":"http://www.clearskysec.com/wp-content/uploads/2017/07/Operation_Wilted_Tulip.pdf","source_name":"ClearSky Wilted Tulip July 2017","description":"ClearSky Cyber Security and Trend Micro. (2017, July). Operation Wilted Tulip: Exposing a cyber espionage apparatus. Retrieved August 21, 2017."},{"url":"https://s3-eu-west-1.amazonaws.com/minervaresearchpublic/CopyKittens/CopyKittens.pdf","source_name":"CopyKittens Nov 2015","description":"Minerva Labs LTD and ClearSky Cyber Security. (2015, November 23). CopyKittens Attack Group. Retrieved September 11, 2017."}],"x_mitre_version":"1.1","type":"intrusion-set","id":"intrusion-set--dcd81c6e-ebf7-4a16-93e0-9a97fa49c88a","aliases":["CopyKittens"]}]
```



#### Get Mitigations
Retrieve information about mitigations that are associated with MITRE attack technique
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Technique ID|Specify the identifier that will be used to find the mitigations related to attack technique.|True|String||
|Identifier Type|Specify what identifier type to use. Possible values: Attack Name (Example: Access Token Manipulation) Attack ID (Example: attack-pattern--478aa214-2ca7-4ec0-9978-18798e514790) External Attack ID (Example: T1050)|True|List|Attack ID|
|Max Mitigations to Return|Specify how many mitigations to return.|False|String|20|



##### JSON Results
```json
[{"created_by_ref":"identity--c78cb6e5-0c4b-4611-8297-d1b8b55e40b5","description":"Identify unnecessary system utilities, third-party tools, or potentially malicious software that may be used to encrypt files, and audit and/or block them by using whitelisting (Citation: Beechey 2010) tools, like AppLocker, (Citation: Windows Commands JPCERT) (Citation: NSA MS AppLocker) or Software Restriction Policies (Citation: Corio 2008) where appropriate. (Citation: TechNet Applocker vs SRP)","created":"2018-10-17T00:14:20.652Z","x_mitre_deprecated":true,"modified":"2019-07-24T14:26:14.411Z","object_marking_refs":["marking-definition--fa42a846-8d90-4e51-bc29-71d5b4802168"],"external_references":[{"url":"https://attack.mitre.org/mitigations/T1022","source_name":"mitre-attack","external_id":"T1022"},{"url":"http://www.sans.org/reading-room/whitepapers/application/application-whitelisting-panacea-propaganda-33599","source_name":"Beechey 2010","description":"Beechey, J. (2010, December). Application Whitelisting: Panacea or Propaganda?. Retrieved November 18, 2014."},{"url":"http://blog.jpcert.or.jp/2016/01/windows-commands-abused-by-attackers.html","source_name":"Windows Commands JPCERT","description":"Tomonaga, S. (2016, January 26). Windows Commands Abused by Attackers. Retrieved February 2, 2016."},{"url":"https://www.iad.gov/iad/library/ia-guidance/tech-briefs/application-whitelisting-using-microsoft-applocker.cfm","source_name":"NSA MS AppLocker","description":"NSA Information Assurance Directorate. (2014, August). Application Whitelisting Using Microsoft AppLocker. Retrieved March 31, 2016."},{"url":"http://technet.microsoft.com/en-us/magazine/2008.06.srp.aspx","source_name":"Corio 2008","description":"Corio, C., & Sayana, D. P. (2008, June). Application Lockdown with Software Restriction Policies. Retrieved November 18, 2014."},{"url":"https://technet.microsoft.com/en-us/library/ee791851.aspx","source_name":"TechNet Applocker vs SRP","description":"Microsoft. (2012, June 27). Using Software Restriction Policies and AppLocker Policies. Retrieved April 7, 2016."}],"x_mitre_version":"1.0","type":"course-of-action","id":"course-of-action--2a8de25c-f743-4348-b101-3ee33ab5871b","name":"Data Encrypted Mitigation"}]
```



#### Get Techniques Details
Retrieve detailed information about MITRE attack techniques.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Technique Identifier|Specify the identifier that will be used to find the detailed information about technique. Comma-separated values.|True|String||
|Identifier Type|Specify what identifier type to use. Possible values: Name (Example: Access Token Manipulation) ID (Example: attack-pattern--478aa214-2ca7-4ec0-9978-18798e514790) External ID (Example: T1050)|True|List|ID|



##### JSON Results
```json
[{"Entity": "course-of-action--4f170666-7edb-4489-85c2-9affa28a72e0", "EntityResult": {"created_by_ref":"identity--c78cb6e5-0c4b-4611-8297-d1b8b55e40b5","external_references":[{"url":"https://attack.mitre.org/techniques/T1022","external_id":"T1022","source_name":"mitre-attack"},{"url":"http://www.netsec.colostate.edu/~zhang/DetectingEncryptedBotnetTraffic.pdf","source_name":"Zhang 2013","description":"Zhang, H., Papadopoulos, C., & Massey, D. (2013, April). Detecting encrypted botnet traffic. Retrieved August 19, 2015."},{"url":"https://en.wikipedia.org/wiki/List_of_file_signatures","source_name":"Wikipedia File Header Signatures","description":"Wikipedia. (2016, March 31). List of file signatures. Retrieved April 22, 2016."}],"created":"2017-05-31T21:30:30.26Z","x_mitre_platforms":["Linux","macOS","Windows"],"type":"attack-pattern","description":"Data is encrypted before being exfiltrated in order to hide the information that is being exfiltrated from detection or to make the exfiltration less conspicuous upon inspection by a defender. The encryption is performed by a utility, programming library, or custom algorithm on the data itself and is considered separate from any encryption performed by the command and control or file transfer protocol. Common file archive formats that can encrypt files are RAR and zip.\n\nOther exfiltration techniques likely apply as well to transfer the information out of the network, such as [Exfiltration Over Command and Control Channel](https://attack.mitre.org/techniques/T1041) and [Exfiltration Over Alternative Protocol](https://attack.mitre.org/techniques/T1048)","kill_chain_phases":[{"phase_name":"exfiltration","kill_chain_name":"mitre-attack"}],"modified":"2018-10-17T00:14:20.652Z","id":"attack-pattern--d54416bd-0803-41ca-870a-ce1af7c05638","object_marking_refs":["marking-definition--fa42a846-8d90-4e51-bc29-71d5b4802168"],"x_mitre_network_requirements":false,"x_mitre_version":"1.0","x_mitre_data_sources":["File monitoring","Process monitoring","Process command-line parameters","Binary file metadata"],"x_mitre_detection":"Encryption software and encrypted files can be detected in many ways. Common utilities that may be present on the system or brought in by an adversary may be detectable through process monitoring and monitoring for command-line arguments for known encryption utilities. This may yield a significant amount of benign events, depending on how systems in the environment are typically used. Often the encryption key is stated within command-line invocation of the software. \n\nA process that loads the Windows DLL crypt32.dll may be used to perform encryption, decryption, or verification of file signatures. \n\nNetwork traffic may also be analyzed for entropy to determine if encrypted data is being transmitted. (Citation: Zhang 2013) If the communications channel is unencrypted, encrypted files of known file types can be detected in transit during exfiltration with a network intrusion detection or data loss prevention system analyzing file headers. (Citation: Wikipedia File Header Signatures)","name":"Data Encrypted"}}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds









