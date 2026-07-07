
# InfobloxNIOS

This integration enables Google SecOps to retrieve IP metadata from Infoblox Grid Manager and manage DNS Firewall protections through RPZs. It allows security teams to define RPZ rules that block DNS resolution for malicious or unauthorized domains, or redirect users to a walled garden by modifying DNS responses. In case of any queries, please reach out to support@infoblox.com.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|The base URL of the API, used as the entry point for all API requests.|True|String|https://{address}:{port}|
|Username|The Infoblox account name used to authenticate API access.|True|String||
|Password|The corresponding password for the provided Infoblox username.|True|Password|*****|
|Verify SSL|Verify SSL|False|Boolean|true|


#### Dependencies
| |
|-|
|google_api_python_client-2.186.0-py3-none-any.whl|
|typing_extensions-4.15.0-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|google_auth_httplib2-0.2.1-py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|googleapis_common_protos-1.71.0-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|proto_plus-1.26.1-py3-none-any.whl|
|pyparsing-3.2.5-py3-none-any.whl|
|urllib3-2.5.0-py3-none-any.whl|
|httplib2-0.31.0-py3-none-any.whl|
|google_api_core-2.28.1-py3-none-any.whl|
|certifi-2025.10.5-py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|cachetools-6.2.1-py3-none-any.whl|
|protobuf-6.33.0-py3-none-any.whl|
|TIPCommon-2.2.11-py2.py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|google_auth-2.42.1-py2.py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|charset_normalizer-3.4.4-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|idna-3.11-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|anyio-4.11.0-py3-none-any.whl|


## Actions
#### DHCP Lease Lookup
Retrieves DHCP lease details for a MAC or IP address.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|IP Address|Lease IP address (IPv4 or IPv6).|False|String||
|Hardware|MAC address for IPv4 leases. Regex or exact search supported.|False|String||
|Hostname|Hostname sent via DHCP option 12. Regex/exact search.|False|String|None|
|IPv6 DUID|IPv6 DUID identifier for IPv6 leases. Regex/exact search.|False|String|None|
|Protocol|One of: BOTH, IPV4, IPV6; exact match only.|False|List|Both|
|Fingerprint|DHCP client fingerprint; case‑insensitive or regex search.|False|String|None|
|Username|User associated with lease request; case-insensitive/regex search.|False|String|None|
|Limit|Maximum numbers of objects to be returned.|False|String|100|



##### JSON Results
```json
[{"_ref": "lease/ZG5zLmxlYXNlJDAvMTAuNTAuMTUuMTA1LzAv:10.50.15.105/default", "address": "10.50.15.105", "binding_state": "ACTIVE", "client_hostname": "win10-50-3-19", "cltt": 1754034987, "ends": 1754078187, "fingerprint": "Microsoft Windows 10", "hardware": "00:50:56:81:bc:0e", "ipv6_prefix_bits": 0, "is_invalid_mac": false, "network": "10.50.0.0/20", "network_view": "default", "never_ends": false, "never_starts": false, "next_binding_state": "FREE", "protocol": "IPV4", "served_by": "10.50.3.71", "server_host_name": "infoblox.localdomain", "starts": 1754034987, "uid": "\"\\001\\000PV\\201\\274\\016\"", "variable": "vendor-class-identifier=\"MSFT 5.0\""}]
```



#### Create RPZ NAPTR Rule
Adds a NAPTR override in RPZ to control DNS-based service discovery. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Specify the name of the rule.|True|String||
|RP Zone|The zone to assign the rule to.|True|String||
|Order|Order parameter in NAPTR record defines the sequence of rule application when multiple rules exist.|True|String||
|Preference|The preference of the Substitute (NAPTR Record) Rule record.|True|String||
|Replacement|Substitute rule object `replacement` field of the NAPTR record. For non-terminal NAPTR records, this field specifies the next domain name to look up. |True|String||
|Comment|Comment for this rule.|False|String||
|Additional Parameters|JSON object containing additional parameters to create response policy zone. |False|String|None|



