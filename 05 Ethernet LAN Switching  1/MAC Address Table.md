---
tags:
  - ccna
  - networking
  - ethernet
  - switching
  - mac
aliases:
  - MAC Address Table
  - MAC Table
---

# 🗂️ The MAC Address Table

> [!abstract] In one line
> A switch learns where devices are by reading the **source MAC address** of each arriving frame and recording it with the **incoming interface** in its MAC address table.

![[Pasted image 20261125152415.png]]

## 👀 Learning From the Source MAC

When SW1 receives PC1's frame:

1. It looks at the **source MAC address** field.
2. It sees `AAAA.AA00.0001`.
3. It adds that MAC address to its MAC address table.
4. It associates the address with interface **F0/1**, because the frame arrived on F0/1.

| MAC address | Interface |
| --- | --- |
| `AAAA.AA00.0001` | `F0/1` |

## 🧠 How Every Switch Fills the Table

![[Pasted image 20261125152547.png]]

- **Every switch** keeps a MAC address table.
- The table is filled **dynamically** by looking at the **source MAC** of received frames.
- If a frame from source MAC X arrives on port Y, the switch knows: **"X can be reached via Y."**

> [!important] Most important rule in this folder
> Switches learn from the **SOURCE MAC**, never from the destination MAC. The association means *reachable through that interface* — not necessarily directly connected.

> [!tip] Repeat it until it is automatic
> **Source MAC → incoming port → table entry.** This is how a switch dynamically discovers where devices are on the LAN.

## ⚠️ The Remaining Problem

SW1 now knows where **PC1** is, but it still does not know where **PC2** is. The destination `AAAA.AA00.0002` is not in the table, so SW1 cannot forward the frame normally yet.

> [!success] Key takeaway
> The MAC address table maps **source MAC addresses to the ports where they were seen**. SW1 has learned PC1 on F0/1, but because PC2 is unknown, the next step is **flooding**.

---

### 🧭 Learning Path
← Previous: [[Unicast Frames]] · Up: [[Ethernet LAN Switching]] · Next → [[Unknown Unicast Flooding]]

### 🔗 Related Notes
[[Ethernet LAN Switching]] · [[Unicast Frames]] · [[Unknown Unicast Flooding]] · [[Known Unicast Forwarding]] · [[MAC Learning Frame Flooding and Forwarding Process]] · [[MAC Address]]
