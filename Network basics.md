# Networking Basics

A beginner-friendly networking study note covering the important concepts used in cybersecurity.

---

## 1. What is a Network?

A **network** is a group of two or more devices connected together so they can communicate and share data, resources, and services.

### Examples
- Computers connected in an office
- Mobile phones connected to Wi-Fi
- Servers communicating over the Internet

### Main purposes
- Data sharing
- Resource sharing
- Communication
- Access to services

### Types of Networks
- **LAN (Local Area Network):** Covers a small area such as a home, office, or lab.
- **WAN (Wide Area Network):** Covers a large geographical area and connects multiple networks.
- **MAN (Metropolitan Area Network):** Covers a city or large metropolitan area.
- **PAN (Personal Area Network):** A small personal network, such as a phone connected to Bluetooth headphones.

---

## 2. IP Address

An **IP (Internet Protocol) address** is a logical address assigned to a device on a network. It helps identify devices and enables communication between networks.

### IPv4
IPv4 uses a **32-bit** address written in four decimal parts.

Example:
`192.168.1.10`

### IPv6
IPv6 uses a **128-bit** address and was developed to provide a much larger address space.

Example:
`2001:db8::1`

### Purpose of an IP Address
- Identifies a device logically
- Helps deliver packets
- Enables communication between networks
- Helps routers determine where traffic should go

---

## 3. MAC Address

A **MAC (Media Access Control) address** is a hardware/link-layer address associated with a network interface.

Example:
`00:1A:2B:3C:4D:5E`

### Important Points
- Used mainly at the **Data Link Layer**
- Used for communication within a local network
- Associated with a network interface
- Switches use MAC addresses when forwarding Ethernet frames

### IP vs MAC
- **IP address:** Logical network address
- **MAC address:** Link-layer address

---

## 4. Private and Public IP

### Private IP

A private IP address is used inside a local network and is not directly routable on the public Internet.

Common private IPv4 ranges:
- `10.0.0.0/8`
- `172.16.0.0/12`
- `192.168.0.0/16`

Example:
`192.168.1.10`

### Public IP

A public IP address is used for communication across the Internet.

A home router commonly uses a public IP for its Internet connection while devices inside the home may use private IP addresses.

### Example

`Laptop (192.168.1.10) → Router/NAT → Internet`

---

## 5. Static and Dynamic IP

### Static IP

A static IP remains fixed unless it is manually changed.

Common uses:
- Servers
- Network devices
- Services that need a consistent address

### Dynamic IP

A dynamic IP is assigned automatically, commonly using **DHCP**.

Dynamic addresses are commonly used for normal client devices.

### Difference

- **Static:** Usually manually configured and remains consistent.
- **Dynamic:** Automatically assigned and may change.

---

## 6. Subnet Mask and Subnetting

A **subnet mask** determines which part of an IPv4 address represents the network and which part represents the host.

Example:

IP Address: `192.168.1.10`  
Subnet Mask: `255.255.255.0`

CIDR notation:
`192.168.1.10/24`

### What is Subnetting?

**Subnetting** is the process of dividing a larger network into smaller networks called subnets.

### Benefits
- Better organization
- Efficient IP address usage
- Smaller broadcast domains
- Improved network management
- Can help with network segmentation

---

## 7. Default Gateway

A **default gateway** is the device that forwards traffic from a local network to other networks.

In a typical home network, the router acts as the default gateway.

### Example

`Computer → Router → Internet`

If a device wants to communicate with a destination outside its local network, it normally sends the traffic to the default gateway.

---

## 8. DNS

**DNS (Domain Name System)** translates human-readable domain names into IP addresses.

Example:

`google.com → IP address`

### Why DNS is useful

Humans can remember names more easily than numerical IP addresses.

### Common DNS-related terms
- **Domain name:** Human-readable name such as `example.com`
- **DNS server:** Server that answers DNS queries
- **DNS resolution:** Process of finding the IP address for a domain

---

## 9. DHCP

**DHCP (Dynamic Host Configuration Protocol)** automatically provides network configuration to devices.

### DHCP can provide
- IP address
- Subnet mask
- Default gateway
- DNS server

### DORA Process

