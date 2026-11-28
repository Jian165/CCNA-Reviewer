---
tags:
  - ccna
  - networking
  - ethernet
  - switching
  - mac
  - cli
aliases:
  - MAC Address Table
  - MAC Table (Cisco IOS)
  - show mac address-table
---

# 🗂️ The MAC Address Table on a Cisco Switch

> [!abstract] In one line
> `show mac address-table` reveals the switch's learned **VLAN / MAC / type / port** entries — dynamic entries are learned from frames and **aged out after 5 minutes**.

## 🔁 Where We Left Off

If device **A** wants to send traffic to device **B** on the **same network**, A first uses **ARP** to learn B's MAC address (see [[ARP]]), and only then can it send traffic to B. Both switches in the path have also been learning MAC → port mappings from the frames they forwarded.

## 🔎 The Command

```bash
show mac address-table
```

> [!info] Command name changed between IOS versions
> **Old** Cisco IOS used `show mac-address-table` (hyphen after "mac"). **Newer** versions removed that first hyphen: **`show mac address-table`**.

![[Pasted image 20261128134332.png]]

## 📊 Reading Each Column

| Column | Meaning | Example |
| --- | --- | --- |
| **VLAN** | Virtual Local Area Network — covered later in the course. **Default is 1**. | `1` |
| **MAC Address** | The learned address — here PC1 (top) and PC3 (bottom). | `0c2f.b011.9d00` |
| **Type** | How the entry was learned. Both entries here are **dynamic** — not manually configured. | `DYNAMIC` |
| **Ports** | Another word for **interface**. | `Gi0/0`, etc. |

> [!important] Dynamic means learned, not configured
> Entries marked **dynamic** were discovered automatically from the **source MAC** of arriving frames (see [[ARP Request]] and [[ARP Reply]]). Nothing was typed into the switch to create them.

The table matches the small MAC address table drawn in the earlier topology diagram — PC1 maps to its interface, and PC3 maps to its interface.

## ⏳ Aging of Dynamic Entries

![[Pasted image 20261128134450.png]]

- Dynamic MAC addresses are removed from the table after **5 minutes** of inactivity.
- When the host sends traffic again, the switch **relearns** the MAC dynamically.

> [!tip] Where to go next
> The 5-minute aging rule leads directly into the manual removal commands in [[Clearing The MAC address Table]].

> [!success] Key takeaway
> `show mac address-table` shows **VLAN, MAC, type, and port**. The default VLAN is **1**, learned entries are **dynamic**, and they expire after **5 minutes** of no traffic.

---

### 🧭 Learning Path
← Previous: [[Ping]] · Up: [[Ethernet LAN Switching 2]] · Next → [[Clearing The MAC address Table]]

### 🔗 Related Notes
[[Ethernet LAN Switching 2]] · [[CCNA/05 Ethernet LAN Switching  1/MAC Address Table]] · [[Clearing The MAC address Table]] · [[ARP Request]] · [[ARP Reply]] · [[CCNA/05 Ethernet LAN Switching  1/Known Unicast Forwarding]]
