# Global 3-Site Enterprise Network Infrastructure Assessment & Audit

> **Project type:** Enterprise Network Assessment / Technical Documentation  
> **Scope:** Headquarters (HQ) + Branch Office 1 + Branch Office 2  
> **Focus:** Existing network discovery, active infrastructure assessment, WAN connectivity, routing and switching, firewall security, wireless, performance, risk analysis, and improvement recommendations.

## 1. Project Overview

This project provides a repeatable framework for assessing an existing enterprise network across three geographically distributed sites. It is designed to help network engineers document the deployed environment, validate connectivity and resilience, identify technical gaps, and present evidence-based recommendations to stakeholders.

The framework covers both physical and logical network assessment. It does **not** assume a specific vendor or WAN technology. The actual environment may use MPLS, Cisco SD-WAN, IPsec VPN, dedicated Internet circuits, or a hybrid design.

## 2. Project Objectives

- Discover and document active network devices at all three sites.
- Record physical connectivity, uplinks, racks, power, and cabling observations.
- Assess Layer 2 switching and Layer 3 routing.
- Validate inter-site, Internet, and critical application connectivity.
- Review WAN capacity, latency, packet loss, jitter, and failover design.
- Assess firewall configuration, VPNs, high availability, and administrative controls.
- Review wireless infrastructure, coverage, authentication, and segmentation.
- Examine monitoring, logs, configuration backups, and device health.
- Maintain an evidence-based findings and risk register.
- Produce an existing-state topology and a separately labelled proposed architecture.

## 3. Scope

| Site | Role | Assessment focus |
|---|---|---|
| Site 1 | Headquarters (HQ) | Core/distribution, firewall, WAN edge, services, Internet |
| Site 2 | Branch Office 1 | Branch routing, switching, firewall, wireless, WAN |
| Site 3 | Branch Office 2 | Branch routing, switching, firewall, wireless, WAN |

### Assessment domains

1. Network device inventory
2. Physical infrastructure and connectivity
3. Layer 2 switching
4. Layer 3 routing and IP addressing
5. WAN, ISP, VPN, and inter-site connectivity
6. Firewall and network security
7. Wireless LAN
8. Performance, capacity, and availability
9. Monitoring, logging, and configuration management
10. Risks, gaps, and recommendations

## 4. Repository Structure

```text
global-3-site-network-assessment/
├── README.md
├── LICENSE
├── .gitignore
├── docs/
│   ├── assessment-methodology.md
│   ├── survey-workflow.md
│   ├── client-report-outline.md
│   └── risk-rating-guide.md
├── diagrams/
│   ├── existing-network-topology.mmd
│   └── proposed-network-topology-example.mmd
├── templates/
│   ├── device-inventory.csv
│   ├── site-assessment-matrix.csv
│   ├── findings-risk-register.csv
│   ├── wan-circuit-assessment.csv
│   └── survey-checklist.csv
└── references/
    └── read-only-command-reference.md
```

## 5. Assessment Methodology

### Phase 1 — Pre-assessment

- Obtain written authorization and scope approval.
- Confirm site contacts, access windows, and change restrictions.
- Request existing diagrams, IP plans, device inventories, ISP details, and monitoring reports.
- Confirm permitted read-only access and evidence-handling requirements.

### Phase 2 — Physical discovery

- Inspect MDF/IDF rooms, racks, power, UPS, cooling, and access controls.
- Record device make, model, serial number, software version, and management address.
- Trace critical uplinks and document fiber/copper media, optics, and port mapping.
- Capture approved photographs and note missing labels or diagrams.

### Phase 3 — Logical assessment

- Review VLANs, trunks, STP, EtherChannel, port security, and interface health.
- Review IP addressing, gateways, routing tables, OSPF/BGP where deployed, and first-hop redundancy.
- Review firewall zones, policies, NAT, VPNs, HA, authentication, and logging.
- Review wireless SSIDs, VLAN mapping, authentication, AP status, and coverage.

### Phase 4 — Connectivity and performance

- Test approved paths between HQ, Branch 1, and Branch 2.
- Test Internet and critical application reachability.
- Record latency, packet loss, jitter where relevant, interface errors, and utilization.
- Review historical performance and availability data where available.
- Test failover only with explicit approval and an agreed maintenance window.

### Phase 5 — Analysis and reporting

- Validate each observation against collected evidence.
- Assign risk and business impact.
- Recommend corrective actions with priority, owner, and target timeframe.
- Separate verified facts, client-provided information, assumptions, and unverified items.
- Deliver the existing-state diagram, assessment report, registers, and executive presentation.

## 6. Deliverables

| Deliverable | Output |
|---|---|
| Executive summary | Overall condition, major risks, key recommendations |
| Existing topology | Verified HQ and branch connectivity |
| Device inventory | Hardware, software, IP, role, status |
| Physical assessment | Rack, cabling, uplinks, power observations |
| Logical assessment | VLANs, routing, gateways, segmentation |
| WAN assessment | ISP, circuit, bandwidth, latency, resilience |
| Security assessment | Firewall, VPN, HA, access control, logging |
| Performance assessment | Utilization, errors, loss, latency, capacity |
| Findings register | Evidence, impact, severity, recommendation |
| Improvement roadmap | Prioritized corrective actions |

## 7. Risk Rating

Use the rating guide in [`docs/risk-rating-guide.md`](docs/risk-rating-guide.md). A finding must include evidence and business impact. Do not label an item as a confirmed vulnerability or outage unless it has been verified.

## 8. Tools and Technologies

- **Device access:** SSH, PuTTY, MobaXterm
- **Network analysis:** Wireshark, ping, traceroute, MTR
- **Discovery:** Approved IP scanning and network management tools
- **Monitoring:** SolarWinds, PRTG, ManageEngine, vendor platforms
- **Wireless:** Ekahau or approved Wi-Fi survey tools
- **Documentation:** Microsoft Excel, Word, PowerPoint, Visio, draw.io
- **Diagrams:** Mermaid

Actual tool selection depends on client authorization, installed platforms, and available access.

## 9. Safety, Authorization, and Data Handling

- Obtain written authorization before connecting to or testing production systems.
- Prefer read-only commands for discovery.
- Do not run configuration changes, scans, packet captures, or failover tests outside the approved scope.
- Do not store passwords, private keys, VPN pre-shared keys, SNMP communities, or sensitive personal data in this repository.
- Sanitize public examples: replace real IPs, hostnames, circuit IDs, serial numbers, customer names, and diagrams with fictional values.
- Store client evidence in an approved, access-controlled location—not in a public GitHub repository.
- Follow the client's retention, confidentiality, and data-classification policies.

## 10. How to Use This Repository

1. Review the methodology and obtain authorization.
2. Make a working copy of the CSV templates.
3. Complete a separate inventory and assessment for each site.
4. Record evidence references without embedding secrets.
5. Update the topology only after validating the links.
6. Populate the findings register with verified observations.
7. Prepare the client report using the outline in `docs/client-report-outline.md`.

## 11. Project Status

This repository is a reusable assessment framework and sample documentation structure. It does not contain a real client's network data or claim that any assessment has been completed.

## 12. Author

**Network Infrastructure & Cybersecurity Assessment Portfolio Project**

Add your professional profile and contact details here before publishing, if desired.
