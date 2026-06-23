<p align="center">
<img src="./Copy of Default.png" 
     alt="Copy of Default" width="200"/></p>
     
# Copy of Default

### Description
Default alert visualization and entities extraction.

### Rules
|Primary Source|Secondary Source|Third Source|Forth Source|Type|Primary Destination|Secondary Destination|Third Destination|Forth Destination|
|--------------|----------------|------------|------------|----|-------------------|---------------------|-----------------|-----------------|
|SourceUserName|SourceHostName|SourceAddress||Type|DestinationUserName|DestinationHostName|DestinationAddress||
|SourceUserName||||Linked|SourceHostName||||
|SourceUserName||||Linked|SourceAddress||||
|SourceHostName||||Linked|SourceAddress||||
|DestinationUserName||||Linked|DestinationHostName||||
|DestinationUserName||||Linked|DestinationAddress||||
|DestinationHostName||||Linked|DestinationAddress||||
|SourceHostName|SourceAddress|SourceUserName||Linked|SourceProcessName||||
|DestinationHostName|DestinationAddress|DestinationUserName||Linked|DestinationProcessName||||
|SourceUserName|SourceHostName|DestinationUserName||Linked|DestinationURL||||
|SourceUserName|SourceHostName|SourceAddress||Linked|FileName||||
|SourceUserName|SourceHostName|SourceAddress||Linked|FileHash||||
|SourceUserName|SourceHostName|SourceAddress||Linked|EmailSubject||||
|SourceUserName|SourceHostName|SourceAddress||Linked|USB||||
|SourceUserName|SourceHostName|DestinationUserName||Linked|Deployment||||
|DestinationUserName|DestinationHostName|DestinationAddress||Linked|Deployment||||
|SourceHostName|SourceAddress|DestinationHostName||Linked|DestinationMacAddress||||
|SourceUserName||||Linked|SourceMacAddress||||
|SourceUserName|DestinationUserName|||Linked|CreditCard||||
|SourceUserName|DestinationUserName|||Linked|PhoneNumber||||
|SourceHostName|SourceAddress|DestinationHostName||Linked|CVE||||
|SourceUserName|SourceHostName|SourceAddress||Linked|ThreatActor||||
|DestinationUserName|DestinationHostName|DestinationAddress||Linked|ThreatActor||||
|SourceUserName|SourceHostName|SourceAddress||Linked|ThreatCampaign||||
|DestinationUserName|DestinationHostName|DestinationAddress||Linked|ThreatCampaign||||
|SourceUserName|SourceHostName|SourceAddress||Linked|ThreatSignature||||
|DestinationUserName|DestinationHostName|DestinationAddress||Linked|ThreatSignature||||
|SourceUserName|SourceHostName|SourceAddress||Linked|GenericEntity||||
|DestinationUserName|DestinationHostName|DestinationAddress||Linked|GenericEntity||||
