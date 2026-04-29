
🌐 RIP Routing Lab (Packet Tracer)

📌 Lab Title  
Configure RIP Routing on a Network

🎯 Objectives  
Part 1:  
Assign IP addresses to router interfaces and PCs

Part 2:  
Configure RIP on all routers

Part 3:  
Verify RIP operation and learned routes

Part 4:  
Test full connectivity between all LANs

📚 Background  
In a routed network, each router automatically knows only its **directly connected networks**. To reach remote networks, routers must either:

- Be configured manually with **static routes**
- Or learn routes dynamically using a **routing protocol**

In this lab, **RIP (Routing Information Protocol)** is used to allow the routers to exchange routing information and learn about remote networks automatically.

<img width="1550" height="692" alt="image" src="https://github.com/user-attachments/assets/b523399e-acd5-47d4-9d4b-dfa7c2fe0436" />


The topology contains **three routers** connected through two serial links, with each router serving one local LAN:

- **R1 LAN** → 192.168.1.0/24
- **R2 LAN** → 192.168.3.0/24
- **R3 LAN** → 192.168.5.0/24

The router-to-router links are:

- **192.168.2.0/24** between R1 and R2
- **192.168.4.0/24** between R2 and R3

This lab helps build understanding of:

- Dynamic routing basics
- RIP configuration
- Route advertisement
- Routing table learning
- End-to-end connectivity verification

🧪 Part 1: IP Address Assignment  
🔹 Step 1: Configure Router Interfaces  
Assign IP addresses to all router interfaces as follows:

**R1**
- Fa0/0 → **192.168.1.1 /24**
- S0/0/0 → **192.168.2.1 /24**

**R2**
- Fa0/0 → **192.168.3.1 /24**
- S0/0/0 → **192.168.2.2 /24**
- S0/0/1 → **192.168.4.2 /24**

**R3**
- Fa0/0 → **192.168.5.1 /24**
- S0/0/1 → **192.168.4.1 /24**

🔹 Step 2: Configure PC Addressing  
Assign IP addresses and default gateways to the end devices:

**PC1**
- IP Address: **192.168.1.10**
- Subnet Mask: **255.255.255.0**
- Default Gateway: **192.168.1.1**

**PC2**
- IP Address: **192.168.3.10**
- Subnet Mask: **255.255.255.0**
- Default Gateway: **192.168.3.1**

**PC3**
- IP Address: **192.168.5.10**
- Subnet Mask: **255.255.255.0**
- Default Gateway: **192.168.5.1**

🔹 Step 3: Verify Local Configuration  
After assigning the IP addresses:

- Make sure interfaces are enabled
- Confirm each PC can reach its default gateway
- Verify each router knows its directly connected networks

Observation:

- At this stage, remote LAN communication will not work until routing is configured

🧪 Part 2: Configure RIP  
🔹 Step 1: Enter RIP Routing Mode  
On each router, enter global configuration mode and start RIP using:

- `router rip`

This enables the RIP process on the router.

🔹 Step 2: Advertise Directly Connected Networks  
Each router must advertise the networks directly connected to it.

**R1 networks**
- `192.168.1.0`
- `192.168.2.0`

**R2 networks**
- `192.168.2.0`
- `192.168.3.0`
- `192.168.4.0`

**R3 networks**
- `192.168.4.0`
- `192.168.5.0`

By advertising these networks, routers begin exchanging routing updates and learning about remote destinations.

🔹 Step 3: Save the Configuration  
After configuring RIP, save the running configuration to startup configuration so the settings remain after reboot.

🧪 Part 3: Verify RIP Operation  
🔹 Step 1: Examine RIP Parameters  
Use the command:

- `show ip protocols`

This command helps verify:

- RIP is running
- Which networks are being advertised
- Routing update settings
- RIP timers and parameters

🔹 Step 2: Examine the Routing Table  
Use the command:

- `show ip route`

The routing table should contain entries for all **five networks** in the topology:

- 192.168.1.0/24
- 192.168.2.0/24
- 192.168.3.0/24
- 192.168.4.0/24
- 192.168.5.0/24

Observation:

- Directly connected routes appear with **C**
- RIP-learned routes appear with **R**

This confirms that the routers are learning remote networks dynamically.

🧪 Part 4: Check Connectivity  
🔹 Step 1: Test End-to-End Communication  
After RIP has converged, verify connectivity by pinging:

- From **PC1** to **PC2**
- From **PC1** to **PC3**
- From **PC2** to **PC1**
- From **PC2** to **PC3**
- From **PC3** to **PC1**
- From **PC3** to **PC2**

🔹 Step 2: Confirm Network Reachability  
If RIP is configured correctly:

- All LANs should be reachable
- All routers should know the remote networks
- Full communication between all PCs should succeed

🧠 Key Learning Outcomes  
- Understand why dynamic routing is needed
- Learn how RIP advertises directly connected networks
- Configure RIP on multiple routers
- Verify RIP operation using `show ip protocols`
- Examine learned routes using `show ip route`
- Confirm full network communication using ping
- Build a strong foundation before studying more advanced routing protocols like OSPF and EIGRP


🚀 Conclusion  
This lab introduces the fundamentals of **dynamic routing with RIP** in a multi-router topology. Instead of manually defining every remote route, routers use RIP to exchange information and automatically learn how to reach other networks.

By completing this lab, you gain practical experience in:

- Router configuration
- Route advertisement
- Routing table analysis
- Connectivity troubleshooting

It is an important step toward understanding how real networks scale beyond static routing.

👨‍💻 Author  
Saif Elnagar  
Electronics & Communication Engineering Graduate  
Network & Cloud Engineer 🚀
