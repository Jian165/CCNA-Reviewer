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
> - Suggested time: **20 minutes**.
> - Click **Show answer** to check each question.
> - Target score: **80% or higher**.

| Section | Topic | Marks |
| --- | --- | --- |
| A | Multiple choice | 10 |
| B | True or false | 5 |
| C | Fill in the blank | 5 |
| D | Short answer | 6 |
| E | Scenario | 4 |
| **Total** | | **30** |

---

## 🅰️ Section A — Multiple Choice (10 marks)

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

### 5. Which of these is an **IETF** protocol?
- A. 802.3
- B. 802.11
- C. TCP
- D. RJ-45

> [!success]- Show answer
> **C. TCP** — the IETF defines TCP, IP, UDP, HTTP, and DNS.

### 6. **Wi-Fi** is defined by which IEEE standard?
- A. 802.3
- B. 802.11
- C. 802.1Q
- D. NCP

> [!success]- Show answer
> **B. 802.11** — 802.3 is Ethernet; 802.11 is Wi-Fi.

### 7. When did **ARPANET** come online?
- A. 1969
- B. 1974
- C. 1983
- D. 1991

> [!success]- Show answer
> **A. 1969** — ARPANET connected mainframes at universities and labs.

### 8. What protocol did **ARPANET originally use**?
- A. TCP/IP
- B. NCP
- C. HTTP
- D. UDP

> [!success]- Show answer
> **B. NCP** — the Network Control Program. There was no TCP/IP in the early days.

### 9. Who began developing **TCP** in 1974?
- A. Vint Cerf and Bob Kahn
- B. Bill Gates and Paul Allen
- C. Alexander Graham Bell
- D. Tim Berners-Lee

> [!success]- Show answer
> **A. Vint Cerf and Bob Kahn** — two of the fathers of the modern Internet. TCP originally meant "Transmission Control Program".

### 10. When did ARPANET **fully switch to TCP/IP**?
- A. 1969
- B. 1974
- C. 1 January 1983
- D. 1989

> [!success]- Show answer
> **C. 1 January 1983** — the official TCP/IP cutover date.

---

## 🅱️ Section B — True or False (5 marks)

### 1. Vendor-proprietary protocols make communication between different vendors easy.
> [!success]- Show answer
> **False** — proprietary protocols make interoperability difficult, if not impossible.

### 2. IEEE standards cover both physical specifications and how messages are formatted.
> [!success]- Show answer
> **True** — e.g. cable types and radio frequency, plus message formatting over the medium.

### 3. RFCs are published by the IEEE.
> [!success]- Show answer
> **False** — RFCs are published by the **IETF**.

### 4. TCP originally stood for "Transmission Control Program".
> [!success]- Show answer
> **True** — the name later changed to "Transmission Control **Protocol**" when TCP was split from IP.

### 5. TCP/IP became dominant because it was open and could run over many network types.
> [!success]- Show answer
> **True** — open standards any vendor could implement beat vendor-proprietary solutions.

---

## 🅲 Section C — Fill in the Blank (5 marks)

### 1. A ________ is a set of rules defining how data is communicated over a network.
> [!success]- Show answer
> **protocol**

### 2. IEEE defines Ethernet in the ________ set of standards.
> [!success]- Show answer
> **802.3**

### 3. The IETF publishes its standards as ________ (Requests for Comments).
> [!success]- Show answer
> **RFCs**

### 4. ARPANET was funded by the US Department of Defense agency ________.
> [!success]- Show answer
> **ARPA** (Advanced Research Projects Agency)

### 5. TCP and ________ together form the TCP/IP protocol suite.
> [!success]- Show answer
> **IP** (Internet Protocol)

---

## 🅳 Section D — Short Answer (6 marks)

### 1. Why are vendor-neutral standards needed? (2 marks)
> [!success]- Show answer
> - With **proprietary** protocols, devices from different vendors cannot understand each other.
> - **Vendor-neutral standards** are agreed-upon specifications that all vendors implement, so devices of all types can communicate.

### 2. Compare the IEEE and the IETF. (2 marks)
> [!success]- Show answer
> - **IEEE** develops LAN technologies — **802.3 Ethernet** and **802.11 Wi-Fi** — covering physical specs and message formatting.
> - **IETF** is an open community defining Internet protocols such as **TCP, IP, UDP, HTTP, DNS**, published as **RFCs**.

### 3. Why did TCP/IP become dominant? (2 marks)
> [!success]- Show answer
> - It was published as **open standards** that any vendor could implement.
> - It could run over **many different types of networks**, unlike vendor-proprietary solutions.

---

## 🅴 Section E — Scenario (4 marks)

A **MacBook** accesses a website hosted on a **Linux server**, while a **Windows PC** sends an email read on an **Android** phone. Separately, in the early days of networking, an **Apple iMac** using its vendor's proprietary protocol could not talk to an **IBM server** using its own proprietary protocol. Explain why the first two work and the third fails, and name the organizations behind the standards.

> [!success]- Show answer
> 1. The MacBook, Linux server, Windows PC, and Android phone all follow the **same vendor-neutral standards**, so they can exchange data regardless of manufacturer or OS.
> 2. The iMac and IBM server used **vendor-proprietary protocols** with no agreed-upon specification in common, so neither could understand the other's requests.
> 3. **IEEE** defines the LAN standards (802.3 Ethernet, 802.11 Wi-Fi) that carry this traffic; **IETF** defines the Internet protocols (TCP, IP, HTTP, DNS) published as **RFCs**.
> 4. Vendors implement these standards, and grouping their jobs into **layers** makes the overall communication problem manageable.

---

## 📊 Score Tracker

| Score | Level | Next Step |
| --- | --- | --- |
| **27–30** | Excellent | Move on to the next topic |
| **22–26** | Good | Review missed questions |
| **18–21** | Needs work | Re-read the TCP/IP notes |
| **Below 18** | Restudy | Start from [[TCP IP]] |

## 🔁 Review These Notes

- [[Standards And Protocols]] — protocols, standards, and vendor neutrality
- [[History]] — ARPANET, NCP, and the rise of TCP/IP
- [[Who Defines The Standards]] — IEEE, IETF, and RFCs

---

### 🧭 Learning Path
← Previous: [[Who Defines The Standards]] · Up: [[TCP IP]]

### 🔗 Related Notes
[[TCP IP]] · [[Standards And Protocols]] · [[History]] · [[Who Defines The Standards]] · [[Network Protocols]] · [[Interfaces And Cables]]