##### JSON Results
```json
{"_ref": "record:rpz:naptr/ZG5zLmJpbmRfbmFwdHIkLl9kZWZhdWx0LmNvbS5ycHoudGhyZWF0LG5pZ2h0bHkyLXRlc3Qtc3J2LXN1YiwxLDIsLCwsdGhyZWF0LnJwei5jb20:nightly2-test-srv-sub.threat.rpz.com/default", "comment": "threat.rpz.com", "disable": false, "extattrs": {}, "flags": "", "name": "nightly1-test-srv-sub.threat.rpz.com", "order": 1, "preference": 2, "regexp": "", "replacement": "threat.rpz.com", "rp_zone": "threat.rpz.com", "services": "", "use_ttl": false, "view": "default", "zone": "threat.rpz.com"}
```



#### List Network Info
Lists defined IPv4/IPv6 networks and subnets in IPAM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Network|The network address in CIDR notation (e.g., "192.168.1.0/24") .|False|String||
|Limit|Maximum numbers of objects to be returned.|False|String|100|
|Extended Attributes|The comma-separated key/value formatted filter for extended attributes, e.g. "Site=New York,OtherProp=MyValue". |False|String|None|



##### JSON Results
```json
[{"_ref": "network/ZG5zLm5ldHdvcmskMTAuNTAuMC4wLzIwLzA:10.50.0.0/20/default", "authority": false, "conflict_count": 1, "ddns_generate_hostname": false, "ddns_server_always_updates": true, "ddns_ttl": 0, "ddns_update_fixed_addresses": false, "ddns_use_option81": false, "deny_bootp": false, "dhcp_utilization": 818, "dhcp_utilization_status": "NORMAL", "disable": false, "discover_now_status": "NONE", "discovered_bgp_as": null, "discovered_bridge_domain": null, "discovered_tenant": null, "discovered_vlan_id": null, "discovered_vlan_name": null, "discovered_vrf_description": null, "discovered_vrf_name": null, "discovered_vrf_rd": null, "discovery_basic_poll_settings": {"auto_arp_refresh_before_switch_port_polling": true, "cli_collection": true, "complete_ping_sweep": false, "device_profile": false, "netbios_scanning": false, "port_scanning": false, "smart_subnet_ping_sweep": false, "snmp_collection": true, "switch_port_data_collection_polling": "PERIODIC", "switch_port_data_collection_polling_interval": 3600}, "discovery_blackout_setting": {"enable_blackout": false}, "discovery_engine_type": "NONE", "dynamic_hosts": 9, "email_list": [], "enable_ddns": false, "enable_dhcp_thresholds": false, "enable_discovery": false, "enable_email_warnings": false, "enable_ifmap_publishing": false, "enable_pxe_lease_time": false, "enable_snmp_warnings": false, "extattrs": {}, "high_water_mark": 95, "high_water_mark_reset": 85, "ignore_dhcp_option_list_request": false, "ignore_id": "NONE", "ignore_mac_addresses": [], "ipam_email_addresses": [], "ipam_threshold_settings": {"reset_value": 85, "trigger_value": 95}, "ipam_trap_settings": {"enable_email_warnings": false, "enable_snmp_warnings": true}, "ipv4addr": "10.50.0.0", "lease_scavenge_time": -1, "logic_filter_rules": [], "low_water_mark": 0, "low_water_mark_reset": 10, "members": [{"_struct": "dhcpmember", "ipv4addr": "10.50.3.71", "ipv6addr": null, "name": "infoblox.localdomain"}], "mgm_private": false, "mgm_private_overridable": true, "netmask": 20, "network": "10.50.0.0/20", "network_container": "/", "network_view": "default", "options": [{"name": "dhcp-lease-time", "num": 51, "use_option": false, "value": "43200", "vendor_class": "DHCP"}], "port_control_blackout_setting": {"enable_blackout": false}, "recycle_leases": true, "rir": "NONE", "rir_registration_status": "NOT_REGISTERED", "same_port_control_discovery_blackout": false, "static_hosts": 0, "subscribe_settings": null, "total_hosts": 11, "unmanaged": false, "unmanaged_count": 1148, "update_dns_on_lease_renewal": false, "use_authority": false, "use_blackout_setting": false, "use_bootfile": false, "use_bootserver": false, "use_ddns_domainname": false, "use_ddns_generate_hostname": false, "use_ddns_ttl": false, "use_ddns_update_fixed_addresses": false, "use_ddns_use_option81": false, "use_deny_bootp": false, "use_discovery_basic_polling_settings": false, "use_email_list": false, "use_enable_ddns": false, "use_enable_dhcp_thresholds": false, "use_enable_discovery": false, "use_enable_ifmap_publishing": false, "use_ignore_dhcp_option_list_request": false, "use_ignore_id": false, "use_ipam_email_addresses": false, "use_ipam_threshold_settings": false, "use_ipam_trap_settings": false, "use_lease_scavenge_time": false, "use_logic_filter_rules": false, "use_mgm_private": false, "use_nextserver": false, "use_options": false, "use_pxe_lease_time": false, "use_recycle_leases": false, "use_subscribe_settings": false, "use_update_dns_on_lease_renewal": false, "use_zone_associations": true, "utilization": 283, "utilization_update": 1754052846, "zone_associations": []}]
```