The common DHCP process is remembered as **DORA**:

1. **Discover** – Client searches for a DHCP server.
2. **Offer** – DHCP server offers an IP configuration.
3. **Request** – Client requests the offered configuration.
4. **Acknowledgment** – Server confirms the assignment.

---

## 10. TCP and UDP

TCP and UDP are **Transport Layer** protocols.

### TCP

**TCP (Transmission Control Protocol)** is connection-oriented and provides reliable, ordered delivery.

### TCP Features
- Connection-oriented
- Reliable delivery
- Ordered data
- Error checking
- Flow/congestion control mechanisms

### UDP

**UDP (User Datagram Protocol)** is connectionless and has lower overhead.

### UDP Features
- Connectionless
- Lower overhead
- No built-in guarantee of delivery
- No built-in guarantee of ordering
- Useful when low overhead or timing is important

### Simple Difference

**TCP:** Reliability is a priority.  
**UDP:** Lower overhead and speed can be a priority.

---

## 11. TCP 3-Way Handshake

TCP commonly establishes a connection using a three-step handshake.

### Steps

1. **SYN** – Client requests a connection.
2. **SYN-ACK** – Server acknowledges and responds.
3. **ACK** – Client acknowledges the response.

After this process, the TCP connection can proceed with data transfer.

---

## 12. Ports and Protocols

A **port** identifies a service or application endpoint on a device.

### Common Ports

| Protocol | Port | Purpose |
|---|---:|---|
| FTP | 21 | File Transfer |
| SSH | 22 | Secure Remote Access |
| SMTP | 25 | Email Sending |
| DNS | 53 | Domain Name System |
| HTTP | 80 | Web Traffic |
| HTTPS | 443 | Secure Web Traffic |

### Important Note

A port number by itself does not guarantee exactly what service is running. The actual service should be verified when performing network analysis.

---

## 13. Firewall

A **firewall** is a security mechanism that monitors and controls network traffic according to configured rules.

### Firewall rules can consider
- Source IP
- Destination IP
- Port
- Protocol
- Direction
- Connection state

### Purpose
- Block unauthorized traffic
- Allow legitimate traffic
- Reduce exposure
- Enforce network access policies

### Types
- Host-based firewall
- Network firewall
- Stateful firewall
- Next-generation firewall

---

## 14. NAT

**NAT (Network Address Translation)** translates addresses between network address spaces.

It is commonly used by routers to allow devices using private IP addresses to access the Internet through a public IP address.

### Example

`Private IP → Router/NAT → Public IP → Internet`

### Benefits
- Conserves public IPv4 addresses
- Allows private addressing inside local networks
- Can simplify some network designs

---

## 15. LAN, WAN, MAN and PAN

### LAN – Local Area Network
A network covering a limited area.

Example:
Home, office, computer lab.

### WAN – Wide Area Network
A network covering a large geographical area.

Example:
The Internet.

### MAN – Metropolitan Area Network
A network covering a city or metropolitan area.

### PAN – Personal Area Network
A small network around an individual.

Example:
Phone connected to Bluetooth headphones.

---

## 16. OSI Model

**OSI (Open Systems Interconnection)** is a seven-layer conceptual model used to understand network communication.

### Layer 7 – Application

The **Application Layer** provides network-related services to applications used by users.

Examples:
- HTTP
- HTTPS
- FTP
- DNS
- SMTP

### Layer 6 – Presentation

The **Presentation Layer** handles how data is represented.

Common responsibilities include:
- Data formatting
- Encoding/translation
- Encryption/decryption concepts
- Compression

### Layer 5 – Session

The **Session Layer** establishes, manages, and terminates communication sessions between applications.

Responsibilities include:
- Session establishment
- Session management
- Session termination

### Layer 4 – Transport

The **Transport Layer** provides end-to-end communication between applications.

Examples:
- TCP
- UDP

Responsibilities include:
- Segmentation
- Delivery management
- Reliability mechanisms in protocols such as TCP
- Flow/congestion control mechanisms

### Layer 3 – Network

The **Network Layer** handles logical addressing and routing between networks.

Examples:
- IPv4
- IPv6
- ICMP

