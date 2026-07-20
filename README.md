# Enterprise Network Design
### Cisco Packet Tracer — Computer Networks Project

A fully working enterprise network simulation for a 100×50m office building built in Cisco Packet Tracer. The network covers 200+ devices across 8 VLANs with internet access, wireless, security, redundancy and remote work support.

---

## What's in this repo

```
enterprise-network-design/
├── README.md
├── packet-tracer/
│   └── enterprise_network.pkt
├── documentation/
│   ├── 01_adding_a_pc.docx
│   ├── 02_network_topology.docx
│   ├── 03_network_evaluation.docx
│   ├── 04_technical_issues.docx
│   ├── 05_methodology.docx
│   ├── 06_terminology_guide.docx
│   ├── 07_lecturer_qa.docx
│   └── 08_updated_paragraphs.docx
└── diagrams/
    └── network_flow_diagram.html
```

---

## Network at a glance

| | |
|---|---|
| Building | 100 × 50m, single story, 15 rooms |
| VLANs | 8 — one per zone + dedicated Wi-Fi VLAN |
| Wired devices | 100+ access ports across all rooms |
| Wireless | WPA2 staff and guest SSIDs |
| Internet | NAT through core router |
| Redundancy | Dual distribution switches, STP failover |
| Remote access | Simulated VPN path via ISP router |

---

## VLAN breakdown

| VLAN | Zone | Subnet |
|------|------|--------|
| 10 | Offices | 192.168.10.0/24 |
| 20 | Technicians office | 192.168.20.0/24 |
| 30 | Open floor space | 192.168.30.0/24 |
| 40 | Meeting room | 192.168.40.0/24 |
| 50 | Kitchen | 192.168.50.0/24 |
| 60 | Reception | 192.168.60.0/24 |
| 70 | Machine room | 192.168.70.0/24 |
| 80 | Wi-Fi (all rooms) | 192.168.80.0/24 |

---

## How to open the simulation

1. Download [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) — it's free with a Cisco NetAcad account
2. Download `enterprise_network.pkt` from the `/packet-tracer` folder
3. Open it in Packet Tracer
4. To watch traffic flow, switch to **Simulation Mode** in the bottom right

---

## Key things implemented

- 8-VLAN segmentation by physical zone and trust level
- Inter-VLAN routing via Cisco 3560 Layer 3 switch
- NAT so all internal devices share one public IP
- Centralised DHCP and DNS on a dedicated server
- ACLs blocking Wi-Fi devices from accessing wired subnets
- WPA2 wireless with separate staff and guest SSIDs
- Dual distribution switch redundancy with STP automatic failover tested live
- Remote work path simulated through ISP router

---

## Technologies used

`Cisco IOS` `VLANs` `802.1Q Trunking` `NAT` `DHCP` `ACLs` `Spanning Tree Protocol` `WPA2` `Static Routing` `Cisco Packet Tracer`

---

## Documentation

All project documentation is in the `/documentation` folder. Start with **05_methodology.docx** for the full network flow, or **06_terminology_guide.docx** if you're new to networking concepts.
