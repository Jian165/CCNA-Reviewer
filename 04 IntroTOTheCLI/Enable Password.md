---
tags:
  - ccna
  - networking
  - cisco
  - cli
  - security
aliases:
  - Enable Password
  - enable password command
---

# 🔑 The `enable password` Command

> [!abstract] In one line
> Use **`enable password <password>`** in global configuration mode to require a password before a user can enter privileged EXEC mode. Passwords are **case-sensitive**.

## 🛡️ Why Protect Privileged EXEC Mode?

You don't want just anyone to be able to **view** the configuration (a security risk), let alone **change** it.

- Configure the password with the `enable password` command in **global configuration mode**.
- After that, entering `enable` from user EXEC mode prompts for the password.
- 
## ❓ Using `?` While Typing a Command

The question mark behaves differently depending on the **space**:

```
Router(config)#enable password? password
Router(config)#enable password ?
  7      Specifies a HIDDEN password will follow
  LINE   The UNENCRYPTED (cleartext) 'enable' password
  level  Set exec level password
Router(config)#enable password CCNA ?
  <cr>
Router(config)#enable password CCNA
Router(config)#
```

| What you type | What `?` shows |
| --- | --- |
| `enable password?` (**no space**) | All possible **completions of the current word** — only `password` fits here |
| `enable password ?` (**with a space**) | All **options for the next part** of the command |

> [!important] Reading the options
> - **`LINE`** in ALL CAPS means you do **not** type the word `LINE` — you type a line of text which becomes the password (here `CCNA`).
> - **`7`** means a hidden/encrypted password will follow.
> - **`level`** sets an exec-level password.
> - **`<cr>`** means there are no further options — just press **Enter** to run the command.

> [!warning] Case-sensitive
> Passwords are **case-sensitive**. `CCNA` and `ccna` are **different** passwords.

## 🧪 Testing the Password

```
Router(config)#enable password CCNA
Router(config)#exit
Router#
%SYS-5-CONFIG_I: Configured from console by console
Router#exit
```

- `exit` from global configuration mode returns to **privileged EXEC mode**.
- The message `%SYS-5-CONFIG_I: Configured from console by console` simply confirms a configuration change was made.
- `exit` again from privileged EXEC mode **logs you out** and returns to the starting screen.

```
Router>enable
Password:
Router#
```

- The password is **not displayed as you type it** — a security measure.
- Three wrong attempts produce **`% Bad secrets`** and deny access.

```
Router>enable
Password:
Password:
Password:
% Bad secrets
Router>
```

## 🔁 Full Review: Set and Test

```
Router>enable
Router#configure terminal
Enter configuration commands, one per line. End with CNTL/Z.
Router(config)#enable password CCNA
Router(config)#exit
Router#
%SYS-5-CONFIG_I: Configured from console by console

Router#exit

Router>enable
Password:
Router#
```

> [!tip] Practice is essential
> The CLI takes time to get used to. Work through these same tasks yourself in the [[Day 04 Lab - Basic Device Security.pkt|Packet Tracer lab]] — hands-on practice is **essential** to getting comfortable.

> [!success] Key takeaway
> `enable password <password>` (global config) protects privileged EXEC mode. Use `?` with **no space** for word completions and with a **space** for next-option help. Passwords are **case-sensitive**, hidden when typed, and three failures give **bad secrets**.

---

### 🧭 Learning Path
← Previous: [[Global Configuration Mode]] · Up: [[Intro To The CLI]] · Next → [[Saving Configuration]]

### 🔗 Related Notes
[[Intro To The CLI]] · [[Privileged EXEC Mode]] · [[Global Configuration Mode]] · [[Enable Secret Command]] · [[Service Password Encryption]]
