## Physical Layer


![[Pasted image 20261125144253.png]]

First let’s review. This is a slide from Day 3’s video of describing the physical layer of the OSI model. The physical layer defines physical characteristics of the medium used to transfer data between devices.For example, voltage levels, maximum transmission distances (like Ethernet UTP cables’ 100 meter limit), physical connectors, cable specifications, etc.Digital bits are converted into electrical (for wired connections) or radio (for wireless connections) signals. All of the information in Day 2’s video (cables, pin layouts, etc.) is related to the Physical Layer.So, we’ve covered a good amount about the physical layer, learning about copper UTP cables, fiber-optic cables, RJ45 connectors, etc.

## Data Link Layer

![[Pasted image 20261125144425.png]]

Let’s also review this slide about Layer 2, the data link layer, from Day 3’s video. Layer 2 provides node-to-node connectivity and data transfer, for example PC to switch, or switch to router, or router to router, etc. It defines how data is formatted for transmission over a physical medium (for example, copper UTP cables). IT detects and possibly corrects Physical Layer errors. It uses Layer 2 addressing, which is separate from Layer 3 addressing. Remember, IP addresses are Layer 3 addresses, not Layer 2. Switches operate at Layer 2. So, in this video we’ll be talking about Ethernet LAN switching, and Ethernet involves Layer 1 and Layer 2 of the OSI model. Since we’ve already covered the Layer 1 Ethernet standards like UTP cables, this video will be about Layer 2. Then, as we continue with this series, we’ll move up the layers of the OSI model, until you get a complete image of how data is sent and received over networks.

## PDUs 

![[Pasted image 20261125145015.png]]

This shows the encapsulation process as data is prepared to be sent over a network.At the top, the data prepared by the upper layers of the OSI model is simply called data.A layer 4 header is added, and this combination of data and layer 4 header is called a segment. A layer 3 header is added to the segment, and it is now called a packet.  Finally, a Layer 2 header and trailer are added to the packet, and it becomes a frame. Once again, these different stages of preparing data to be forwarded are called ‘protocol data units, or PDUs. For example, the Layer 2 PDU is a frame. Today we’re going to focus on how switches receive and forward frames, specifically Ethernet frames, since it’s the Layer 2 protocol used in virtually every LAN in existence today. Let’s take a look at the actual contents of this Ethernet header and trailer. So, here’s an Ethernet frame, encapsulating the packet with a header and trailer.


