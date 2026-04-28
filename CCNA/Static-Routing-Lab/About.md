
🌐 Static Routing Lab (Packet Tracer)

📌 Lab Title  
Packet Tracer - IP Addressing and Static Routing Between Three Routers

🎯 Objectives  
Part 1:  
Assign IP addresses to PCs and router interfaces

Part 2:  
Configure static routes between the routers

Part 3:  
Verify end-to-end communication between the two LANs

📚 Background  
This lab focuses on building connectivity between two remote LANs through **three routers** using **static routing**.

The topology contains:

- One LAN on the left side using network **10.0.0.0/8**
- One LAN on the right side using network **40.0.0.0/8**
- Two point-to-point router links using:
  - **20.0.0.0/8**
  - **30.0.0.0/8**

This lab demonstrates how routers communicate with directly connected networks by default, but require **static routes** to reach remote networks.

It helps strengthen understanding of:

- IPv4 addressing
- Router interface configuration
- Directly connected vs remote networks
- Static route configuration
- End-to-end connectivity testing

🧪 Part 1: IP Address Assignment  
🔹 Step 1: Configure End Devices  
Assign IP addresses to the PCs:

- Left PC: **10.0.0.2/8**
- Right PC: **40.0.0.2/8**

Configure the default gateways:

- Left PC gateway: **10.0.0.1**
- Right PC gateway: **40.0.0.1**

🔹 Step 2: Configure Router Interfaces  
Assign IP addresses to router interfaces as shown in the topology:

**Router 1**
- Gig0/0/0 → **10.0.0.1/8**
- Gig0/0/1 → **20.0.0.1/8**

**Router 2**
- Gig0/0/0 → **20.0.0.2/8**
- Gig0/0/1 → **30.0.0.1/8**

**Router 3**
- Gig0/0/0 → **30.0.0.2/8**
- Gig0/0/1 → **40.0.0.1/8**

🔹 Step 3: Verify Local Connectivity  
After assigning the IP addresses:

- Check that each router interface is active
- Confirm each PC belongs to the correct subnet
- Verify that local communication works with the default gateway

Observation:

- Each router automatically knows its directly connected networks
- Remote networks will still need static routes

🧪 Part 2: Static Routing  
🔹 Step 1: Understand the Routing Requirement  
In this topology, each router only knows the networks directly attached to it.

For full connectivity:

- **Router 1** must know how to reach **30.0.0.0/8** and **40.0.0.0/8**
- **Router 2** must know how to reach **10.0.0.0/8** and **40.0.0.0/8**
- **Router 3** must know how to reach **10.0.0.0/8** and **20.0.0.0/8**

🔹 Step 2: Configure Static Routes  
Static routes are added manually so that traffic can be forwarded to remote networks through the correct next-hop router.

This allows:

- Router 1 to send remote traffic toward Router 2
- Router 2 to forward traffic between both sides
- Router 3 to send remote traffic back toward Router 2

🔹 Step 3: Why Static Routing Works Here  
Static routing is suitable in this lab because:

- The topology is small
- The paths are simple and predictable
- Manual control of routes helps build routing fundamentals

🧪 Part 3: Verify Connectivity  
🔹 Step 1: Test the Network  
After IP addressing and static route configuration, test connectivity using:

- `ping` from the left PC to the right PC
- `ping` from the right PC to the left PC
- `ping` between routers
- `ping` to remote router interfaces

🔹 Step 2: Confirm Successful Communication  
Successful results indicate that:

- IP addressing is correct
- Router interfaces are enabled
- Static routes are configured properly
- Packets can travel across all three routers to reach the destination

🧠 Key Learning Outcomes  
- Practice assigning IPv4 addresses in a multi-router topology
- Understand the difference between directly connected and remote networks
- Learn how static routing enables communication across multiple hops
- Identify the correct next-hop path for each remote network
- Verify routing behavior using ping tests
- Build a strong routing foundation before moving to dynamic protocols

📂 Lab Files  
📄 static_routing_three_routers.pkt

🚀 Conclusion  
This lab provides a practical introduction to **static routing in a multi-router environment**. It shows how devices in different LANs can communicate only after correct IP addressing and manual route configuration are applied.

By completing this lab, you gain a better understanding of how routers make forwarding decisions and how traffic moves step by step across intermediate networks.

👨‍💻 Author  
Saif Elnagar  
Electronics & Communication Engineering Student  
Network & Cloud Engineer 🚀
