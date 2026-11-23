---
tags:
  - ccna
  - networking
  - cisco
  - cli
aliases:
  - Privileged EXEC Mode
  - Privileged Mode
  - Enable Mode
---

# 🔐 Privileged EXEC Mode

> [!abstract] In one line
> Enter `enable` in user EXEC mode to reach **privileged EXEC mode**, marked by the **`#`** prompt (`Router#`). It gives full access to **view** the configuration, save it, restart the device, and more.

## 🔑 Entering Privileged EXEC Mode

```
Router>enable
Router#
```

| Prompt | Mode |
| --- | --- |
| `Router>` | User EXEC mode (`>`) |
| `Router#` | **Privileged** EXEC mode (`#`, also called a pound sign or hash tag) |

## 🛠️ What It Allows

Privileged EXEC mode provides **complete access** to:

- **View** the device's configuration.
- **Restart** (reload) the device.
- **Save** the current configuration file.
- **Change the time** on the device.
- Many other administrative tasks.

> [!warning] Not the configuration mode
> Privileged EXEC mode is **not** where you actually change the configuration. For that you need [[Global Configuration Mode]] (`configure terminal`).

![[Pasted image 20261123135114.png]]

## ❓ Discovering Commands with `?`

Type a **question mark** to see the commands available in the current mode:

- User EXEC mode (left screenshot) shows a short list.
- Privileged EXEC mode (right screenshot) shows many more.

> [!info] Packet Tracer screenshots
> These comparisons were captured in **Cisco Packet Tracer**, a network simulator. It is a **fantastic resource for the CCNA** and you don't really need anything else for the exam — but it is limited beyond CCNA. On a real device you would see **even more** commands.

![[Pasted image 20261123135439.png]]

> [!success] Key takeaway
> `enable` takes you from `Router>` to `Router#`. Privileged EXEC mode gives full **view and administrative** access (including saving config), but actual configuration changes happen in global configuration mode. Use `?` to list available commands.

---

### 🧭 Learning Path
← Previous: [[User EXEC Mode]] · Up: [[Intro To The CLI]] · Next → [[Cisco IOS CLI Shortcuts]]

### 🔗 Related Notes
[[Intro To The CLI]] · [[User EXEC Mode]] · [[Cisco IOS CLI Shortcuts]] · [[Global Configuration Mode]] · [[Enable Password]]
