---
tags:
  - ccna
  - networking
  - fundamentals
aliases:
  - Bits and Bytes
  - Bits & Bytes
---

# 🔢 Bits & Bytes

> [!abstract] Core idea
> Connections between devices operate at a set **speed**, measured in **bits per second**. Storage, however, is measured in **bytes** — and 1 byte = 8 bits.

## ⚡ Network Speed

Every connection between devices in a [[Network]] operates at a set speed. These speeds are measured in **bits per second**.

A **bit** is a value represented by either a **0** or a **1**. This binary code is how computers work.

## 🧮 Bit vs Byte

| Term | Definition | Size |
| --- | --- | --- |
| **Bit** | A single binary value — `0` or `1` | 1 bit |
| **Byte** | A series of **8 bits** | 8 bits |

> [!tip] Memory hook
> **b**its are **b**inary digits. A **B**yte is **B**igger — 8 bits.

## 🔌 How Bits Travel

When communicating across a **copper network cable**, a variation in the electrical signal is interpreted by the receiving device as a `0` or a `1`.

## 📤 Serial Transmission

A byte — 8 bits of data — is sent along a wire **one bit at a time**.

![[Pasted image 20261112145646.png]]

It does **not** operate one byte at a time like this:

![[Pasted image 20261112145711.png]]

> [!important] Exam point
> Data travels **serially** — one bit after another — not as a whole byte in one step.

## 📏 Speed Units

Network speed is measured in **bits per second** — kilobits, megabits, gigabits — **not bytes per second**.

![[Pasted image 20261112145939.png]]

| Unit | Symbol | Value in bits |
| --- | --- | --- |
| Kilobit | Kb | 1,000 |
| Megabit | Mb | 1,000,000 |
| Gigabit | Gb | 1,000,000,000 |
| Terabit | Tb | 1,000,000,000,000 |
| Petabit | Pb | 10¹⁵ |
| Exabit | Eb | 10¹⁸ |
| Zettabit | Zb | 10²¹ |
| Yottabit | Yb | 10²⁴ |

> [!note] Beyond terabit
> Larger units exist — petabits, exabits, zettabits, yottabits — but you will rarely see them in network speeds today. Speeds keep increasing, so terabit-per-second links may become commonplace.

## 💾 Bits vs Bytes in Practice

- Network **speed** → bits per second (e.g. **1 Gbps**)
- Hard drive **storage** → bytes (e.g. **1 GB**)
- Because 1 byte = 8 bits, a **gigabyte is 8 times larger than a gigabit**.

> [!example] Worked conversions
> - 1 Gbps = 1,000,000,000 bits/s ÷ 8 = **125 MB/s**
> - 100 Mbps ÷ 8 = **12.5 MB/s**
> - A **1 GB** file over a **1 Gbps** link ≈ **8 seconds** (theoretical, ignoring overhead)

## ⚠️ Exam Traps

> [!warning] Watch out for these
> - Speed is **bits**/s — not **bytes**/s.
> - A **byte = 8 bits**.
> - Lowercase **b** = bit; uppercase **B** = byte.
> - Network units use **1,000** (decimal), not 1,024.
> - Transmission is **one bit at a time** (serial), not one byte at a time.
> - **1 GB = 8 Gb** — a gigabyte is 8× a gigabit.

## ✅ Quick Recap

| Topic | Fact |
| --- | --- |
| **Bit** | A `0` or `1` |
| **Byte** | 8 bits |
| Network **speed unit** | Bits per second (Kbps, Mbps, Gbps) |
| **Transmission** | One bit at a time (serial) |
| **1 GB vs 1 Gb** | A gigabyte is **8× larger** (1 byte = 8 bits) |

---

### 🧭 Learning Path
← Previous: [[Firewall]] · Up: [[Interfaces And Cables]] · Next → [[Network Protocols]]

### 🔗 Related Notes
[[Interfaces And Cables]] · [[Ethernet]] · [[Ethernet Standards (copper)]] · [[Network Protocols]] · [[Network]]
