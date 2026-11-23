---
tags:
  - ccna
  - networking
  - exam
aliases:
  - TCP IP Exam
  - TCP/IP Practice Exam
---

# 📝 TCP/IP — Practice Exam

> [!info] How to use this exam
> - Answer everything **without looking at your notes**.
> - Suggested time: **30 minutes**.
> - Click **Show answer** to check each question.
> - Target score: **80% or higher**.

| Section | Topic | Marks |
| --- | --- | --- |
| A | Multiple choice | 12 |
| B | True or false | 6 |
| C | Fill in the blank | 6 |
| D | Short answer | 10 |
| E | Scenario | 6 |
| **Total** | | **40** |

---

## 🅰️ Section A — Multiple Choice (12 marks)

### 1. What is a **protocol**?
- A. A type of network cable
- B. A set of rules defining how data is communicated
- C. A hardware vendor
- D. A network device

> [!success]- Show answer
> **B.** A protocol is a set of rules defining how data should be communicated between devices over a network.

### 2. What is a **standard**?
- A. An agreed-upon specification for how a protocol or technology works
- B. A private rule used by one vendor
- C. A type of RJ-45 connector
- D. The speed of a network link

> [!success]- Show answer
> **A.** A standard is an agreed-upon specification that describes how a protocol or technology should work.

### 3. Which organization defines **Ethernet (802.3)**?
- A. IETF
- B. IEEE
- C. ARPA
- D. IBM

> [!success]- Show answer
> **B. IEEE** — the Institute of Electrical and Electronics Engineers develops LAN standards such as 802.3 Ethernet.

### 4. Which organization publishes standards as **RFCs**?
- A. IEEE
- B. IETF
- C. Cisco
- D. DoD

> [!success]- Show answer
> **B. IETF** — the Internet Engineering Task Force publishes its standards as Requests for Comments (RFCs).

### 5. When did **ARPANET** come online?
- A. 1969
- B. 1974
- C. 1983
- D. 1991

> [!success]- Show answer
> **A. 1969** — ARPANET connected mainframes at universities and labs.

### 6. What protocol did **ARPANET originally use**?
- A. TCP/IP
- B. NCP
- C. HTTP
- D. UDP

> [!success]- Show answer
> **B. NCP** — the Network Control Program. There was no TCP/IP in the early days.

### 7. When did ARPANET **fully switch to TCP/IP**?
- A. 1969
- B. 1974
- C. 1 January 1983
- D. 1989

> [!success]- Show answer
> **C. 1 January 1983** — the official TCP/IP cutover date.

### 8. Which layer uses **port numbers** to identify application processes?
- A. Physical
- B. Local Network
- C. Internet
- D. Transport

> [!success]- Show answer
> **D. Transport** — Layer 4 uses port numbers for process-to-process communication.

### 9. Which layer uses **IP addresses** and is mainly used by routers?
- A. Application
- B. Internet
- C. Local Network
- D. Physical

> [!success]- Show answer
> **B. Internet** — Layer 3 provides host-to-host delivery using IP addresses.

### 10. Which layer uses **MAC addresses** for delivery to the next hop?
- A. Application
- B. Transport
- C. Local Network
- D. Internet

> [!success]- Show answer
> **C. Local Network** — Layer 2 provides hop-to-hop delivery on a local network using MAC addresses.

### 11. What does **encapsulation** do?
- A. Removes headers going up the stack
- B. Adds headers and trailers going down the stack
- C. Converts fiber signals to copper signals
- D. Changes IP addresses at every router

> [!success]- Show answer
> **B.** Encapsulation adds the information each layer needs as data moves down the stack.

### 12. In the OSI model, what is **Layer 2** commonly called?
- A. Network
- B. Transport
- C. Data Link
- D. Session

> [!success]- Show answer
> **C. Data Link** — Layer 3 is Network, Layer 2 is Data Link, and Layer 7 is Application.

---

## 🅱️ Section B — True or False (6 marks)

### 1. Vendor-proprietary protocols make communication between different vendors easy.
> [!success]- Show answer
> **False** — proprietary protocols make interoperability difficult, if not impossible.

### 2. IEEE standards cover both physical specifications and how messages are formatted.
> [!success]- Show answer
> **True** — e.g. cable types and radio frequency, plus message formatting over the medium.

### 3. RFCs are published by the IEEE.
> [!success]- Show answer
> **False** — RFCs are published by the **IETF**.

### 4. TCP originally stood for “Transmission Control Program”.
> [!success]- Show answer
> **True** — the name later changed to “Transmission Control **Protocol**” when TCP was split from IP.

### 5. Layer 3 uses MAC addresses to deliver data to the final host.
> [!success]- Show answer
> **False** — Layer 3 uses **IP addresses**. MAC addresses are used at Layer 2 for the next hop.

### 6. Layer 2 adds both a header and a trailer.
> [!success]- Show answer
> **True** — the Layer 2 trailer helps the receiving device check for transmission errors.

---

## 🅲 Section C — Fill in the Blank (6 marks)

### 1. A ________ is a set of rules defining how data is communicated over a network.
> [!success]- Show answer
> **protocol**

