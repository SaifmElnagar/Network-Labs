
🌐 WAN Connectivity Between Multiple LANs Lab (Packet Tracer)

📌 Lab Title  
Packet Tracer - Connecting Multiple LANs Over a Serial WAN Link

🎯 Objectives  
Part 1:  
Build the network topology in Packet Tracer

Part 2:  
Configure a WAN connection between two routers using a Serial DCE link

Part 3:  
Assign IP addresses to all router interfaces and end devices

Part 4:  
Test end-to-end connectivity between the different LANs

📚 Background  
This lab demonstrates how multiple LANs at two different locations can communicate through routers over a point-to-point WAN connection.

The topology represents two sites:

- **Cairo**
- **Alex**

Each site contains:

- Two separate LANs
- One router
- Switches connecting local PCs
- A serial WAN link connecting both routers

This lab helps build a strong understanding of:

- Router-based network interconnection
- WAN serial communication
- IPv4 subnetting in real topology design
- Interface labeling and documentation
- Connectivity verification using ping

As part of this lab, different subnet sizes are used across the network, which also gives practical exposure to subnet allocation and interface addressing.

🧪 Part 1: Place Devices in Packet Tracer  
🔹 Step 1: Build the Topology  
Place the required devices in Packet Tracer:

- 2 Routers
- 4 Switches
- 4 PCs

Create two sites:

- **Cairo Site**
- **Alex Site**

Each site contains two LAN segments connected to the local router.

🔹 Step 2: Connect the Devices  
Use the correct cable types to connect:

- PC to Switch
- Switch to Router
- Router to Router using **Serial connection**

Observation:

- Each router serves as the gateway for its local LANs
- The serial connection acts as the WAN link between both sites

🧪 Part 2: Understand the WAN Link  
🔹 Step 1: Configure the Serial Connection  
The two routers are connected through a **point-to-point WAN link** using a **Serial DCE cable**.

WAN Network:

- **192.168.1.232/30**
- Usable IPs:
  - 192.168.1.233
  - 192.168.1.234

This subnet is used only for communication between the two routers.

🔹 Step 2: Understand the Role of Serial DCE  
The Serial DCE side is responsible for providing clocking on the WAN link.

Key idea:

- Serial WAN links are commonly used in labs to simulate communication between remote sites
- A /30 subnet is ideal for point-to-point links because it provides exactly two usable addresses

🧪 Part 3: Label Interfaces  
🔹 Step 1: Add Labels to the Topology  
Labels were added to clearly identify:

- Router interfaces
- LAN names
- Subnet addresses
- Interface IP addresses

This improves:

- Topology readability
- Troubleshooting
- Documentation quality

🔹 Interfaces Used  
On the Cairo router:

- **Gig0/0/0** → Cairo LAN A
- **Gig0/0/1** → Cairo LAN B
- **Se0/1/0** → WAN link

On the Alex router:

- **Gig0/0/0** → Alex LAN A
- **Gig0/0/1** → Alex LAN B
- **Se0/1/0** → WAN link

🧪 Part 4: IP Addressing  
🔹 Step 1: Assign IP Addresses to Each Network  

**Cairo LAN A**
- Network: **192.168.1.0/25**
- Mask: **255.255.255.128**
- Router Interface: **192.168.1.1**
- PC0: **192.168.1.2**

**Cairo LAN B**
- Network: **192.168.1.224/29**
- Mask: **255.255.255.248**
- Router Interface: **192.168.1.225**
- PC1: **192.168.1.226**

**WAN Link**
- Network: **192.168.1.232/30**
- Mask: **255.255.255.252**
- Cairo Router Serial: **192.168.1.233**
- Alex Router Serial: **192.168.1.234**

**Alex LAN B**
- Network: **192.168.1.128/26**
- Mask: **255.255.255.192**
- Router Interface: **192.168.1.129**
- PC2: **192.168.1.130**

**Alex LAN A**
- Network: **192.168.1.192/27**
- Mask: **255.255.255.224**
- Router Interface: **192.168.1.193**
- PC3: **192.168.1.194**

🔹 Step 2: Verify Addressing Logic  
This addressing plan shows how one major network can be subnetted into different subnet sizes depending on the required number of hosts.

Subnet sizes used in this lab:

- /25
- /26
- /27
- /29
- /30

This gives practical experience with **VLSM-style subnet usage** in a routed environment.

🧪 Part 5: Test the Network  
🔹 Step 1: Perform Connectivity Tests  
After assigning IP addresses and completing the topology, test the network using:

- `ping` between PCs
- `ping` to router interfaces
- remote connectivity between Cairo and Alex networks

🔹 Step 2: Verify Communication  
Successful ping results confirm that:

- Devices are correctly addressed
- Router interfaces are active
- The WAN link is operational
- Remote LANs can communicate through the routers

🧠 Key Learning Outcomes  
- Understand how routers connect multiple LANs
- Learn how WAN links are used between remote sites
- Practice assigning IP addresses across different subnet sizes
- Recognize the importance of interface labeling and documentation
- Verify network communication using ping tests
- Strengthen understanding of subnetting in practical topologies

📂 Lab Files  
📄 wan_multi_lan_topology.pkt

🚀 Conclusion  
This lab provides a practical introduction to building a routed network that connects multiple LANs across two locations using a serial WAN link.

It combines several important CCNA skills in one exercise:

- Topology building
- WAN fundamentals
- Interface planning
- IPv4 addressing
- Connectivity testing

It is a strong foundational lab for understanding how communication happens between different networks through routers.

👨‍💻 Author  
Saif Elnagar  
Electronics & Communication Engineering Student  
Network & Cloud Engineer 🚀
