---
tags:
  - ccna
  - networking
  - ethernet
  - frames
  - padding
aliases:
  - Ethernet Frame 2
  - Ethernet Frame Size
  - Minimum Ethernet Frame Size
  - Frame Padding
---

# 🧱 Ethernet Frame — Size & Padding

> [!abstract] In one line
> The **Ethernet header is 3 fields (18 bytes with the trailer)**, and the **minimum frame is 64 bytes**, so the payload must be at least **46 bytes** — shorter payloads get **zero padding**.

![[Pasted image 20261127144031.png]]

## 📏 What Counts as the Header?

The **preamble + SFD** is usually **not** considered part of the Ethernet header, although it is sent with every Ethernet frame.

| Definition | Fields counted | Size |
| --- | --- | --- |
| **Header only (strict)** | Destination, Source, Type | 14 bytes |
| **Header + trailer** (without preamble/SFD) | Destination 6 + Source 6 + Type 2 + FCS 4 | **18 bytes** |
| **Header + trailer** (with preamble/SFD) | Preamble 7 + SFD 1 + the 18 bytes above | **26 bytes** |

> [!important] Exam nuance
> Depending on how you define the header, the preamble and SFD may or may not be included — but they are **included with every Ethernet frame**. When a question says "header + trailer" without preamble/SFD, the answer is **18 bytes**.

## 📉 Minimum Frame Size

- The **minimum Ethernet frame size is 64 bytes**, including the encapsulated payload (the packet).
- This minimum **does not include the preamble and SFD**.

**The calculation:**

```text
64 bytes (minimum frame) − 18 bytes (header + trailer) = 46 bytes (minimum payload)
```

| Rule | Value |
| --- | --- |
| Minimum frame | **64 bytes** |
| Header + trailer (no preamble/SFD) | **18 bytes** |
| Minimum payload | **46 bytes** |

## 🧩 Padding

> [!warning] Payload smaller than 46 bytes?
> If the payload is less than 46 bytes, **padding bytes are added** — and those padding bytes are **all 0s**.

| Original payload | Padding added | Resulting payload |
| --- | --- | --- |
| 34 bytes | **12 bytes** of zeros | 46 bytes |
| 36 bytes | **10 bytes** of zeros | 46 bytes |

![[Pasted image 20261127144143.png]]

## 🧠 Quick Recap

| Fact | Value |
| --- | --- |
| Fields in the Ethernet header | **Destination, Source, Type** |
| Preamble + SFD | Sent with every frame; often excluded from the header |
| Header + trailer without preamble/SFD | **18 bytes** |
| Minimum frame size | **64 bytes** (excluding preamble/SFD) |
| Minimum payload | **46 bytes** |
| Padding | All **0s**, added when payload < 46 bytes |

> [!success] Key takeaway
> Remember three numbers: **18** (header + trailer), **64** (minimum frame), **46** (minimum payload). Anything shorter gets **zero padding** — verified later in [[Wireshark packet capture]] with a 36-byte ping.

---

### 🧭 Learning Path
← Previous: [[Ethernet LAN Switching Exam]] · Up: [[Ethernet LAN Switching 2]] · Next → [[ARP]]

### 🔗 Related Notes
[[Ethernet LAN Switching 2]] · [[CCNA/05 Ethernet LAN Switching  1/Ethernet Frame]] · [[Wireshark packet capture]] · [[ARP]] · [[ARP Request]]
