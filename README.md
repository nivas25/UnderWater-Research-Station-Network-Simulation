# Underwater Research Station Network Simulation

A network infrastructure simulation designed in Cisco Packet Tracer to model the communication systems for a multi-level underwater research facility.

## Table of Contents

- [Project Overview](#project-overview)
- [Network Topology](#network-topology)
- [Key Features and Technologies Implemented](#key-features-and-technologies-implemented)
- [IP Addressing Scheme](#ip-addressing-scheme)
- [Software Requirements](#software-requirements)
- [How to Use the Simulation](#how-to-use-the-simulation)
- [Testing and Verification](#testing-and-verification)

## Project Overview

This Cisco Packet Tracer project simulates a robust and resilient network for an underwater research station. The scenario involves a surface control station connected to multiple submerged research labs. The network is designed to ensure reliable data transfer, communication between scientists, and secure access to centralized servers, all while addressing the unique challenges of a remote and isolated environment.

## Network Topology

The network is logically divided into several key areas:

- **Surface Control Station (SCS):** The main hub located above water. It houses the primary servers (DNS, Web, FTP) and connects the facility to the external internet (simulated).
- **Underwater Hub (UWH):** A central routing and switching point located at the main entry point to the submerged section. It distributes the network to the various labs.
- **Research Lab Alpha & Beta:** Two separate VLANs representing different scientific departments. Each lab contains workstations for researchers, IP phones for communication, and other network devices.
- **Sensor Network:** A dedicated network segment for collecting data from various underwater sensors.

The connection between the Surface Control Station and the Underwater Hub is established via a high-speed fiber optic link to simulate a reliable, long-distance connection.

## Key Features and Technologies Implemented

### Routing

- OSPF, EIGRP, or Static Routing is configured for dynamic or static routing between the different network segments (SCS, UWH, Labs).

### Switching

- **VLANs:** The research labs are segregated into different VLANs (e.g., VLAN 10 for Lab Alpha, VLAN 20 for Lab Beta) to enhance security and manage broadcast traffic.
- **VTP (VLAN Trunking Protocol):** Used to manage and synchronize VLAN information across switches.
- **STP (Spanning Tree Protocol):** Enabled to prevent switching loops.

### Network Services

- **DHCP Server:** Dynamically assigns IP addresses to end devices within each lab.
- **DNS Server:** Resolves domain names (e.g., www.research.net) to IP addresses.
- **HTTP Server:** Hosts an internal research portal accessible to all staff.
- **FTP Server:** Allows for the transfer of large research data files.

### Security

- **Access Control Lists (ACLs):** Implemented to filter traffic and restrict access between different VLANs (e.g., preventing the Sensor Network from accessing the main lab network directly).
- **Port Security:** Configured on switches to limit access to specific MAC addresses.

## IP Addressing Scheme

| Network Segment        | Network Address     | Subnet Mask         | VLAN ID |
|------------------------|---------------------|----------------------|---------|
| Surface Control (SCS)  | 192.168.1.0         | 255.255.255.0        | N/A     |
| Research Lab Alpha     | 192.168.10.0        | 255.255.255.0        | 10      |
| Research Lab Beta      | 192.168.20.0        | 255.255.255.0        | 20      |
| Sensor Network         | 192.168.30.0        | 255.255.255.0        | 30      |
| WAN Link (SCS to UWH)  | 10.0.0.0            | 255.255.255.252      | N/A     |

## Software Requirements

- **Cisco Packet Tracer** version 8.2.1 or higher. The project file may not be compatible with older versions.

## How to Use the Simulation

1. Download and install the required version of Cisco Packet Tracer.
2. Download the `.pkt` project file from this repository.
3. Open the `.pkt` file using Cisco Packet Tracer.
4. Allow the simulation time to converge. Wait for all the link lights on the devices to turn green.
5. Switch to Simulation Mode to visualize traffic flow in detail, or remain in Realtime Mode for immediate command testing.

## Testing and Verification

### Test DHCP Functionality

- Open a PC in Research Lab Alpha or Beta.
- Navigate to the Desktop tab and select IP Configuration.
- Ensure the PC has received an IP address via DHCP from the correct VLAN pool.

### Test Local and Remote Connectivity (Ping)

- Open the Command Prompt on a PC.
- Ping the default gateway: `ping 192.168.10.1`
- Ping a PC in the other lab: `ping 192.168.20.10`
- Ping the web server at the Surface Control Station: `ping 192.168.1.100`

### Test Network Services (DNS and HTTP)

- Open the Web Browser on a PC.
- Enter the URL: `http://www.research.net`
- The internal research portal hosted on the HTTP server should load successfully.