Device commonly associated:
- Router

### Layer 2 – Data Link

The **Data Link Layer** handles communication over a local network link.

Responsibilities include:
- Frames
- MAC addressing
- Local delivery
- Error detection mechanisms

Examples:
- Ethernet
- Wi-Fi

Device commonly associated:
- Switch

### Layer 1 – Physical

The **Physical Layer** transmits raw bits through physical or radio media.

Examples:
- Ethernet cable
- Fiber optic cable
- Radio signals

Devices commonly associated:
- Hub
- Repeater

### OSI Layer Order

7. Application  
6. Presentation  
5. Session  
4. Transport  
3. Network  
2. Data Link  
1. Physical

### Mnemonic

**All People Seem To Need Data Processing**

- A – Application
- P – Presentation
- S – Session
- T – Transport
- N – Network
- D – Data Link
- P – Physical

---

## 17. TCP/IP Model

The **TCP/IP model** is the protocol architecture commonly associated with Internet communication.

### 1. Application Layer

Provides protocols used by applications.

Examples:
- HTTP/HTTPS
- DNS
- FTP
- SMTP

### 2. Transport Layer

Provides end-to-end transport.

Examples:
- TCP
- UDP

### 3. Internet Layer

Handles logical addressing and routing.

Examples:
- IP
- ICMP

### 4. Network Access Layer

Handles communication over the local network technology.

Examples:
- Ethernet
- Wi-Fi

### OSI vs TCP/IP

The OSI model has **7 layers**, while the commonly taught TCP/IP model has **4 layers**.

---

## 18. ARP

**ARP (Address Resolution Protocol)** is used in IPv4 local networks to discover the MAC address associated with a known IPv4 address.

### Example

`IP: 192.168.1.5`  
`↓`  
`ARP request/reply`  
`↓`  
`MAC address`

### Important Point

ARP operates within the local network and is associated with IPv4. IPv6 uses different mechanisms such as Neighbor Discovery.

---

## 19. ICMP

**ICMP (Internet Control Message Protocol)** is used for network diagnostics, control messages, and error reporting.

Examples:
- Ping
- Network unreachable messages
- Time exceeded messages

ICMP is associated with the Network/Internet layer rather than TCP or UDP.

---

## 20. Ping

**Ping** is a network diagnostic tool commonly used to test whether a host is reachable and to measure response time.

Example:

```bash
ping 8.8.8.8
```

### Ping can help identify
- Whether a host responds
- Approximate round-trip time
- Packet loss

Ping commonly uses **ICMP Echo Request and Echo Reply** for IPv4.

---

## 21. Routing

**Routing** is the process of selecting a path for packets to travel from one network to another.

Routers use routing information to forward packets toward their destinations.

### Example

`Network A → Router → Network B`

### Routing can be
- Static
- Dynamic

Dynamic routing uses routing protocols to learn and update routes.

---

## 22. Routing Table

A **routing table** contains information used to decide where packets should be forwarded.

It may contain:
- Destination network
- Prefix/subnet
- Next hop/gateway
- Interface
- Route metric

### Simple Example

`Destination → Next Hop → Interface`

The most appropriate matching route is selected according to routing rules.

---

## 23. Switch vs Hub

### Switch

A **switch** connects devices on a local network and forwards Ethernet frames based primarily on MAC address information.

### Hub

A **hub** is a basic Layer 1 device that repeats incoming signals to all connected ports.

### Main Difference

**Switch:** Forwards traffic selectively based on learned information.  
**Hub:** Sends/repeats traffic to all ports.

Switches are much more common in modern networks.

---

## 24. Router vs Switch

### Router

A **router** connects different networks and forwards packets between them.

Example:
`LAN → Router → Internet`

### Switch

A **switch** connects devices within a local network.

Example:
`PC → Switch → PC`

### Simple Difference

**Router:** Connects networks.  
**Switch:** Connects devices within a network.

---

## 25. Modem

A **modem** is a device that converts signals to enable communication over a particular access medium.

The word modem comes from:
**Modulator + Demodulator**

In modern home networks, modem and router functions may be combined into one device.

---

## 26. Network Topology

