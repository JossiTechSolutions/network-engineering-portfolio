# IP Addressing Table

## 1. Network Overview

This project implements a small business network for two departments: Administration and IT. The network uses VLANs to separate departmental traffic and IPv4 subnets to organise device addressing.

## 2. VLAN and Subnet Allocation

| VLAN ID | Department     | Network Address | Subnet Mask   | Usable Host Range              |
| ------- | -------------- | --------------- | ------------- | ------------------------------ |
| 10      | Administration | 192.168.10.0    | 255.255.255.0 | 192.168.10.1 to 192.168.10.254 |
| 20      | IT             | 192.168.20.0    | 255.255.255.0 | 192.168.20.1 to 192.168.20.254 |

## 3. End Device Addressing

### Administration: VLAN 10

| Device | IP Address    | VLAN |
| ------ | ------------- | ---- |
| PC1    | 192.168.10.21 | 10   |
| PC2    | 192.168.10.22 | 10   |
| PC3    | 192.168.10.23 | 10   |
| PC4    | 192.168.10.24 | 10   |
| PC5    | 192.168.10.25 | 10   |

### IT: VLAN 20

| Device | IP Address    | VLAN |
| ------ | ------------- | ---- |
| PC6    | 192.168.20.21 | 20   |
| PC7    | 192.168.20.22 | 20   |
| PC8    | 192.168.20.23 | 20   |
| PC9    | 192.168.20.24 | 20   |
| PC10   | 192.168.20.25 | 20   |

## 4. Default Gateway Addressing

The network uses a router on a stick design, with R1 providing inter VLAN routing through subinterfaces.

| Interface       | VLAN | Gateway IP Address |
| --------------- | ---- | ------------------ |
| R1 subinterface | 10   | 192.168.10.1       |
| R1 subinterface | 20   | 192.168.20.1       |

**Verification note:** Confirm the gateway addresses against the actual R1 configuration before treating them as verified values.

## 5. Design Notes

1. VLAN 10 separates Administration devices from the IT department.
2. VLAN 20 provides a separate logical network for IT devices.
3. Each VLAN uses a dedicated IPv4 subnet.
4. R1 provides inter VLAN routing through its subinterfaces.
5. The SW1 to R1 connection must support the configured VLANs using 802.1Q trunking.

## 6. Verification

The addressing plan should be checked against the Packet Tracer configuration. Connectivity tests should confirm that devices communicate as intended and that any configured access controls are enforced.
