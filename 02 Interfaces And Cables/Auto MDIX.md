---
tags:
  - ccna
  - networking
  - cabling
aliases:
  - Auto MDI-X
  - Auto-MDIX
---

# 🤖 Auto MDI-X

> [!abstract] In one line
> **Auto MDI-X** lets modern devices automatically detect which pins their neighbor is transmitting on and adjust their own transmit and receive pins — removing the need to worry about straight-through vs crossover cables.

## 🆕 The Problem It Solves

Straight-through and crossover cable rules are still important to know, and they can cause issues in networks even today. However, most modern networking devices have evolved **beyond** having to worry about them.

Previously, if two **switches** were connected with a **straight-through** cable, they would be **unable to communicate** — each one would try to transmit on the same pins.

![[Pasted image 20261114150351.png]]

## ⚙️ How It Works

Auto MDI-X lets devices:

1. Automatically **detect** which pins their neighbor is transmitting data on.
2. **Adjust** which pins they use to transmit and receive data.
3. Then **exchange data normally**.

## 🌍 Real World and Exam

> [!tip] Practical takeaway
> Unless you're working with **old** network equipment, you generally **don't** have to worry about straight-through and crossover cables.

> [!important] Still know the theory
> The concept of **auto MDI-X** is worth learning for both the **exam** and **real-world networking** — you should still understand why crossover cables exist.

> [!success] Key takeaway
> **Auto MDI-X automatically corrects** mismatched transmit/receive pins, so modern devices work with either cable type — but the underlying straight-through and crossover rules are still exam material.

---

### 🔗 Related Notes
[[Interfaces And Cables]] · [[Straight-through cable]] · [[Cross Over Cable]] · [[10BASE-T, 100BASE-T]] · [[1000BASE -T, 10GBASE-T]]
