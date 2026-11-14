---
tags:
  - ccna
  - networking
  - cabling
aliases:
  - Crossover Cable
  - Cross Over Cable
---

# 🔀 Crossover Cable

> [!abstract] In one line
> A **crossover** cable connects **like** devices by reversing the transmit and receive pairs: pin 1 → pin 3, pin 2 → pin 6, pin 3 → pin 1, and pin 6 → pin 2.

## ❌ Why a Straight-Through Cable Fails

Networks don't always connect PC to switch or switch to router. Sometimes we need:

- **Router to router**
- **Switch to switch**
- **PC to PC**

If the device on the left sends data to the device on the right, it simply **does not work** — the right device is not prepared to **receive** on pins **1 & 2**.

![[Pasted image 20261114145418.png]]

The same problem applies to **two switches**: if the left switch transmits to the right switch, communication fails.

![[Pasted image 20261114145709.png]]

## 🔄 How a Crossover Cable Works

In a **straight-through** cable, pin 1 connects to pin 1, pin 2 to pin 2, and so on. In a **crossover** cable, a pin on one end **does not** connect to the same pin on the other end — the pairs are **reversed**.

| One End | Other End |
| --- | --- |
| Pin **1** | Pin **3** |
| Pin **2** | Pin **6** |
| Pin **3** | Pin **1** |
| Pin **6** | Pin **2** |

The two pairs — **1&2** and **3&6** — are reversed on each end, so the wires are "crossed over", hence the name **crossover cable**.

![[Pasted image 20261114145841.png]]

> [!important] Why it works
> The **transmit** pins on one side connect to the **receive** pins on the other side, so both devices can send data to each other without problems.

## ⚖️ Straight-Through vs Crossover

| Cable | Wiring | Connects |
| --- | --- | --- |
| **Straight-through** | 1→1, 2→2, 3→3, 6→6 | **Unlike** devices |
| **Crossover** | 1→3, 2→6, 3→1, 6→2 | **Like** devices |

## ✅ When to Use It

| Connection | Cable |
| --- | --- |
| Router ↔ router | **Crossover** |
| Switch ↔ switch | **Crossover** |
| PC ↔ PC | **Crossover** |

> [!success] Key takeaway
> Use a **crossover** cable between **like** devices because both use the **same** transmit/receive pins, so the cable must reverse pairs **1&2** with **3&6**.

---

### 🔗 Related Notes
[[Interfaces And Cables]] · [[Straight-through cable]] · [[Auto MDIX]] · [[10BASE-T, 100BASE-T]] · [[UTP Cable]]
