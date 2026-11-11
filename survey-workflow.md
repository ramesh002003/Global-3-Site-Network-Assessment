# Site Survey Workflow

## Before visiting the site

- [ ] Confirm scope, written authorization, contacts, and access window.
- [ ] Confirm permitted devices, protocols, tests, and read-only access.
- [ ] Request existing topology, IP plan, inventory, WAN/ISP details, and monitoring reports.
- [ ] Confirm photography and evidence-storage rules.
- [ ] Prepare sanitized inventory and checklist templates.

## At each site

- [ ] Record site name/code, date, time zone, assessor, and escort.
- [ ] Inspect MDF/IDF, racks, UPS, power, cooling, and physical access.
- [ ] Inventory switches, routers, firewalls, controllers, APs, and ISP CPE.
- [ ] Trace critical links and record source/destination ports and media.
- [ ] Collect approved read-only device information.
- [ ] Review Layer 2 and Layer 3 configuration/state.
- [ ] Review WAN, VPN, and inter-site paths.
- [ ] Review firewall and wireless controls.
- [ ] Review monitoring, logs, backups, and capacity history.
- [ ] Record evidence and unresolved questions.

## After each site

- [ ] Reconcile inventory and topology.
- [ ] Validate observations with the responsible network team.
- [ ] Identify missing evidence and request clarification.
- [ ] Add verified findings to the risk register.
- [ ] Compare the site against the other two sites.
- [ ] Prepare recommendations and implementation dependencies.

## Inter-site test matrix

| Source | Destination | Test | Result / evidence |
|---|---|---|---|
| HQ | Branch 1 | Approved reachability, latency, loss | Record |
| HQ | Branch 2 | Approved reachability, latency, loss | Record |
| Branch 1 | Branch 2 | Approved reachability, latency, loss | Record |
| Each site | Approved Internet target | DNS and reachability | Record |
| Each site | Critical application | Application path/availability | Record |

A failed ping alone does not prove an outage; ICMP may be filtered. Validate with the appropriate approved application or service test.
