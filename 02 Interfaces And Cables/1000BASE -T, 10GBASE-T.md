---
tags:
  - ccna
  - networking
  - cabling
aliases:
  - 1000BASE-T
  - 10GBASE-T
  - Gigabit Ethernet
---

# ⚡ 1000BASE-T & 10GBASE-T

> [!abstract] In one line
> Gigabit and 10-Gigabit copper Ethernet use **all four pairs (8 wires)**, and each pair is **bidirectional** — carrying data in both directions.

## 🔌 All Pairs Used

For **1000BASE-T** and **10GBASE-T**, **all 8 wires** are used. The last two pairs are **4 & 5** and **7 & 8**.

| Pair | Pins |
| --- | --- |
| Pair 1 | 1 & 2 |
| Pair 2 | 3 & 6 |
| Pair 3 | 4 & 5 |
| Pair 4 | 7 & 8 |

![[Pasted image 20261114150848.png]]

## 🔄 Bidirectional Pairs

The big difference from 10BASE-T and 100BASE-T is that in 1000BASE-T and 10GBASE-T, **each pair is bidirectional**.

- No pair is dedicated only to **transmitting** or only to **receiving**.
- Each pair can carry data in **both directions**.
- This is part of the reason these standards can operate at **much faster speeds**.

## ⚖️ 10/100 vs 1000/10G

| Feature | 10BASE-T & 100BASE-T | 1000BASE-T & 10GBASE-T |
| --- | --- | --- |
| **Pairs used** | 2 | 4 |
| **Wires used** | 4 | 8 |
| **Direction** | Dedicated Tx and Rx pairs | Each pair is **bidirectional** |
| **Speed** | 10 / 100 Mbps | 1 / 10 Gbps |

> [!success] Key takeaway
> Higher-speed copper Ethernet uses **all four pairs**, with **bidirectional** signalling on each pair, enabling **1 Gbps** and **10 Gbps** over twisted pair.

---

### 🔗 Related Notes
[[Interfaces And Cables]] · [[Ethernet Standards (copper)]] · [[UTP Cable]] · [[10BASE-T, 100BASE-T]] · [[Straight-through cable]] · [[Auto MDIX]]
