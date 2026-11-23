---
tags:
  - ccna
  - networking
  - cisco
  - cli
  - exam
aliases:
  - Intro To The CLI Exam
  - Intro to the CLI Practice Exam
---

# 📝 Intro to the CLI — Practice Exam

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

### 1. What is **Cisco IOS**?
- A. A standard for copper cabling
- B. The operating system used on Cisco devices
- C. A graphical configuration tool
- D. A routing protocol

> [!success]- Show answer
> **B.** Cisco IOS is the operating system on Cisco devices — like Windows on a PC. It is **not** related to Apple's iOS.

### 2. What does **CLI** stand for?
- A. Cisco LAN Interface
- B. Command Line Interface
- C. Configured Logical Interface
- D. Console Link Interface

> [!success]- Show answer
> **B. Command Line Interface** — the text interface used to configure Cisco devices.

### 3. Which port must you use when configuring a device for the first time?
- A. Ethernet port
- B. USB mini-B port only
- C. Console port
- D. Auxiliary port

> [!success]- Show answer
> **C. Console port** — you bring your laptop to the device and connect directly. Remote methods are covered later.

### 4. What is the actual name of the cable used to connect a PC to an RJ-45 console port?
- A. Straight-through cable
- B. Crossover cable
- C. Rollover cable
- D. Console-over-Ethernet cable

> [!success]- Show answer
> **C. Rollover cable** — pin 1→8, 2→7, 3→6, 4→5. It is different from an Ethernet crossover cable.

### 5. What is the default **baud rate** for a Cisco console connection?
- A. 1,200 bps
- B. 4,800 bps
- C. 9,600 bps
- D. 115,200 bps

> [!success]- Show answer
> **C. 9,600 bits per second** — with 8 data bits, 1 stop bit, no parity, and no flow control.

### 6. Which prompt indicates **privileged EXEC mode**?
- A. `Router>`
- B. `Router#`
- C. `Router(config)#`
- D. `Router(config-if)#`

> [!success]- Show answer
> **B. `Router#`** — the `#` (pound/hash) appears after the `enable` command.

### 7. Which command enters **global configuration mode**?
- A. `enable`
- B. `configure terminal`
- C. `show running-config`
- D. `write memory`

> [!success]- Show answer
> **B. `configure terminal`** — short form `conf t`. The prompt becomes `Router(config)#`.

### 8. Which command gives the **strongest** protection for privileged EXEC mode?
- A. `enable password`
- B. `service password-encryption`
- C. `enable secret`
- D. `no service password-encryption`

> [!success]- Show answer
> **C. `enable secret`** — it uses MD5 type 5 encryption, is always encrypted, and overrides `enable password`.

### 9. In the config line `enable password 7 08026F6028`, what does the **7** mean?
- A. Seven characters in the password
- B. MD5 encryption
- C. Cisco's proprietary type 7 encryption from `service password-encryption`
- D. Seven failed login attempts

> [!success]- Show answer
> **C.** Type 7 is Cisco's proprietary (and weak) encryption produced by `service password-encryption`. MD5 is type **5**.

### 10. Which command **saves** the running configuration to the startup configuration?
- A. `show startup-config`
- B. `copy startup-config running-config`
- C. `copy running-config startup-config`
- D. `reload`

> [!success]- Show answer
> **C. `copy running-config startup-config`** — also `write` or `write memory` do the same thing.

---

## 🅱️ Section B — True or False (5 marks)

### 1. Cisco IOS is the same operating system as Apple's iOS.
> [!success]- Show answer
> **False** — they are unrelated operating systems that share a name.

### 2. A rollover cable and an Ethernet crossover cable wire the pins the same way.
> [!success]- Show answer
> **False** — rollover is 1→8, 2→7, 3→6, 4→5; crossover is 1→3, 2→6, 3→1, 6→2.

### 3. You can change the device configuration from user EXEC mode.
> [!success]- Show answer
> **False** — user EXEC mode (`Router>`) is limited/read-only. Use privileged EXEC and then global configuration mode.

### 4. `enable secret` is always encrypted, even without `service password-encryption`.
> [!success]- Show answer
> **True** — the secret uses MD5 type 5 regardless of the `service password-encryption` setting.

### 5. `no service password-encryption` decrypts passwords that were already encrypted.
> [!success]- Show answer
> **False** — existing passwords stay encrypted; only **future** passwords are stored in clear text.

