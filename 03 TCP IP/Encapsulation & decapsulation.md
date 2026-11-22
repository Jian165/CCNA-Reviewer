---
tags:
  - ccna
  - networking
  - tcpip
  - layers
aliases:
  - Encapsulation
  - Decapsulation
  - De-encapsulation
---

# 📦 Encapsulation & Decapsulation

> [!abstract] In one line
> **Encapsulation** adds headers and trailers as data moves down the stack; **decapsulation** removes them as data moves up.

## ⬇️ Encapsulation: Sending Data

As a message moves down the stack, each layer adds the information the matching layer on the receiver will need.

| Layer | What it adds | Result |
| --- | --- | --- |
| **Application** | Creates the data | Data |
| **Transport** | Layer 4 header: source/destination ports | Segment or datagram |
| **Internet** | Layer 3 header: source/destination IP addresses | Packet |
| **Local Network** | Layer 2 header **and trailer**: MAC addresses and error check | Frame |
| **Physical** | Converts the frame into bits | Signals |

Each layer adds a header containing the information the matching layer on the receiver will need — ports, IP addresses, and MAC addresses. The Layer 2 header is transmitted first, and the Layer 2 trailer is transmitted last.

![[Pasted image 20261122140817.png]]

> [!important] Layer 2 is special
> Layer 2 adds both a **header** and a **trailer**. The trailer helps the receiving device check for transmission errors.

## ⬆️ Decapsulation: Receiving Data

The receiving device reverses the process.

| Layer | What happens |
| --- | --- |
| **Physical** | Receives bits as signals |
| **Local Network** | Checks the frame, then removes the Layer 2 header/trailer |
| **Internet** | Reads and removes the Layer 3 header |
| **Transport** | Reads and removes the Layer 4 header |
| **Application** | Processes the original data |

## 🔄 Full Host-to-Host Flow

Every device has its own network stack.

1. PC1's message goes **down** PC1's stack.
2. It crosses the network as signals.
3. It goes **up** SRV1's stack.
4. SRV1's application processes the request.
5. A response goes down SRV1's stack and up PC1's stack.
6. Routers and switches can add extra handling steps, but the overall **down → across → up** flow stays the same.

![[Pasted image 20261122141023.png]]

> [!tip] Exam memory hook
> **Encapsulation = add on the way down. Decapsulation = remove on the way up.**

## ⚠️ Exam Traps

> [!warning] Watch out for these
> - The Physical layer sends **bits**, not complete frames.
> - Layer 2 adds a **header and trailer**; Layers 3 and 4 add headers.
> - Routers and switches add extra steps, but the overall down-across-up flow is still the same.

## 🧠 Quick Recap

| Topic | Fact |
| --- | --- |
| **Encapsulation** | Add headers/trailers going down |
| **Decapsulation** | Remove headers/trailers going up |
| **Layer 4 header** | Port numbers |
| **Layer 3 header** | IP addresses |
| **Layer 2 header/trailer** | MAC addresses and error check |

> [!success] Key takeaway
> Encapsulation prepares data for transmission; decapsulation restores it so the destination application can process it.

---

### 🧭 Learning Path
← Previous: [[Same Layer Interaction]] · Up: [[TCP IP]] · Next → [[OSI Model]]

### 🔗 Related Notes
[[TCP IP]] · [[Same Layer Interaction]] · [[Adjacent-layer interaction]] · [[Layer 4 Transport Layer]] · [[Local 3 Internet Layer]] · [[Local 2 Network Layer]]
