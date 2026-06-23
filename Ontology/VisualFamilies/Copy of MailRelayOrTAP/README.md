<p align="center">
<img src="./Copy of MailRelayOrTAP.png" 
     alt="Copy of MailRelayOrTAP" width="200"/></p>
     
# Copy of MailRelayOrTAP

### Description
Email monitoring event

### Rules
|Primary Source|Secondary Source|Third Source|Forth Source|Type|Primary Destination|Secondary Destination|Third Destination|Forth Destination|
|--------------|----------------|------------|------------|----|-------------------|---------------------|-----------------|-----------------|
|SourceUserName|SourceHostName|SourceAddress||Type|DestinationUserName|DestinationHostName|DestinationAddress||
|SourceUserName||||Linked|SourceHostName|SourceAddress|||
|SourceHostName||||Linked|SourceAddress||||
|DestinationUserName||||Linked|DestinationHostName|DestinationAddress|||
|DestinationHostName||||Linked|DestinationAddress||||
|SourceUserName|DestinationUserName|||Linked|EmailSubject||||
|SourceUserName|DestinationUserName|||Linked|DestinationURL||||
|SourceUserName|DestinationUserName|||Linked|ThreatSignature||||
|SourceUserName|DestinationUserName|||Linked|FileName||||
|FileName|DestinationUserName|||Linked|FileHash||||
