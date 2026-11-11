# Read-Only Network Assessment Command Reference

> Commands are examples for Cisco IOS/IOS-XE. Availability and syntax vary by platform and software release. Use only with client authorization and appropriate privilege. Do not run configuration commands during discovery.

## Device and interface health

```text
show version
show inventory
show clock
show ip interface brief
show interfaces status
show interfaces counters errors
show logging
show processes cpu sorted
show processes memory
show environment all
```

## Layer 2

```text
show vlan brief
show interfaces trunk
show spanning-tree
show spanning-tree root
show etherchannel summary
show mac address-table
show port-security
show power inline
```

## Layer 3

```text
show ip route
show ip protocols
show ip ospf neighbor
show ip bgp summary
show standby brief
show arp
```

## Connectivity tests

```text
ping <approved-destination>
traceroute <approved-destination>
```

## FortiGate examples

```text
get system status
get system ha status
get system performance status
get router info routing-table all
get vpn ipsec tunnel summary
diagnose hardware deviceinfo nic
```

## Assessment notes

- Confirm command support for the exact model and release.
- Capture timestamps and device identity with outputs.
- Avoid collecting secrets from full configurations.
- Redact internal addressing and identifiers before publishing examples.
- Use approved monitoring systems for historical utilization and availability.
- Do not test failover or modify production state without written change approval.
