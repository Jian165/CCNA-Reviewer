---
tags:
  - ccna
  - networking
  - device
aliases:
  - Router
---

# 📡 Router

> [!abstract] In one line
> Routers connect **different networks** — such as two separate LANs — and forward data between them, often over the Internet.

## 🗺️ How Routers Fit In

We connect [[Switches]] to routers, and then connect the routers to the Internet.

![[Pasted image 20261111141458.png]]

When end hosts in the **New York Branch LAN** want to communicate with end hosts in the **Tokyo Branch LAN**, they send the data to their router, **R1**, which forwards it to Tokyo via the Internet.

> [!example] Step by step
> 1. PC1 in New York requests a file on SRV1 in Tokyo.
> 2. The request goes from PC1 to **R1** via **SW1**.
> 3. R1 forwards it over the Internet to **R2**.
> 4. R2 sends it to **SRV1** via **SW2**.
> 5. The reply follows the reverse path back to PC1.

## ⚙️ Characteristics of Routers

| Characteristic | Detail |
| --- | --- |
| **Interfaces** | Fewer network interfaces than switches |
| **Connectivity** | Provides connectivity **between** LANs |
| **Purpose** | Used to send data over the Internet |

> [!success] Key takeaway
> [[Switches]] connect devices **inside** a LAN; routers connect **separate** LANs together.

---

### 🔗 Related Notes
[[Network]] · [[Switches]] · [[Firewall]] · [[Interfaces And Cables]]
