---
tags:
  - ccna
  - networking
  - wireshark
  - packet-capture
  - ethernet
  - arp
aliases:
  - Wireshark
  - Packet Capture
  - Ethernet Frame Review
---

# 🔬 Wireshark Packet Capture & Frame Review

> [!abstract] In one line
> **Wireshark packet captures** expose the real frame sequence — **ARP request → ARP reply → ICMP echo requests/replies** — and confirm frame fields such as **Type** and **padding**.

![[Pasted image 20261128133437.png]]

## 👀 What Wireshark Shows

Wireshark performs **packet captures** to analyse the **contents of network traffic**. In the Protocol column, the capture shows **ARP**, followed by **ICMP** (ping).

## 1️⃣ ARP Request

| Field | Value |
| --- | --- |
| Source MAC | `0c2f.b011.9d00` — **PC1** |
| Destination MAC | Broadcast — **all Fs** (`FF:FF:FF:FF:FF:FF`) |
| Info | **"Who has 192.168.1.3? Tell 192.168.1.1"** |

> [!info] Reading the info line
> The ARP request asks **which MAC address has IP `192.168.1.3`**, and tells the receiver to send the reply to **`192.168.1.1`** (PC1 itself).

## 2️⃣ ARP Reply

| Field | Value |
| --- | --- |
| Source MAC | `0c2f.b06a.3900` — **PC3** |
| Destination MAC | **PC1's MAC** |
| Info | **"192.168.1.3 is at 0c2f.b06a.3900"** — PC3 telling PC1 its MAC address |

## 3️⃣ ICMP Echo Requests & Replies

After ARP, the capture shows **4 ICMP echo requests** and **4 ICMP echo replies**.

| Message | Source IP | Destination IP |
| --- | --- | --- |
| ICMP echo request | PC1 | PC3 |
| ICMP echo reply | PC3 | PC1 |

> [!tip] Why only 4?
> The **first ping failed** while ARP was resolving the MAC address (see [[Ping]]), so only 4 of the 5 default requests are followed by replies.

## 🧱 Ethernet Frame Review

![[Pasted image 20261128135209.png]]

A **36-byte ping** is sent with:

```bash
ping 192.168.1.3 SIZE 36
```

### Type Field

![[Pasted image 20261128135236.png]]

| Ethernet Type | Hex value | Identifies |
| --- | --- | --- |
| IPv4 | **`0x0800`** | The `0x` prefix means hexadecimal — really `0800` |
| IPv6 | **`0x86DD`** | IPv6 packet |
| ARP | **`0x0806`** | An **ARP packet** is inside the Ethernet frame |

### Padding Field

- Minimum payload for an Ethernet frame = **46 bytes**.
- A **36-byte** ping therefore needs **10 bytes of padding**.
- Each **hexadecimal digit = 4 bits**, so **2 digits = 8 bits = 1 byte**.
- The capture shows **20 zeroes = 10 bytes** of padding — ten pairs of zeroes added to reach the 46-byte payload minimum.

![[Pasted image 20261128135655.png]]

> [!warning] Padding is hexadecimal zeros
> The zeroes seen in Wireshark are hex zeroes. Count **pairs**: 20 hex digits → **10 bytes** of padding (see [[Ethernet Frame 2]] for the 64-byte minimum calculation).

## 🧠 Quick Recap

| Capture order | Protocol | Key detail |
| --- | --- | --- |
| 1 | ARP request | Broadcast; "Who has 192.168.1.3? Tell 192.168.1.1" |
| 2 | ARP reply | Unicast; "192.168.1.3 is at 0c2f.b06a.3900" |
| 3 | ICMP | 4 echo requests + 4 echo replies |
| Frame check | Type `0800` / `86DD` / `0806` | IPv4 / IPv6 / ARP |
| Frame check | Padding | 36-byte ping + 10 bytes zeros = 46-byte payload |

> [!success] Key takeaway
> Wireshark confirms the theory: **ARP before ping**, unicast replies, and an Ethernet frame whose **Type** field identifies the payload and whose **padding** enforces the **46-byte minimum payload**.

---

### 🧭 Learning Path
← Previous: [[Clearing The MAC address Table]] · Up: [[Ethernet LAN Switching 2]] · Next → [[Ethernet LAN Switching 2 Exam]]

### 🔗 Related Notes
[[Ethernet LAN Switching 2]] · [[Ethernet Frame 2]] · [[ARP Request]] · [[ARP Reply]] · [[Ping]] · [[CCNA/05 Ethernet LAN Switching  1/Ethernet Frame]] · [[ARP Table]]
