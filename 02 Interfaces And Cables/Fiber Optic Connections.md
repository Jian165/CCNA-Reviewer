---
tags:
  - ccna
  - networking
  - cabling
  - ethernet
aliases:
  - Fiber Optic Connections
  - Fiber Optic Cabling
  - SFP
---

# 💡 Fiber Optic Connections

> [!abstract] In one line
> Fiber-optic connections use **SFP transceivers** and **glass fiber cables** that carry **light** instead of electrical signals, with separate **transmit (Tx)** and **receive (Rx)** paths.

## 🔌 SFP Transceivers

**SFP** means **small form-factor pluggable**. You insert one into the device, but the connection is not complete until a fiber-optic cable is plugged into it.

![[Pasted image 20261119133200.png]]

## 🧵 Fiber Optic Cable

A **fiber-optic cable** connects to the SFP. Rather than an electrical signal over copper wiring, these cables send **light over glass fibers**.

![[Pasted image 20261119133249.png]]

Notice that there are **two connectors on each end** — one connector **transmits** data and one **receives** data.

![[Pasted image 20261119133609.png]]

## 🔄 Transmit vs Receive

Copper **UTP** cables use separate **wire pairs** within the cable to transmit and receive. Fiber-optic cables instead use **separate strands**:

- **Transmit (Tx)** on the left connects to **receive (Rx)** on the right.
- **Transmit (Tx)** on the right connects to **receive (Rx)** on the left.

![[Pasted image 20261119133752.png]]

> [!important] Why the strands cross
> A transmitter must always feed a receiver. Connecting **Tx → Rx** at both ends is what lets both devices send data at the same time.

## 🧱 Layers of a Fiber Optic Cable

| # | Layer | Purpose |
| --- | --- | --- |
| **1** | **Fiberglass core** | Carries the light that transmits data |
| **2** | **Cladding** | Reflects light back into the core |
| **3** | **Protective buffer** | Protects the glass fiber from breaking |
| **4** | **Outer jacket** | Outer protective covering of the cable |

There are two main types of fiber-optic cable: [[Single-Mode Fiber|single-mode]] and [[Multimode Fiber|multimode]].

## 📐 Fiber Optic Standards

Just like the copper UTP standards, fiber-optic standards define speed, cabling, and maximum distances.

![[Pasted image 20261119134753.png]]

| Standard | IEEE | Speed | Fiber Type | Maximum Distance |
| --- | --- | --- | --- | --- |
| **1000BASE-LX** | 802.3z | 1 Gbps | Multimode | 550 m |
| **1000BASE-LX** | 802.3z | 1 Gbps | Single-mode | 5 km (5,000 m) |
| **10GBASE-SR** | 802.3ae | 10 Gbps | Multimode | 400 m |
| **10GBASE-LR** | 802.3ae | 10 Gbps | Single-mode | 10 km |
| **10GBASE-ER** | 802.3ae | 10 Gbps | Single-mode | 30 km |

> [!tip] Pattern to remember
> In **10GBASE-SR / LR / ER**, the last letter hints at the reach: **S**hort (multimode), **L**ong (single-mode), **E**xtended (single-mode).

## ⚖️ UTP vs Fiber-Optic Cabling

| Feature | UTP (Copper) | Fiber-Optic |
| --- | --- | --- |
| **Cost** | Cheaper cable | More expensive cable |
| **Distance** | Shorter — about **100 m** max | Much longer — up to **30 km** in these standards |
| **Interference** | Vulnerable to **EMI**; the twist helps protect it | Carries light, so no electrical interference issue |
| **Ports** | **RJ-45** ports are cheaper | **SFPs** are more expensive; **single-mode** ports cost more than **multimode** |
| **Signal leakage** | Leaks a faint signal — possible **security risk** | No signal outside the cable — no leakage risk |

> [!success] Key takeaway
> Fiber carries **light over glass** via **SFPs** using **separate Tx/Rx strands**. It costs more than UTP but reaches much farther, and it does not leak signal outside the cable.

---

### 🧭 Learning Path
← Previous: [[Auto MDIX]] · Up: [[Interfaces And Cables]] · Next → [[Multimode Fiber]]

### 🔗 Related Notes
[[Interfaces And Cables]] · [[Ethernet]] · [[Ethernet Standards (copper)]] · [[UTP Cable]] · [[Multimode Fiber]] · [[Single-Mode Fiber]]
