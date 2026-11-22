---
tags:
  - ccna
  - networking
  - tcpip
  - layers
aliases:
  - Adjacent Layer Interaction
  - Layer Services
---

# 🤝 Adjacent-Layer Interaction

> [!abstract] In one line
> **Adjacent-layer interaction** is the service relationship between a layer and the layer directly above or below it.

## ⬆️⬇️ How It Works

In diagrams, generic layer names are often replaced with common protocols such as **HTTP, TCP, IP, Ethernet, and UTP**.

Inside one device:

- Each layer **provides a service** to the layer above it.
- Each layer **uses the service** of the layer below it.
- Every layer relies on the layers beneath it to do its job.

![[Pasted image 20261122141206.png]]

## 🧭 Example Service Chain

| Service provider | Service receiver | Service provided |
| --- | --- | --- |
| **Layer 5 — Application** | Application process | Formats and interprets the data |
| **Layer 4 — Transport** | Layer 5 | Delivers data to the correct application using **port numbers** |
| **Layer 3 — Internet** | Layer 4 | Delivers segments/datagrams to the correct host using **IP addresses** |
| **Layer 2 — Local Network** | Layer 3 | Delivers packets to the next hop using **MAC addresses** |
| **Layer 1 — Physical** | Layer 2 | Sends and receives frame bits as electrical, optical, or radio signals |

> [!tip] Memory hook
> **Ports → IP → MAC → bits**. Each lower layer helps the layer above it.

## ⚠️ Ethernet Appears at Two Layers

| Ethernet role | Layer | Details |
| --- | --- | --- |
| Logical LAN delivery | **Layer 2** | MAC addresses and frames |
| Physical signaling | **Layer 1** | Cables, connectors, and signal rules |

> [!important] Do not mix these up
> Layer 2 Ethernet builds and addresses frames. Layer 1 Ethernet sends the frame's bits as signals.

## 🧠 Quick Recap

| Topic | Fact |
| --- | --- |
| **Direction** | Up and down inside one device |
| **Upper layer** | Uses services from the lower layer |
| **Lower layer** | Provides services to the upper layer |
| **Example** | Layer 3 uses Layer 2 to reach the next hop |

> [!success] Key takeaway
> Adjacent layers cooperate inside a device: each lower layer provides a service that helps the layer above complete its job.

---

### 🧭 Learning Path
← Previous: [[Separation of Layers]] · Up: [[TCP IP]] · Next → [[Same Layer Interaction]]

### 🔗 Related Notes
[[TCP IP]] · [[Layered models]] · [[Separation of Layers]] · [[Same Layer Interaction]] · [[Encapsulation & decapsulation]] · [[Local 2 Network Layer]]
