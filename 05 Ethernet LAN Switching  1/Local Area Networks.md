---
tags:
  - ccna
  - networking
  - lan
  - ethernet
  - switching
aliases:
  - Local Area Network
  - LAN
  - Local Area Networks
---

# 🌍 Local Area Networks (LANs)

> [!abstract] In one line
> A **LAN** is a network contained in a relatively small area; **routers connect separate LANs**, while **switches expand an existing LAN**.

![[Pasted image 20261125144648.png]]

## 🏠 What Is a LAN?

There are different ways to define a LAN, and your understanding becomes more complete as you learn more networking. At its simplest, it is a network in a **relatively small area**, such as:

- An **office floor**
- A **home network**

> [!info] Definition used here
> A LAN is the group of devices that share the same local network segment — end hosts, switch(es), and the **router interface** they connect to.

## 🚦 Routers Separate, Switches Expand

| Device | Effect on LAN boundaries |
| --- | --- |
| **Router** | Connects **separate LANs**; each router interface can belong to a different LAN |
| **Switch** | Connects devices to the **same LAN**; adding switches **expands** the LAN rather than splitting it |

> [!important] Exam point
> **Switches do not separate LANs.** Two switches connected together can still be one LAN. A LAN boundary appears where a **router interface** separates one local network from another.

## 🗺️ Reading the Diagram

| Color in the diagram | Devices shown | Number of LANs | Why |
| --- | --- | --- | --- |
| **Green** | Three PCs, one switch, and the router interface they connect to | **1** | All devices share one local network |
| **Red** | End hosts and **two connected switches** with one router interface | **1** | Two switches still form one LAN |
| **Blue** | Two switches, each connected to a **different router interface** | **2** | The router interface separates the two local networks |

## 🎯 Scope of This Folder

This folder looks at how traffic is sent and received **within** a LAN — for example, one PC sending a frame to another PC on the same LAN. Sending data **between** LANs is covered later.

> [!success] Key takeaway
> A LAN is a small-area network. **Routers separate LANs; switches expand them.** This folder focuses on switching inside a LAN, not routing between LANs.

---

### 🧭 Learning Path
← Previous: [[Intro To The CLI Exam]] · Up: [[Ethernet LAN Switching]] · Next → [[OSI Model Review]]

### 🔗 Related Notes
[[Ethernet LAN Switching]] · [[OSI Model Review]] · [[Local 2 Network Layer]] · [[Router]] · [[Switches]] · [[Network]]
