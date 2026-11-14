---
tags:
  - ccna
  - networking
  - exam
aliases:
  - Interfaces And Cables Exam
  - Interfaces and Cables Practice Exam
---

# 📝 Interfaces & Cables — Practice Exam

> [!info] How to use this exam
> - Answer everything **without looking at your notes**.
> - Suggested time: **20 minutes**.
> - Click **Show answer** to check each question.
> - Target score: **80% or higher**.

| Section | Topic | Marks |
| --- | --- | --- |
| A | Multiple choice | 10 |
| B | True or false | 5 |
| C | Fill in the blank | 5 |
| D | Short answer | 6 |
| E | Scenario | 4 |
| **Total** | | **30** |

---

## 🅰️ Section A — Multiple Choice (10 marks)

### 1. What does **UTP** stand for?
- A. Universal Twisted Pair
- B. Unshielded Twisted Pair
- C. Unified Transmission Pair
- D. Unshielded Transmission Port

> [!success]- Show answer
> **B. Unshielded Twisted Pair** — copper Ethernet cable with no metallic shield.

### 2. How many wires are in a UTP cable?
- A. 2
- B. 4
- C. 6
- D. 8

> [!success]- Show answer
> **D. 8** — four twisted pairs make eight wires.

### 3. Which standard defines Ethernet?
- A. IEEE 802.11
- B. IEEE 802.3
- C. IEEE 802.1Q
- D. IEEE 802.15

> [!success]- Show answer
> **B. IEEE 802.3** — all copper Ethernet standards begin with IEEE 802.3.

### 4. In **10BASE-T**, what does the **T** mean?
- A. Transmission
- B. Twisted pair
- C. Terabit
- D. Terminal

> [!success]- Show answer
> **B. Twisted pair** — BASE means baseband, T means twisted pair.

### 5. How many pairs does **1000BASE-T** use?
- A. 1
- B. 2
- C. 3
- D. 4

> [!success]- Show answer
> **D. 4** — gigabit and 10-gigabit copper use all four pairs (8 wires).

### 6. A PC transmits data on which pins?
- A. 1 and 2
- B. 3 and 6
- C. 4 and 5
- D. 7 and 8

> [!success]- Show answer
> **A. 1 and 2** — PCs, routers, and firewalls transmit on 1 & 2 and receive on 3 & 6.

### 7. A switch transmits data on which pins?
- A. 1 and 2
- B. 3 and 6
- C. 4 and 5
- D. 7 and 8

> [!success]- Show answer
> **B. 3 and 6** — the switch is the opposite of PCs, routers, and firewalls.

### 8. A **straight-through** cable connects pin 1 on one end to:
- A. Pin 1 on the other end
- B. Pin 2 on the other end
- C. Pin 3 on the other end
- D. Pin 6 on the other end

> [!success]- Show answer
> **A. Pin 1** — a straight-through cable keeps each pin on the same number.

### 9. Which cable is used to connect **two switches** on older equipment?
- A. Straight-through
- B. Crossover
- C. Rollover
- D. Console

> [!success]- Show answer
> **B. Crossover** — like devices use the same pin pairs, so the cable must reverse them.

### 10. What does **Auto MDI-X** do?
- A. Doubles the cable speed
- B. Detects the neighbor's pins and adjusts automatically
- C. Blocks electromagnetic interference
- D. Converts copper to fibre

> [!success]- Show answer
> **B.** It automatically detects which pins the neighbor transmits on and adjusts its own transmit/receive pins.

---

## 🅱️ Section B — True or False (5 marks)

### 1. UTP cables have a metallic shield that protects against interference.
> [!success]- Show answer
> **False** — UTP is **unshielded**. The **twist** helps protect against EMI instead.

### 2. Twisting the wire pairs helps reduce electromagnetic interference.
> [!success]- Show answer
> **True** — the twist protects against EMI.

### 3. 10BASE-T uses all four pairs of wires.
> [!success]- Show answer
> **False** — 10BASE-T uses only **2 pairs (4 wires)**.

