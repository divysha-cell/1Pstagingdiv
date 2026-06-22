# playbook with block and widget




**Enabled:** True

**Version:** 1

**Type:** Playbook

**Priority:** 2

**Playbook Simulator:** False



### Playbook Trigger
**Trigger Type:** All

**Conditions Operator:** And

##### Conditions
|Key|Operator|Value|
|---|--------|-----|
||Equals||



### Involved Steps (Unordered)
|Step Name|Description|Integration|Original Action|
|---------|-----------|-----------|---------------|
|SiemplifyUtilities_Ping_1|Test Connectivity|SiemplifyUtilities|Ping|
|Siemplify_Case Tag_1|Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|

### Involved Blocks
|Name|Description|
|----|-----------|
|Crowdstrike Falcon Containment|This block performs containment on endpoints by targeting case-related IPs and hostnames to prevent further compromise. A boolean input controls manual or automatic execution. In automatic mode, the Upload IOCs and Isolate Endpoint flags determine which actions run. It returns true if successful, false on failure, or empty if no action is taken.|
|New Block|An embedded workflow that can receive inputs and return an output.|