#### Create RPZ TXT Rule
Adds a TXT record rule in RPZ to associate text data with a DNS response. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|RP Zone|The zone to assign the rule to. |True|String||
|Name|Specify the name of the rule.|True|String||
|Text|Text associated with the record. |True|String||
|Comment|Comment for this rule. |False|String|None|
|Additional Parameters|JSON object containing additional parameters to create response policy zone. |False|String|None|



##### JSON Results
```json
{"_ref": "record:rpz:txt/ZG5zLmJpbmRfdHh0JC5fZGVmYXVsdC5jb20ucnB6LnRocmVhdC5uaWdodGx5LXRlc3QtbXgtc3ViLiJ0ZXN0MSI:nightly-test-mx-sub.threat.rpz.com/default", "comment": "nightly-test-mx-sub", "disable": false, "extattrs": {}, "name": "nightly-test-mx-sub.threat.rpz.com", "rp_zone": "threat.rpz.com", "text": "Threat Zone", "use_ttl": false, "view": "default", "zone": "threat.rpz.com"}
```



#### Create RPZ SRV Rule
Adds an SRV record override in RPZ for service-based DNS lookups.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Specify the name of the rule.|True|String||
|Priority|The priority of the Substitute (SRV Record) Rule.|True|String||
|RP Zone|The name of a response policy zone in which the record resides. |True|String||
|Port|The port of the Substitute (SRV Record) Rule.|True|String||
|Target|Text associated with the record.|True|String||
|Weight|The weight of the Substitute (SRV Record) Rule.|True|String||
|Comment|Comment for this rule.|False|String||
|Additional Parameters|JSON object containing additional parameters to create response policy zone.|False|String||



##### JSON Results
```json
{"_ref": "record:rpz:srv/ZG5zLmJpbmRfc3J2JC5fZGVmYXVsdC5jb20ucnB6LnRocmVhdC9uaWdodGx5My10ZXN0LXNydi1zdWIvMTAvMTAvMjIvdGhyZWF0LnJwei5jb20:nightly3-test-srv-sub.threat.rpz.com/default", "comment": "nightly-test-srv-sub", "disable": false, "extattrs": {}, "name": "nightly3-test-srv-sub.threat.rpz.com", "port": 22, "priority": 10, "rp_zone": "threat.rpz.com", "target": "threat.rpz.com", "use_ttl": false, "view": "default", "weight": 10, "zone": "threat.rpz.com"}
```



#### Create Response Policy Zone
Creates a new Response Policy Zone (RPZ) to define custom DNS responses.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|FQDN|The name of this DNS zone is in FQDN format.|True|String||
|Substitute Name|The alternative name of the redirect target is a substitute response policy zone.|False|String|None|
|Comment|Comment for the zone.|False|String|None|
|RPZ Policy|The override policy of the response policy zone. |False|List|GIVEN|
|RPZ Severity|The severity of the response policy zone.|False|List|MAJOR|
|RPZ Type|The type of the Response Policy Zone.|False|List|LOCAL|
|Fireeye Rule Mapping|Rules to map fireeye alerts.|False|String|None|
|Additional Parameters|JSON object containing additional parameters to create response policy zone.|False|String|None|



