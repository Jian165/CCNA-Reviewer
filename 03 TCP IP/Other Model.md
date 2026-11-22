---
tags:
  - ccna
  - networking
  - tcpip
  - models
aliases:
  - Other Models
  - Model Names
  - Four-Layer TCP/IP Model
---

# 🧭 Other Model Names

> [!abstract] In one line
> Different resources use different layer counts and names, but the jobs performed by the layers are mostly the same.

## 🧩 Common Models

| Model | Layers | Layer names |
| --- | --- | --- |
| **Original TCP/IP model** | 4 | Application, Transport, Internet, Link |
| **OSI model** | 7 | Application, Presentation, Session, Transport, Network, Data Link, Physical |
| **Adapted 5-layer model** | 5 | Application, Transport, Network, Data Link, Physical |
| **This course's model** | 5 | Application, Transport, Internet, Local Network, Physical |

The adapted 5-layer model is probably the most common in books and other resources. This course recommends its own names because they match each layer's job, but the common names are also widely used.

![[Pasted image 20261122142227.png]]

## 🔍 Main Differences

| Course name | Common/Often-used name | Layer number |
| --- | --- | --- |
| Application | Application / Layer 7 | 5 in this course, 7 in OSI |
| Transport | Transport | 4 |
| Internet | Network | 3 |
| Local Network | Data Link | 2 |
| Physical | Physical | 1 |

> [!tip] Memory hook
> When someone says **Layer 2**, think **MAC addresses and frames**. When they say **Layer 3**, think **IP addresses and packets**.

## 🎯 What the CCNA Expects

> [!important] Do not memorize one “perfect” model
> The CCNA focuses on what each layer **does**, not on arguing about model names. Different books use different names, but the concepts are the same.

- Use the course's five-layer model while learning.
- Understand the common OSI names you will see elsewhere.
- Focus on each layer's job, addressing, protocols, and devices.

## 🧠 Quick Recap

| Topic | Fact |
| --- | --- |
| **Models vary** | 4-layer, 5-layer, and 7-layer versions exist |
| **Jobs stay similar** | Application, transport, addressing, LAN delivery, signals |
| **Layer 3** | Often called Network layer |
| **Layer 2** | Often called Data Link layer |
| **Exam focus** | Know the role, not just the name |

> [!success] Key takeaway
> Model names vary, but the layer jobs do not: ports at Layer 4, IP at Layer 3, MAC at Layer 2, and signals at Layer 1.

---

### 🧭 Learning Path
← Previous: [[OSI Model]] · Up: [[TCP IP]] · Next → [[Day 03 Lab - OSI Model.pkt]]

### 🔗 Related Notes
[[TCP IP]] · [[OSI Model]] · [[Layered models]] · [[The TCP IP Model]] · [[TCP IP Exam]]
