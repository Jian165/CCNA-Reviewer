---
tags:
  - ccna
  - networking
  - ethernet
  - switching
  - arp
  - exam
aliases:
  - Ethernet LAN Switching 2 Exam
  - Ethernet LAN Switching 2 Practice Exam
---

# 📝 Ethernet LAN Switching 2 — Practice Exam

> [!info] How to use this exam
> - Answer everything **without looking at your notes**.
> - Suggested time: **20 minutes**.
> - Click **Show answer** to check each question.
> - Target score: **80% or higher**.

| Section | Topic | Marks |
| --- | --- | --- |
| A | Multiple choice | 8 |
| B | True or false | 5 |
| C | Fill in the blank | 5 |
| D | Short answer | 8 |
| E | Scenario | 4 |
| **Total** | | **30** |

---

## 🅰️ Section A — Multiple Choice (8 marks)

### 1. What does ARP discover?
- A. The IP address of a known MAC address
- B. The MAC address of a known IP address
- C. The default gateway of a network
- D. The VLAN of a switch port

> [!success]- Show answer
> **B.** ARP (Address Resolution Protocol) discovers the **Layer 2 MAC address** of a known **Layer 3 IP address**.

### 2. What destination MAC address does an ARP request use?
- A. The requester's MAC
- B. The target's MAC
- C. `FFFF.FFFF.FFFF`
- D. `0000.0000.0000`

> [!success]- Show answer
> **C. `FFFF.FFFF.FFFF`** — the broadcast MAC, used to reach all hosts on the local network because the target's MAC is unknown.

### 3. How is the ARP reply sent?
- A. Broadcast to all hosts
- B. Unicast to the requester
- C. Multicast to a group
- D. Flooded by every switch

> [!success]- Show answer
> **B. Unicast.** PC3 knows PC1's MAC from the **source MAC** of the ARP request, so it replies directly without broadcasting.

### 4. What is the minimum Ethernet frame size, excluding preamble and SFD?
- A. 18 bytes
- B. 46 bytes
- C. 64 bytes
- D. 26 bytes

> [!success]- Show answer
> **C. 64 bytes.** With an 18-byte header + trailer, this leaves a **46-byte minimum payload**.

### 5. How much padding is added to a 34-byte payload to meet the minimum?
- A. 10 bytes
- B. 12 bytes
- C. 20 bytes
- D. 30 bytes

> [!success]- Show answer
> **B. 12 bytes** of zeros: 46 − 34 = 12. Padding bytes are **all 0s**.

### 6. Which Ethernet Type value indicates an ARP packet?
- A. `0x0800`
- B. `0x86DD`
- C. `0x0806`
- D. `0x1536`

> [!success]- Show answer
> **C. `0x0806`** = ARP. `0x0800` = IPv4 and `0x86DD` = IPv6. The `0x` prefix means hexadecimal.

### 7. What are the Cisco IOS defaults for `ping`?
- A. 3 × 64-byte echos
- B. 5 × 100-byte echos
- C. 10 × 32-byte echos
- D. 5 × 46-byte echos

> [!success]- Show answer
> **B.** IOS sends **5 ICMP Echo Requests of 100 bytes** by default. `!` = success, `.` = failure.

### 8. How does GNS3 differ from Packet Tracer?
- A. Packet Tracer runs real IOS; GNS3 only simulates
- B. GNS3 runs actual Cisco IOS virtually; Packet Tracer simulates the network
- C. Both are paid Cisco products
- D. Wireshark only works with Packet Tracer

> [!success]- Show answer
> **B.** GNS3 runs **real Cisco IOS** (you must supply your own IOS licence); **Packet Tracer** is a free **simulator** and covers almost everything needed for the CCNA. GNS3 integrates with Wireshark.

---

## 🅱️ Section B — True or False (5 marks)

### 1. The ARP reply is broadcast to every host on the LAN.
> [!success]- Show answer
> **False** — the ARP request is the broadcast; the **reply is unicast** to the requester.

### 2. A switch learns MAC addresses from the destination MAC of a frame.
> [!success]- Show answer
> **False** — switches learn from the **source MAC** and the **incoming interface**.

### 3. A `static` ARP table entry was learned by sending an ARP request and receiving a reply.
> [!success]- Show answer
> **False** — `static` entries are defaults that were **not** learned via ARP. `dynamic` entries were learned by request/reply.

### 4. Cisco switches remove dynamic MAC entries after 5 minutes of inactivity.
> [!success]- Show answer
> **True** — this is **aging**. The entry is relearned from the next frame's source MAC when the host sends traffic again.

### 5. Preamble and SFD are sent with every frame but are often excluded from the Ethernet header.
> [!success]- Show answer
> **True** — header + trailer is **18 bytes** without them, **26 bytes** with them.

---

## 🅲 Section C — Fill in the Blank (5 marks)

### 1. The broadcast MAC address used in an ARP request is ________.
> [!success]- Show answer
> **`FFFF.FFFF.FFFF`**

### 2. The minimum payload of an Ethernet frame is ________ bytes.
> [!success]- Show answer
> **46** (64-byte minimum frame − 18-byte header + trailer).

### 3. An ARP table entry with Type ________ was learned by ARP request and reply.
> [!success]- Show answer
> **dynamic** (a `static` entry was not learned via ARP).

