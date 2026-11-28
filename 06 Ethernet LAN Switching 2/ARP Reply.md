---
tags:
  - ccna
  - networking
  - ethernet
  - arp
  - unicast
aliases:
  - ARP Reply
  - ARP Response
---

# 📨 The ARP Reply

> [!abstract] In one line
> The **ARP reply** is a **unicast** frame sent directly back to the requester, carrying the sender's MAC address so the requester can update its **ARP table**.

![[Pasted image 20261127145712.png]]

## 🧱 Address Fields in the Reply

| Field | Value |
| --- | --- |
| Source IP | PC3's IP (`192.168.1.3`) |
| Destination IP | PC1's IP (`192.168.1.1`) |
| Source MAC | PC3's MAC (`0C2F.B06A.3900`) |
| Destination MAC | PC1's MAC (`0C2F.B011.9D00`) |

## 💡 Why No Broadcast Is Needed

> [!important] The request taught PC3 the answer
> The ARP request was a **broadcast** frame, **but PC1's MAC address was used as the source MAC** of that request. PC3 therefore already knows PC1's MAC address and can send the ARP reply **directly to PC1 as a unicast frame**, without broadcasting.

## 🔀 Switching the Reply Through the Network

1. **PC3** sends the frame out of its network interface → received by **SW2**.
2. **SW2 learns PC3's MAC address** from the source field and enters it into the MAC address table, associating it with interface **G0/0** (the port the frame arrived on).

![[Pasted image 20261127145812.png]]

3. Because PC1's MAC is now known, SW2 does **not** flood — it **forwards the frame out the matching interface** (known unicast forwarding).

![[Pasted image 20261127145921.png]]

4. **PC1** finally receives the ARP reply.

## 🗃️ Updating the ARP Table

PC1 uses the information in the reply to add an entry for **PC3** to its **ARP table** — the table that stores **IP address → MAC address** associations. PC1 can now send the original data to PC3.

> [!tip] Both tables are updated
> During this exchange the **switches** learn MAC → port in their **MAC address tables**, and the **hosts** learn IP → MAC in their **ARP tables**. They are different tables with different purposes.

> [!success] Key takeaway
> ARP reply = **unicast**, source = responder's IP/MAC, destination = requester's IP/MAC. PC3 knows PC1's MAC from the request's **source MAC**, so no flood is needed, and PC1 records PC3 in its ARP table.

---

### 🧭 Learning Path
← Previous: [[ARP Request]] · Up: [[Ethernet LAN Switching 2]] · Next → [[ARP Table]]

### 🔗 Related Notes
[[Ethernet LAN Switching 2]] · [[ARP]] · [[ARP Request]] · [[ARP Table]] · [[CCNA/05 Ethernet LAN Switching  1/Known Unicast Forwarding]] · [[Wireshark packet capture]]
