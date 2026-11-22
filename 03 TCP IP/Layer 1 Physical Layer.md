---
tags:
  - ccna
  - networking
  - tcpip
  - layers
aliases:
  - Physical Layer
  - Layer 1
---

# ⚡ Physical Layer (Layer 1)

> [!abstract] In one line
> The **Physical layer** sends and receives bits as electrical, optical, or radio signals over the physical medium.

## 🎯 Role of Layer 1

Layer 1 handles the physical part of communication: the actual signals that carry bits between devices.

> [!important] Bits, not messages
> Layer 1 does not interpret the message. It sends and receives the **bits** that represent the message. The low-level electrical and optical engineering is complex, but network engineers usually do not need those details.

![[Pasted image 20261122135618.png]]

## 🧰 What Layer 1 Defines

| Item | Examples |
| --- | --- |
| **Cables and connectors** | UTP, fiber-optic cable, RJ-45, SFP |
| **Signals** | Electrical, optical, radio |
| **Signal levels** | How bits are represented as signals |
| **Link speeds** | 100 Mbps, 1 Gbps, 10 Gbps |

## 🌐 Physical Media Examples

| Medium | Signal type | Related note |
| --- | --- | --- |
| Copper UTP | Electrical | [[UTP Cable]] |
| Fiber optic | Optical/light | [[Fiber Optic Connections]] |
| Wi-Fi | Radio | Wireless LANs |

## 🖧 NICs and Transceivers

Each network interface has a **NIC — network interface card** inside the device.

- A NIC sends and receives signals.
- Fiber connections use transceivers such as SFPs.
- Network engineers usually do not need to know the low-level electrical or optical engineering.

> [!tip] Course design
> In some models this layer is combined with the next layer. This course separates **physical concerns** in Layer 1 — cables, connectors, signals, and speeds — from **logical LAN delivery** in Layer 2.

## 🧠 Quick Recap

| Topic | Fact |
| --- | --- |
| **Layer number** | 1 |
| **Main job** | Send and receive bits as signals |
| **Addressing** | None |
| **Examples** | UTP, fiber, Wi-Fi radios, NICs |
| **Data unit** | Bits |

> [!success] Key takeaway
> Layer 1 turns bits into signals and sends them over the physical medium; it does not understand addresses or application data.

---

### 🧭 Learning Path
← Previous: [[Local 2 Network Layer]] · Up: [[TCP IP]] · Next → [[Separation of Layers]]

### 🔗 Related Notes
[[TCP IP]] · [[The TCP IP Model]] · [[Local 2 Network Layer]] · [[UTP Cable]] · [[Fiber Optic Connections]] · [[Interfaces And Cables]]
