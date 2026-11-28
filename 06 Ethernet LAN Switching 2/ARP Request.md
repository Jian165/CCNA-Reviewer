---
tags:
  - ccna
  - networking
  - ethernet
  - arp
  - broadcast
aliases:
  - ARP Request
  - ARP Broadcast
---

# 📢 The ARP Request

> [!abstract] In one line
> The **ARP request** asks every host on the LAN "who has this IP?" by using the **broadcast MAC address `FFFF.FFFF.FFFF`** — switches flood it, and only the matching host replies.

![[Pasted image 20261127145109.png]]

## 🧱 Building the Request Frame

PC1 has prepared the ARP request to send. Compared with the original frame PC1 wanted to send:

| Field | In the ARP request | Changed? |
| --- | --- | --- |
| Source IP | `192.168.1.1` (PC1) | Same |
| Destination IP | `192.168.1.3` (PC3) | Same |
| Source MAC | PC1's MAC (`0C2F.B011.9D00`) | Same |
| Destination MAC | **`FFFF.FFFF.FFFF`** | **Changed to broadcast** |

> [!important] The broadcast MAC
> **`FFFF.FFFF.FFFF`** is the broadcast MAC address. A device uses it when it wants to send an Ethernet frame to **all other devices on the local network**. It is the equivalent of "all Fs" seen in Wireshark.

## 🔀 How the Switches Handle It

1. **PC1** sends the frame out of its network interface → received by **SW1**.
2. **SW1** adds PC1's MAC address to its MAC address table.
   - Because it was learned from an arriving frame, it is a **dynamic MAC address**.
3. Destination MAC is all Fs, so SW1 **broadcasts (floods)** the frame out of **all interfaces except the one it was received on**.
   - Out **G0/1** and **G0/2** — **not G0/0**, because the frame arrived on G0/0.
   - This behaves exactly like **unknown unicast flooding**.
4. **PC2** receives the frame but **ignores** it: the destination IP does not match PC2's IP, so the request is meant for a different PC.
5. **SW2** receives the frame on **G0/2**, learns PC1's MAC, and associates it with **G0/2** in its MAC address table.

![[Pasted image 20261127145423.png]]

6. **SW2** floods the frame out of **G0/0 and G0/1** (all ports except the incoming G0/2).
7. **PC4** ignores the frame — destination IP does not match its own.
8. **PC3** recognises that the destination IP **does** match its own IP, so it processes the request instead of dropping it.

![[Pasted image 20261127145517.png]]

## 🎯 What Happens at PC3

PC3 does not ignore the ARP request. It answers with the other ARP message: the **ARP reply** (see [[ARP Reply]]).

> [!warning] Two different "filters"
> - A **switch** decides where to send a frame using the **destination MAC** (broadcast → flood).
> - A **host** decides whether to process a frame using the **destination IP** — PC2 and PC4 drop it because the IP does not match; PC3 keeps it because it does.

> [!success] Key takeaway
> ARP request = **source MAC of the sender + broadcast destination MAC**. Every switch **learns the source MAC** and **floods the broadcast** out all other ports; only the host with the matching **destination IP** responds.

---

### 🧭 Learning Path
← Previous: [[ARP]] · Up: [[Ethernet LAN Switching 2]] · Next → [[ARP Reply]]

### 🔗 Related Notes
[[Ethernet LAN Switching 2]] · [[ARP]] · [[ARP Reply]] · [[ARP Table]] · [[CCNA/05 Ethernet LAN Switching  1/Unknown Unicast Flooding]] · [[CCNA/05 Ethernet LAN Switching  1/MAC Address Table]]
