---
tags:
  - ccna
  - networking
  - icmp
  - ping
  - cli
aliases:
  - Ping
  - ICMP Echo Request
  - ICMP Echo Reply
---

# 📡 Ping & ICMP

> [!abstract] In one line
> **Ping** tests reachability and measures **round-trip time** using **ICMP Echo Request / Echo Reply** — and because it is unicast, **ARP must resolve the MAC address first**.

## 🎯 What Ping Does

- A network utility used to test **reachability** — for example, whether two computers can reach each other.
- Measures the **round-trip time** — e.g. PC1 → PC3 → back to PC1.

## 🔄 Two Messages (Like ARP)

| Ping message | Sent by | Purpose |
| --- | --- | --- |
| **ICMP Echo Request** | Source host (PC1) | Asks the destination to reply |
| **ICMP Echo Reply** | Destination host (PC3) | Answers the request |

> [!important] ARP comes first
> Unlike the ARP request, the ICMP Echo Request is **not broadcast** — it is sent to a **specific host**. The sender must already know the destination's **MAC address**, which is why **ARP must be used first**.

## ⌨️ The Command

```bash
ping 192.168.1.3
```

Followed by the **IP address** you want to ping (`192.168.1.3` = PC3 in this topology).

![[Pasted image 20261127151104.png]]

## 🖥️ Reading Cisco IOS Ping Output

The example is run from the **Cisco IOS CLI** — Cisco routers are used to simulate PCs because it is easier than setting up virtual PCs in GNS3.

```text
Sending 5, 100-byte ICMP Echos to 192.168.1.3
```

| Item | Meaning |
| --- | --- |
| **5** echos | Cisco IOS sends **5 ICMP Echo Requests** by default and expects **5 replies** |
| **100 bytes** | Default size of each ping |
| **`!`** | A **successful** ping (reply received) |
| **`.`** | A **failed** ping |
| **Success rate is 80 percent (4/5)** | 4 replies arrived out of 5 requests |
| **min / avg / max** | Round-trip times of the **4 successful** pings |

![[Pasted image 20261127151349.png]]

> [!warning] Why the first ping failed
> The first ping failed **because of ARP**: PC1 did not know PC3's destination MAC address, so it had to run ARP first. After PC1 learned PC3's MAC, the remaining pings succeeded. **The first ping after a MAC/ARP lookup is commonly lost.**

## 🗃️ Checking the ARP Table on IOS

```bash
show arp
```

- On **Windows, macOS, Linux**: `arp -a` (see [[ARP Table]]).
- On **Cisco IOS**: `show arp`, from **privileged EXEC mode**.

![[Pasted image 20261127151517.png]]

The table shows `192.168.1.1` (PC1 itself) and `192.168.1.3` (PC3), confirming ARP resolved PC3 before the pings succeeded.

> [!success] Key takeaway
> Ping = **ICMP Echo Request → Echo Reply**, unicast, **5 × 100-byte** packets by default in IOS. `!` = success, `.` = failure; a lost **first** ping usually means ARP had to resolve the destination MAC first.

---

### 🧭 Learning Path
← Previous: [[GNS3 Sim]] · Up: [[Ethernet LAN Switching 2]] · Next → [[CCNA/06 Ethernet LAN Switching 2/MAC Address Table]]

### 🔗 Related Notes
[[Ethernet LAN Switching 2]] · [[ARP Table]] · [[Wireshark packet capture]] · [[GNS3 Sim]] · [[ARP]] · [[ARP Request]] · [[ARP Reply]]
