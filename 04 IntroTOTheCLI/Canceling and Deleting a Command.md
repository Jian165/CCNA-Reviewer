---
tags:
  - ccna
  - networking
  - cisco
  - cli
  - security
aliases:
  - Canceling and Deleting a Command
  - The `no` Command
  - no command
---

# 🗑️ Canceling and Deleting a Command

> [!abstract] In one line
> Put **`no`** in front of a command to cancel/undo it — for example `no service password-encryption` stops *future* passwords from being encrypted, but it does **not** decrypt passwords that are already encrypted.

## 🚫 The `no` Prefix

To cancel or delete a command you entered, type **`no`** in front of it:

```
Router(config)#no service password-encryption
Router(config)#do sh run
Building configuration...

Current configuration: 769 bytes
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Router
!
enable secret 5 $1$mERr$YlCkLMCTYWwkF1Ccndt11.
enable password 7 08026F6028
```

> [!warning] Already-encrypted passwords stay encrypted
> Disabling `service password-encryption` does **not** decrypt existing passwords. A **new** password you enter afterwards will be in **clear text**, not encrypted.

## 📊 `service password-encryption` Summary

| State | Current passwords | Future passwords | `enable secret` |
| --- | --- | --- | --- |
| **Enabled** | Encrypted | Encrypted | Always encrypted — **unaffected** |
| **Disabled** (with `no`) | Remain encrypted — **not decrypted** | **Not encrypted** (clear text) | Always encrypted — **unaffected** |

## 🧭 Review: CLI Modes Learned

| Mode | Prompt | How to enter | What you can do |
| --- | --- | --- | --- |
| **User EXEC** | `Router>` | Default on connect | Limited viewing only |
| **Privileged EXEC** | `Router#` | `enable` | View config, save, reload |
| **Global configuration** | `Router(config)#` | `configure terminal` | Make configuration changes |

> [!success] Key takeaway
> Prefix a command with **`no`** to undo it. With `no service password-encryption`, existing passwords stay encrypted, new ones are clear text, and **`enable secret` is always encrypted either way**.

---

### 🧭 Learning Path
← Previous: [[Enable Secret Command]] · Up: [[Intro To The CLI]] · Next → [[Day 04 Lab - Basic Device Security.pkt]]

### 🔗 Related Notes
[[Intro To The CLI]] · [[Service Password Encryption]] · [[Enable Password]] · [[Enable Secret Command]] · [[Global Configuration Mode]]
