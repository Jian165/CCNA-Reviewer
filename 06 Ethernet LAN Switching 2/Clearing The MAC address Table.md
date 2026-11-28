---
tags:
  - ccna
  - networking
  - ethernet
  - switching
  - mac
  - cli
aliases:
  - Clearing the MAC Address Table
  - clear mac address-table dynamic
  - MAC Address Aging
---

# 🧹 Clearing the MAC Address Table

> [!abstract] In one line
> Dynamic MAC entries **age out after 5 minutes** of inactivity, or you can remove them manually with `clear mac address-table dynamic`, optionally filtered by **address** or **interface**.

![[Pasted image 20261128134736.png]]

## ⏳ Aging (Automatic Removal)

> [!info] The 5-minute rule
> If the switch receives **no traffic from a MAC address for 5 minutes**, it removes that entry from the MAC address table. This is called **aging**.

## 🧽 Manual Removal — All Dynamic Entries

First confirm what is in the table:

```bash
show mac address-table
```

Then clear **all** dynamic MAC addresses:

```bash
clear mac address-table dynamic
```

> [!important] Memorise this command
> **`clear mac address-table dynamic`** removes every dynamically learned entry. Static entries are not affected.

## 🎯 Clear a Specific MAC Address

Add the `address` option to remove just one entry:

```bash
clear mac address-table dynamic address 0c2f.b011.9d00
```

![[Pasted image 20261128134910.png]]

- Before: both PC1 and PC3 entries are shown by `show mac address-table`.
- After: **only PC3's MAC address remains** — PC1's entry (`0c2f.b011.9d00`) was removed.

## 🔌 Clear All Entries on One Interface

Add the `interface` option to clear everything learned on a port:

```bash
clear mac address-table dynamic interface gi0/0
```

- This clears **all MAC address table entries for a specific interface**.
- PC1's MAC is removed because **PC1 is connected to G0/0**.

## 📋 Command Summary

| Command | Effect |
| --- | --- |
| `show mac address-table` | Display the MAC address table |
| `clear mac address-table dynamic` | Clear **all** dynamic entries |
| `clear mac address-table dynamic address <mac>` | Clear **one specific MAC address** |
| `clear mac address-table dynamic interface <interface>` | Clear **all entries learned on that interface** |

> [!warning] Check before you clear
> Use `show mac address-table` first to confirm which entries exist, then choose the narrowest command that achieves your goal. After clearing, the switch **relearns** entries from the next frames' **source MACs**.

> [!success] Key takeaway
> Dynamic entries expire after **5 minutes** automatically, or are removed with **`clear mac address-table dynamic`** — optionally narrowed with **`address <mac>`** or **`interface <port>`**.

---

### 🧭 Learning Path
← Previous: [[CCNA/06 Ethernet LAN Switching 2/MAC Address Table]] · Up: [[Ethernet LAN Switching 2]] · Next → [[Wireshark packet capture]]

### 🔗 Related Notes
[[Ethernet LAN Switching 2]] · [[CCNA/05 Ethernet LAN Switching  1/MAC Address Table]] · [[CCNA/06 Ethernet LAN Switching 2/MAC Address Table]] · [[CCNA/05 Ethernet LAN Switching  1/Known Unicast Forwarding]] · [[ARP Table]]
