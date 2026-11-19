---
tags:
  - ccna
  - networking
  - standards
aliases:
  - Who Defines the Standards
  - Standards Organizations
  - IEEE and IETF
---

# 🏛️ Who Defines The Standards

> [!abstract] In one line
> Networking standards are created by **independent standards organizations** — mainly **IEEE** for LANs and **IETF** for Internet protocols — then implemented by vendors such as Cisco.

## 🏢 Independent Standards Organizations

> [!important] Not a single vendor
> Most networking standards are created by **independent standards organizations**, not by a single vendor. Engineers from **many different companies** participate in the process. The two organizations you should know are the **IEEE** and the **IETF**.

## ⚖️ IEEE vs IETF

| | **IEEE** | **IETF** |
| --- | --- | --- |
| **Full name** | Institute of Electrical and Electronics Engineers | Internet Engineering Task Force |
| **What it is** | Standards organization | Open community |
| **Focus** | Local area network technologies | Protocols used on the Internet |
| **Examples** | **802.3 = Ethernet**, **802.11 = Wi-Fi** | **TCP, IP, UDP, HTTP, DNS** |
| **Publishes as** | 802.x standards | **RFCs** — Requests for Comments |

## 🖧 IEEE — LAN Standards

The **IEEE** develops many of the technologies we use on **local area networks**:

- **Ethernet** — defined in the **802.3** set of standards (mentioned earlier with Ethernet cables).
- **Wi-Fi** — defined in the **802.11** standards.

These standards cover both:

- **Physical specifications** — Ethernet cable types, Wi-Fi radio frequency, and how signals are transmitted over the physical medium (cable or radio wave).
- **Message formatting** — how to format messages to send them to another device over that medium.

![[Pasted image 20261119143747.png]]

> [!tip] Both matter
> Physical specs **and** message formatting are important topics covered in this course.

## 🌐 IETF — Internet Protocols

The **IETF** is an **open community** that defines many of the protocols used on the Internet:

- **TCP**, **IP**, **UDP**, **HTTP**, and **DNS** — all covered later in this course.
- It publishes its standards in documents called **RFCs — Requests for Comments**, all **freely available** on the Internet.

![[Pasted image 20261119143811.png]]

## 🔗 From Standard to Device

> [!example] How it comes together
> 1. The **IEEE** and **IETF** create the standards.
> 2. Vendors such as **Cisco** implement them.
> 3. Devices from **different companies** can then work together on the network.

## 🧱 Why Layers?

> [!info] Making sense of many standards
> There are many different standards and protocols, each solving a **different part** of the overall communication problem. To make sense of them, it helps to group their jobs into **layers** — a **layered model**.

> [!success] Key takeaway
> **IEEE** defines LAN standards (802.3 Ethernet, 802.11 Wi-Fi); **IETF** defines Internet protocols in **RFCs**. Vendors implement these open standards so devices interoperate, and grouping their jobs into **layers** makes them easier to understand.

---

### 🧭 Learning Path
← Previous: [[History]] · Up: [[TCP IP]] · Next → [[TCP IP Exam]]

### 🔗 Related Notes
[[TCP IP]] · [[Standards And Protocols]] · [[History]] · [[Ethernet]] · [[Ethernet Standards (copper)]] · [[Network Protocols]]
