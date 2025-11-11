Below is a complete README.md file generated specifically for the practicals/topics in your original text. The format follows professional standards for project documentation and maintains clarity, completeness, and usability. Headings, bullets, and code blocks are fully Markdown-compatible for direct use as README.md in any repository or project.[11]

***

# Computer Networks Lab Practicals

This repository contains practical implementations covering fundamental concepts in computer networking, including networking devices, topologies, troubleshooting commands, socket programming, protocol analysis, flow control, and routing algorithms.

## Table of Contents

1. [Practical 1: Networking Devices, Topologies & Troubleshooting](#practical-1-networking-devices-topologies--troubleshooting)
2. [Practical 2: TCP Client](#practical-2-tcp-client)
3. [Practical 3: TCP Server](#practical-3-tcp-server)
4. [Practical 4: UDP Client](#practical-4-udp-client)
5. [Practical 5: UDP Server](#practical-5-udp-server)
6. [Practical 6: DNS Packet Analysis](#practical-6-dns-packet-analysis)
7. [Practical 7: DNS and HTTP Analysis](#practical-7-dns-and-http-analysis)
8. [Practical 8.1: Go-Back-N ARQ](#practical-81-go-back-n-arq)
9. [Practical 8.2: Selective Repeat ARQ](#practical-82-selective-repeat-arq)
10. [Practical 9.1: Leaky Bucket Algorithm](#practical-91-leaky-bucket-algorithm)
11. [Practical 9.2: Token Bucket Algorithm](#practical-92-token-bucket-algorithm)
12. [Practical 10: Distance Vector Routing](#practical-10-distance-vector-routing)

***

## Practical 1: Networking Devices, Topologies & Troubleshooting

**Objective:** Understand fundamental networking devices, network topologies, and basic troubleshooting commands.

### Part A: Networking Devices

- **Router**: Connects different networks, assigns IPs, acts as a gateway and firewall.
- **Switch**: Connects devices in a LAN, forwards by MAC, smarter than a hub.
- **Hub**: Broadcasts data to all ports, no filtering, legacy device.
- **Modem**: Converts digital ↔ analog for ISP connectivity.
- **Access Point (AP)**: Adds Wi-Fi, extends wired network.
- **Network Interface Card (NIC)**: Wired or wireless, enables network connection.
- **Bridge**: Connects/separates LAN segments, filters by MAC.
- **Gateway**: Protocol translator connecting different networks.
- **Repeater**: Amplifies signals to extend network range.
- **Firewall**: Security filter for network traffic, hardware or software.
- **Brouter**: Combines bridging and routing, hybrid device.

### Part B: Network Topologies

- **Bus**: Single backbone cable, easy, cheap, but one fault brings the network down.
- **Star**: Devices via a central hub/switch. Central device is critical.
- **Ring**: Circular path, each device connects to two others; faults break loop.
- **Mesh**: Direct links between all (full/partial), high reliability, costly.
- **Tree**: Hierarchical, scalable, backbone is a single point of failure.
- **Hybrid**: Blend of topologies, flexible but complex and costly.

### Part C: Basic Network Troubleshooting Commands

- `ping [address]` - Tests connectivity, response, loss.
- `ipconfig` (Windows) / `ifconfig` (Linux/macOS) - Shows/configures interfaces.
- `tracert` (Win) / `traceroute` (Linux/macOS) - Path/hop check.
- `nslookup [domain]` - DNS lookup.
- `route print` (Win) / `route -n` (Linux) - Routing table view.

#### Exercises

- Identify all networking devices in your lab/home.
- Map out the topology and analyze pros/cons.
- Practice troubleshooting: connectivity, path, and DNS.
- Draw and document your network, label all devices.

#### Learning Outcomes

- Understanding of core networking devices and topology pros/cons.
- Mastery of basic troubleshooting.
- Ability to document and diagnose network issues.

***

## Practical 2: TCP Client

**Objective:** Implement a TCP client for file transfer.

**Description:** Connects to the server and transfers files reliably over TCP.

**Key Features:**
- Socket creation and connection
- File transfer
- Network error handling

**Usage:**
```bash
gcc "PRACTICAL 2 TCP CLIENT.c" -o tcp_client
./tcp_client <filename>
```
**Port:** 10146

***

## Practical 3: TCP Server

**Objective:** Implement a TCP server that receives files.

**Key Features:**
- Listens for client connections
- File storage from clients
- Supports concurrent clients

**Usage:**
```bash
gcc "PRACTICAL 3 TCP SERVER.c" -o tcp_server
./tcp_server
```
**Port:** 10035

***

## Practical 4: UDP Client

**Objective:** UDP client for connectionless file transfer.

**Key Features:**
- UDP socket communication
- File transfer by datagram

**Usage:**
```bash
gcc "PRACTICAL 4 UDP CLIENT.c" -o udp_client
./udp_client
```
**Port:** 9146

***

## Practical 5: UDP Server

**Objective:** UDP server to receive files.

**Key Features:**
- UDP socket handle
- Packet reception & file reconstruct

**Usage:**
```bash
gcc "PRACTICAL 5 UDP SERVER.c" -o udp_server
./udp_server
```
**Port:** 9146

***

## Practical 6: DNS Packet Analysis

**Objective:** Analyze DNS packets using CLI tools and Wireshark.

**Key Tools:**
- Windows/Linux terminal
- nslookup
- Wireshark

**Key Concepts:**
- Query/response, A & MX records, UDP port 53

**Commands:**
```bash
nslookup www.example.com
nslookup -query=MX example.com
```

***

## Practical 7: DNS and HTTP Analysis

**Objective:** Analyze DNS and HTTP protocol packets in Wireshark.

**Tools:**
- Wireshark
- Browser
- Command line

**What to Observe:**
- DNS queries, transaction IDs, record types
- HTTP methods, status codes, headers

***

## Practical 8.1: Go-Back-N ARQ

**Objective:** Simulate the Go-Back-N ARQ error control protocol.

**Key Points:**
- Sliding window, cumulative ACK
- Retransmits window on error
- Sequence number control

**Usage:**
```bash
gcc "PRACTICAL8.1 Go-Back-N ARQ.c" -o gobackn
./gobackn
```

***

## Practical 8.2: Selective Repeat ARQ

**Objective:** Simulate Selective Repeat ARQ.

**Key Points:**
- Independent frame ACKs
- Selective retransmission
- Higher efficiency than Go-Back-N

**Usage:**
```bash
gcc "PRACTICAL 8.2 Selective Repeat ARQ.c" -o selective_repeat
./selective_repeat
```

***

## Practical 9.1: Leaky Bucket Algorithm

**Objective:** Traffic shaping with leaky bucket algorithm.

**Key Points:**
- Constant output, smooths bursts
- Overflow handling & packet loss

**Usage:**
```bash
gcc "PRACTICAL 9_1 Leaky Bucket.c" -o leaky_bucket
./leaky_bucket
```

***

## Practical 9.2: Token Bucket Algorithm

**Objective:** Traffic shaping with token bucket for burst traffic.

**Key Points:**
- Token-based transmission control
- Allows bursts, flexible rate control

**Usage:**
```bash
gcc "PRACTICAL 9_2 Token Bucket.c" -o token_bucket
./token_bucket
```

***

## Practical 10: Distance Vector Routing

**Objective:** Implement Distance Vector Routing (Bellman-Ford).

**Key Points:**
- Iterative routing table creation
- Next-hop determination, cost matrix input

**Usage:**
```bash
gcc "PRACTICAL 10 Distance Vector Algorithm.c" -o distance_vector
./distance_vector
```
**Algorithm:**
- $$ D(x,y) = \min \{ c(x,v) + D(v,y) \} $$
- Supports infinity blocks (use 999 for no link)

***

## Prerequisites

- GCC compiler
- C programming basics
- Linux/Unix or Windows (MinGW)
- Wireshark (for analysis)
- Admin privileges, Internet (where needed)

***

## Compilation Instructions

**Linux/Unix:**
```bash
gcc <source_file> -o <output_name>
./<output_name>
```
**Windows (MinGW):**
```bash
gcc <source_file> -o <output_name>.exe -lws2_32
<output_name>.exe
```

***

## Important Notes

- TCP is reliable; UDP is faster but not reliable.
- Ensure client and server port numbers match.
- Firewall and admin/root privileges may be required for network programs.
- Leaky bucket smooths rate; token bucket allows bursts.
- Watch for count-to-infinity in distance vector routing.

***

## Troubleshooting

- Server not reachable? Check firewall, port, and ensure server is running.
- Compilation errors? Link socket libraries, use proper headers, check OS compatibility.
- Wireshark issues? Run as administrator, select the right network interface.

***

## References

- Computer Networks by Andrew S. Tanenbaum
- TCP/IP Protocol Suite by Behrouz A. Forouzan
- Unix Network Programming by W. Richard Stevens
- Wireshark User Guide

***

## License

These practicals are for educational purposes only.

[1](https://people.iitism.ac.in/~download/lab%20manuals/cse/CSC307.pdf)
[2](https://stannescet.ac.in/cms/staff/qbank/CSE/Lab_Manual/CS8581-NETWORKS%20LABORATORY-138238095-CS8581CN%20%20LAB%20MANUAL.pdf)
[3](https://www.cittumkur.org/wp-content/uploads/2023/10/CN-LAB-Manual-for-PRINT.pdf)
[4](https://sjce.ac.in/wp-content/uploads/2018/01/CCNA-lab-Manual.pdf)
[5](https://www.scribd.com/document/809652140/CN-LAB-MANUAL-TEMPLATE-203105256)
[6](https://mrcet.com/pdf/Lab%20Manuals/CSE/COMPUTER%20NETWORKS%20LAB.pdf)
[7](https://sircrrengg.ac.in/images/newsletter/ITMATERIALS/CNLab.pdf)
[8](https://github.com/AbhishekMali21/COMPUTER-NETWORK-LABORATORY)
[9](https://cdlsiet.ac.in/wp-content/uploads/2022/08/Computer-Networks-Lab-Manual.pdf)
[10](https://bca.klesnc.edu.in/wp-content/uploads/2024/07/Computer-Network-Lab-Manual.pdf)
[11](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/144592492/01711ec9-370a-40a1-a26f-f916aa062b43/README.md)