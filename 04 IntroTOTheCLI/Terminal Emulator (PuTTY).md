---
tags:
  - ccna
  - networking
  - cisco
  - cli
aliases:
  - Terminal Emulator
  - PuTTY
  - Terminal Emulator (PuTTY)
---

# 🖥️ Terminal Emulator (PuTTY)

> [!abstract] In one line
> After connecting the console cable, you use a **terminal emulator** such as **PuTTY** to reach the CLI. Cisco's serial defaults are **9600 baud, 8 data bits, 1 stop bit, no parity, no flow control**.

## 📥 Getting PuTTY

- A **terminal emulator** is the program that gives you access to the device's CLI.
- **PuTTY** is a popular free choice, available at **putty.org**.

![[Pasted image 20261123133941.png]]

## 🔗 Connecting

1. Select **Serial** as the connection type.
2. Click **Open**.
3. You should now be connected to the CLI.

> [!tip] Default settings work
> You can usually connect with the default settings. But click **Serial** in the left-hand menu to view and edit them — the defaults match Cisco devices, so you should **never need to change them**.

## ⚙️ Cisco Serial Defaults (Exam Material)

| Setting | Cisco default | What it means |
| --- | --- | --- |
| **Speed (baud rate)** | **9,600 bits per second** | How fast data is sent over the serial line |
| **Data bits** | **8** | 8 bits of data are sent at a time |
| **Stop bits** | **1** | One stop bit marks the end of each 8-bit group |
| **Parity** | **None** | Parity is used to detect errors |
| **Flow control** | **None** | Controls the flow of data from transmitter to receiver |

> [!important] Remember for the exam
> **9600 / 8 / 1 / none / none.** Data bits, stop bits, parity, and flow control details are **outside the scope of the CCNA** — just memorise Cisco's defaults.

## 🚀 First Boot

When you connect to a device that is booting for the first time:

1. You are asked whether you would like to enter the **initial configuration dialog**.
2. Answer **no**.
3. Press **Enter** to get started.
4. You are now free to type commands into the CLI.

![[Pasted image 20261123134157.png]]

> [!success] Key takeaway
> Use a **terminal emulator** (e.g. PuTTY) with **Serial** selected. Cisco's serial defaults — **9600 baud, 8 data bits, 1 stop bit, no parity, no flow control** — are exam material. Decline the initial configuration dialog on first boot.

---

### 🧭 Learning Path
← Previous: [[Console Port]] · Up: [[Intro To The CLI]] · Next → [[User EXEC Mode]]

### 🔗 Related Notes
[[Intro To The CLI]] · [[Console Port]] · [[User EXEC Mode]] · [[Privileged EXEC Mode]]
