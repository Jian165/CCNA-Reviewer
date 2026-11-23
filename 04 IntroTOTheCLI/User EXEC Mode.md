---
tags:
  - ccna
  - networking
  - cisco
  - cli
aliases:
  - User EXEC Mode
  - User Mode
---

# 👤 User EXEC Mode

> [!abstract] In one line
> When you first enter the CLI you are in **user EXEC mode**, shown by the **`>`** prompt (for example `Router>`). You can **look** at a few things, but you **cannot change the configuration**.

## 🖥️ Reading the Prompt

```
Router>
```

| Part of the prompt | Meaning |
| --- | --- |
| **Router** | The device's **hostname** — the text shown always tells you which device you are on |
| **>** | The **greater-than sign** indicates **user EXEC mode** |

> [!info] Default hostname
> All devices have a hostname. The default hostname for a Cisco **router** is **Router**; a switch defaults to **Switch**.

![[Pasted image 20261123134747.png]]

## 🔒 What You Can Do

- View a **limited** set of things.
- **Cannot** make any changes to the configuration.
- Usually, you don't do anything in this mode — you move on quickly.

> [!tip] Also called...
> User EXEC mode is sometimes shortened to just **user mode**.

> [!success] Key takeaway
> `Router>` means **user EXEC mode**: limited read-only access, no configuration changes. Move to [[Privileged EXEC Mode]] with the `enable` command to get real access.

---

### 🧭 Learning Path
← Previous: [[Terminal Emulator (PuTTY)]] · Up: [[Intro To The CLI]] · Next → [[Privileged EXEC Mode]]

### 🔗 Related Notes
[[Intro To The CLI]] · [[CLI]] · [[Terminal Emulator (PuTTY)]] · [[Privileged EXEC Mode]] · [[Global Configuration Mode]]
