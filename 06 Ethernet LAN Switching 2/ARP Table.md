---
tags:
  - ccna
  - networking
  - arp
  - windows
  - cli
aliases:
  - ARP Table
  - ARP Cache
---

# 🗃️ The ARP Table

> [!abstract] In one line
> The **ARP table** stores **IP address → MAC address** mappings so a host does not have to repeat ARP for every packet; view it with `arp -a` on Windows, macOS, and Linux.

![[Pasted image 20261127150423.png]]

## 🔎 Viewing the Table

```bash
arp -a
```

> [!info] Cross-platform
> `arp -a` works on **Windows, macOS, and Linux**. On Cisco IOS the equivalent command is `show arp` from privileged EXEC mode (see [[Ping]]).

## 📊 Reading the Columns

| Column | Contents |
| --- | --- |
| **Internet address** | IP addresses |
| **Physical address** | The MAC address that corresponds to each IP address |
| **Type** | `static` or `dynamic` — how the entry was created |

| Type | Meaning |
| --- | --- |
| **static** | A **default entry** — it was **not** learned by sending an ARP request. |
| **dynamic** | The entry **was learned** by sending an ARP request and receiving an ARP reply. |

## 🏠 Real-World Example

In the example table, the dynamic entry `192.168.0.1` with its MAC address is the **home router**. The PC used ARP to learn the router's MAC address.

> [!important] Dynamic vs static
> Normal communication entries are **dynamic** — created through the ARP request/reply process seen in [[ARP Request]] and [[ARP Reply]]. Entries marked **static** were preconfigured and never learned through ARP.

> [!success] Key takeaway
> Use `arp -a` to inspect the IP-to-MAC mappings a host has learned. `dynamic` = learned via ARP; `static` = default/preconfigured entry.

---

### 🧭 Learning Path
← Previous: [[ARP Reply]] · Up: [[Ethernet LAN Switching 2]] · Next → [[GNS3 Sim]]

### 🔗 Related Notes
[[Ethernet LAN Switching 2]] · [[ARP]] · [[ARP Request]] · [[ARP Reply]] · [[Ping]] · [[Wireshark packet capture]]
