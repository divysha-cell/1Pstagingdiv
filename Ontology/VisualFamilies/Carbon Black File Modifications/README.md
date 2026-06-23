<p align="center">
<img src="./Carbon Black File Modifications.png" 
     alt="Carbon Black File Modifications" width="200"/></p>
     
# Carbon Black File Modifications

### Description
VMware Carbon Black EDR captures four types of file system activity: File creation – the creation of a new file. File Write – the first time a file is written to after being opened or created. File Write Complete – the closing of a file that was written to.This event includes both the file path and also the MD5/SHA256 of the written file. The event is only captured for binaries (Windows PE files such as EXE, DLL and drivers), Adobe Docs (PDF), OfficeXML docs (docx, doc, xlsx, xls, pptx, ppt)  and zip archives (zip) that are smaller than 10MB in size. Can be enabled or disabled independently of filemod collection by deselecting "Non-binary file writes" Not available on macOS and Linux sensors File deletion – the deletion of an existing file.

### Rules
|Primary Source|Secondary Source|Third Source|Forth Source|Type|Primary Destination|Secondary Destination|Third Destination|Forth Destination|
|--------------|----------------|------------|------------|----|-------------------|---------------------|-----------------|-----------------|
|SourceProcessName||||Type|FileName|FileHash|||
|FileName||||Linked|FileHash||||
|SourceHostName||||Linked|SourceAddress||||
|SourceHostName|SourceAddress|||Linked|SourceProcessName|FileName|FileHash||