##### JSON Results
```json
{"_ref": "zone_rp/ZG5zLnpvbmUkLl9kZWZhdWx0LmlwMTI5LnRocmVhdC5kbnM:dns.threat.ip129/default", "comment": "Malicious domain blocking zone", "disable": false, "display_domain": "dns.threat.ip", "extattrs": {}, "external_primaries": [], "external_secondaries": [], "fireeye_rule_mapping": null, "fqdn": "dns.threat.ip129", "grid_primary": [], "grid_secondaries": [], "locked": false, "log_rpz": true, "member_soa_mnames": [], "member_soa_serials": [], "network_view": "default", "parent": "", "primary_type": "None", "rpz_drop_ip_rule_enabled": false, "rpz_drop_ip_rule_min_prefix_length_ipv4": 29, "rpz_drop_ip_rule_min_prefix_length_ipv6": 112, "rpz_policy": "SUBSTITUTE", "rpz_priority": 1005, "rpz_priority_end": 999, "rpz_severity": "MAJOR", "rpz_type": "LOCAL", "substitute_name": "dns.threat.ip", "use_external_primary": false, "use_log_rpz": false, "use_record_name_policy": false, "use_rpz_drop_ip_rule": false, "view": "default"}
```



#### Create Host Record
Adds a host record to Infoblox with associated IP addresses. When configure_for_dns is enabled, it also creates corresponding A/AAAA and PTR DNS records. Useful for IPAM and DNS inventory management.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|The name of the host in FQDN format `{name}.{auth_zone}` (e.g. server1.auth.threat.zone). It must belong to an existing DNS zone.|True|String||
|IPv4 Addresses|Array of IPv4 address objects in the following format. (e.g. [{"ipv4addr":"192.168.1.100","mac":"00:11:22:33:44:55","configure_for_dhcp":true},...] ).|False|String|None|
|IPv6 Addresses|Array of IPv6 address objects in the following format. (e.g. [{"ipv6addr":"2001:db8::1"},{"ipv6addr":"2001:db8::2", etc.}])|False|String|None|
|View|The DNS view in which the record resides (e.g., "default").|False|String|default|
|Comment|Additional information or notes about this host record.|False|String|None|
|Aliases|Comma-separated list of DNS aliases (CNAMEs) for this host (e.g., "alias1.auth zone,alias2.auth zone").|False|String|None|
|Configure for DNS|When false, the host record doesn't have associated DNS records.|False|Boolean|true|
|Extended Attributes|Comma-separated key/value formatted filter for extended attributes, e.g. "Site=New York,OtherProp=MyValue"|False|String|None|
|Additional Parameters|Comma-separated key/value formatted string for additional parameters supported by the API (e.g., "use_ttl=true,network_view=default").|False|String|None|



##### JSON Results
```json
{"_ref": "record:host/ZG5zLmhvc3QkLl9kZWZhdWx0LmF1dGggem9uZS5uaW9zLWhvc3QtYWRtaW4:nios-host-admin.auth%20zone/default", "aliases": ["admin-1.auth zone", "ownder-1.auth zone"], "allow_telnet": false, "configure_for_dns": true, "creation_time": 1754300315, "ddns_protected": false, "disable": false, "disable_discovery": false, "dns_aliases": ["admin-1.auth zone", "ownder-1.auth zone"], "dns_name": "nios-host-admin.auth zone", "extattrs": {"IB Discovery Owned": {"value": "admin"}, "Site": {"value": "site-1"}}, "ipv4addrs": [{"_ref": "record:host_ipv4addr/ZG5zLmhvc3RfYWRkcmVzcyQuX2RlZmF1bHQuYXV0aCB6b25lLm5pb3MtaG9zdC1hZG1pbi4xOTIuMTY4LjIwLjIwLg:192.168.20.20/nios-host-admin.auth%20zone/default", "configure_for_dhcp": true, "host": "nios-host-admin.auth zone", "ipv4addr": "192.168.20.20", "mac": "00:1a:2b:9c:7d:5e"}], "ipv6addrs": [{"_ref": "record:host_ipv6addr/ZG5zLmhvc3RfYWRkcmVzcyQuX2RlZmF1bHQuYXV0aCB6b25lLm5pb3MtaG9zdC1hZG1pbi4yMDAxOmRiODo4NWEzOjo4YTJlOjM3MDo3NjUu:2001%3Adb8%3A85a3%3A%3A8a2e%3A370%3A765/nios-host-admin.auth%20zone/default", "configure_for_dhcp": false, "host": "nios-host-admin.auth zone", "ipv6addr": "2001:db8:85a3::8a2e:370:765"}], "name": "nios-host-admin.auth zone", "network_view": "default", "rrset_order": "cyclic", "use_cli_credentials": false, "use_dns_ea_inheritance": false, "use_snmp3_credential": false, "use_snmp_credential": false, "use_ttl": false, "view": "default", "zone": "auth zone"}
```