### 2. IEEE defines Ethernet in the ________ set of standards.
> [!success]- Show answer
> **802.3**

### 3. The IETF publishes its standards as ________ (Requests for Comments).
> [!success]- Show answer
> **RFCs**

### 4. ARPANET fully switched to TCP/IP on 1 January ________.
> [!success]- Show answer
> **1983**

### 5. Layer 4 uses ________ numbers to identify processes on a host.
> [!success]- Show answer
> **port**

### 6. In common naming, Layer 3 is called the ________ layer.
> [!success]- Show answer
> **Network**

---

## 🅳 Section D — Short Answer (10 marks)

### 1. Why are vendor-neutral standards needed? (2 marks)
> [!success]- Show answer
> - With **proprietary** protocols, devices from different vendors cannot understand each other.
> - **Vendor-neutral standards** are agreed-upon specifications that all vendors implement, so devices of all types can communicate.

### 2. Compare the IEEE and the IETF. (2 marks)
> [!success]- Show answer
> - **IEEE** develops LAN technologies — **802.3 Ethernet** and **802.11 Wi-Fi** — covering physical specs and message formatting.
> - **IETF** defines Internet protocols such as **TCP, IP, UDP, HTTP, DNS**, published as **RFCs**.

### 3. Why do we use a layered model? (2 marks)
> [!success]- Show answer
> - It splits a complex communication problem into smaller jobs.
> - Each layer can be changed or improved without redesigning every other layer.

### 4. Explain adjacent-layer interaction vs same-layer interaction. (2 marks)
> [!success]- Show answer
> - **Adjacent-layer interaction** happens inside one device: each layer provides services to the layer above and uses the layer below.
> - **Same-layer interaction** happens logically between matching layers on different devices, such as Layer 3 on PC1 communicating with Layer 3 on SRV1.

### 5. Explain encapsulation vs decapsulation. (2 marks)
> [!success]- Show answer
> - **Encapsulation** adds headers and trailers as data moves down the sending device's stack.
> - **Decapsulation** removes headers and trailers as data moves up the receiving device's stack.

---

## 🅴 Section E — Scenario (6 marks)

A web browser on **PC1** requests a web page from **SRV1**. The path includes switches and routers. Explain how the five layers handle the request, name the addressing used at each layer, and describe what happens at SRV1.

> [!success]- Show answer
> 1. **Application:** Chrome creates an HTTP request for the web server on SRV1.
> 2. **Transport:** Port numbers identify the source and destination processes; the web server commonly uses port **80**.
> 3. **Internet:** IP addresses identify the source host and final destination host, such as SRV1 at **10.1.1.1**; routers use the destination IP to forward the packet.
> 4. **Local Network:** MAC addresses deliver the frame to the **next hop** on each local network; switches forward frames within the LAN.
> 5. **Physical:** The frame becomes bits sent as electrical, optical, or radio signals over the medium.
> 6. **At SRV1:** The message moves up the stack. Layers 2, 3, and 4 remove their headers/trailers, and the Application layer processes the HTTP request. If Wi-Fi replaced Ethernet, Layers 1 and 2 could change while the upper layers stay the same.

---

## 📊 Score Tracker

| Score | Level | Next Step |
| --- | --- | --- |
| **34–40** | Excellent | Move on to the next topic |
| **27–33** | Good | Review missed questions |
| **21–26** | Needs work | Re-read the TCP/IP layer notes |
| **Below 21** | Restudy | Start from [[TCP IP]] |

## 🔁 Review These Notes

- [[Standards And Protocols]] — protocols, standards, and vendor neutrality
- [[History]] — ARPANET, NCP, and the rise of TCP/IP
- [[Who Defines The Standards]] — IEEE, IETF, and RFCs
- [[Layered models]] — why networking uses layers
- [[Analogy building a Model]] — the mail system analogy
- [[The TCP IP Model]] — the five-layer overview
- [[Layer 5 Application Layer]] — application data and protocols
- [[Layer 4 Transport Layer]] — ports, TCP, and UDP
- [[Local 3 Internet Layer]] — IP addresses and routers
- [[Local 2 Network Layer]] — MAC addresses and next hops
- [[Layer 1 Physical Layer]] — bits and signals
- [[Separation of Layers]] — modularity
- [[Adjacent-layer interaction]] — services between neighboring layers
- [[Same Layer Interaction]] — logical peer communication
- [[Encapsulation & decapsulation]] — headers, trailers, and message flow
- [[OSI Model]] — the 7-layer reference model
- [[Other Model]] — different model names

---

### 🧭 Learning Path
← Previous: [[Day 03 Lab - OSI Model.pkt]] · Up: [[TCP IP]] · Next → [[Intro To The CLI]]

### 🔗 Related Notes
[[TCP IP]] · [[Standards And Protocols]] · [[History]] · [[Who Defines The Standards]] · [[Layered models]] · [[The TCP IP Model]] · [[Layer 4 Transport Layer]] · [[Local 3 Internet Layer]] · [[Local 2 Network Layer]] · [[Encapsulation & decapsulation]] · [[OSI Model]]
