<p align="center">
<img src="./Carbon Black Process Event.png" 
     alt="Carbon Black Process Event" width="200"/></p>
     
# Carbon Black Process Event

### Description
Cross Process Event and Child Process Events: VMware Carbon Black EDR provides a cross-process event type that records an occurrence of a process that crosses the security boundary of another process. While some of these events are benign, others can indicate an attempt to change the behavior of the target process by a malicious process.

### Rules
|Primary Source|Secondary Source|Third Source|Forth Source|Type|Primary Destination|Secondary Destination|Third Destination|Forth Destination|
|--------------|----------------|------------|------------|----|-------------------|---------------------|-----------------|-----------------|
|SourceProcessName|FileHash|||Type|ChildProcess|ChildHash|||
|SourceHostName||||Linked|SourceAddress||||
|SourceProcessName||||Linked|FileHash||||
|ChildProcess||||Linked|ChildHash||||
|SourceUserName||||Linked|SourceHostName|SourceAddress|||
|SourceHostName|SourceAddress|SourceUserName||Linked|SourceProcessName|FileHash|||
