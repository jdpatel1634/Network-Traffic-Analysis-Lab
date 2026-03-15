
# Network Traffic Analysis Report

## Overview

This analysis was performed to investigate network traffic generated in a Mininet virtual network environment. The objective was to capture and analyze packets using Wireshark while generating different types of network traffic including ICMP, HTTP, TCP, and UDP.

The lab environment simulated a small network with multiple hosts and switches to observe packet flow and network performance.

---

# Network Topology

The network topology consisted of multiple hosts connected through Open vSwitch switches within the Mininet emulator.

Each link was configured with the following parameters:

- Bandwidth: 6 Mbps
- Delay: 14 ms
- Packet Loss: 2%

This configuration allowed testing network performance under constrained network conditions.

---

# Connectivity Testing

Connectivity between hosts was verified using the following command:

```

pingall

```

This command sends ICMP echo requests between all hosts in the topology.

Results showed that communication between hosts was successful, although some packet loss occurred due to the configured network conditions.

Observed results:

- 16% packet loss
- Successful ICMP communication between hosts

This confirms that the network topology was correctly configured.

---

# Network Delay and Packet Loss Analysis

To further analyze network performance, ICMP traffic was generated between host **h1** and **h4** using:

```

h1 ping h4

```

The results showed:

- Average delay around **149 ms**
- Packet loss approximately **33%**

This packet loss is expected due to the link configuration which introduced network delay and packet loss.

---

# HTTP Traffic Analysis

A simple HTTP server was started on host **h2** using Python.

Another host accessed the server to generate HTTP traffic.

This allowed observation of application layer traffic within the network.

Key observations:

- HTTP GET requests from the client
- HTTP responses from the server
- Packet exchange between hosts

---

# Packet Capture using Wireshark

Wireshark was used to capture packets on the network interface connected to the host.

Filters were applied to analyze specific protocols.

Examples of observed packets:

- ICMP packets during ping tests
- HTTP requests and responses
- TCP communication between hosts

Packet analysis confirmed correct packet exchange between nodes in the network.

---

# TCP Traffic Analysis

TCP traffic was generated using the following command:

```

iperf

```

This command measures network throughput between two hosts.

The results showed stable TCP communication and provided throughput statistics over time.

This helps analyze the reliability and performance of TCP connections in the network.

---

# UDP Traffic Analysis

UDP traffic was also generated using the following command:

```

iperf -u

```

UDP traffic analysis allowed observation of packet transmission without connection establishment.

Key observations:

- Higher packet transmission rate
- Some packet loss during transmission
- No retransmission since UDP is connectionless

This demonstrates the behavioral difference between TCP and UDP protocols.

---

# Security Insights

Traffic analysis helps security analysts detect suspicious activity in real networks.

Examples include:

- abnormal traffic spikes
- unauthorized connections
- suspicious packet payloads
- port scanning activity

Packet capture tools such as Wireshark are commonly used in SOC environments for investigating security incidents.

---

# Conclusion

This lab demonstrated how network traffic can be generated, captured, and analyzed using Mininet and Wireshark.

Key skills developed:

- packet capture
- traffic analysis
- network troubleshooting
- performance testing
- protocol inspection

Understanding network traffic behavior is essential for security analysts when detecting malicious activity or investigating security incidents.
```

---