---

## 🅲 Section C — Fill in the Blank (5 marks)

### 1. The prompt `Router>` uses the ________ symbol to indicate user EXEC mode.
> [!success]- Show answer
> **`>`** (greater-than sign). Privileged EXEC uses `#`.

### 2. The short form of `configure terminal` is ________ ________.
> [!success]- Show answer
> **`conf t`**

### 3. Cisco console defaults are 9600 baud, 8 data bits, 1 stop bit, no parity, and no ________ ________.
> [!success]- Show answer
> **flow control**

### 4. The number ________ in `enable secret 5 ...` indicates MD5 encryption.
> [!success]- Show answer
> **5** (type 7 is Cisco's weaker proprietary encryption).

### 5. Prefix a command with ________ to cancel or undo it.
> [!success]- Show answer
> **`no`**

---

## 🅳 Section D — Short Answer (6 marks)

### 1. Name the three CLI modes, their prompts, and how to reach them. (2 marks)
> [!success]- Show answer
> - **User EXEC** — `Router>` — the default mode on connection.
> - **Privileged EXEC** — `Router#` — reached with `enable`.
> - **Global configuration** — `Router(config)#` — reached from privileged EXEC with `configure terminal`.

### 2. Compare `enable password` and `enable secret`. (2 marks)
> [!success]- Show answer
> - `enable password` stores a clear-text password (or weak type 7 if `service password-encryption` is on).
> - `enable secret` uses strong **MD5 type 5**, is **always encrypted**, and if both are configured the `enable password` is **ignored**. Always use `enable secret`.

### 3. Name three commands that save the configuration and explain why saving matters. (2 marks)
> [!success]- Show answer
> - `write`, `write memory`, and `copy running-config startup-config` (all from privileged EXEC).
> - The **running-config** lives in RAM and is lost on reload; copying it to **startup-config** in NVRAM makes it load at boot so your changes survive a restart.

---

## 🅴 Section E — Scenario (4 marks)

You set `enable password CCNA`, save the configuration, and then view `show startup-config`. You can read the password in plain text. Explain the risk, describe how to hide it, explain why that method is still weak, and state the best solution.

> [!success]- Show answer
> 1. **Risk:** anyone who glances at the config knows the password and can enter privileged EXEC mode, then global configuration mode, to change the device.
> 2. **Quick fix:** run `service password-encryption` in global configuration mode. The password becomes `enable password 7 08026F6028` — type 7 Cisco proprietary encryption.
> 3. **Why it is weak:** type 7 can be cracked with freely available tools in seconds, so it only hides the password from a casual glance.
> 4. **Best solution:** use `enable secret <password>` instead — MD5 type 5, always encrypted. If both commands are set, IOS ignores the `enable password`.

---

## 📊 Score Tracker

| Score | Level | Next Step |
| --- | --- | --- |
| **27–30** | Excellent | Move on to the next topic |
| **22–26** | Good | Review missed questions |
| **18–21** | Needs work | Re-read the CLI notes |
| **Below 18** | Restudy | Start from [[Intro To The CLI]] |

## 🔁 Review These Notes

- [[CLI]] — Cisco IOS, CLI vs GUI
- [[Console Port]] — console ports, rollover cable
- [[Terminal Emulator (PuTTY)]] — serial defaults
- [[User EXEC Mode]] — `Router>` read-only mode
- [[Privileged EXEC Mode]] — `enable`, `Router#`, `?`
- [[Cisco IOS CLI Shortcuts]] — Tab, abbreviations
- [[Global Configuration Mode]] — `conf t`
- [[Enable Password]] — protecting privileged EXEC
- [[Saving Configuration]] — running vs startup config
- [[Service Password Encryption]] — type 7 encryption
- [[Enable Secret Command]] — MD5 type 5 encryption
- [[Canceling and Deleting a Command]] — the `no` prefix

---

### 🧭 Learning Path
← Previous: [[Day 04 Lab - Basic Device Security.pkt]] · Up: [[Intro To The CLI]]

### 🔗 Related Notes
[[Intro To The CLI]] · [[CLI]] · [[Console Port]] · [[Privileged EXEC Mode]] · [[Global Configuration Mode]] · [[Enable Password]] · [[Saving Configuration]] · [[Service Password Encryption]] · [[Enable Secret Command]]
