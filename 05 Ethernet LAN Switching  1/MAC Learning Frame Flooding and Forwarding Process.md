---
tags:
  - ccna
  - networking
  - ethernet
  - switching
  - mac
aliases:
  - MAC Learning and Flooding
  - Two-Switch Switching Example
  - Frame Flooding and Forwarding Process
---

# 🔄 MAC Learning, Flooding and Forwarding — Two-Switch Example

> [!abstract] In one line
> This full walkthrough shows two switches with **empty MAC tables** learning from **source MACs**, flooding an **unknown unicast**, and then forwarding the reply as a **known unicast**.

![[Pasted image 20261125153415.png]]

## 🧭 Starting State and Goal

- **Two switches**, SW1 and SW2.
- Both MAC address tables are **empty**.
- **PC1 wants to send information to PC3.**

| Frame field | Value |
| --- | --- |
| **Source MAC** | `aaaa.aa00.0001` (PC1) |
| **Destination MAC** | `aaaa.aa00.0003` (PC3) |

> [!info] Abbreviated addresses
> Only short forms of the MAC addresses are written in the diagrams to save space. Real frames and real MAC address tables contain the **full 48-bit addresses**.

## 1️⃣ PC1 Sends the Frame

PC1 sends the frame out of its network interface; it arrives at **SW1** on **F0/1**.

## 2️⃣ SW1 Learns PC1

SW1 reads the **source MAC** field and associates `aaaa.aa00.0001` with the interface where the frame arrived: **F0/1**.

![[Pasted image 20261125153446.png]]

> [!important] Dynamic MAC
> This is a **dynamically learned MAC address**, usually just called a **dynamic MAC**. It was learned from an arriving frame's **source** field.

## 3️⃣ SW1 Floods the Unknown Unicast

SW1 knows PC1 is on F0/1, but it still does **not** know where PC3 is. Therefore this is an **unknown unicast frame**.

- Flood out **all ports except F0/1**.
- In this diagram: **F0/2 and F0/3**.
- **PC2 drops** the frame because the destination MAC does not match its own.

![[Pasted image 20261125153520.png]]

## 4️⃣ SW2 Learns and Floods

The frame reaches **SW2 on F0/3**. The exact same rules apply:

1. SW2 uses the **source MAC** to dynamically learn that PC1 is reachable via **F0/3**.
2. SW2 still does not know the destination PC3, so the frame is an **unknown unicast**.
3. It arrived on F0/3, so SW2 floods it out **F0/1 and F0/2**, but **not F0/3**.
4. **PC4 drops** the frame; **PC3 accepts** it because the destination MAC matches its own.

![[Pasted image 20261125153632.png]]

![[Pasted image 20261125160544.png]]

> [!warning] Interface ≠ direct connection
> An interface in the MAC address table means **"reachable via this interface."** It does **not** mean the device is directly plugged into that port. SW2 reaches PC1 through F0/3 because that port leads toward SW1.

## 5️⃣ PC3 Replies to PC1

PC3 sends a reply back to PC1. Notice that the **destination and source MAC fields are reversed**:

| Field | Reply value |
| --- | --- |
| **Source MAC** | PC3 |
| **Destination MAC** | PC1 |

SW2 receives the reply and learns PC3's MAC address with its corresponding interface.

![[Pasted image 20261125160753.png]]

> [!important] Why learning always uses the source
> If a frame from source X arrives on a port, the switch knows X can be reached via that port. That is why the switch fills the table from the **SOURCE MAC ADDRESS** field.

## 6️⃣ SW2 Forwards as a Known Unicast

SW2 already has an entry for the destination `aaaa.aa00.0001` (PC1), so there is **no need to flood**.

- The frame is forwarded normally out **F0/3**, the interface mapped to PC1.

![[Pasted image 20261125160854.png]]

## 7️⃣ SW1 Learns PC3 and Forwards to PC1

SW1 receives the frame and adds an entry for **PC3's MAC** with interface **F0/3**, because that is where the frame arrived.

SW1 already has an entry for the destination PC1, so it forwards the frame out that corresponding interface. The frame reaches **PC1**.

![[Pasted image 20261125161045.png]]

## 🧠 Quick Recap

| Step | Switch action | Rule demonstrated |
| --- | --- | --- |
| 1 | PC1 → SW1 | Unicast frame has one destination |
| 2 | SW1 learns PC1 on F0/1 | Learn from **source MAC** |
| 3 | SW1 floods out F0/2, F0/3 | Unknown unicast floods all other ports |
| 4 | SW2 learns PC1 on F0/3, then floods | Same rules on every switch |
| 5 | PC3 replies; source/destination reversed | Reply swaps MAC fields |
| 6 | SW2 forwards out F0/3 | Known unicast uses the table |
| 7 | SW1 learns PC3 on F0/3, forwards to PC1 | Learning happens in both directions |

![[Pasted image 20261125161131.png]]

> [!success] Key takeaway
> Every switch independently learns from **source MACs** and looks up **destination MACs**. Unknown destinations are **flooded**; known destinations are **forwarded**. After the reply, both switches have learned both PCs.

---

### 🧭 Learning Path
← Previous: [[Known Unicast Forwarding]] · Up: [[Ethernet LAN Switching]] · Next → [[Ethernet LAN Switching Exam]]

### 🔗 Related Notes
[[Ethernet LAN Switching]] · [[Ethernet Frame]] · [[CCNA/05 Ethernet LAN Switching  1/MAC Address Table]] · [[Unknown Unicast Flooding]] · [[Known Unicast Forwarding]] · [[Local Area Networks]]
