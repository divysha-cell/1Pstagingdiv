<p align="center">
<img src="./EDR Network Event.png" 
     alt="EDR Network Event" width="200"/></p>
     
# EDR Network Event

### Description
EDR Network Event

### Rules
|Primary Source|Secondary Source|Third Source|Forth Source|Type|Primary Destination|Secondary Destination|Third Destination|Forth Destination|
|--------------|----------------|------------|------------|----|-------------------|---------------------|-----------------|-----------------|
|FileName|FileHash|||Linked|SourceProcessName||||
|FileName|FileHash|||Linked|ThreatSignature||||
|FileName||||Linked|FileHash||||
|DestinationHostName||||Linked|DestinationAddress||||
|SourceAddress|SourceHostName|DestinationProcessName||Type|DestinationProcessName|FileName|DestinationHostName||
|DestinationHostName|DestinationAddress|||Linked|ThreatSignature||||
|SourceHostName||||Linked|SourceAddress||||
|SourceProcessName|FileName|||Linked|FileName|FileHash|||
|DestinationHostName||||Linked|FileName||||
|SourceProcessName||||Linked|DestinationHostName|DestinationAddress|||
|DestinationUserName||||Linked|DestinationHostName||||
