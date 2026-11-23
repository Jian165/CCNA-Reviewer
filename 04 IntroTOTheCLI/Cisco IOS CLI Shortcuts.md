---
tags:
  - ccna
  - networking
  - cisco
  - cli
aliases:
  - Cisco IOS CLI Shortcuts
  - CLI Shortcuts
  - Tab Completion
---

# ⌨️ Cisco IOS CLI Shortcuts

> [!abstract] In one line
> The **Tab** key completes a command for you, and you can often type only an **unambiguous abbreviation** (like `en` for `enable`) and press Enter.

## 🔄 Tab Completion

```
Router>en
Router>enable
Router#
```

Press **Tab** and the CLI automatically finishes the word, showing the complete command on a new line.

> [!tip] Even faster
> You don't even need Tab. Typing **`en`** and pressing Enter is enough — the router knows you mean `enable` and takes you straight to privileged EXEC mode. This saves a lot of typing when entering many commands.

![[Pasted image 20261123135632.png]]

## ⚠️ The Limit: Ambiguous Commands

Abbreviations only work when the command is **unique**:

```
Router>e
Ambiguous command: "e"
Router>
```

- `en` works because **enable** is the only command starting with **en** in user EXEC mode.
- `e` fails because **more than one** command starts with **e**.

Use `?` to see them:

```
Router>e?
enable exit
Router>e
```

- `enable` and `exit` both start with `e`.
- Shortest form of **enable** → **`en`**
- Shortest form of **exit** → **`ex`**

> [!success] Key takeaway
> **Tab** completes commands, and short forms like `en`, `ex`, and `conf t` are valid. If an abbreviation matches more than one command, IOS reports **Ambiguous command** — use `?` to check your options.

---

### 🧭 Learning Path
← Previous: [[Privileged EXEC Mode]] · Up: [[Intro To The CLI]] · Next → [[Global Configuration Mode]]

### 🔗 Related Notes
[[Intro To The CLI]] · [[Privileged EXEC Mode]] · [[Global Configuration Mode]] · [[Enable Password]]
