---
tags:
  - ccna
  - networking
  - cisco
  - cli
  - security
aliases:
  - Enable Secret
  - enable secret command
  - MD5 enable secret
---

# 🛡️ The `enable secret` Command

> [!abstract] In one line
> **`enable secret <password>`** is the **more secure** way to protect privileged EXEC mode: it is always encrypted with **MD5 (type 5)**, and it **overrides** `enable password` if both are set.

## 🔐 Configuring the Secret

```
Router(config)#enable secret Cisco
Router(config)#do sh run
Building configuration...

Current configuration: 766 bytes
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
service password-encryption
!
hostname Router
!
enable secret 5 $1$mERr$YlCkLMCTYWwkF1Ccndt11.
enable password 7 08026F6028
```

- The password used here is `Cisco` with an **upper-case C** — still **case-sensitive**.
- The running configuration shows:
  - `enable secret 5 $1$mERr$YlCkLMCTYWwkF1Ccndt11.`
  - `enable password 7 08026F6028`

## 💡 The `do` Trick

Because you are still in **global configuration mode**, the `show running-config` command is prefixed with **`do`**:

| Typed | Meaning |
| --- | --- |
| `do sh run` | Run the privileged EXEC command `show running-config` from a configuration mode |

> [!tip] Shortcuts used
> `sh` = `show`, `run` = `running-config`. The `do` trick lets you run privileged EXEC commands like `show running-config` or `show startup-config` from **any configuration level**.

## 🔢 Understanding the Encryption Numbers

| Number in config | Encryption type | Source | Security |
| --- | --- | --- | --- |
| **5** | **MD5** | `enable secret` | **Much more secure** — can still be cracked, but no password is invincible |
| **7** | Cisco proprietary | `service password-encryption` | Weak — crackable in seconds |

> [!success] Key takeaway
> **`5` = MD5 = strong; `7` = Cisco proprietary = weak.**

## ⚖️ `enable secret` vs `enable password`

| Question | Answer |
| --- | --- |
| Is `enable password` replaced/removed? | **No** — it remains in the configuration |
| If both are configured, which one works? | Only **`enable secret`** — `enable password` is **ignored** |
| Does `service password-encryption` affect `enable secret`? | **No** — the secret is **always encrypted**, whether or not that command is set |

> [!important] Best practice
> **Always use `enable secret` instead of `enable password`** — it is more secure.

---

### 🧭 Learning Path
← Previous: [[Service Password Encryption]] · Up: [[Intro To The CLI]] · Next → [[Canceling and Deleting a Command]]

### 🔗 Related Notes
[[Intro To The CLI]] · [[Enable Password]] · [[Service Password Encryption]] · [[Saving Configuration]] · [[Canceling and Deleting a Command]]
