# CCNA Lab Portfolio

Hands-on networking labs built in Cisco Packet Tracer, documented from initial design through configuration, verification, and troubleshooting. This repo demonstrates the CCNA-level skills behind my certification, using the same documentation methodology I'd apply in production environments.

## About Me

I'm a Computer Engineering graduate (First-Class Honours) and CCNA-certified network engineer, building this portfolio to demonstrate hands-on proficiency for enterprise networking and security roles. This portfolio documents the labs I've built while studying for CCNA (and now CompTIA Security+), each one designed to demonstrate not just that a configuration works, but that I understand *why* it works.

## Lab Index

| # | Lab | Topics Covered | Status |
|---|-----|-----------------|--------|
| 01 | [Basic Device Config & Security Baseline](./01-basic-security) | Hostnames, banners, SSH, local AAA, password encryption | ✅ |
| 02 | [VLANs & Trunking](./02-vlans-trunking) | VLAN creation, access/trunk ports, native VLAN, DTP | ✅ |
| 03 | [Inter-VLAN Routing](./03-inter-vlan-routing) | Router-on-a-stick vs. SVI/L3 switching | ✅ |
| 04 | [EtherChannel & Redundancy](./04-etherchannel-redundancy) | LACP/PAgP, STP, HSRP | 🔧 |
| 05 | [DHCP & DHCP Snooping](./05-dhcp-snooping) | DHCP server/relay, snooping, exclusions | 🔧 |
| 06 | [OSPF Single-Area](./06-ospf-single-area) | Neighbor adjacency, DR/BDR election, route verification | 🔧 |
| 07 | [OSPF Multi-Area](./07-ospf-multi-area) | ABR/ASBR, LSA types, summarization | 🔧 |
| 08 | [NAT (Static, Dynamic, PAT)](./08-nat) | Address translation and verification | 🔧 |
| 09 | [ACLs (Standard & Extended)](./09-acls) | Traffic filtering, placement logic | 🔧 |
| 10 | [WAN & Security Services](./10-wan-security-services) | NTP, SNMP, port security | 🔧 |
| 11 | [Capstone: Small Enterprise Network](./11-capstone-enterprise-network) | Full integration of all topics above | 🔧 |

✅ = complete &nbsp;&nbsp; 🔧 = in progress

## Repo Structure

Each lab folder follows the same format:

```
##-lab-name/
├── README.md          # Objective, topology, config steps, verification, troubleshooting
├── topology.png        # Network diagram
├── lab##.pkt            # Packet Tracer file
└── configs/              # Plain-text running-configs per device
```

## Tools & Study Resources

- **Simulation:** Cisco Packet Tracer
- **Study:** Jeremy's IT Lab (CCNA course), Boson ExSim practice exams
- **Documentation:** Markdown, draw.io / Packet Tracer topology exports

## Certification Path

CCNA (achieved) → CompTIA Security+ (in progress) → CCNP Enterprise (planned, ENSDWI/SD-WAN concentration)

## Connect

- [LinkedIn](http://linkedin.com/in/nathanadegbite)

