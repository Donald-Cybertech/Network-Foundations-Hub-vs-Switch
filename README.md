# Network Fundamentals: Hub Topology & Broadcast Behavior

### 📌 Project Overview
This project demonstrates a basic Star Topology using a Network Hub in Cisco Packet Tracer. The objective is to visualize and understand how a Hub operates at Layer 1 (Physical Layer) of the OSI model, specifically its "blind" broadcasting behavior.


### 🛠️ Technologies Used

Cisco Packet Tracer 8.x

Networking Concepts: IPv4 Addressing, Star Topology, OSI Layer 1, ICMP (Ping).


### 🛰️ Topology Details

The network consists of one Central Hub connected to four end devices using Copper Straight-Through cables:

PC0: 192.168.1.10

PC1: 192.168.1.11

PC2: 192.168.1.12

Laptop0: 192.168.1.13


### 🚀 Lab Objectives

Connectivity: Established physical links between PCs and the Hub.

Addressing: Configured static IPv4 addresses for all end devices.

Verification: Tested connectivity using the ping command in Simulation Mode.

Security/Efficiency Analysis: Observed the Hub's inability to filter traffic based on MAC or IP addresses.

### 🔍 Key Observations (The Hub Problem)

During the simulation of an ICMP packet from PC0 to Laptop0, the following was observed:

Broadcasting: Instead of sending the packet directly to the destination (Laptop0), the Hub repeated the electrical signal out of every single port.

Security Risk: PC1 and PC2 received the packet even though it was not addressed to them. They only discarded it because the IP header did not match their own.

Collision Domain: All devices connected to the Hub share a single collision domain, which leads to network congestion as the number of devices grows.

Conclusion: This lab highlights why Hubs are obsolete in modern networks and have been replaced by Switches, which use a MAC address table to forward traffic intelligently.


### 📸 Simulation Screenshot

Figure 1: Packet Tracer simulation showing the Hub broadcasting packets to all connected nodes.
[Hub Topology Screenshot](https://github.com/Donald-Cybertech/Network-Foundations-Hub-vs-Switch/blob/main/hub_topology.jpeg)


### 📝 How to Run

Download the .pkt file from the [hub-topology.pkt](https://github.com/Donald-Cybertech/Network-Foundations-Hub-vs-Switch/blob/main/hub-topology.pkt)

Open it in Cisco Packet Tracer.

Enter Simulation Mode.

Use the Add Simple PDU tool to send a packet from one PC to another and click Play to watch the broadcast behavior.
