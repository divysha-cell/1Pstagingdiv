<p align="center">
<img src="./DLP Files.png" 
     alt="DLP Files" width="200"/></p>
     
# DLP Files

### Description
Files being exfiltrated

### Rules
|Primary Source|Secondary Source|Third Source|Forth Source|Type|Primary Destination|Secondary Destination|Third Destination|Forth Destination|
|--------------|----------------|------------|------------|----|-------------------|---------------------|-----------------|-----------------|
|SourceHostName||||Linked|SourceAddress||||
|SourceUserName||||Linked|SourceHostName|SourceAddress|||
|FileName||||Linked|SourceUserName|SourceHostName|SourceAddress||
|FileName|SourceHostName|SourceAddress||Type|DestinationHostName|DestinationAddress|||
|DestinationHostName||||Linked|DestinationAddress||||
