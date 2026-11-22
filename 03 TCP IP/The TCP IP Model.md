---
tags:
  - ccna
  - networking
  - tcpip
  - model
aliases:
  - TCP/IP Model
  - Five-Layer TCP/IP Model
  - Course Model
---

# 🧭 The TCP/IP Model (5 Layers)

> [!abstract] In one line
> This course uses five layers — **Application, Transport, Internet, Local Network, and Physical** — to explain how a message travels from one application to another.

## 🧩 Example Network

![[Pasted image 20261122134957.png]]

- **PC1** is a client running a web browser.
- **SRV1** is a server running a web server and a file server.
- **R1** and **R2** are routers that connect different networks.
- **SW1** and **SW2** are switches that connect devices on local networks.

> [!tip] Why only one host per switch?
> The diagram shows one host per switch to stay simple. A switch can connect many devices to the same LAN.

## 🔄 One Request Through the Five Layers

| Layer | Question it answers | In this example |
| --- | --- | --- |
| **5 — Application** | What data is being sent? | Chrome creates an HTTP request |
| **4 — Transport** | Which process should receive it? | Port **80** = web server; port **21** = file server |
| **3 — Internet** | Which host should receive it? | SRV1's IP address, e.g. **10.1.1.1** |
| **2 — Local Network** | Which next hop carries it? | MAC addresses move the message PC1 → R1 → R2 → SRV1 |
| **1 — Physical** | How are the bits sent? | Electrical, optical, or radio signals over the medium |

> [!example] Why each layer is needed
> - **Application:** creates the request.
> - **Transport:** SRV1 runs several services, so ports choose the correct process.
> - **Internet:** even with the correct port, the message must first reach SRV1.
> - **Local Network:** multiple devices sit on the path, so the message is passed from one local hop to the next.
> - **Physical:** the hop is only completed when the bits are sent as signals over the medium.

> [!important] Port number ≠ physical port
> A **port number** is a logical number that identifies a process on a host. It is not the same as a physical RJ-45 or SFP port.

> [!tip] Host
> A **host** is any device that can send or receive data on a network, such as a PC, server, or phone.

## 🗺️ Mail-to-Model Mapping

![[Pasted image 20261122134750.png]]

| Mail system | TCP/IP model |
| --- | --- |
| Content | Application |
| Recipient | Transport |
| Address | Internet |
| Local Delivery | Local Network |
| Infrastructure | Physical |

## 📌 Layer Summary

| Layer | Common name | Main addressing | Main devices/protocols |
| --- | --- | --- | --- |
| **5** | Application | Message format | HTTP, HTTPS, FTP, DNS |
| **4** | Transport | Port numbers | TCP, UDP |
| **3** | Internet | IP addresses | IP, ICMP, routers |
| **2** | Local Network | MAC addresses | Ethernet, Wi-Fi, switches |
| **1** | Physical | Signals/bits | UTP, fiber, Wi-Fi radios, NICs |

> [!success] Key takeaway
> A single message needs all five layers: the application creates it, ports identify the process, IP identifies the host, MAC addresses identify the next hop, and the Physical layer sends the bits.

---

### 🧭 Learning Path
← Previous: [[Analogy building a Model]] · Up: [[TCP IP]] · Next → [[Layer 5 Application Layer]]

### 🔗 Related Notes
[[TCP IP]] · [[Layered models]] · [[Analogy building a Model]] · [[Layer 5 Application Layer]] · [[Layer 4 Transport Layer]] · [[Local 3 Internet Layer]] · [[Local 2 Network Layer]] · [[Layer 1 Physical Layer]]
