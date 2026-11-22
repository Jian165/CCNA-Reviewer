---
tags:
  - ccna
  - networking
  - tcpip
  - layers
aliases:
  - Internet Layer
  - Layer 3
  - Network Layer
---

# 🌍 Internet Layer (Layer 3)

> [!abstract] In one line
> The **Internet layer** provides end-to-end delivery between hosts across multiple networks using **IP addresses**.

## 🎯 Role of Layer 3

Layer 3 gets a message from the source host to the final destination host, even when many networks and routers are in between.

> [!tip] Meaning of “Internet”
> Here, **Internet** means **internetwork** — multiple networks connected together. It does not only mean the public Internet.

![[Pasted image 20261122140050.png]]

## 📮 IP Addresses

An **IP address** identifies a host on a network.

| Example | Meaning |
| --- | --- |
| **10.1.1.1** | The IP address of SRV1 |
| Source IP | The host that sent the message |
| Destination IP | The final host that should receive it |

> [!important] Host-to-host delivery
> Layer 3 answers: **Which host should receive this message?** It does not choose the application process — that is Layer 4. An IP address is like a home address: it identifies the final destination host, and routers use it to forward the message toward that host.

## 🛣️ Routers Work Here

Routers operate mainly at Layer 3.

- They read the destination IP address.
- They forward the message toward the final destination.
- They do not need to know which application process will receive it.

## 🧱 Main Internet Layer Protocols

There are two IP versions in use today — **IPv4** and **IPv6** — and both are important CCNA topics.

| Protocol | Full name |
| --- | --- |
| **IPv4** | Internet Protocol version 4 |
| **IPv6** | Internet Protocol version 6 |
| **ICMP** | Internet Control Message Protocol |

## 🧠 Quick Recap

| Topic | Fact |
| --- | --- |
| **Layer number** | 3 |
| **Main job** | End-to-end delivery between hosts |
| **Addressing** | IP addresses |
| **Main device** | Router |
| **Examples** | IPv4, IPv6, ICMP |

> [!success] Key takeaway
> Layer 3 uses IP addresses and routers to deliver messages from one host to another across multiple networks.

---

### 🧭 Learning Path
← Previous: [[Layer 4 Transport Layer]] · Up: [[TCP IP]] · Next → [[Local 2 Network Layer]]

### 🔗 Related Notes
[[TCP IP]] · [[The TCP IP Model]] · [[Layer 4 Transport Layer]] · [[Local 2 Network Layer]] · [[Adjacent-layer interaction]]