#### Create RPZ CNAME Rule
Adds a CNAME rule to an existing RPZ to override DNS behavior. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Substitute Name|The substitute name to assign (substitute domain only). |False|String|None|
|Rule Type|The type of the rule to create.|True|List|Block (No data)|
|Object Type|The type of the object for which to assign the rule.|True|List|Domain Name|
|Name|The rule name in a FQDN format.|True|String||
|RP Zone|The zone to assign the rule to.|True|String||
|Comment|Comment for this rule.|False|String|None|
|View|The DNS view in which the records are located. By default, the 'default' DNS view is searched.|False|String|default|
|Additional Parameters|JSON object containing additional parameters to create rpz rule.|False|String|None|



##### JSON Results
```json
[{"_ref": "record:rpz:cname:ipaddress/ZG5zLmJpbmRfY25hbWUkLl9kZWZhdWx0LmNvbS5ycHoudGhyZWF0LnJwei1pcC4xMC4yLjIuMTEuMzI:10.2.2.11.threat.rpz.com/default", "canonical": "*", "comment": "Block test1", "disable": false, "extattrs": {}, "name": "10.2.2.11.threat.rpz.com", "rp_zone": "threat.rpz.com", "use_ttl": false, "view": "default", "zone": "threat.rpz.com"}, {"_ref": "record:rpz:cname:clientipaddress/ZG5zLmJpbmRfY25hbWUkLl9kZWZhdWx0LmNvbS5ycHoudGhyZWF0LnJwei1jbGllbnQtaXAuMTAuMi4yLjE5LjMy:10.2.2.19.threat.rpz.com/default", "canonical": "*", "comment": "Block test1", "disable": false, "extattrs": {}, "is_ipv4": true, "name": "10.2.2.19.threat.rpz.com", "rp_zone": "threat.rpz.com", "use_ttl": false, "view": "default", "zone": "threat.rpz.com"}]
```



#### Create RPZ AAAA Rule
Creates an RPZ Substitute rule which maps domain name (AAAA record) or an IPv6 address to a substitute IPv6 address for DNS redirection or blocking. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Object Type|The type of the object for which to create record.|True|List|Domain Name|
|Name|Specify the name of the rule.|True|String||
|RP Zone|The zone to assign the rule to.|True|String||
|IPv6 Address|The IPv6 address of the substitute rule.|True|String||
|Comment|Comment for this rule.|False|String|None|
|Additional Parameters|JSON object containing additional parameters to create response policy zone.|False|String|None|



##### JSON Results
```json
{"_ref": "record:rpz:aaaa:ipaddress/ZG5zLmJpbmRfYWFhYSQuX2RlZmF1bHQuY29tLnJwei50aHJlYXQscnB6LWlwLmQ2MC5lMzIuZjFiOS56ei4yLjEyOCwyMDAxOmRiODo4NWEzOjo4YTJlOjM3MDo3MzM0:d60%3Ae32%3Af1b9%3A%3A2.threat.rpz.com/default", "comment": "nightly-test-a-sub", "disable": false, "extattrs": {}, "ipv6addr": "2001:db8:85a3::8a2e:370:7334", "name": "d60:e32:f1b9::2.threat.rpz.com", "rp_zone": "threat.rpz.com", "use_ttl": false, "view": "default", "zone": "threat.rpz.com"}
```



#### IP Lookup
Returns IPAM info for a given IP. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Limit|Maximum numbers of objects to be returned.|False|String|100|
|IP Address|The IP address for which to retrieve information, e.g. "192.168.1.1". Cannot be used in conjunction with network or from/to_ip arguments.|False|String|None|
|Network|The network that the IP belongs to is in FQDN/CIDR format, e.g. "192.168.1.0/24". Cannot be used in conjunction with ip or from/to_ip arguments.|False|String|None|
|From IP|The beginning of the IP range, e.g. "192.168.1.0". Must be used in conjunction with to_ip.|False|String|None|
|To IP|The end of the IP range, e.g. "192.168.1.254". Must be used in conjunction with from_ip.|False|String|None|
|Status|The status of the IP device. Used in conjunction with the network or ip argument. Possible values are All, Active, Used and Unused.|False|List|All|
|Extended Attributes|Comma-separated key/value formatted filter for extended attributes, e.g. "Site=New York,OtherProp=MyValue".|False|String|None|



