---
tags:
  - ccna
  - networking
  - ethernet
  - switching
  - frames
aliases:
  - Unicast
  - Unicast Frame
---

# 📨 Unicast Frames

> [!abstract] In one line
> A **unicast frame** is a frame destined for **a single target device** — PC2 in this example.

![[Pasted image 20261125152122.png]]

## 🎯 One Target, Not Everyone

| Frame type | Meaning | Covered here? |
| --- | --- | --- |
| **Unicast** | Destined for **one** specific device | ✅ Yes |
| **Broadcast** | Destined for all devices in the broadcast domain | Later lesson |

> [!important] Exam point
> **Unicast** does not mean "the switch knows where the device is." It only means the frame has **one intended destination**. Whether the switch knows the path is a separate question — that is where **known** vs **unknown unicast** comes in.

## 📤 The Example Path

The MAC addresses in the diagram are abbreviated because there is limited space on the slide.

1. **PC1** builds a frame with:
   - **Source MAC** = PC1
   - **Destination MAC** = PC2
2. PC1 sends the frame out its **network interface card (NIC)**.
3. The NIC is connected to **SW1**, so **SW1 receives the frame**.

> [!success] Key takeaway
> A unicast frame has one destination. PC1 sends its frame through its NIC to SW1; what SW1 does next depends on whether PC2's MAC is already in its MAC address table.

---

### 🧭 Learning Path
← Previous: [[Hexadecimal Number System]] · Up: [[Ethernet LAN Switching]] · Next → [[CCNA/05 Ethernet LAN Switching  1/MAC Address Table]]

### 🔗 Related Notes
[[Ethernet LAN Switching]] · [[Ethernet Frame]] · [[MAC Address]] · [[CCNA/05 Ethernet LAN Switching  1/MAC Address Table]] · [[Unknown Unicast Flooding]] · [[Known Unicast Forwarding]]
