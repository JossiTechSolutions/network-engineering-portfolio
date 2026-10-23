# JossiTech Small Business Network

## Project Overview

This project demonstrates the design, configuration, and verification of a small business network using Cisco Packet Tracer.

The network serves two departments, Administration and IT. It uses VLANs to separate departmental traffic and a router on a stick configuration to support inter VLAN routing.

## Project Objectives

1. Design a small business network topology.
2. Configure VLANs for departmental separation.
3. Assign IPv4 addresses to end devices.
4. Configure router sub-interfaces for inter VLAN routing.
5. Configure trunking between the switch and router.
6. Test network connectivity and document the results.
7. Practice network administration and troubleshooting.

## Network Topology

The network contains two routers, one switch, and ten PCs.

**Logical connection:**

`ISP → R1 → SW1 → PCs`

The switch connects five Administration PCs to VLAN 10 and five IT PCs to VLAN 20.

**Topology diagram:** See the `topology/` folder for the network diagram.

## VLAN Configuration

| VLAN ID | Department     | Network         | Subnet Mask   |
| ------- | -------------- | --------------- | ------------- |
| 10      | Administration | 192.168.10.0/24 | 255.255.255.0 |
| 20      | IT             | 192.168.20.0/24 | 255.255.255.0 |

## IP Addressing

### Administration: VLAN 10

| Device | IP Address    |
| ------ | ------------- |
| PC1    | 192.168.10.21 |
| PC2    | 192.168.10.22 |
| PC3    | 192.168.10.23 |
| PC4    | 192.168.10.24 |
| PC5    | 192.168.10.25 |

### IT: VLAN 20

| Device | IP Address    |
| ------ | ------------- |
| PC6    | 192.168.20.21 |
| PC7    | 192.168.20.22 |
| PC8    | 192.168.20.23 |
| PC9    | 192.168.20.24 |
| PC10   | 192.168.20.25 |

**Note:** Confirm the actual default gateway addresses against the router configuration before documenting them as verified.

## Technologies and Concepts

* Cisco Packet Tracer
* IPv4 addressing and subnetting
* Virtual LANs (VLANs)
* IEEE 802.1Q trunking
* Router on a stick
* Inter VLAN routing
* Network connectivity testing
* SSH management, where configured
* DHCP and NAT/PAT, where configured

## Project Files

| Folder            | Contents                                         |
| ----------------- | ------------------------------------------------ |
| `packet-tracer/`  | Packet Tracer network simulation                 |
| `configurations/` | Device configuration files                       |
| `topology/`       | Network topology diagram                         |
| `evidence/`       | Screenshots of verification commands and tests   |
| `documentation/`  | IP addressing table and supporting documentation |

## Verification and Testing

Verification evidence is stored in the `evidence/` folder.

The project verification process includes checking VLAN membership, trunk status, interface status, routing information, DHCP operation where configured, and end to end connectivity.

Actual results should be reviewed before claiming that every feature works as intended.

## Skills Demonstrated

* Network topology design
* VLAN planning and segmentation
* IPv4 addressing
* Router and switch configuration
* Inter VLAN routing
* Network troubleshooting
* Technical documentation
* Configuration verification

## Future Improvements

Potential extensions include implementing and testing access control lists, documenting NAT/PAT behavior, strengthening secure device management, and expanding the topology with additional switches or departments.

## Author

JossiTech

Network Engineering Portfolio

**Build. Configure. Connect.**
