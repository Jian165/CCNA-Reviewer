---
tags:
  - ccna
  - networking
  - number-systems
  - ipv6
aliases:
  - Hexadecimal Number System
  - Hexadecimal
  - Hex
  - Base 16
---

# 🧮 Hexadecimal Number System (Base 16)

> [!abstract] In one line
> Hexadecimal uses **16 digits — `0–9` and `A–F`** — so the second column is worth **16**, not 10.

![[Pasted image 20261125151819.png]]

## 🔤 Sixteen Possible Digits

| Hex digit | Decimal value | Hex digit | Decimal value |
| --- | --- | --- | --- |
| `0`–`9` | 0–9 | `A` | **10** |
|  |  | `B` | **11** |
|  |  | `C` | **12** |
|  |  | `D` | **13** |
|  |  | `E` | **14** |
|  |  | `F` | **15** |

> [!important] A–F are numbers here
> Although `A`–`F` are letters of the alphabet, in hexadecimal they represent the numbers **10 through 15**.

## 🔁 Counting in Hex

![[Pasted image 20261125151715.png]]

| Hex | Decimal | Meaning |
| --- | --- | --- |
| `0`–`9` | 0–9 | Same as decimal |
| `A`–`F` | 10–15 | Letter digits |
| `10` | **16** | 1 sixteen + 0 ones |
| `11` | **17** | 1 sixteen + 1 one |
| `12` | **18** | 1 sixteen + 2 ones |
| `13` | **19** | 1 sixteen + 3 ones |
| `14` | **20** | 1 sixteen + 4 ones |
| `15` | **21** | 1 sixteen + 5 ones |
| `16` | **22** | 1 sixteen + 6 ones |
| `17` | **23** | 1 sixteen + 7 ones |
| `18` | **24** | 1 sixteen + 8 ones |
| `19` | **25** | 1 sixteen + 9 ones |
| `1A` | **26** | 1 sixteen + 10 ones |
| `1B` | **27** | 1 sixteen + 11 ones |
| `1C` | **28** | 1 sixteen + 12 ones |

> [!warning] Hex `10` is not decimal `10`
> Hex `10` means **1 sixteen and 0 ones = decimal 16**. The second column in hex is worth **16**.

## 🧭 Course Scope

This is only an introduction. Hexadecimal appears in:

- **MAC addresses** — 12 hex characters
- **Ethernet Type field** values such as `0x0800` and `0x86DD`
- **IPv6**, which will be covered in more depth in a later lesson

> [!tip] Exam focus for now
> A general understanding is enough at this stage: know the digits `0–F`, that `F = 15`, and that `0x10 = 16`.

> [!success] Key takeaway
> Hexadecimal is **base 16**: `0–9` then `A–F` (`10–15`). After `F`, roll over into the sixteens column, so hex `10` equals decimal **16**.

---

### 🧭 Learning Path
← Previous: [[Decimal Number System]] · Up: [[Ethernet LAN Switching]] · Next → [[Unicast Frames]]

### 🔗 Related Notes
[[Ethernet LAN Switching]] · [[Decimal Number System]] · [[MAC Address]] · [[Ethernet Frame]]
