---
tags:
  - ccna
  - networking
  - ethernet
  - switching
  - flooding
aliases:
  - Unknown Unicast
  - Unknown Unicast Frame
  - Flooding
---

# 🌊 Unknown Unicast Flooding

> [!abstract] In one line
> An **unknown unicast** frame has a destination MAC that is **not in the switch's table**, so the switch **floods** it out every port except the one it arrived on.

## ❓ What Makes It "Unknown"?

PC1 sends a frame destined for `AAAA.AA00.0002` (PC2), but SW1 has no entry for that address.

> [!important] Definition
> An **unknown unicast** frame is a unicast frame for which the switch has **no destination MAC entry** in its MAC address table.

## 📢 The Flood Rule

Because SW1 does not know how to reach PC2, it has only one option: **flood** the frame.

- **Flood** = forward the frame out **ALL interfaces except the one it was received on**.
- The frame arrived on **F0/1**, so SW1 copies it out **F0/2 and F0/3** only.

![[Pasted image 20261125152824.png]]

| Interface | Action | Reason |
| --- | --- | --- |
| `F0/1` | **Not used** | Frame was received here |
| `F0/2` | Flooded | Possible path to PC2 |
| `F0/3` | Flooded | Possible path to PC2 |

## 🎯 What the Receivers Do

![[Pasted image 20261125153031.png]]

- **PC3** ignores and drops the frame because the destination MAC does not match its own.
- **PC2** receives the frame and processes it normally **up the OSI stack**.

> [!tip] Only the true destination accepts it
> Flooding sends copies to many ports, but a NIC only processes a frame when the **destination MAC matches its own MAC**.

## 🔁 No Reply = No Learning

Unless PC2 sends a reply, the process stops there.

- SW1 never receives a frame from PC2.
- Therefore SW1 cannot learn PC2's MAC address.
- Its MAC address table remains incomplete.

If PC1 sends **another** frame to PC2:

1. SW1 already knows PC1, so it does **not** add PC1 again.
2. SW1 still does **not** know PC2, so it **floods again**.
3. PC3 drops the frame; PC2 receives and processes it again.

![[Pasted image 20261125152948.png]]

> [!example] What finally fixes this?
> PC2 sends data back to PC1 — perhaps a reply to what PC1 sent. Now SW1 sees PC2's **source MAC** on an incoming frame and can finally add PC2 to the MAC address table.

> [!success] Key takeaway
> Unknown unicast → **flood all other ports**. Flooding reaches the true destination, but the switch only learns that device's MAC once the device **sends a frame itself**.

---

### 🧭 Learning Path
← Previous: [[CCNA/05 Ethernet LAN Switching  1/MAC Address Table]] · Up: [[Ethernet LAN Switching]] · Next → [[Known Unicast Forwarding]]

### 🔗 Related Notes
[[Ethernet LAN Switching]] · [[CCNA/05 Ethernet LAN Switching  1/MAC Address Table]] · [[Known Unicast Forwarding]] · [[Unicast Frames]] · [[MAC Learning Frame Flooding and Forwarding Process]]
