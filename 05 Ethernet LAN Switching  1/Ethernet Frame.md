---
tags:
  - ccna
  - networking
  - ethernet
  - switching
  - frames
aliases:
  - Ethernet Frame
  - Ethernet Header and Trailer
  - FCS
---

# 🧱 The Ethernet Frame

> [!abstract] In one line
> An Ethernet frame wraps a packet in a **Layer 2 header and trailer**: synchronization, source/destination MAC addresses, type or length, and an FCS for error detection.

![[Pasted image 20261125145730.png]]

The header can be drawn on either side of the diagram; here the **header is on the left** and the **trailer on the right**. The important thing is the fields and their sizes.

## 🧩 Frame Overview

| Part | Field | Size | Purpose |
| --- | --- | --- | --- |
| Header | **Preamble** | 7 bytes | Synchronization |
| Header | **SFD** | 1 byte | Start-frame delimiter |
| Header | **Destination** | 6 bytes | Layer 2 address of the recipient |
| Header | **Source** | 6 bytes | Layer 2 address of the sender |
| Header | **Type/Length** | 2 bytes | Identifies the encapsulated packet or its length |
| Trailer | **FCS** | 4 bytes | Error detection |
| **Total** | Header + trailer | **26 bytes** | 7 + 1 + 6 + 6 + 2 + 4 |

## 🔁 Preamble & SFD

![[Pasted image 20261125150155.png]]

| Field | Size | Bit pattern | Job |
| --- | --- | --- | --- |
| **Preamble** | **7 bytes = 56 bits** | `10101010` repeated **7 times** | Allows devices to **synchronize receiver clocks** and get ready for the rest of the frame |
| **SFD** (Start Frame Delimiter) | **1 byte = 8 bits** | `10101011` | Same as a preamble byte except the **last bit is 1**; marks the **end of the preamble** and start of the rest of the frame |

> [!tip] Remember the pattern
> Preamble = `10101010` × 7. SFD = `10101011` — the final `1` says "the frame starts now."

## 📮 Destination & Source

![[Pasted image 20261125150416.png]]

The destination and source fields identify who the frame is for and who sent it, much like **email addresses** or addresses on a mailed letter.

- These are **Layer 2 MAC addresses**.
- **MAC** stands for **Media Access Control**.
- A MAC address is **6 bytes / 48 bits** and is a **physical address** assigned to the device when it is made.
- It is separate from a **logical address** such as an IP address.

> [!important] Exam point
> These are the fields a switch cares about most: it learns from the **source MAC** and forwards based on the **destination MAC**.

## 🧾 Type/Length

![[Pasted image 20261125151021.png]]

The final header field is **2 bytes / 16 bits**. Its meaning depends on its value and the version of Ethernet in use.

| Value in field | Meaning | Example |
| --- | --- | --- |
| **1500 or less** | **Length** of the encapsulated packet in bytes | `1400` = packet is 1400 bytes long |
| **1536 or greater** | **Type** of encapsulated packet; length is found by other methods | IPv4 or IPv6 |

| Hex value | Decimal value | Identifies |
| --- | --- | --- |
| `0x0800` | **2048** | **IPv4** packet |
| `0x86DD` | **34525** | **IPv6** packet |

> [!tip] Reading hex
> The **`0x`** prefix means the number is written in **hexadecimal**. `0x0800` = 2048, which is greater than 1536, so it is a **type** field, not a length.

## ✅ FCS — Frame Check Sequence

![[Pasted image 20261125151308.png]]

The **only field in the Ethernet trailer** is the **FCS**:

- **4 bytes / 32 bits**
- Detects corrupted data by running a **CRC** over the received data
- **CRC** = **Cyclic Redundancy Check**
  - **Cyclic** → based on cyclic codes
  - **Redundancy** → the 4 bytes enlarge the message without adding new information
  - **Check** → verifies the data for errors

> [!important] For the CCNA
> Know that the Ethernet **FCS is a CRC** used to **detect** errors. You do not need the detailed CRC math for the exam.

## 🧠 Quick Recap

| Field | Bytes | Bits | Remember it as |
| --- | --- | --- | --- |
| **Preamble** | 7 | 56 | Clock synchronization |
| **SFD** | 1 | 8 | `10101011`, frame begins |
| **Destination MAC** | 6 | 48 | Where it is going |
| **Source MAC** | 6 | 48 | Where it came from; switch learns this |
| **Type/Length** | 2 | 16 | ≤1500 length, ≥1536 type |
| **FCS** | 4 | 32 | CRC error detection |

> [!success] Key takeaway
> The Ethernet header and trailer total **26 bytes**. Switches focus on the **source and destination MAC fields**: the source teaches the switch where a device is, and the destination determines where the frame should go.

---

### 🧭 Learning Path
← Previous: [[OSI Model Review]] · Up: [[Ethernet LAN Switching]] · Next → [[MAC Address]]

### 🔗 Related Notes
[[Ethernet LAN Switching]] · [[OSI Model Review]] · [[MAC Address]] · [[Unicast Frames]] · [[CCNA/05 Ethernet LAN Switching  1/MAC Address Table]] · [[Local 2 Network Layer]]
