---
tags:
  - ccna
  - networking
  - cabling
aliases:
  - 10BASE-T
  - 100BASE-T
  - Ethernet and Fast Ethernet
---

# 🔀 10BASE-T & 100BASE-T

> [!abstract] In one line
> **10BASE-T** (Ethernet) and **100BASE-T** (Fast Ethernet) use only **2 pairs (4 wires)** — pins **1&2** and **3&6** — and run **full-duplex**.

## 🔌 Pin Usage

![[Pasted image 20261114144340.png]]

These pin numbers represent the pins on the **RJ-45** connector, on both the PC's network interface card (NIC) and the switch's interface. Although there are **8 pins**, only **4 wires (2 pairs)** are used for 10BASE-T and 100BASE-T.

| Pair | Pins | Notes |
| --- | --- | --- |
| Pair 1 | **1 & 2** | One direction |
| Pair 2 | **3 & 6** | Opposite direction |

> [!warning] Remember
> The second pair is **3 and 6** — **not** 3 and 4.

In a UTP cable these pairs are **twisted together**, so the wires drawn straight in a diagram are physically twisted in the real cable.

## 🔄 Transmit and Receive

- The **PC** transmits (Tx) on pins **1 & 2**.
- The **switch** receives (Rx) on pins **1 & 2**.
- The **switch** transmits (Tx) on pins **3 & 6**.
- The **PC** receives (Rx) on pins **3 & 6**.

> [!important] Full-duplex
> Because each device transmits and receives on **separate wires**, both can send data at the **same time**. This is **full-duplex** transmission, and it avoids **collisions**.

## 📌 Pin Roles by Device

![[Pasted image 20261114150030.png]]

| Device | Transmits On | Receives On |
| --- | --- | --- |
| **Router** | 1 & 2 | 3 & 6 |
| **Firewall** | 1 & 2 | 3 & 6 |
| **PC** | 1 & 2 | 3 & 6 |
| **Switch** | 3 & 6 | 1 & 2 |

> [!tip] Memory hook
> Everything except a **switch** transmits on **1 & 2**. The switch is the odd one out — it transmits on **3 & 6**.

> [!success] Key takeaway
> 10BASE-T and 100BASE-T use **2 pairs (4 wires)** and **full-duplex**, with PCs/routers/firewalls transmitting on **1&2** and switches transmitting on **3&6**.

---

### 🧭 Learning Path
← Previous: [[UTP Cable]] · Up: [[Interfaces And Cables]] · Next → [[1000BASE -T, 10GBASE-T]]

### 🔗 Related Notes
[[Interfaces And Cables]] · [[Ethernet Standards (copper)]] · [[UTP Cable]] · [[1000BASE -T, 10GBASE-T]] · [[Straight-through cable]] · [[Cross Over Cable]]
