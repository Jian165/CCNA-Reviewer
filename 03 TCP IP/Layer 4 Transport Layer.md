---
tags:
  - ccna
  - networking
  - tcpip
  - layers
aliases:
  - Transport Layer
  - Layer 4
---

# 🚚 Transport Layer (Layer 4)

> [!abstract] In one line
> The **Transport layer** provides end-to-end communication between application processes using **port numbers**.

## 🎯 Role of Layer 4

A server can run several services at the same time. The Transport layer makes sure a message reaches the correct one.

| Server process | Port number |
| --- | --- |
| Web server | **80** |
| File server | **21** |

> [!important] Process-to-process
> Layer 4 communication is also called **process-to-process** or **service-to-service** communication. It lets a host keep several data streams separate at the same time.

![[Pasted image 20261122140310.png]]

## 🔢 Port Numbers

A **port number** identifies a process running on a host.

- PC1 sends a web request to **port 80** on SRV1.
- If PC1 wanted the file server, it would send the request to **port 21**.
- Port numbers let one host run many services at once.

> [!warning] Do not confuse ports
> A **port number** is logical. It is not a physical port like an RJ-45 connector or SFP port.

## 🧱 Main Transport Protocols

The two most prominent Transport-layer protocols are **TCP** and **UDP**. They offer different features, which are covered in more detail later.

| Protocol | Full name | Exam idea |
| --- | --- | --- |
| **TCP** | Transmission Control Protocol | Reliable, connection-oriented transport |
| **UDP** | User Datagram Protocol | Faster, connectionless transport |

> [!tip] Later topic
> TCP and UDP differences are covered in more detail later. For now, know that both are major Layer 4 protocols.

## 📍 Where It Runs

- Layer 4 mainly runs on the communicating **hosts**.
- Routers normally operate at Layer 3 using IP addresses.
- There are exceptions, but they are covered later.

## 🧠 Quick Recap

| Topic | Fact |
| --- | --- |
| **Layer number** | 4 |
| **Main job** | End-to-end communication between processes |
| **Addressing** | Port numbers |
| **Examples** | TCP, UDP |
| **Runs mainly on** | End hosts |

> [!success] Key takeaway
> Layer 4 uses port numbers to deliver data to the correct application process on the destination host.

---

### 🧭 Learning Path
← Previous: [[Layer 5 Application Layer]] · Up: [[TCP IP]] · Next → [[Local 3 Internet Layer]]

### 🔗 Related Notes
[[TCP IP]] · [[The TCP IP Model]] · [[Layer 5 Application Layer]] · [[Local 3 Internet Layer]] · [[Encapsulation & decapsulation]]