##### JSON Results
```json
[{"_ref": "ipv4address/Li5pcHY0X2FkZHJlc3MkMTkyLjE2OC4xLjAvMA:192.168.1.0", "comment": "", "conflict_types": ["NONE"], "discover_now_status": "NONE", "extattrs": {}, "ip_address": "192.168.1.0", "is_conflict": false, "is_invalid_mac": false, "mac_address": "", "names": [], "network": "192.168.1.0/24", "network_view": "default", "objects": [], "status": "USED", "types": ["NETWORK"], "usage": []}, {"_ref": "ipv6address/Li5pcHY2X2FkZHJlc3MkMjAwMTpkYjg6MTIzNDo6MS8w:2001%3Adb8%3A1234%3A%3A1", "comment": "HOST Wizard", "conflict_types": ["NONE"], "discover_now_status": "NONE", "duid": "", "extattrs": {"IB Discovery Owned": {"value": "host-wiz"}, "Site": {"value": "host-site"}}, "ip_address": "2001:db8:1234::1", "is_conflict": false, "lease_state": "FREE", "names": ["auth zone"], "network": "2001:db8:1234::/64", "network_view": "default", "objects": ["record:host/ZG5zLmhvc3QkLl9kZWZhdWx0LmF1dGggem9uZS4:auth%20zone/default"], "status": "USED", "types": ["HOST", "RESERVED_RANGE"], "usage": ["DNS"]}]
```



#### List Host Info
Retrieves host records from Infoblox including hostname, associated IPv4/IPv6 addresses (A/AAAA records), PTR records, DNS view information, and any configured extensible attributes.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|IPv4 Address|IPv4 address information.|False|String|None|
|Name|The hostname for the record. |False|String||
|IPv6 Address|IPv6 address information. |False|String|None|
|Extended Attributes|Comma-separated key/value formatted filter for extended attributes, e.g. "Site=New York,OtherProp=MyValue".|False|String|None|
|Limit|Maximum numbers of objects to be returned.|False|String|100|



##### JSON Results
```json
[{"_ref": "record:host/ZG5zLmhvc3QkLl9kZWZhdWx0LmF1dGggem9uZS4:auth%20zone/default", "allow_telnet": false, "comment": "HOST Wizard", "configure_for_dns": true, "creation_time": 1753968112, "ddns_protected": true, "disable": false, "disable_discovery": false, "dns_name": "auth zone", "extattrs": {"IB Discovery Owned": {"value": "host-wiz"}, "Site": {"value": "host-site"}}, "ipv4addrs": [{"_ref": "record:host_ipv4addr/ZG5zLmhvc3RfYWRkcmVzcyQuX2RlZmF1bHQuYXV0aCB6b25lLi4xOTIuMTY4LjEuMi4:192.168.1.2/auth%20zone/default", "configure_for_dhcp": false, "host": "auth zone", "ipv4addr": "192.168.1.2"}, {"_ref": "record:host_ipv4addr/ZG5zLmhvc3RfYWRkcmVzcyQuX2RlZmF1bHQuYXV0aCB6b25lLi4xOTIuMTY4LjEuMy4:192.168.1.3/auth%20zone/default", "configure_for_dhcp": false, "host": "auth zone", "ipv4addr": "192.168.1.3"}], "ipv6addrs": [{"_ref": "record:host_ipv6addr/ZG5zLmhvc3RfYWRkcmVzcyQuX2RlZmF1bHQuYXV0aCB6b25lLi4yMDAxOmRiODoxMjM0OjoxLg:2001%3Adb8%3A1234%3A%3A1/auth%20zone/default", "configure_for_dhcp": false, "host": "auth zone", "ipv6addr": "2001:db8:1234::1"}, {"_ref": "record:host_ipv6addr/ZG5zLmhvc3RfYWRkcmVzcyQuX2RlZmF1bHQuYXV0aCB6b25lLi4yMDAxOmRiODoxMjM0OjoyLg:2001%3Adb8%3A1234%3A%3A2/auth%20zone/default", "configure_for_dhcp": false, "host": "auth zone", "ipv6addr": "2001:db8:1234::2"}], "name": "auth zone", "network_view": "default", "rrset_order": "cyclic", "use_cli_credentials": false, "use_dns_ea_inheritance": false, "use_snmp3_credential": false, "use_snmp_credential": false, "use_ttl": false, "view": "default", "zone": "auth zone"}]
```



