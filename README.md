# Departmental VLAN Network

_Level: foundation — Enterprise Campus & LAN — VLANs · 802.1Q Trunking · Access Ports · Broadcast Domains_

**Status: Verified.** Completed on 2026-11-20; every requirement was machine-checked against the network built in BuildTheNet and passed.

Snapshot taken 2026-11-20. Built in a simulation — no physical or production equipment was involved.

## Scenario

Pemberton Logistics shares one wiring closet between Sales, Engineering and HR, and HR has asked why payroll broadcasts reach every desk. Split the two floor switches into three named VLANs, put each department's ports in its own, and carry all three between the switches.

### Why it matters

VLANs are where most CCNA candidates first lose track of what is a trunk and what is an access port. Doing it to keep payroll traffic away from the sales floor makes the distinction permanent.

## Requirements

| # | Requirement | Status | Checked by |
|---|---|---|---|
| 1 | Create three VLANs with meaningful names for three departments. | Passed | Sandbox check |
| 2 | Assign access ports to the right VLAN on both switches. | Passed | Sandbox check |
| 3 | Trunk the inter-switch link and carry all three VLANs. | Passed | Sandbox check |
| 4 | Set a non-default native VLAN on the trunk. | Passed | Sandbox check |

## Topology

![Topology diagram](topology.svg)

## Device configurations

Running-configs as `show running-config` prints them in the BuildTheNet sandbox. Passwords, secrets, keys and SNMP communities are replaced with `<removed>`.

- [S1](configs/S1.txt)
- [S2](configs/S2.txt)

---

Built on [BuildTheNet](https://www.buildthenet.io/projects/proj-pt-03-departmental-vlan)
