---
tags:
  - ccna
  - networking
  - gns3
  - wireshark
  - tools
aliases:
  - GNS3
  - GNS3 Simulation
  - Packet Tracer vs GNS3
---

# 🧪 GNS3, Packet Tracer & Wireshark

> [!abstract] In one line
> **GNS3 runs real Cisco IOS virtually** while **Packet Tracer simulates** a network; GNS3's Wireshark integration lets you inspect the exact frames passing between devices.

![[Pasted image 20261127150629.png]]

## 🖥️ Packet Tracer vs GNS3

| | **Packet Tracer** | **GNS3** |
| --- | --- | --- |
| What it is | A **network simulator** — software designed to **simulate** the operation of a real network | Runs **actual Cisco IOS software** — real Cisco switches running virtually |
| Cost | **Free** | Software is free, but you must **purchase your own copies of Cisco IOS** |
| Role in this course | Used for the lab videos — free and covers almost everything needed for the CCNA | Shown occasionally; useful later as you progress in your networking studies |

> [!info] Availability
> GNS3 can be downloaded at **gns3.com**. No need to use it right now unless you want to try it out — **Packet Tracer is enough for CCNA practice**.

![[Pasted image 20261127150837.png]]

## 🔍 The Magnifying Glass — GNS3 + Wireshark

GNS3 integrates with **Wireshark**, used here to analyse exactly what traffic passes between **PC1 and SW1**. This leads into the packet capture analysis in [[Wireshark packet capture]].

## 🔁 Ping from PC1 to PC3 — Full Recap

1. **PC1 does not know the destination MAC address**, so it must send an **ARP request**.
2. The ARP request is sent to **all other hosts** on the network (broadcast).
3. **PC3 responds** because its IP address matches the destination IP in the ARP request.
4. PC1 learns PC3's MAC, adds it to its **ARP table**, and uses it as the **destination MAC** of the ping it wants to send.

> [!tip] Tools and concepts
> The traffic flow is identical to the earlier ARP walkthrough — only the **tool** changes. GNS3 + Wireshark make the invisible frames visible.

> [!success] Key takeaway
> Packet Tracer **simulates**; GNS3 runs **real IOS** (IOS licence not included). GNS3's Wireshark integration captures the ARP → ICMP exchange end to end.

---

### 🧭 Learning Path
← Previous: [[ARP Table]] · Up: [[Ethernet LAN Switching 2]] · Next → [[Ping]]

### 🔗 Related Notes
[[Ethernet LAN Switching 2]] · [[Ping]] · [[Wireshark packet capture]] · [[ARP]] · [[ARP Request]] · [[ARP Reply]]
