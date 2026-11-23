---
tags:
  - ccna
  - networking
  - cisco
  - cli
  - cabling
aliases:
  - Console Port
  - Console Connection
  - Rollover Cable
---

# 🔌 Connecting via the Console Port

> [!abstract] In one line
> The first time you configure a Cisco device, you connect your laptop directly to its **console port** — usually with a **rollover cable** and a USB adapter.

## 🧭 Why the Console Port?

There are several ways to connect to a Cisco device, but this course starts with the **console port**:

- You typically **bring your laptop to the device** and plug into its console port.
- Remote connection methods exist, but they are covered later.
- **When you first configure a device, you must use the console port.**

![[Pasted image 20261123133455.png]]

## 🔎 Console Ports on a Cisco Switch

A Cisco Catalyst switch typically has **two console ports**:

| Console port | Connector |
| --- | --- |
| **RJ-45** | Looks just like the switch's network ports |
| **USB mini-B** | Smaller USB-style connector |

You can use either one. The example below uses the **RJ-45** console port.

## 🧵 The Rollover Cable

To use the RJ-45 console port you need the proper cable:

- One end: **RJ-45** connector (like an Ethernet UTP cable).
- Other end: **DB-9** connector (a serial port).
- Most modern laptops have **no serial port**, so you also need a **USB-to-serial adapter**.

![[Pasted image 20261123133702.png]]

> [!important] Name to know
> The actual name of this cable is a **rollover cable**. The name is similar to *crossover cable*, but it is a **different** cable — it is not an Ethernet UTP crossover cable.

## 📌 Rollover Pinout

Like an Ethernet UTP cable, a rollover cable uses **8 pins on each end**. But the pins connect in reverse order:

| This end | Other end |
| --- | --- |
| Pin **1** | Pin **8** |
| Pin **2** | Pin **7** |
| Pin **3** | Pin **6** |
| Pin **4** | Pin **5** |
| Pin **5** | Pin **4** |
| Pin **6** | Pin **3** |
| Pin **7** | Pin **2** |
| Pin **8** | Pin **1** |

> [!tip] Memory hook
> Pin 1 goes to 8, pin 2 goes to 7, and so on — the pin numbers **add up to 9**.

## ⚖️ Rollover vs Crossover

| Cable | Pin mapping | Used for |
| --- | --- | --- |
| **Rollover** | 1→8, 2→7, 3→6, 4→5 | Connecting a PC to a device's **console port** |
| **Crossover** | 1→3, 2→6, 3→1, 6→2 | Connecting **like** Ethernet devices |

> [!success] Key takeaway
> Initial configuration requires a **console connection**. The RJ-45 console cable is a **rollover cable** (1→8, 2→7 …) and usually needs a **USB adapter** on a modern laptop.

---

### 🧭 Learning Path
← Previous: [[CLI]] · Up: [[Intro To The CLI]] · Next → [[Terminal Emulator (PuTTY)]]

### 🔗 Related Notes
[[Intro To The CLI]] · [[CLI]] · [[Terminal Emulator (PuTTY)]] · [[Cross Over Cable]] · [[UTP Cable]]
