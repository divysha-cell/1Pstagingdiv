<p align="center">
<img src="./ActiveDirectory user creation.png" 
     alt="ActiveDirectory user creation" width="200"/></p>
     
# ActiveDirectory user creation

### Description
Suspicious Active Directory activity

### Rules
|Primary Source|Secondary Source|Third Source|Forth Source|Type|Primary Destination|Secondary Destination|Third Destination|Forth Destination|
|--------------|----------------|------------|------------|----|-------------------|---------------------|-----------------|-----------------|
|SourceHostName||||Linked|SourceAddress||||
|DestinationProcessName||||Linked|FileName||||
|SourceUserName||||Linked|SourceHostName|SourceAddress|||
|DestinationUserName||||Linked|DestinationProcessName|FileName|||
|SourceUserName|SourceHostName|SourceAddress||Type|DestinationHostName|DestinationUserName|FileName||
|DestinationHostName||||Linked|DestinationUserName||||
