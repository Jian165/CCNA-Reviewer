---
tags:
  - ccna
  - networking
  - ethernet
  - arp
aliases:
  - Address Resolution Protocol
  - ARP
---

# 🔍 Address Resolution Protocol (ARP)

> [!abstract] In one line
> **ARP** discovers the **Layer 2 MAC address** of a known **Layer 3 IP address**, so a device can build the Ethernet frame needed to send data on the local network.

![[Pasted image 20261127144916.png]]

## 🌐 Adding IP Addresses to the Topology

The network is `192.168.1.0/24`. The short labels used in the diagram stand for these full addresses:

| Device | Short form | Full IP address |
| --- | --- | --- |
| PC1 | `.1` | `192.168.1.1` |
| PC2 | `.2` | `192.168.1.2` |
| PC3 | `.3` | `192.168.1.3` |
| PC4 | `.4` | `192.168.1.4` |

> [!info] Scope
> IP address details are not covered in this folder — they are only added here because ARP needs them to explain how PCs communicate.

## 📦 Two Addresses in Every Message

When a device sends data to another device, it does not only include a source and destination **MAC address**. Encapsulated inside the Ethernet frame is an **IP packet**, and that packet contains a source and destination **IP address**.

PC1 → PC3 example:

| Field | Value | Known? |
| --- | --- | --- |
| Source IP | `192.168.1.1` | Yes |
| Destination IP | `192.168.1.3` | Yes — entered by the user |
| Source MAC | `0C2F.B011.9D00` | Yes — PC1's own MAC |
| Destination MAC | PC3's MAC | **No — must be discovered** |

> [!important] Why ARP is needed
> When you send data you enter an **IP address**, not a MAC address. PC1 knows `192.168.1.3` but has to discover PC3's MAC address by itself. **Switches are Layer 2 devices** — they do not operate at Layer 3, so they forward using **MAC addresses, not IP addresses**.

![[Pasted image 20261127145016.png]]

## 🧾 What ARP Does

**ARP = Address Resolution Protocol.** It is used to discover the **Layer 2 address (MAC)** of a known **Layer 3 address (IP)**.

- PC1 knows PC3's Layer 3 address (`192.168.1.3`) but not its Layer 2 address (MAC).
- ARP resolves that missing piece before the original frame can be sent.

## 🔄 The Two ARP Messages

| Message | Sent by | Purpose | Frame type |
| --- | --- | --- | --- |
| **ARP Request** | The device that wants to know the other device's MAC | Asks for the MAC address | **Broadcast** — sent to all hosts on the network |
| **ARP Reply** | The device that knows the answer | Informs the requester of its MAC address | **Unicast** — sent to only one host (the requester) |

> [!tip] Broadcast vs unicast
> Because the destination's Layer 2 address is **unknown**, the request is **broadcast** to everyone and the sender waits for a reply. The reply is **unicast** because the requester's MAC is already known — it is written as the source MAC of the request.

## 🧠 Quick Recap

| Step | What happens |
| --- | --- |
| 1 | User sends data to an **IP address** (e.g. PC3 at `192.168.1.3`). |
| 2 | The Ethernet frame needs a **destination MAC**, which PC1 does not know. |
| 3 | PC1 sends an **ARP request** as a broadcast frame. |
| 4 | PC3 replies with its MAC using a **unicast ARP reply**. |
| 5 | PC1 adds the IP-to-MAC mapping to its **ARP table** and sends the original frame. |

> [!success] Key takeaway
> ARP bridges Layer 3 and Layer 2: it finds the **MAC address** for a known **IP address**. The process is always **request (broadcast) → reply (unicast)**, and switches still forward frames using MAC addresses only.

---

### 🧭 Learning Path
← Previous: [[Ethernet LAN Switching Exam]] · Up: [[Ethernet LAN Switching 2]] · Next → [[ARP Request]]

### 🔗 Related Notes
[[Ethernet LAN Switching 2]] · [[ARP Request]] · [[ARP Reply]] · [[ARP Table]] · [[Ping]] · [[Wireshark packet capture]] · [[CCNA/05 Ethernet LAN Switching  1/Ethernet Frame]]
