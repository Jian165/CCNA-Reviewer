---
tags:
  - ccna
  - networking
  - cisco
  - cli
aliases:
  - Saving Configuration
  - Running Config and Startup Config
  - copy running-config startup-config
---

# 💾 Saving Configuration

> [!abstract] In one line
> Save the **running-config** (active in RAM) to the **startup-config** (stored in NVRAM) from privileged EXEC mode using `write`, `write memory`, or `copy running-config startup-config`.

## 🔄 Running vs Startup Configuration

| File | Where it lives | Behaviour |
| --- | --- | --- |
| **running-config** | RAM (active) | The configuration currently in use — **lost on reload** if not saved |
| **startup-config** | NVRAM (persistent) | Loaded when the device **boots** — survives a reload |

## 💽 Three Ways to Save

All three commands are run from **privileged EXEC mode** and perform the **same function**.

### 1. `write`

```
Router#write
Building configuration...
[OK]
```

### 2. `write memory`

```
Router#write memory
Building configuration...
[OK]
```

### 3. `copy running-config startup-config`

```
Router#copy running-config startup-config
Destination filename [startup-config]?
Building configuration...
[OK]
Router#
```

> [!tip] Recommended
> `copy running-config startup-config` describes exactly what happens. `write` and `write memory` are older shortcuts you will still see often.

## ✅ Confirming the Save

`show startup-config` now displays the **same configuration** as `show running-config`.

> [!info] Only the beginning is shown
> The output shown is just the start of the configuration — there is more below. The full output is explored in the [[Day 04 Lab - Basic Device Security.pkt|Packet Tracer lab]].

## ⚠️ The Plain-Text Password Problem

The `enable password` appears **in plain text** in the configuration. This is a **security risk**: anyone who glances at it knows how to reach privileged EXEC mode, and then global configuration mode, to change the device.

> [!warning] Fix it
> Level up security with the **`service password-encryption`** command in **global configuration mode** — see [[Service Password Encryption]].

![[Pasted image 20261123143601.png]]

> [!success] Key takeaway
> Save with `write`, `write memory`, or `copy running-config startup-config` (all from `Router#`). Verify with `show startup-config`. Remember that an `enable password` shows in **clear text** until you encrypt it.

---

### 🧭 Learning Path
← Previous: [[Enable Password]] · Up: [[Intro To The CLI]] · Next → [[Service Password Encryption]]

### 🔗 Related Notes
[[Intro To The CLI]] · [[Enable Password]] · [[Service Password Encryption]] · [[Enable Secret Command]] · [[Privileged EXEC Mode]]
