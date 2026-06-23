<p align="center">
<img src="./Custom MailRelayOrTAP.png" 
     alt="Custom MailRelayOrTAP" width="200"/></p>
     
# Custom MailRelayOrTAP

### Description
Email monitoring event

### Rules
|Primary Source|Secondary Source|Third Source|Forth Source|Type|Primary Destination|Secondary Destination|Third Destination|Forth Destination|
|--------------|----------------|------------|------------|----|-------------------|---------------------|-----------------|-----------------|
|DestinationUserName||||Linked|DestinationHostName|DestinationAddress|||
|DestinationHostName||||Linked|DestinationAddress||||
|SourceUserName|DestinationUserName|||Linked|EmailSubject||||
|SourceUserName|DestinationUserName|||Linked|DestinationURL||||
|SourceUserName|DestinationUserName|||Linked|ThreatSignature||||
|SourceUserName|DestinationUserName|||Linked|FileName||||
|FileName|DestinationUserName|||Linked|FileHash||||
|SourceUserName|SourceHostName|SourceAddress||Type|DestinationUserName|DestinationHostName|DestinationAddress||
|SourceUserName||||Linked|SourceHostName|SourceAddress|||
|SourceHostName||||Linked|SourceAddress||||
