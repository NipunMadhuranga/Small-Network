Project Overview: 


Basic LAN Routing Configuration
This project demonstrates the configuration of a Router (R1) acting as the central gateway for four distinct Local Area Networks (LANs). The primary objective was to establish inter-network connectivity by configuring physical router interfaces and static addressing across end devices.

1. Network Topology & Architecture
The network follows a star topology centered around a single router. Each of the router's four interfaces connects to a different subnet via a Layer 2 switch:

Subnet 1: 192.168.1.0/24 (Connects to Server)

Subnet 2: 192.168.2.0/24 (Connects to PC1, PC2)

Subnet 3: 192.168.3.0/24 (Connects to PC3, PC4)

Subnet 4: 192.168.4.0/24 (Connects to PC5, PC6)

2. Router Configuration Details
The router (R1) was configured via the Command Line Interface (CLI) to assign IP addresses to four Fast Ethernet interfaces and activate them.

Key Configuration Summary: 

| Interface        | IP Address  | Subnet Mask   | Status|  
| FastEthernet 0/0 | 192.168.1.1 | 255.255.255.0 | Up/Up |
| FastEthernet 0/1 | 192.168.2.1 | 255.255.255.0 | Up/Up |
| FastEthernet 1/0 | 192.168.3.1 | 255.255.255.0 | Up/Up |
| FastEthernet 1/1 | 192.168.4.1 | 255.255.255.0 | Up/Up |

*"no shutdown" command was applied to each interface to change the administrative status to "Up".

3. End-Device Addressing
All PCs and the Server utilize Static IP addressing. To ensure communication between different subnets, each device is configured with a Default Gateway pointing to its respective router interface IP (e.g., PC1 uses 192.168.2.1 as its gateway).

4. Connectivity Testing (Verification)
Successful communication was verified using the ping command from the PC Command Prompt:

Intra-Subnet Ping: PC1 successfully pinged PC2 (192.168.2.3), showing 0% packet loss.

Inter-Subnet Ping: PC1 successfully pinged the Server (192.168.1.100) across the router.

Conclusion
The project successfully achieves full IP reachability across the entire topology. By configuring the router as the central point of contact, traffic is effectively routed between all four subnets, allowing any PC to communicate with the server or other workstations.
