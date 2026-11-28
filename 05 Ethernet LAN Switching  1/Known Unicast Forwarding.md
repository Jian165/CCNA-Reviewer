---
tags:
  - ccna
  - networking
  - ethernet
  - switching
  - forwarding
aliases:
  - Known Unicast
  - Known Unicast Frame
  - Known Unicast Forwarding
---

# 🎯 Known Unicast Forwarding

> [!abstract] In one line
> A **known unicast** frame has a destination MAC already in the switch's table, so the switch **forwards it only to the matching port** — it does **not** flood.

![[Pasted image 20261125153158.png]]

## ✅ The Destination Is Already Known

Now **PC2 sends data back to PC1** — perhaps a reply to PC1's earlier frame. SW1 already knows PC1's MAC from the original frame and learns PC2 from this frame's **source MAC**. Because the destination is known, this time SW1 does **not** flood the frame.

| Frame type | Table lookup | Switch action |
| --- | --- | --- |
| **Unknown unicast** | Destination not found | Flood out **all other ports** |
| **Known unicast** | Destination found | Forward to the **one mapped port** |

> [!important] Exam point
> "Known" means only that the **destination MAC is in the MAC address table**. It does not change the frame type — it is still a unicast frame.

## 🔄 What Happens at the Destination

PC1 receives the frame and processes it **up the OSI stack** through the **de-encapsulation** process from Day 3: the Layer 2 header/trailer are removed and the packet continues upward.

## ⏳ Dynamic MAC Address Aging

Dynamic MAC addresses do not stay in the table forever.

- On **Cisco switches**, dynamic MAC addresses are removed after **5 minutes of inactivity**.
- If PC1 sends no traffic for more than 5 minutes, SW1 removes PC1's MAC address to clean out the table.
- If PC1 sends traffic again, SW1 **dynamically learns** the address again from the source MAC.

> [!warning] Do not confuse aging with flooding
> Aging removes an **old source-based entry**. Flooding happens when a **destination** cannot be found at forwarding time.

> [!success] Key takeaway
> Known unicast → **forward only to the mapped port**. Cisco switches age out dynamic MAC entries after **5 minutes of inactivity**, then relearn them when the host sends traffic again.

---

### 🧭 Learning Path
← Previous: [[Unknown Unicast Flooding]] · Up: [[Ethernet LAN Switching]] · Next → [[MAC Learning Frame Flooding and Forwarding Process]]

### 🔗 Related Notes
[[Ethernet LAN Switching]] · [[Unknown Unicast Flooding]] · [[CCNA/05 Ethernet LAN Switching  1/MAC Address Table]] · [[MAC Learning Frame Flooding and Forwarding Process]] · [[Encapsulation & decapsulation]]
