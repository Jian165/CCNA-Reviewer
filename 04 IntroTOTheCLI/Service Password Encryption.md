---
tags:
  - ccna
  - networking
  - cisco
  - cli
  - security
aliases:
  - Service Password Encryption
  - service password-encryption
  - Type 7 password
---

# 🔒 Service Password Encryption

> [!abstract] In one line
> **`service password-encryption`** in global configuration mode scrambles plain-text passwords in the running configuration, but its **type 7** encryption is weak and easily cracked — use [[Enable Secret Command|enable secret]] for real security.

## ⚙️ Enabling Encryption

```
Router#conf t
Enter configuration commands, one per line. End with CNTL/Z.
Router(config)#service password-encryption
```

- `conf t` is the short form of `configure terminal` (all commands have shortcuts).
- In instructional videos the full command is used; in labs, shortcuts are used a lot.

## 🔍 Checking the Result

```
Router#show running-config
Building configuration...

Current configuration: 719 bytes
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
service password-encryption
!
hostname Router
!
enable password 7 08026F6028
```

- The password `CCNA` has become **`08026F6028`**.
- The line **`service password-encryption`** appears in the configuration.

> [!important] What the `7` means
> The number **7** means Cisco's **proprietary encryption algorithm**, produced by the `service password-encryption` command. (A different number appears with `enable secret`.)

## ⚠️ Type 7 Is Not Secure

- It is better than nothing, but **still not very secure**.
- Searching for a "cisco type 7 password cracker" online yields tools that crack the password in **a few seconds**.

![[Pasted image 20261123144349.png]]

> [!tip] Looking ahead
> There is a **more secure enable password** available on Cisco devices, using a tougher type of encryption — see [[Enable Secret Command]].

> [!success] Key takeaway
> `service password-encryption` hides passwords as **type 7** (`enable password 7 ...`), but type 7 is **trivially crackable**. Use **`enable secret`** (type 5 MD5) instead.

---

### 🧭 Learning Path
← Previous: [[Saving Configuration]] · Up: [[Intro To The CLI]] · Next → [[Enable Secret Command]]

### 🔗 Related Notes
[[Intro To The CLI]] · [[Saving Configuration]] · [[Enable Password]] · [[Enable Secret Command]] · [[Canceling and Deleting a Command]]
