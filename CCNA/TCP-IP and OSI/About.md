# 🌐 TCP/IP and OSI Models Lab (Packet Tracer)

## 📌 Lab Title
Packet Tracer - Investigating the TCP/IP and OSI Models in Action

---

## 🎯 Objectives

### Part 1:
- Examine HTTP Web Traffic

### Part 2:
- Display Elements of the TCP/IP Protocol Suite

---

## 📚 Background

This simulation activity provides a foundation for understanding the TCP/IP protocol suite and its relationship to the OSI model.

Packet Tracer Simulation mode allows you to:
- View data as it moves through the network
- Observe packet contents at each layer
- Understand how data is encapsulated and transmitted

As data travels through the network:
- It is divided into smaller units called **PDUs (Protocol Data Units)**
- Each PDU is associated with a specific layer in the OSI and TCP/IP models
- Data is reassembled at the destination

This lab helps visualize:
- Encapsulation
- Layer interaction
- Real network communication

---

# 🧪 Part 1: Examine HTTP Web Traffic

## 🔹 Step 1: Switch to Simulation Mode

- Switch from **Realtime** to **Simulation Mode**
- Simulation mode allows you to:
  - Pause time
  - Step through events
  - View packet flow visually

### Filter Events:
- Click **Edit Filters**
- Disable all protocols
- Enable only **HTTP**

---

## 🔹 Step 2: Generate HTTP Traffic

1. Click **Web Client**
2. Go to **Desktop**
3. Open **Web Browser**
4. Enter: www.osi.com
5. Click **Go**
6. Press **Capture/Forward** 4 times

### Observation:
- Events appear in the Event List
- Check if the webpage changes

---

## 🔹 Step 3: Analyze HTTP Packet

Click the first event in the **Info column**

### OSI Model Analysis:

- **Layer 7 (Application):** HTTP request
- **Layer 4 (Transport):** Destination Port (TCP)
- **Layer 3 (Network):** Destination IP
- **Layer 2 (Data Link):** MAC addresses
- **Layer 1 (Physical):** Frame transmission

### Questions to Explore:

- What is shown at Layer 7?
- What is the destination port at Layer 4?
- What is the destination IP at Layer 3?
- What data appears at lower layers?

---

## 🔹 PDU Details Analysis

- Compare OSI Model vs PDU Details
- Look at:
  - IP Section → Layer 3
  - TCP Section → Layer 4
  - HTTP Section → Layer 7

### Key Observations:

- MAC addresses appear under Ethernet II
- TCP manages transport communication
- HTTP contains application-level data

---

## 🔹 Packet Flow Observations

- Layer 1 sends frames physically
- Data flows:
  - From client → server
  - Then server → client (response)

### Analyze:

- Differences between **Inbound vs Outbound Layers**
- Direction of packet flow

---

## 🔹 HTTP Message

- Inspect HTTP section
- Identify:
  - First line of HTTP request

---

# 🌐 Part 2: TCP/IP Protocol Suite

## 🔹 Step 1: Show All Events

- Enable all protocols in filters

### Additional Protocols Observed:

- **DNS** → Domain name resolution
- **ARP** → MAC address resolution
- **TCP** → Connection management

---

## 🔹 DNS Analysis

- Inspect DNS events
- Look at:

### Questions:
- What is the query name?
- Which device responds?
- What IP address is returned?

---

## 🔹 TCP Analysis

- Inspect TCP events after HTTP

### Observations:

- TCP establishes connection
- Shows communication setup steps
- Indicates session establishment

---

## 🔹 Final TCP Event

- Analyze final TCP step

### Question:
- What is the purpose of the last event?

➡️ (Hint: Connection termination)

---

# 🧠 Key Learning Outcomes

- Understand **OSI vs TCP/IP models**
- Visualize **encapsulation process**
- Analyze:
  - HTTP traffic
  - DNS queries
  - TCP connections
- Understand real network communication flow

---

# 📂 Lab Files

- 📄 `tcp_ip_osi.pka`

---

# 🚀 Conclusion

This lab demonstrates how data moves through different network layers and how protocols interact within the TCP/IP suite.

It provides a clear visualization of:
- Encapsulation
- Packet flow
- Real-world networking behavior

---

# 👨‍💻 Author

**Saif Elnagar**  
Electronics & Communication Engineering Student  
Future Network & Cloud Engineer 🚀

