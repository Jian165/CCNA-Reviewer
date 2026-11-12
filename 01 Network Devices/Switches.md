---
tags:
  - ccna
  - networking
  - device
aliases:
  - Switch
  - Switches
---

# 🔀 Switch

> [!abstract] In one line
> Switches forward traffic **within a LAN** (Local Area Network), connecting end hosts such as PCs and servers.

## 🖧 Where Switches Fit In

Imagine an Enterprise with a branch in **New York** and another in **Tokyo**. Real branches have far more than a couple of PCs and servers, but the idea is the same.

End hosts like PCs and servers are not usually connected directly to each other. Instead, their connections are **aggregated** into a device called a **switch**.

![[Pasted image 20261111140135.png]]

The two PCs connect to **SW1**, and the two servers connect to **SW2**. Switches have lots of interfaces — or ports — for plugging in end hosts, usually **24 or more**.

PC1 and PC2, plus other devices plugged into SW1 (such as a network printer or another PC), all reside on the **same local area network**. The same goes for devices connected to SW2 in the Tokyo branch.

![[Pasted image 20261111140605.png]]

> [!warning] Important
> Switches **cannot** connect directly to the Internet or send data between the two LANs.

## ⚙️ Characteristics of Switches

| Characteristic | Detail |
| --- | --- |
| **Interfaces** | Many ports for end hosts — usually 24 or more |
| **Connectivity** | Provides connectivity to hosts within the **same LAN** |
| **Limitation** | Does **not** provide connectivity between LANs or over the Internet |

> [!success] Key takeaway
> To connect separate LANs or reach the Internet, a switch needs another device — a [[Router]].

---

### 🔗 Related Notes
[[Network]] · [[Router]] · [[Firewall]] · [[Interfaces And Cables]]
