# Network Traffic Analysis Lab (Mininet + Wireshark)

This project demonstrates how network traffic can be generated, captured, and analyzed using Mininet and Wireshark.

The goal of this lab is to understand network communication, monitor packets, and analyze network performance through packet inspection and traffic generation.

---

# Lab Environment

The lab was built using a virtual network environment.

Components:

- Mininet emulator
- Open vSwitch
- Wireshark packet analyzer
- Linux terminal
- iperf traffic generator

---

# Network Topology

A linear topology with multiple hosts and switches was created using Mininet.

Each link was configured with:

- 6 Mbps bandwidth
- 14 ms delay
- 2% packet loss

Screenshot:

![Topology](screenshots/topology-creation.png)

---

# Connectivity Testing

Connectivity between hosts was verified using the `pingall` command in Mininet.

This command sends ICMP packets between all hosts to ensure network connectivity.

Screenshot:

![Connectivity](screenshots/connectivity-test.png)

---

# Network Delay & Packet Loss

Packet delay and packet loss were measured using ICMP ping between hosts.

This test helps analyze network performance and reliability.

Screenshot:

![Delay Test](screenshots/delay-packetloss.png)

---

# HTTP Traffic Analysis

A simple HTTP server was started on one host while another host accessed the webpage.

This generated HTTP traffic which was captured using Wireshark.

Screenshot:

![HTTP Server](screenshots/http-server.png)

---

# Packet Capture with Wireshark

Wireshark was used to capture network packets on the interface connected to the host.

Packet filters were applied to analyze specific traffic.

Screenshot:

![Wireshark](screenshots/wireshark-capture.png)

---

# TCP Traffic Analysis

TCP traffic was generated using iperf between two hosts.

This allowed measurement of network throughput and TCP performance.

Screenshot:

![TCP Traffic](screenshots/tcp-throughput.png)

---

# UDP Traffic Analysis

UDP traffic was also generated using iperf to observe differences between TCP and UDP performance.

Screenshot:

![UDP Traffic](screenshots/udp-throughput.png)

---

# Key Skills Demonstrated

- Network traffic analysis
- Packet capture using Wireshark
- Network emulation using Mininet
- TCP/UDP throughput testing
- HTTP traffic monitoring
- ICMP packet analysis

---

# Tools Used

| Tool | Purpose |
|-----|------|
| Mininet | Network emulation |
| Open vSwitch | Virtual switching |
| Wireshark | Packet capture and analysis |
| iperf | Network throughput testing |
| Linux | Network commands |

---

# Learning Outcomes

Through this lab, the following skills were developed:

- Understanding packet-level network communication
- Capturing and analyzing traffic using Wireshark
- Generating network traffic using iperf
- Measuring network performance
- Investigating network behavior

---

# Repository Structure

Network-Traffic-Analysis-Lab
│
├── README.md
├── screenshots
│ ├── topology-creation.png
│ ├── connectivity-test.png
│ ├── delay-packetloss.png
│ ├── http-server.png
│ ├── wireshark-capture.png
│ ├── tcp-throughput.png
│ └── udp-throughput.png

Network-Traffic-Analysis-Lab
│
├── README.md
├── screenshots
│ ├── topology-creation.png
│ ├── connectivity-test.png
│ ├── delay-packetloss.png
│ ├── http-server.png
│ ├── wireshark-capture.png
│ ├── tcp-throughput.png
│ └── udp-throughput.png

---
