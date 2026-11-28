---
tags:
  - ccna
  - networking
  - ethernet
  - mac
  - addressing
aliases:
  - MAC Address
  - Media Access Control Address
  - BIA
  - Burned-In Address
---

# 🆔 MAC Addresses

> [!abstract] In one line
> A **MAC address** is a **6-byte / 48-bit physical address** assigned to a device when it is made — also called a **burned-in address (BIA)**.

![[Pasted image 20261125151440.png]]

## 🏷️ Physical, Not Configured

- A MAC address is a **physical address** assigned during manufacturing.
- An **IP address** is a **logical address** that you assign in the CLI when configuring the device.
- Because the MAC address is "burned in" at the factory, it is also called a **BIA — Burned-In Address**.

## 🌐 Uniqueness

| Statement | Detail |
| --- | --- |
| **Globally unique** | No two devices in the world should have the same MAC address |
| **Locally unique exception** | Some MAC addresses are **locally unique** and do not have to be globally unique |
| **Exam reality** | In almost all cases, MAC addresses are **globally unique** |

## 🧩 Structure: OUI + Device ID

| Portion | Size | Meaning |
| --- | --- | --- |
| **First 3 bytes** | 24 bits | **OUI — Organizationally Unique Identifier**, assigned to the manufacturer |
| **Last 3 bytes** | 24 bits | Unique to the device itself |

Cisco, for example, has various OUIs that only Cisco can use. Other manufacturers have their own OUIs.

> [!important] Exam point
> The **OUI identifies the maker**; the second half identifies the individual device. The OUI alone does **not** identify one specific host.

## 🔢 Written in Hexadecimal

A MAC address is written as **12 hexadecimal characters**.

| Style | Example | Note |
| --- | --- | --- |
| Every 2 digits | `AA.AA.AA.00.00.01` | Also seen in the wild |
| Every 4 digits | `AAAA.AA00.0001` | The style used in these notes |

## 🖥️ Example Topology

![[Pasted image 20261125152011.png]]

| Item | Detail |
| --- | --- |
| **Switch interfaces** | `F0/1`, `F0/2`, `F0/3` |
| **F means** | **FastEthernet** — **100 Mbps** interfaces |
| **MAC addresses shown** | Simplified for the demonstration; real ones will look different |
| **OUI** | `AAAAAA` for every PC → same manufacturer |
| **Device portion** | Last 3 bytes differ for each PC (`000001`, `000002`, `000003`) |
| **Next step** | PC1 wants to send data to PC2 |

> [!success] Key takeaway
> A MAC address is a **48-bit burned-in physical address**. Its first 3 bytes are the manufacturer's **OUI**; its last 3 bytes identify the device. Switches use these addresses at Layer 2.

---

### 🧭 Learning Path
← Previous: [[Ethernet Frame]] · Up: [[Ethernet LAN Switching]] · Next → [[Decimal Number System]]

### 🔗 Related Notes
[[Ethernet LAN Switching]] · [[Ethernet Frame]] · [[Decimal Number System]] · [[Hexadecimal Number System]] · [[CCNA/05 Ethernet LAN Switching  1/MAC Address Table]] · [[Local 2 Network Layer]]
