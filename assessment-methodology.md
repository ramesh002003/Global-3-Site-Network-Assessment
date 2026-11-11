# Assessment Methodology

## Assessment principles

- **Evidence-based:** Every finding should reference a command output, approved screenshot, monitoring report, physical observation, or client-confirmed record.
- **Non-disruptive:** Discovery should be read-only unless a separate change approval exists.
- **Site-by-site:** Assess HQ, Branch 1, and Branch 2 independently before comparing them.
- **Traceable:** Record date, time zone, assessor, device, command/test, result, and evidence reference.
- **Clear status:** Use Verified, Partially Verified, Not Verified, Not Applicable, or Client Confirmation Required.

## Assessment domains

### 1. Device inventory
Record hostname, site, role, vendor, model, serial number, software version, management IP, uptime, support status, and owner.

### 2. Physical infrastructure
Inspect rack condition, power/UPS, cooling, cable management, labeling, fiber/copper paths, optics, and critical uplinks. Record only what can be physically verified.

### 3. Layer 2
Review VLAN purpose and assignment, trunk allowed VLANs, native VLAN, STP mode/root, topology changes, EtherChannel state, port errors, PoE budget, unused ports, and port-security controls.

### 4. Layer 3
Review interface addressing, subnet allocation, default gateways, routing table, static routes, OSPF/BGP neighbors where used, route redistribution, HSRP/VRRP, DHCP relay, DNS reachability, and duplicate-address indicators.

### 5. WAN and inter-site connectivity
Document provider, circuit ID (use a sanitized identifier in public material), access type, committed bandwidth, handoff, public/private addressing, primary/backup path, VPN/MPLS/SD-WAN design, SLA, latency, loss, jitter, and approved failover evidence.

### 6. Security
Review firewall model/software, HA state, interfaces/zones, policy governance, NAT, VPN status, IPS/security profiles, identity integration, administrative access, MFA, logging, backup, and vendor lifecycle.

### 7. Wireless
Review controller/platform, AP inventory, firmware, SSIDs, authentication, VLAN mapping, guest isolation, channel utilization, interference, RSSI, roaming, client load, and rogue AP controls.

### 8. Monitoring and operations
Review SNMP, Syslog, NTP, alerting, configuration backups, access control, incident history, capacity trends, and escalation/ownership processes.

## Evidence record format

For each test or observation capture:

- Evidence ID
- Site and device
- Date/time and time zone
- Assessment area
- Command or test method
- Expected result / reference
- Actual result
- Status
- Evidence file reference
- Assessor notes

Do not place credentials or secret configuration values in evidence files.