### 4. In 1000BASE-T and 10GBASE-T, each pair is bidirectional.
> [!success]- Show answer
> **True** — no pair is dedicated only to transmit or only to receive.

### 5. A crossover cable reverses the 1&2 and 3&6 pairs.
> [!success]- Show answer
> **True** — pin 1→3, 2→6, 3→1, and 6→2.

---

## 🅲 Section C — Fill in the Blank (5 marks)

### 1. Copper Ethernet standards are defined in the IEEE ________ standard.
> [!success]- Show answer
> **802.3**

### 2. UTP stands for Unshielded ________ Pair.
> [!success]- Show answer
> **Twisted**

### 3. One byte is equal to ________ bits.
> [!success]- Show answer
> **8**

### 4. 100BASE-T is also known as ________ Ethernet.
> [!success]- Show answer
> **Fast**

### 5. A ________ cable connects pin 1 on one end to pin 3 on the other.
> [!success]- Show answer
> **crossover**

---

## 🅳 Section D — Short Answer (6 marks)

### 1. Explain the difference between a straight-through and a crossover cable. (2 marks)
> [!success]- Show answer
> - A **straight-through** cable connects each pin to the **same pin** on the other end (1→1, 2→2, 3→3, 6→6) and joins **unlike** devices.
> - A **crossover** cable **reverses** the pairs (1→3, 2→6, 3→1, 6→2) and joins **like** devices.

### 2. Which pins do PCs, routers, and firewalls use compared with switches? (2 marks)
> [!success]- Show answer
> - **PCs, routers, and firewalls** transmit on **1 & 2** and receive on **3 & 6**.
> - **Switches** transmit on **3 & 6** and receive on **1 & 2**.

### 3. What is Auto MDI-X and why does it matter? (2 marks)
> [!success]- Show answer
> - **Auto MDI-X** automatically detects which pins the neighbor is transmitting on and adjusts its own transmit/receive pins.
> - It means modern devices work with either **straight-through** or **crossover** cables, so the cable type no longer matters on newer equipment.

---

## 🅴 Section E — Scenario (4 marks)

Two **switches** are connected with a **straight-through** cable on older equipment, and they cannot communicate. Explain why, and what you would do to fix it.

**Name the cause, the pin problem, and the solution.**

> [!success]- Show answer
> 1. **Both devices are switches**, so both transmit on pins **3 & 6** and receive on pins **1 & 2**.
> 2. Because they use the **same** pin pairs, each switch is transmitting on pins the other is **not receiving** on — so communication fails.
> 3. Replace the cable with a **crossover cable**, which reverses pairs **1&2** and **3&6** so transmit reaches receive.
> 4. On modern equipment, **Auto MDI-X** would detect the mismatch and correct it automatically.

---

## 📊 Score Tracker

| Score | Level | Next Step |
| --- | --- | --- |
| **27–30** | Excellent | Move on to the next topic |
| **22–26** | Good | Review missed questions |
| **18–21** | Needs work | Re-read the cabling notes |
| **Below 18** | Restudy | Start from [[Interfaces And Cables]] |

## 🔁 Review These Notes

- [[Bits and Bytes]] — bits, bytes, and speed units
- [[Network Protocols]] — physical vs logical standards
- [[Ethernet]] — the family of LAN standards
- [[Ethernet Standards (copper)]] — IEEE 802.3 and speeds
- [[UTP Cable]] — twisted pairs and RJ-45
- [[10BASE-T, 100BASE-T]] — 2-pair pin usage
- [[1000BASE -T, 10GBASE-T]] — 4-pair bidirectional wiring
- [[Straight-through cable]] — unlike devices
- [[Cross Over Cable]] — like devices
- [[Auto MDIX]] — automatic pin correction

---

### 🔗 Related Notes
[[Interfaces And Cables]] · [[Ethernet]] · [[Ethernet Standards (copper)]] · [[UTP Cable]] · [[10BASE-T, 100BASE-T]] · [[1000BASE -T, 10GBASE-T]] · [[Straight-through cable]] · [[Cross Over Cable]] · [[Auto MDIX]]
