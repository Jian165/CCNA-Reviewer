---
tags:
  - ccna
  - networking
  - exam
aliases:
  - Network Devices Exam
  - Network Devices Practice Exam
---

# 📝 Network Devices — Practice Exam

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

### 1. Which device forwards traffic **within** a LAN?
- A. Router
- B. Switch
- C. Firewall
- D. Server

> [!success]- Show answer
> **B. Switch** — switches connect and forward traffic between hosts in the same LAN.

### 2. Which device connects **different LANs** and forwards data over the Internet?
- A. Switch
- B. Firewall
- C. Router
- D. Client

> [!success]- Show answer
> **C. Router** — routers provide connectivity between separate networks.

### 3. Which device controls traffic entering and exiting a network using configured rules?
- A. Router
- B. Switch
- C. Server
- D. Firewall

> [!success]- Show answer
> **D. Firewall** — firewalls monitor and control traffic based on security rules.

### 4. Approximately how many interfaces does a typical switch have?
- A. 2
- B. 4
- C. 24 or more
- D. 1

> [!success]- Show answer
> **C. 24 or more** — switches have many ports for connecting end hosts.

### 5. Which of these is a **host-based** firewall?
- A. A hardware device filtering traffic between two networks
- B. Software filtering traffic entering and exiting a PC
- C. A switch with 24 ports
- D. A router connecting two LANs

> [!success]- Show answer
> **B.** Host-based firewalls are software applications that protect an individual host.

### 6. A device that **requests** a service is called a:
- A. Server
- B. Router
- C. Client
- D. Firewall

> [!success]- Show answer
> **C. Client** — clients access services made available by servers.

### 7. A device that **provides** functions or services is called a:
- A. Client
- B. Server
- C. Switch
- D. Firewall

> [!success]- Show answer
> **B. Server** — servers provide services to clients.

### 8. Which device typically has **fewer** network interfaces?
- A. Switch
- B. Router
- C. Server
- D. Client

> [!success]- Show answer
> **B. Router** — routers generally have fewer interfaces than switches.

### 9. A hardware device that filters traffic **between networks** is a:
- A. Host-based firewall
- B. Network firewall
- C. Client
- D. Switch

> [!success]- Show answer
> **B. Network firewall** — network firewalls are hardware devices that filter traffic between networks.

### 10. What does **LAN** stand for?
- A. Local Access Network
- B. Long Area Network
- C. Local Area Network
- D. Linked Area Node

> [!success]- Show answer
> **C. Local Area Network.**

---

## 🅱️ Section B — True or False (5 marks)

### 1. A switch can connect two separate LANs over the Internet.
> [!success]- Show answer
> **False** — switches work within a single LAN. A router is needed to connect separate LANs or reach the Internet.

### 2. A router can connect a LAN to the Internet.
> [!success]- Show answer
> **True** — routers forward traffic between networks, including to the Internet.

### 3. Client and server are fixed device types; a PC can never act as a server.
> [!success]- Show answer
> **False** — client and server are **roles**. The same device can act as either depending on the exchange.

### 4. A firewall can be placed inside or outside the network.
> [!success]- Show answer
> **True** — firewalls can filter traffic before it reaches the router or after it has passed through.

### 5. Next-generation firewalls include more advanced filtering capabilities.
> [!success]- Show answer
> **True** — NGFWs add more modern and advanced filtering features.

---

## 🅲 Section C — Fill in the Blank (5 marks)

### 1. A digital communications network allows ________ to share resources.
> [!success]- Show answer
> **nodes**

### 2. A ________ forwards traffic within a LAN.
> [!success]- Show answer
> **switch**

### 3. A ________ connects different LANs and forwards data over the Internet.
> [!success]- Show answer
> **router**

### 4. A firewall uses configured ________ to decide which traffic is allowed or denied.
> [!success]- Show answer
> **rules**

### 5. A device that provides services for clients is a ________.
> [!success]- Show answer
> **server**

---

## 🅳 Section D — Short Answer (6 marks)

### 1. Explain the difference between a switch and a router. (2 marks)
> [!success]- Show answer
> - A **switch** forwards traffic **within the same LAN** and has many ports for end hosts.
> - A **router** connects **different LANs** and forwards traffic between networks, including over the Internet.

### 2. What is the difference between a client and a server? (2 marks)
> [!success]- Show answer
> - A **client requests** a service.
> - A **server provides** a service.
> - These are roles, so one device can be both at different times.

### 3. Name the two types of firewalls and give an example of each. (2 marks)
> [!success]- Show answer
> - **Network firewall** — a hardware device that filters traffic between networks.
> - **Host-based firewall** — software that filters traffic entering and exiting a host such as a PC.

---

## 🅴 Section E — Scenario (4 marks)

PC1 in the **New York Branch** wants to download a file from SRV1 in the **Tokyo Branch**.

![[Pasted image 20261111141458.png]]

**List the devices the request passes through and explain the role of each.**

> [!success]- Show answer
> 1. **SW1** — forwards the request within the New York LAN.
> 2. **R1** — forwards the request between networks, over the Internet.
> 3. **R2** — forwards the request into the Tokyo LAN.
> 4. **SW2** — forwards the request to SRV1 within the Tokyo LAN.
>
> The reply follows the reverse path back to PC1.
> If a firewall is deployed, it would also inspect the traffic against its rules.

---

## 📊 Score Tracker

| Score | Level | Next Step |
| --- | --- | --- |
| **27–30** | Excellent | Move on to the next topic |
| **22–26** | Good | Review missed questions |
| **18–21** | Needs work | Re-read the device notes |
| **Below 18** | Restudy | Start from [[Network Devices]] |

## 🔁 Review These Notes

- [[Network]] — nodes and client/server roles
- [[Router]] — connecting separate LANs
- [[Switches]] — forwarding within a LAN
- [[Firewall]] — rules, placement, and types
- [[Server]] — providing services
- [[Clients]] — requesting services

---

### 🔗 Related Notes
[[Network Devices]] · [[Network]] · [[Router]] · [[Switches]] · [[Firewall]] · [[Server]] · [[Clients]]
