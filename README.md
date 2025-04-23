🏢 Office Network Infrastructure – Cisco Packet Tracer Simulation
This project demonstrates the physical and logical design of a multi-floor office network simulated in Cisco Packet Tracer. It includes well-structured topologies, organized IP addressing, dynamic routing, and essential server setups to ensure efficient communication and service delivery across all 8 floors.

📚 Table of Contents
Project Overview

Network Topology and Device Setup

IP Addressing Scheme

Routing Setup

Inter-Floor Communication

Server Configuration

Screenshots

Getting Started

Contributors

License

🔍 Project Overview
This network simulation project models a corporate environment spread across 8 floors using Cisco Packet Tracer. It features varied topologies, optimal IP subnetting with FLSM, and services like DHCP, DNS, HTTP, and Mail servers. The network ensures scalability, security, and connectivity between departments.

🗺️ Network Topology and Device Setup
Floor-wise Topologies

Floor(s)	Topology	Devices Used
1–3	Hybrid	Switch, Hub, PCs
4–6	Mesh	Switches, PCs
7–8	Bus	Hubs, PCs
Key Devices
Switch PT – Used in hybrid/mesh setups for reliable connections.

Hub PT – Used in hybrid/bus setups for shared medium.

Routers – Ensure connectivity between floors.

PCs & Laptops – End-user terminals.

Cables – Mix of cross-over and straight-through for suitable connections.

🧮 IP Addressing Scheme
Base Network: 192.122.5.0/24

Subnetting Method: FLSM (/28)

Subnet Mask: 255.255.255.240

Each subnet supports 14 usable IPs.

Sample Subnets

Subnet	Network Address	Usable IPs	Broadcast Address
1	192.122.5.0	192.122.5.1 – 192.122.5.14	192.122.5.15
2	192.122.5.16	192.122.5.17 – 192.122.5.30	192.122.5.31
...	...	...	...
8	192.122.5.112	192.122.5.113 – 192.122.5.126	192.122.5.127
Additional subnets are reserved for inter-router links and server segments.

🔁 Routing Setup
Protocol Used: RIP v2

Configuration Commands
bash
Copy
Edit
Router> enable
Router# config terminal
Router(config)# router rip
Router(config-router)# version 2
Router(config-router)# network 192.122.5.0
Routes are dynamically updated.

All routers communicate through RIP for seamless floor connectivity.

🔄 Inter-Floor Communication
Connectivity: Routers connect floors 1–6 in series.

Additional Router: Connects floors 6–8.

Testing Tool: ping command used to verify network flow and reliability.

🖥️ Server Configuration

Floor	Server Type	Function
4	DHCP Server	Auto IP assignment to connected devices
5	DNS Server	Resolves domain names to IP addresses
6	HTTP Server	Hosts internal web content using HTTP/HTTPS protocols
7	Mail Server	Manages email sending (SMTP) and receiving (POP3/IMAP)
All servers are assigned static IPs from their respective floor's subnet.


🚀 Getting Started
Clone the Repository
bash
Copy
Edit
git clone https://github.com/SETHUKUMAR1709/Netwok-Planning.git
Open the Simulation
Launch Cisco Packet Tracer

Open the .pkt file from the repository

👤 Contributors
Sethukumar Moorthy – GitHub

📄 License
This project is licensed under the MIT License – see the LICENSE file for details.

