---
tags:
  - ccna
  - networking
  - tcpip
  - layers
aliases:
  - Local Network Layer
  - Layer 2
  - Data Link Layer
---

# 🏠 Local Network Layer (Layer 2)

> [!abstract] In one line
> The **Local Network layer** provides hop-to-hop delivery on a local network using **MAC addresses**.

## 🎯 Role of Layer 2

Layer 2 moves a message from one device to the next device on the same local network.

> [!info] What is a hop?
> A **hop** is one step along the path from source to destination.

![[Pasted image 20261122135850.png]]

## 🛣️ Hops in the Example Network

| Hop | From → To |
| --- | --- |
| 1 | PC1 → R1 |
| 2 | R1 → R2 |
| 3 | R2 → SRV1 |

> [!warning] Switches do not count as hops
> A **switch** connects devices to the same local network. It extends the LAN but does not count as a hop. The diagram shows one host per switch to keep things simple, but a switch can connect many devices to the same LAN.

## 🆔 MAC Addresses

Layer 2 uses **MAC — Media Access Control — addresses** to identify interfaces.

- Every LAN interface has a unique MAC address.
- Routers with multiple interfaces have multiple MAC addresses.
- In the diagram, router interfaces are labelled **G1** and **G2** — short for GigabitEthernet1 and GigabitEthernet2, meaning they operate at **1 Gbps**.
- PC1 sends the frame to the MAC address of R1's G1 interface.
- R1 sends the frame to the MAC address of R2's G1 interface.
- R2 sends the frame to the MAC address of SRV1's interface.

> [!tip] Exam focus
> Layer 3 IP address = final destination host. Layer 2 MAC address = next hop on the local network.

## 🧱 Main Layer 2 Protocols

| Protocol | Use |
| --- | --- |
| **Ethernet** | Wired LANs |
| **Wi-Fi** | Wireless LANs |

Other Layer 2 protocols exist, but Ethernet and Wi-Fi are by far the most common today.

## 🧠 Quick Recap

| Topic | Fact |
| --- | --- |
| **Layer number** | 2 |
| **Main job** | Hop-to-hop delivery on a local network |
| **Addressing** | MAC addresses |
| **Main devices** | Switches, NICs |
| **Examples** | Ethernet, Wi-Fi |

> [!success] Key takeaway
> Layer 2 uses MAC addresses to deliver a frame to the next hop, while Layer 3 uses IP addresses to identify the final destination.

---

### 🧭 Learning Path
← Previous: [[Local 3 Internet Layer]] · Up: [[TCP IP]] · Next → [[Layer 1 Physical Layer]]

### 🔗 Related Notes
[[TCP IP]] · [[The TCP IP Model]] · [[Local 3 Internet Layer]] · [[Layer 1 Physical Layer]] · [[Ethernet]] · [[Interfaces And Cables]]
