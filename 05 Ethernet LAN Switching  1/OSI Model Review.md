---
tags:
  - ccna
  - networking
  - osi
  - layers
  - ethernet
  - switching
aliases:
  - OSI Model Review
  - Layer 1 and Layer 2 Review
  - Data Link Layer Review
---

# 🧭 OSI Model Review for Ethernet Switching

> [!abstract] In one line
> Ethernet switching uses **Layer 1 signals** and **Layer 2 frames**: Layer 1 sends bits over the medium, and Layer 2 provides node-to-node delivery using MAC addresses.

## ⚡ Physical Layer — Layer 1

![[Pasted image 20261125144253.png]]

The **Physical Layer** defines the physical characteristics of the medium used to transfer data between devices:

- **Voltage levels**
- **Maximum transmission distances** — for example, Ethernet UTP cable's **100-meter limit**
- **Physical connectors**
- **Cable specifications**

It converts **digital bits** into:

- **Electrical signals** for wired connections
- **Radio signals** for wireless connections

Everything from the cabling lesson — copper UTP, fiber-optic cable, RJ-45 connectors, pin layouts — belongs to Layer 1.

## 🔗 Data Link Layer — Layer 2

![[Pasted image 20261125144425.png]]

Layer 2 provides **node-to-node connectivity and data transfer**, such as:

- PC → switch
- Switch → router
- Router → router

It also:

- Defines how data is formatted for transmission over the physical medium
- Detects and possibly corrects Physical Layer errors
- Uses **Layer 2 addressing**, which is separate from Layer 3 addressing

> [!warning] IP is Layer 3, not Layer 2
> **IP addresses are Layer 3 addresses.** MAC addresses are Layer 2 addresses. Do not mix them up.

**Switches operate at Layer 2.** Ethernet involves both Layer 1 and Layer 2; since the Layer 1 Ethernet standards were covered earlier, this folder focuses on **Layer 2 Ethernet switching**.

## 📦 PDUs and Encapsulation

![[Pasted image 20261125145015.png]]

As data is prepared to be sent over a network, each layer adds its own information. Each stage is a **PDU — Protocol Data Unit**.

| Stage | PDU name | What was added |
| --- | --- | --- |
| Upper-layer data | **Data** | Nothing yet |
| Add Layer 4 header | **Segment** | Layer 4 header |
| Add Layer 3 header | **Packet** | Layer 3 header |
| Add Layer 2 header and trailer | **Frame** | Layer 2 header + trailer |

> [!important] Exam point
> The **Layer 2 PDU is a frame**. This folder focuses on how switches receive and forward **Ethernet frames**, the Layer 2 framing used in virtually every LAN today.

The reverse process on the receiving device is **decapsulation**, which removes the headers and trailers as the message moves up the OSI stack.

## 🎯 Why This Review Matters

- The course continues upward through the layers until the full path from application to network is clear.
- Layer 1 was already covered with UTP, fiber, and RJ-45.
- Now the focus is Layer 2: how Ethernet frames are built and how switches forward them.

> [!success] Key takeaway
> Layer 1 turns bits into signals; Layer 2 packages those bits into **frames** with MAC addresses. Switches work at Layer 2, and the frame is the PDU they forward.

---

### 🧭 Learning Path
← Previous: [[Local Area Networks]] · Up: [[Ethernet LAN Switching]] · Next → [[Ethernet Frame]]

### 🔗 Related Notes
[[Ethernet LAN Switching]] · [[Local Area Networks]] · [[Ethernet Frame]] · [[OSI Model]] · [[Local 2 Network Layer]] · [[Layer 1 Physical Layer]] · [[Encapsulation & decapsulation]]
