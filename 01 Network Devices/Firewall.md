---
tags:
  - networking
  - security
  - device
aliases:
  - Firewall
---

# 🛡️ Firewall

> [!abstract] In one line
> Firewalls are specialty network security devices that control network traffic **entering and exiting** your network.

## 📍 Where Firewalls Sit

![[Pasted image 20261111142306.png]]

Firewalls can be placed **outside** your [[Router]] (like FW1) or **inside** your network (like FW2). What matters is that they protect the end hosts inside — such as the PCs and [[Server]]s.

Firewalls must be configured with **security rules** that determine which traffic is allowed and which is denied.

![[Pasted image 20261111142408.png]]

> [!example] Allowed vs blocked
> - ✅ PC1 in New York should be able to reach SRV1 in Tokyo, and the return traffic should also be allowed.
> - ❌ An attacker trying to access anything inside the network should be blocked.

## ⚙️ Characteristics of Firewalls

- Monitor and control network traffic based on **configured rules**.
- Can be placed **inside** or **outside** the network — filtering traffic before it reaches the router, or after it has passed through.
- Are called **next-generation firewalls** when they include more modern, advanced filtering capabilities.

## 🧩 Types of Firewalls

| Type | Description |
| --- | --- |
| **Network Firewall** | Hardware devices that filter traffic between networks |
| **Host-based Firewall** | Software applications that filter traffic entering and exiting a host machine, such as a PC |

> [!success] Key takeaway
> Firewalls enforce **security policy** through rules — protecting internal hosts while permitting legitimate traffic.

---

### 🧭 Learning Path
← Previous: [[Router]] · Up: [[Network Devices]] · Next → [[Day 01 Lab - Packet Tracer Introduction.pkt]]

### 🔗 Related Notes
[[Network]] · [[Router]] · [[Switches]] · [[Server]]