#### Update RPZ CNAME Rule
Updates an existing rule in RPZ CNAME to modify DNS behavior. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|The rule name in a FQDN format.|True|String||
|Comment|Comment for this rule.|False|String|None|
|RP Zone|The zone to assign the rule to.|True|String||
|Reference ID|The reference ID of the existing RPZ rule to update.|True|String||
|Rule Type|The type of the rule to update.|True|List|Block (No such Domain)|
|Substitute Name|The substitute name to assign (substitute domain only). |False|String|None|
|View|The DNS view in which the records are located. By default, the 'default' DNS view is searched.|False|String|default|
|Additional Parameters|JSON object containing additional parameters to create rpz rule.|False|String|None|



##### JSON Results
```json
{"_ref": "record:rpz:cname/ZG5zLmJpbmRfY25hbWUkLl9kZWZhdWx0LmlwLnRocmVhdC5kbnMuMS4xLjEwLjEw:10.10.1.1.dns.threat.ip/default", "canonical": "", "comment": "Block IP", "disable": false, "extattrs": {}, "name": "10.10.1.1.dns.threat.ip", "rp_zone": "dns.threat.ip", "use_ttl": false, "view": "default", "zone": "dns.threat.ip"}
```



#### Search RPZ Rule
Searches for a specific RPZ rule by its name.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Object Type|The Infoblox object type.|True|List|record:rpz:cname|
|Rule Name|The full rule name (usually the rule name followed by its zone.(e.g. name.domain.com).|False|String|None|
|Output Fields|The comma-separated fields to include in the returned object (e.g., address, comment, etc.) .|False|String|None|
|Limit|Maximum number of objects to be returned. |False|String|100|



##### JSON Results
```json
[{"canonical": "1.4.5.infoblow.com", "disable": false, "extattrs": {}, "name": "1.4.5.infoblow.com", "_ref": "record:rpz:cname/ZG5zLmJpbmRfY25hbWUkLl9kZLmNvbS5pbmZvYmxvdy41LjQuNwew3:1.4.5.infoblow.com/default", "use_ttl": false, "view": "default", "zone": "infoblow.com"}]
```



#### Get Response Policy Zone Details
Retrieves configuration details for a specified RPZ.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|FQDN|The name of this DNS zone in FQDN format.|False|String|None|
|View|The name of the DNS view in which the zone resides ( e.g. “external”).|False|String|None|
|Comment|Comment for the zone.|False|String|None|
|Limit|Maximum number of objects to be returned.|False|String|100|



##### JSON Results
```json
[{"_ref": "zone_rp/ZG5zLnpvbmUkLl9kZWZhdWx0LmlwLnRocmVhdC5kbnM:dns.threat.ip/default", "comment": "Malicious domain blocking zone", "disable": false, "display_domain": "dns.threat.ip", "extattrs": {}, "external_primaries": [], "external_secondaries": [], "fireeye_rule_mapping": null, "fqdn": "dns.threat.ip", "grid_primary": [], "grid_secondaries": [], "locked": false, "log_rpz": true, "member_soa_mnames": [], "member_soa_serials": [], "network_view": "default", "parent": "", "primary_type": "None", "rpz_drop_ip_rule_enabled": false, "rpz_drop_ip_rule_min_prefix_length_ipv4": 29, "rpz_drop_ip_rule_min_prefix_length_ipv6": 112, "rpz_policy": "SUBSTITUTE", "rpz_priority": 1001, "rpz_priority_end": 999, "rpz_severity": "CRITICAL", "rpz_type": "LOCAL", "substitute_name": "blocked.example.com", "use_external_primary": false, "use_log_rpz": false, "use_record_name_policy": false, "use_rpz_drop_ip_rule": false, "view": "default"}]
```



#### Delete RPZ Rule
Deletes a rule from a specified RPZ. Supports all RPZ record types by dynamically determining the object type from user input.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Reference ID|The reference ID of the RPZ rule. |True|String||



##### JSON Results
```json
{}
```



#### Create RPZ MX Rule
Adds a mail exchange override rule to an RPZ.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Specify the name of the rule.|True|String||
|RP Zone|The zone to assign the rule to.|True|String||
|Mail Exchanger|Specify the mail exchanger for the rule.|True|String||
|Preference|Preference value for the rule.|True|String|0|
|Comment|Comment for this rule.|False|String|None|
|Additional Parameters|JSON object containing additional parameters to create response policy zone.|False|String|None|



##### JSON Results
```json
{"_ref": "record:rpz:mx/ZG5zLmJpbmRfbXgkLl9kZWZhdWx0LmNvbS5ycHoudGhyZWF0Lm5pZ2h0bHkxLXRlc3QtbXgtc3ViLjAuMC4wLjAuNQ:nightly1-test-mx-sub.threat.rpz.com/default", "comment": "nightly-test-mx-sub", "disable": false, "extattrs": {}, "mail_exchanger": "0.0.0.0", "name": "nightly1-test-mx-sub.threat.rpz.com", "preference": 5, "rp_zone": "threat.rpz.com", "use_ttl": false, "view": "default", "zone": "threat.rpz.com"}
```



#### Create RPZ A Rule
Creates an RPZ Substitute rule which maps domain name (A record) or an IPv4 address to a substitute IPv4 address for DNS redirection or blocking. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Object Type|The type of the object for which to create record.|True|List|Domain Name|
|Name|Specify the name of the rule.|True|String||
|RP Zone|The zone to assign the rule to.|True|String||
|IPv4 Address|The IPv4 address of the substitute rule.|True|String||
|Comment|Comment for this rule.|False|String|None|
|Additional Parameters|JSON object containing additional parameters to create response policy zone.|False|String|None|



##### JSON Results
```json
{"_ref": "record:rpz:a/ZG5zLmJpbmRfYSQuX2RlZmF1bHQuY29tLnJwei50aHJlYXQsMTEuMi4xMi4xMCwwLjAuMC4w:10.12.2.11.threat.rpz.com/default", "comment": "nightly-test-a-sub", "disable": false, "extattrs": {}, "ipv4addr": "0.0.0.0", "name": "10.12.2.11.threat.rpz.com", "rp_zone": "threat.rpz.com", "use_ttl": false, "view": "default", "zone": "threat.rpz.com"}
```



#### Create RPZ PTR Rule
Adds a reverse DNS lookup override in RPZ for an IP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|PTR DName|The domain name of the RPZ substitute rule object of the PTR record.|True|String||
|RP Zone|The zone to assign the rule to.|True|String||
|Name|The name of the RPZ Substitute rule object of the PTR record.|False|String|None|
|Comment|Comment for this rule.|False|String|None|
|IPv4 Address|The IPv4 address of the substitute rule.|False|String|None|
|IPv6 Address|The IPv6 address of the substitute rule.|False|String|None|
|Additional Parameters|JSON object containing additional parameters to create response policy zone.|False|String|None|



##### JSON Results
```json
{"_ref": "record:rpz:ptr/ZG5zLmJpbmRfcHRyJC5fZGVmYXVsdC5jb20ucnB6LnRocmVhdC5hcnBhLmlwNi5mLmQuNi4wLjAuZS4zLjIuZi4xLmIuOS4wLjAuMC4wLjAuMC4wLjAuMC4wLjAuMC4wLjAuMC4wLjAuMC4wLjIuYWJjczEudGhyZWF0LnJwei5jb20:2.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.9.b.1.f.2.3.e.0.0.6.d.f.ip6.arpa.threat.rpz.com/default", "comment": "nightly-test-mx-sub", "disable": false, "extattrs": {}, "ipv4addr": "", "ipv6addr": "fd60:e32:f1b9::2", "name": "2.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.9.b.1.f.2.3.e.0.0.6.d.f.ip6.arpa.threat.rpz.com", "ptrdname": "abcs1.threat.rpz.com", "rp_zone": "threat.rpz.com", "use_ttl": false, "view": "default", "zone": "threat.rpz.com"}
```



#### Ping
Use the Ping action to test the connectivity to API Service.
Timeout - 600 Seconds



#### Delete Response Policy Zone
Removes an existing Response Policy Zone from Infoblox.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Reference ID|The reference ID of the response policy zone.|True|String||



##### JSON Results
```json
{}
```