**Network topology** describes how devices and connections are arranged in a network.

### Star Topology

All devices connect to a central device, usually a switch.

**Advantage:** Easy to manage.  
**Disadvantage:** Failure of the central device can affect connected devices.

### Bus Topology

Devices share a common communication line.

### Ring Topology

Devices are connected in a circular arrangement.

### Mesh Topology

Devices have multiple interconnections.

**Advantage:** Redundancy and multiple paths.  
**Disadvantage:** More complex and expensive.

### Tree Topology

A hierarchical arrangement of network segments.

---

## 27. Bandwidth and Latency

### Bandwidth

**Bandwidth** is the maximum data transfer capacity of a connection over a given period.

Example:
`100 Mbps`

Higher bandwidth can allow more data to be transferred per second, depending on other network conditions.

### Latency

**Latency** is the time delay involved in sending data between endpoints.

Lower latency generally means faster response.

### Simple Difference

**Bandwidth:** How much data can be transferred.  
**Latency:** How long communication takes.

---

## 28. Packet

A **packet** is a unit of data carried across a network at the Network Layer.

Data is divided into smaller units for transmission.

A packet can contain information such as:
- Source address
- Destination address
- Payload/data
- Control information

At different layers, data may be referred to by different names, such as **segment** at the TCP layer and **frame** at the Data Link layer.

---

## 29. Client and Server

### Client

A **client** is a device or application that requests a service or resource.

Example:
Web browser.

### Server

A **server** is a device or application that provides a service or resource.

Example:
Web server.

### Communication

`Client → Request → Server`

`Client ← Response ← Server`

Examples:
- Browser → Web server
- Email client → Mail server
- SSH client → SSH server

---

## 30. Proxy Server

A **proxy server** acts as an intermediary between a client and another server.

### Basic Flow

`Client → Proxy → Internet/Server`

### Possible Uses
- Traffic filtering
- Access control
- Caching
- Logging
- Network policy enforcement
- Privacy-related network configuration

### Important Point

A proxy does not automatically make a user anonymous or secure. Its security and privacy benefits depend on how it is configured and used.

---

# Quick Revision

| Topic | Key Point |
|---|---|
| Network | Connected devices communicating |
| IP | Logical network address |
| MAC | Link-layer address |
| Private IP | Used inside local networks |
| Public IP | Used for Internet communication |
| DHCP | Automatically provides network configuration |
| DNS | Resolves domain names to IP addresses |
| TCP | Reliable, connection-oriented transport |
| UDP | Connectionless, low-overhead transport |
| Port | Identifies a service/application endpoint |
| Firewall | Controls network traffic |
| NAT | Translates network addresses |
| ARP | Finds MAC address for an IPv4 address on a local network |
| ICMP | Diagnostics and control/error messages |
| Ping | Tests reachability and response time |
| Router | Connects/forwards between networks |
| Switch | Connects devices on a local network |
| OSI | Seven-layer networking model |
| TCP/IP | Internet protocol architecture |
| Packet | Unit of data at the network layer |

---

# Important Networking Commands

```bash
ip addr
```
Displays network interfaces and IP addresses.

```bash
ip route
```
Displays the routing table.

```bash
ping 8.8.8.8
```
Tests connectivity to a host.

```bash
ip neigh
```
Displays the local neighbor/ARP-related table.

```bash
ss -tuln
```
Displays listening TCP/UDP sockets.

```bash
traceroute example.com
```
Shows the path packets may take toward a destination.

```bash
nslookup example.com
```
Queries DNS information.

```bash
curl https://example.com
```
Makes an HTTP request and displays the response.

---

# Key Things to Remember

- **IP = logical address**
- **MAC = link-layer address**
- **DNS = domain name resolution**
- **DHCP = automatic network configuration**
- **TCP = reliable transport**
- **UDP = connectionless transport**
- **ARP = IPv4 address-to-MAC resolution on a local network**
- **ICMP = diagnostics/control messages**
- **Router = connects networks**
- **Switch = connects devices on a LAN**
- **Firewall = controls traffic**
- **NAT = translates addresses**
- **OSI = 7 layers**
- **TCP/IP = commonly taught as 4 layers**
