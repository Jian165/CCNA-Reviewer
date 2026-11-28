---
tags:
  - ccna
  - networking
  - ethernet
  - switching
  - exam
aliases:
  - Ethernet LAN Switching Exam
  - Ethernet LAN Switching Practice Exam
---

# 📝 Ethernet LAN Switching — Practice Exam

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

### 1. Which device separates one LAN from another?
- A. Switch
- B. Hub
- C. Router
- D. NIC

> [!success]- Show answer
> **C. Router.** Routers connect separate LANs. Switches **expand** a LAN but do not create LAN boundaries.

### 2. What is the Layer 2 PDU called?
- A. Data
- B. Segment
- C. Packet
- D. Frame

> [!success]- Show answer
> **D. Frame.** L4 adds a header → **segment**; L3 adds a header → **packet**; L2 adds a header and trailer → **frame**.

### 3. What is the size and purpose of the Ethernet preamble?
- A. 1 byte; marks the frame start
- B. 7 bytes; synchronizes receiver clocks
- C. 6 bytes; identifies the sender
- D. 4 bytes; detects errors

> [!success]- Show answer
> **B. 7 bytes (56 bits)** of alternating `10101010`, used to **synchronize receiver clocks**.

### 4. What is the SFD bit pattern?
- A. `10101010`
- B. `11111111`
- C. `10101011`
- D. `00000000`

> [!success]- Show answer
> **C. `10101011`.** It is like a preamble byte except the final bit is `1`; it marks the **start of the rest of the frame**.

### 5. What does the Ethernet Type/Length value `0x0800` identify?
- A. A 1400-byte packet
- B. An IPv4 packet
- C. An IPv6 packet
- D. A CRC error

> [!success]- Show answer
> **B. IPv4.** `0x0800` = decimal **2048**, which is ≥ 1536, so it is a **type** value. `0x86DD` = 34525 = **IPv6**.

### 6. Which field detects corrupted data with a CRC?
- A. Preamble
- B. SFD
- C. Type/Length
- D. FCS

> [!success]- Show answer
> **D. FCS — Frame Check Sequence.** It is **4 bytes / 32 bits** and uses **CRC — Cyclic Redundancy Check** to detect errors.

### 7. Which part of a MAC address identifies the manufacturer?
- A. Last 3 bytes
- B. First 3 bytes (OUI)
- C. The FCS
- D. The Type field

> [!success]- Show answer
> **B. First 3 bytes = OUI — Organizationally Unique Identifier**, assigned to the maker. The last 3 bytes identify the device itself.

### 8. What does a switch do with an unknown unicast frame?
- A. Drops it immediately
- B. Sends it only to the router
- C. Floods it out all ports except the incoming port
- D. Forwards it to the NIC with the lowest MAC address

> [!success]- Show answer
> **C. Floods it.** Unknown unicast = no destination entry in the MAC address table → flood out **all interfaces except the one it arrived on**.

---

## 🅱️ Section B — True or False (5 marks)

### 1. A switch learns MAC addresses by reading the destination MAC of a frame.
> [!success]- Show answer
> **False.** Switches learn from the **SOURCE MAC** and the incoming interface.

### 2. Adding another switch creates a new LAN boundary.
> [!success]- Show answer
> **False.** Switches expand an existing LAN. **Routers** separate LANs.

### 3. A MAC address is a 48-bit physical address assigned when the device is made.
> [!success]- Show answer
> **True.** It is 6 bytes / 48 bits and is also called a **burned-in address (BIA)**.

### 4. On Cisco switches, dynamic MAC entries are removed after 5 minutes of inactivity.
> [!success]- Show answer
> **True.** When the host sends traffic again, the switch **dynamically relearns** its MAC address.

### 5. Hexadecimal `10` equals decimal `10`.
> [!success]- Show answer
> **False.** Hex `10` = **1 sixteen + 0 ones = decimal 16**.

---

## 🅲 Section C — Fill in the Blank (5 marks)

### 1. The preamble is 7 bytes, which is ______ bits.
> [!success]- Show answer
> **56 bits** — 7 bytes × 8 bits per byte.

### 2. A MAC address is written as ______ hexadecimal characters.
> [!success]- Show answer
> **12** hexadecimal characters, for example `AAAA.AA00.0001`.

### 3. Hexadecimal `F` equals decimal ______.
> [!success]- Show answer
> **15.** Hex uses `0–9` then `A=10`, `B=11`, `C=12`, `D=13`, `E=14`, `F=15`.

