<p align="center">
<img src="./BlueCoat Proxy.png" 
     alt="BlueCoat Proxy" width="200"/></p>
     
# BlueCoat Proxy

### Description
Suspicious outgoing web access

### Rules
|Primary Source|Secondary Source|Third Source|Forth Source|Type|Primary Destination|Secondary Destination|Third Destination|Forth Destination|
|--------------|----------------|------------|------------|----|-------------------|---------------------|-----------------|-----------------|
|DestinationURL||||Linked|DestinationHostName|DestinationAddress|||
|DestinationURL|DestinationHostName|DestinationAddress||Linked|FileName||||
|DestinationURL|DestinationHostName|DestinationAddress||Linked|ThreatSignature||||
|SourceHostName||||Linked|SourceAddress||||
|SourceAddress|SourceHostName|DestinationURL||Type|DestinationURL|DestinationHostName|DestinationAddress||
