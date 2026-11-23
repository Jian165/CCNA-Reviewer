---
tags:
  - ccna
  - networking
  - cisco
  - cli
aliases:
  - Global Configuration Mode
  - Configuration Mode
  - configure terminal
  - conf t
---

# ⚙️ Global Configuration Mode

> [!abstract] In one line
> From privileged EXEC mode, run **`configure terminal`** (short form **`conf t`**) to enter **global configuration mode**, where you actually make changes to the device. The prompt becomes `Router(config)#`.

## 🚪 Entering Configuration Mode

```
Router>enable
Router#configure terminal
Enter configuration commands, one per line. End with CNTL/Z.
Router(config)#
```

| Item | Detail |
| --- | --- |
| **Command** | `configure terminal` |
| **Prompt after entering** | `Router(config)#` — **config** is inserted after the hostname |
| **On-screen message** | "Enter configuration commands, one per line. End with CNTL/Z." |

## 🔤 Building the Shortcut with `?`

You don't have to type the full command:

```
Router>enable
Router#con?
configure connect
Router#conf t?
terminal
Router#conf t
Enter configuration commands, one per line. End with CNTL/Z.
Router(config)#
```

1. `con?` → two options: **configure** and **connect**.
2. `conf` is therefore the **shortest unique form** of `configure`.
3. `conf t?` → only **terminal** starts with `t`, so `t` is enough.
4. Result: **`conf t`** works.

> [!tip] Remember both
> Labs often use `conf t`, but the **full command is `configure terminal`** — know it for the exam.

> [!success] Key takeaway
> `configure terminal` (`conf t`) moves you from `Router#` to `Router(config)#` — the mode where configuration changes are made. Use `?` to discover the shortest unambiguous abbreviation.

---

### 🧭 Learning Path
← Previous: [[Cisco IOS CLI Shortcuts]] · Up: [[Intro To The CLI]] · Next → [[Enable Password]]

### 🔗 Related Notes
[[Intro To The CLI]] · [[Privileged EXEC Mode]] · [[Cisco IOS CLI Shortcuts]] · [[Enable Password]] · [[Service Password Encryption]]
