---
tags:
  - ccna
  - networking
  - tcpip
  - osi
aliases:
  - OSI Model
  - Open Systems Interconnection
  - Seven-Layer Model
---

# 🏛️ OSI Model

> [!abstract] In one line
> **OSI** is a 7-layer reference model created by the **ISO**; its protocols lost to TCP/IP, but its layer names are still widely used.

## 📜 Background

TCP/IP development began in the **1970s** with work on ARPANET and the early TCP/IP specifications.

| Item | Detail |
| --- | --- |
| **Full name** | Open Systems Interconnection |
| **Created by** | **ISO** — International Organization for Standardization |
| **When** | Late 1970s and 1980s |
| **Goal** | International, vendor-neutral networking standards that could unify proprietary stacks |
| **Also created** | A matching OSI protocol suite |
| **Result** | The model survived; the protocol suite did not become dominant |

## 🏗️ The Seven Layers

| OSI layer | Name | Simple role |
| --- | --- | --- |
| **7** | Application | Application data and protocols |
| **6** | Presentation | Format and translate data |
| **5** | Session | Manage sessions |
| **4** | Transport | Process-to-process communication |
| **3** | Network | Host-to-host delivery and routing |
| **2** | Data Link | Hop-to-hop delivery on a LAN |
| **1** | Physical | Bits as signals over the medium |

![[Pasted image 20261122141910.png]]

## ❌ Why OSI Did Not Win

| Reason | Explanation |
| --- | --- |
| **Too late** | TCP/IP was already widely used |
| **Too complex** | The full OSI protocol suite was difficult to implement |
| **Top-down design** | Committees designed protocols in detail before implementation |
| **TCP/IP was practical** | Open, simpler, and developed bottom-up |

> [!important] Key historical point
> **TCP/IP won as the real protocol stack. OSI survived as a reference model and common language.**

## ✅ Why OSI Still Matters

- Almost all modern networks use TCP/IP.
- Governments, including the US, promoted OSI as the preferred stack, and for a while many people thought OSI was the future.
- Some OSI technologies are still used.
- The **7-layer OSI model** is still used for teaching and discussion.
- Many resources use a **5-layer model** with names borrowed from OSI.
- This is why the Application layer is often called **Layer 7**.
- People commonly say **Layer 2** and **Layer 3** even in TCP/IP discussions.

## 🔁 Course Model vs OSI Names

| Course layer | Course name | OSI/common name |
| --- | --- | --- |
| **5** | Application | Layer 7 — Application |
| **4** | Transport | Layer 4 — Transport |
| **3** | Internet | Layer 3 — Network |
| **2** | Local Network | Layer 2 — Data Link |
| **1** | Physical | Layer 1 — Physical |

## 🧠 Quick Recap

| Topic | Fact |
| --- | --- |
| **OSI layers** | 7 |
| **Created by** | ISO |
| **Main goal** | Vendor-neutral standards |
| **Outcome** | TCP/IP won in deployment; OSI remains a reference model |
| **Common names** | Layer 7 Application, Layer 3 Network, Layer 2 Data Link |

> [!success] Key takeaway
> Know OSI as a 7-layer reference model and map its names to the 5-layer TCP/IP model used in this course.

---

### 🧭 Learning Path
← Previous: [[Encapsulation & decapsulation]] · Up: [[TCP IP]] · Next → [[Other Model]]

### 🔗 Related Notes
[[TCP IP]] · [[Layered models]] · [[Other Model]] · [[The TCP IP Model]] · [[Local 3 Internet Layer]] · [[Local 2 Network Layer]]
