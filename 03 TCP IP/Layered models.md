---
tags:
  - ccna
  - networking
  - tcpip
  - models
aliases:
  - Layered Models
  - Network Models
  - Layered Model
---

# 🧱 Layered Models

> [!abstract] In one line
> A **layered model** groups the many jobs of networking into smaller layers, each with one clear role.

## 🧩 Why Layers?

Networks do many jobs at once. A layered model separates those jobs so each one can be studied and solved on its own.

| Networking job | Meaning |
| --- | --- |
| **Physical transmission** | Send signals over a cable, fiber, or radio |
| **Local delivery** | Move a message across a local area network (LAN) |
| **Routing** | Forward messages between networks |
| **End-to-end conversations** | Keep communication between two hosts organized |
| **Applications** | Create, send, and interpret the actual data |

| Problem | How layers help |
| --- | --- |
| Networking is too complex to handle as one task | Split it into smaller jobs |
| Many protocols work together | Group them by what they do |
| One technology may change | Replace one layer without redesigning everything |
| Different vendors build different devices | Everyone follows the same layer roles |

> [!important] The layer rule
> Each layer **uses the services of the layer below** and **provides services to the layer above**.

## 📚 Protocols Form a Stack

A **protocol** usually belongs mainly to one layer. Examples: **HTTP**, **TCP**, **IP**, and **Ethernet**.

Together these protocols form a **protocol stack** — often called the **network stack**.

Most protocols live mainly at one layer, but some lines are blurred. Treat layers as a guide for understanding the job of each protocol, not as perfect boxes.

![[Pasted image 20261122134120.png]]

> [!tip] Remember
> A stack is a team of protocols. Each protocol has a different job, but they work together to move data.

## 🧭 Models Are Descriptions, Not Laws

Different books and courses use different models: some have **4 layers**, some have **5 layers**, and some have more.

The model itself is not a physical thing — it is a way to describe and understand networking.

For example, **RFC 791** defined IP in **1981** and is still the current standard. RFCs are freely available online, but they are dense reading; you do not need to read them for CCNA.

| Model idea | Meaning |
| --- | --- |
| **Layer** | A group of related jobs |
| **Service** | What a layer does for the layer above it |
| **Protocol** | The rules used at a layer |
| **Stack** | The layers and protocols working together |

## 🔢 The 5-Layer Course Model

This course uses five layers because their names clearly match their jobs.

| Model view | Layer names |
| --- | --- |
| **Original TCP/IP view** | Application, Transport, Internet, Link |
| **This course** | Application, Transport, Internet, Local Network, Physical |

| Layer | Name | Main question it answers |
| --- | --- | --- |
| **5** | [[Layer 5 Application Layer|Application]] | What data is being sent? |
| **4** | [[Layer 4 Transport Layer|Transport]] | Which application process receives it? |
| **3** | [[Local 3 Internet Layer|Internet]] | Which destination host receives it? |
| **2** | [[Local 2 Network Layer|Local Network]] | Which next hop carries it? |
| **1** | [[Layer 1 Physical Layer|Physical]] | How are the bits sent as signals? |

## 🧠 Quick Recap

| Topic | Fact |
| --- | --- |
| **Why layers exist** | To divide a complex task into smaller jobs |
| **Each layer** | Has its own role and works with the layers around it |
| **Lower layer** | Provides a service to the layer above |
| **Upper layer** | Uses the service provided by the layer below |
| **Model** | A description, not a physical rule |

> [!success] Key takeaway
> A layered model makes networking easier to learn, troubleshoot, and improve because each layer has one clear job.

---

### 🧭 Learning Path
← Previous: [[Who Defines The Standards]] · Up: [[TCP IP]] · Next → [[Analogy building a Model]]

### 🔗 Related Notes
[[TCP IP]] · [[Analogy building a Model]] · [[The TCP IP Model]] · [[OSI Model]] · [[Other Model]] · [[Standards And Protocols]]