### 4. A Type/Length value of ______ or less means the field indicates length in bytes.
> [!success]- Show answer
> **1500.** A value of **1536 or greater** indicates the packet **type**.

### 5. The trailer field that carries the CRC is called the ______.
> [!success]- Show answer
> **FCS — Frame Check Sequence.**

---

## 🅳 Section D — Short Answer (8 marks)

### 1. Why does SW1 not learn PC2's MAC when it merely receives a frame addressed *to* PC2? (2 marks)
> [!success]- Show answer
> Because switches learn only from the **source MAC** of an arriving frame. A frame sent *to* PC2 has PC2 as the **destination**, so SW1 only learns the sender (PC1). SW1 learns PC2 only when **PC2 sends a frame itself**, such as a reply.

### 2. Compare known unicast and unknown unicast. (2 marks)
> [!success]- Show answer
> - **Unknown unicast:** destination MAC is not in the table → **flood** out all other ports.
> - **Known unicast:** destination MAC is in the table → **forward only** out the mapped port; no flooding.

### 3. In `AAAA.AA00.0001`, explain the two halves. (2 marks)
> [!success]- Show answer
> - `AAAAAA` is the **OUI**, the first 3 bytes assigned to the manufacturer; all example PCs share it.
> - `000001` is the last 3 bytes, unique to that device. Written in the grouped form `AAAA.AA00.0001`, it appears across the final two groups. The other PCs have different values here.

### 4. Why does a MAC table entry not necessarily mean a device is directly connected to that port? (2 marks)
> [!success]- Show answer
> The entry means the MAC address is **reachable via that interface**. In the two-switch example, SW2 reaches PC1 through F0/3 because F0/3 leads to SW1 — PC1 is not plugged directly into SW2.

---

## 🅴 Section E — Scenario (4 marks)

SW1 and SW2 both have **empty MAC address tables**. PC1 (`aaaa.aa00.0001`) sends a frame to PC3 (`aaaa.aa00.0003`). PC1 is connected to SW1 F0/1; SW1 F0/3 connects to SW2 F0/3. Describe what both switches do, what PC3 does next, and why the return trip does not need flooding.

> [!success]- Show answer
> 1. **SW1** receives the frame on F0/1 and learns PC1's **source MAC** → F0/1 as a **dynamic MAC**.
> 2. PC3 is unknown, so SW1 **floods** the frame out F0/2 and F0/3, but not F0/1. PC2 drops it.
> 3. **SW2** receives it on F0/3, learns PC1 → F0/3, still has no PC3 entry, and **floods** out F0/1 and F0/2. PC4 drops it; PC3 accepts it because the destination MAC matches.
> 4. **PC3 replies** with source/destination MAC fields reversed. SW2 learns PC3 from the source field and already knows PC1, so it **forwards** out F0/3 only. SW1 then learns PC3 → F0/3 and forwards to PC1 out its known PC1 port. Both directions now use **known unicast forwarding**.

---

## 📊 Score Tracker

| Score | Level | Next Step |
| --- | --- | --- |
| **27–30** | Excellent | Move on to the next topic |
| **22–26** | Good | Review missed questions |
| **18–21** | Needs work | Re-read [[Ethernet LAN Switching]] |
| **Below 18** | Restudy | Start from [[Local Area Networks]] |

## 🔁 Review These Notes

- [[Local Area Networks]] — LAN boundaries
- [[OSI Model Review]] — Layers 1/2 and PDUs
- [[Ethernet Frame]] — fields, sizes, FCS/CRC
- [[MAC Address]] — 48-bit address and OUI
- [[Decimal Number System]] — base 10 columns
- [[Hexadecimal Number System]] — base 16 and `A–F`
- [[Unicast Frames]] — one target
- [[CCNA/05 Ethernet LAN Switching  1/MAC Address Table]] — source-MAC learning
- [[Unknown Unicast Flooding]] — flood all other ports
- [[Known Unicast Forwarding]] — forward to one port; 5-minute aging
- [[MAC Learning Frame Flooding and Forwarding Process]] — full two-switch example

---

### 🧭 Learning Path
← Previous: [[MAC Learning Frame Flooding and Forwarding Process]] · Up: [[Ethernet LAN Switching]]

### 🔗 Related Notes
[[Ethernet LAN Switching]] · [[Local 2 Network Layer]] · [[Encapsulation & decapsulation]] · [[Intro To The CLI Exam]]
