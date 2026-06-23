<p align="center">
<img src="./Carbon Black Network Connections Event.png" 
     alt="Carbon Black Network Connections Event" width="200"/></p>
     
# Carbon Black Network Connections Event

### Description
VMware Carbon Black EDR captures network connections with the following characteristics: Both TCP over IPv4 or UDP over IPv4 connections Both inbound and outbound connections Network connections record TCP or UDP protocol, the remote IPv4 address, port and the domain name associated with the remote IPv4 Address Inbound connections capture the local port. If the sensor is installed on a typically configured web server, the reported port is 80. Outbound connections capture the remote port, uutbound connections made after DNS resolution the name that resolves to the captured IPV4 address is also reported. The sensor utilizes a passive sensing approach to capturing the domain name, so no additional network traffic is generated in order to capture the name. For DNS/DHCP servers, high CPU and/or memory can be seen due to the high number of netconn events. Rather than disabling all netconns, disable DNS capture on that machine. CB Response: Windows Sensor Causing High CPU/memory Utilization on Netconn Intense Server.

### Rules
|Primary Source|Secondary Source|Third Source|Forth Source|Type|Primary Destination|Secondary Destination|Third Destination|Forth Destination|
|--------------|----------------|------------|------------|----|-------------------|---------------------|-----------------|-----------------|
|SourceHostName||||Linked|SourceAddress||||
|SourceHostName|SourceAddress|||Linked|ParentProcess|ParentHash|||
|DestinationHostName||||Linked|DestinationAddress||||
|SourceProcessName|FileHash|||Type|DestinationHostName|DestinationAddress|||
|ParentProcess|ParentHash|||Linked|SourceProcessName|FileHash|||
|SourceProcessName||||Linked|FileHash||||
|ParentProcess||||Linked|ParentHash||||
|SourceUserName||||Linked|SourceHostName|SourceAddress|||
