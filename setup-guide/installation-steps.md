# Network Traffic Analysis Lab Setup Guide

This guide explains how to recreate the network traffic analysis lab environment using Mininet and Wireshark.

---

# Lab Environment

The lab was created using the following tools:

- Ubuntu Linux
- Mininet
- Open vSwitch
- Wireshark
- Python HTTP Server
- iperf

---

# Step 1 — Install Mininet

Update system packages:

```

sudo apt update
sudo apt upgrade

```

Install Mininet:

```

sudo apt install mininet

```

Verify installation:

```

sudo mn --test pingall

```

---

# Step 2 — Start Mininet Topology

Create a linear topology with four hosts:

```

sudo mn --topo=linear,4 --switch ovsk --link=tc,bw=6,delay=14ms,loss=2

```

This configuration creates:

- 4 hosts
- Open vSwitch switches
- Links with bandwidth, delay, and packet loss parameters

---

# Step 3 — Test Network Connectivity

Verify communication between hosts:

```

pingall

```

This command sends ICMP packets between all hosts in the network.

---

# Step 4 — Measure Delay and Packet Loss

Run ping between hosts:

```

h1 ping h4

```

This measures:

- round-trip latency
- packet loss

---

# Step 5 — Start HTTP Server

Start a simple HTTP server on host **h2**:

```

h2 python3 -m http.server 80

```

---

# Step 6 — Access HTTP Server

From another host:

```

h3 wget [http://10.0.0.2](http://10.0.0.2)

```

This generates HTTP traffic in the network.

---

# Step 7 — Capture Traffic Using Wireshark

Start Wireshark:

```

sudo wireshark

```

Select the network interface connected to the Mininet host and apply filters such as:

```

icmp
http
tcp

```

This allows monitoring of captured packets.

---

# Step 8 — Generate TCP Traffic

Open xterm terminals for hosts:

```

xterm h2 h4

```

Start iperf server on host h2:

```

iperf -s

```

Generate TCP traffic from host h4:

```

iperf -c 10.0.0.2

```

---

# Step 9 — Generate UDP Traffic

Run UDP traffic test:

```

iperf -c 10.0.0.2 -u

```

This allows comparison between TCP and UDP performance.

---

# Lab Cleanup

Stop Mininet and clean processes:

```

sudo mn -c

```

---

# Outcome

By completing this lab you will learn:

- network traffic generation
- packet capture and inspection
- network performance testing
- protocol analysis using Wireshark
```

---

