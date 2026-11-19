---
tags:
  - ccna
  - networking
  - cabling
aliases:
  - Straight-through
  - Straight through cable
---

# 🔌 Straight-Through Cable

> [!abstract] In one line
> A **straight-through** cable connects **unlike** devices — pin 1 on one end connects straight through to pin 1 on the other end, pin 2 to pin 2, pin 3 to pin 3, and so on.

## 🧭 Pin Wiring

![[Pasted image 20261114144908.png]]

| One End | Other End |
| --- | --- |
| Pin **1** | Pin **1** |
| Pin **2** | Pin **2** |
| Pin **3** | Pin **3** |
| Pin **6** | Pin **6** |

The cable is called **straight-through** because each pin connects straight through to the **same pin** on the other end.

## 🖥️ Why It Works: Opposite Pin Roles

A **router** transmits data on pins **1 & 2** and receives on pins **3 & 6** — the **same as a PC**. A **switch** is the opposite: it **receives** on pins **1 & 2** and **transmits** on pins **3 & 6**.

| Device | Transmits On | Receives On |
| --- | --- | --- |
| **PC** | 1 & 2 | 3 & 6 |
| **Router** | 1 & 2 | 3 & 6 |
| **Switch** | 3 & 6 | 1 & 2 |

Because the two device types transmit and receive on **opposite pin pairs**, a straight-through cable works.

> [!example] Full-duplex in action
> Ethernet uses **full-duplex** transmission, so the two devices can send data at the **same time** with no issues.

## ✅ When to Use It

| Connection | Cable |
| --- | --- |
| PC ↔ switch | **Straight-through** |
| Router ↔ switch | **Straight-through** |

> [!success] Key takeaway
> Use a **straight-through** cable between **unlike** devices — such as a **PC or router to a switch** — because their transmit and receive pins already line up.

---

### 🧭 Learning Path
← Previous: [[1000BASE -T, 10GBASE-T]] · Up: [[Interfaces And Cables]] · Next → [[Cross Over Cable]]

### 🔗 Related Notes
[[Interfaces And Cables]] · [[10BASE-T, 100BASE-T]] · [[Cross Over Cable]] · [[Auto MDIX]] · [[UTP Cable]]
