---
tags:
  - ccna
  - networking
  - number-systems
  - fundamentals
aliases:
  - Decimal Number System
  - Decimal
  - Base 10
---

# 🔢 Decimal Number System (Base 10)

> [!abstract] In one line
> Decimal uses **10 digits (`0–9`)** and columns worth **1, 10, 100, 1000…**; each time a column maxes out, you add one to the column on the left.

![[Pasted image 20261125151606.png]]

## 🔟 Ten Possible Digits

The decimal system uses:

`0 1 2 3 4 5 6 7 8 9`

Counting starts at `0` and goes up to `9`. The number `9` means **9 ones**, or `9 × 1`.

## 🪜 Place Values

| Column | 1000s | 100s | 10s | 1s |
| --- | --- | --- | --- | --- |
| **Value** | 1000 | 100 | 10 | 1 |

Reading `10` as "one ten and zero ones" is the key idea needed for hexadecimal later.

## 🔁 How Counting Works

- `9` → 9 ones
- `10` → **1 ten and 0 ones**; a new **10s column** is added
- `11` → 1 ten and 1 one
- `12`–`19` → increase the ones column
- `20` → **2 tens and 0 ones**; the ones column reset
- `21`, `22`, … up to `99`
- At `99`, both the 10s and 1s columns are maxed out, so add the **100s column**
- `100` → **1 hundred, 0 tens, 0 ones**
- `101`–`999` follow the same pattern
- At `999`, add the **1000s column** → `1000`

> [!tip] Memory hook
> A column works like an odometer: when it rolls over from maximum back to `0`, the column to its left increases by **1**.

## 🔗 Why Review This?

Decimal is reviewed so it can be compared directly with **hexadecimal**. The counting process is the same; only the **number of digits before rollover** changes — **10** in decimal, **16** in hex.

> [!success] Key takeaway
> Decimal is **base 10**. Columns represent **1, 10, 100, 1000**; when a column reaches its maximum, you carry **1** into the next column.

---

### 🧭 Learning Path
← Previous: [[MAC Address]] · Up: [[Ethernet LAN Switching]] · Next → [[Hexadecimal Number System]]

### 🔗 Related Notes
[[Ethernet LAN Switching]] · [[MAC Address]] · [[Hexadecimal Number System]] · [[Bits and Bytes]]