### 4. The command to clear all dynamic MAC entries is `clear ________ dynamic`.
> [!success]- Show answer
> **`mac address-table`** — `clear mac address-table dynamic`.

### 5. The Ethernet Type value for IPv6 is `0x________`.
> [!success]- Show answer
> **`86DD`** (IPv4 is `0800`; ARP is `0806`).

---

## 🅳 Section D — Short Answer (8 marks)

### 1. Why can the ARP reply be unicast instead of broadcast? (2 marks)
> [!success]- Show answer
> > The ARP request was broadcast, but it carried **PC1's MAC as the source MAC**. PC3 therefore already knows PC1's MAC address and can send the reply **directly to PC1** as a unicast frame.

### 2. Why does the first ping commonly fail, and how does ping use ARP? (2 marks)
> [!success]- Show answer
> > Ping sends a **unicast** ICMP Echo Request to a specific host, so the destination MAC must be known first. If ARP has not resolved it, PC1 must send an ARP request and wait for the reply — during that time the **first ping fails**. After the MAC is learned, the remaining pings succeed.

### 3. Name the four columns of `show mac address-table` and the default VLAN. (2 marks)
> [!success]- Show answer
> > **VLAN** (default **1**), **MAC Address**, **Type** (`dynamic` = learned, not configured), and **Ports** (another word for interface). Older IOS used `show mac-address-table`.

### 4. Give the two commands that narrow `clear mac address-table dynamic` to one MAC or one port. (2 marks)
> [!success]- Show answer
> > - `clear mac address-table dynamic address 0c2f.b011.9d00` — clears **one specific MAC**.
> > - `clear mac address-table dynamic interface gi0/0` — clears **all entries learned on that interface**.

---

## 🅴 Section E — Scenario (4 marks)

PC1 (`192.168.1.1`, MAC `0c2f.b011.9d00`) pings PC3 (`192.168.1.3`, MAC `0c2f.b06a.3900`) through **SW1** and **SW2**. SW1 receives PC1's frame on **G0/0**; SW2 receives the forwarded frame on **G0/2**. All MAC tables start empty.

**Describe the ARP request and reply through both switches, what each switch learns, and what a Wireshark capture would show.**

> [!success]- Show answer
> 1. **ARP request:** PC1 broadcasts with destination MAC `FFFF.FFFF.FFFF`, source IP `192.168.1.1`, destination IP `192.168.1.3`, source MAC `0c2f.b011.9d00`. SW1 learns PC1 → G0/0 (**dynamic**) and floods out G0/1 and G0/2 — not G0/0. SW2 receives on G0/2, learns PC1 → G0/2, and floods out G0/0 and G0/1 (and other ports except G0/2). PC2 and PC4 ignore it because the destination IP does not match.
> 2. **ARP reply:** PC3 matches the IP and replies **unicast** — source `192.168.1.3` / `0c2f.b06a.3900`, destination `192.168.1.1` / PC1's MAC — because it learned PC1's MAC from the request's source MAC. SW2 learns PC3 on the port the reply arrived on and **forwards** (known unicast, no flood); SW1 learns PC3 and forwards to PC1 out the known PC1 port.
> 3. **ARP tables:** PC1 adds PC3's IP → MAC (`dynamic`); all switches hold MAC → port entries that age out after **5 minutes** unless cleared with `clear mac address-table dynamic`.
> 4. **Wireshark:** capture order is ARP request ("Who has 192.168.1.3? Tell 192.168.1.1", destination all Fs) → ARP reply ("192.168.1.3 is at 0c2f.b06a.3900") → 4 ICMP echo requests and 4 echo replies (the first of 5 failed during ARP). The ARP frame's Type is `0x0806`; a 36-byte ping (`SIZE 36`) shows Type `0x0800` and **10 bytes / 20 hex zeros** of padding to reach the **46-byte** minimum payload.

---

## 📊 Score Tracker

| Score | Level | Next Step |
| --- | --- | --- |
| **27–30** | Excellent | Move on to the next topic |
| **22–26** | Good | Review missed questions |
| **18–21** | Needs work | Re-read [[Ethernet LAN Switching 2]] |
| **Below 18** | Restudy | Start from [[ARP]] |

## 🔁 Review These Notes

- [[Ethernet Frame 2]] — 18/26-byte header, 64-byte frame, 46-byte payload, padding
- [[ARP]] — resolving IP to MAC
- [[ARP Request]] — broadcast, switch learning and flooding
- [[ARP Reply]] — unicast and ARP table update
- [[ARP Table]] — `arp -a`, static vs dynamic
- [[GNS3 Sim]] — simulator vs real IOS, Wireshark integration
- [[Ping]] — ICMP echo, first-ping failure, `show arp`
- [[CCNA/06 Ethernet LAN Switching 2/MAC Address Table]] — columns, dynamic, aging
- [[Clearing The MAC address Table]] — clear command variants
- [[Wireshark packet capture]] — capture sequence, Type values, padding proof

---

### 🧭 Learning Path
← Previous: [[Wireshark packet capture]] · Up: [[Ethernet LAN Switching 2]]

### 🔗 Related Notes
[[Ethernet LAN Switching 2]] · [[ARP]] · [[ARP Request]] · [[ARP Reply]] · [[Ping]] · [[Wireshark packet capture]] · [[Ethernet LAN Switching Exam]]
