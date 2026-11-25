
The destination of the frame is AAAA.AA00.0002, but SW1 doesn’t know where that is.  
This, by the way, is called an ‘unknown unicast’ frame, a frame for which the switch doesn’t have an entry in its MAC Address table.  
Because the switch doesn’t know how to reach the destination, it has only one option. That is to FLOOD the frame.  
Flood means to forward the frame out of ALL of its interfaces, except the one it received the packet on. So, that would look like this.  
SW1 copies the frame and sends it out its F0/2 and F0/3 interfaces.  
It doesn’t send it out of its F0/1 interface, because that’s the interface it received the frame on. So, what happens next?

![[Pasted image 20261125152824.png]]


Well, PC3 ignores the packet, because the destination MAC address doesn’t match its own MAC address, it simply drops the packet.  
PC2, however, receives the packet, and then processes it normally, up the OSI stack.  

![[Pasted image 20261125153031.png]]

However, unless PC2 sends a reply of some sort, it stops there.  
SW1 never receives a packet from PC2, so it can’t learn PC2’s MAC address and use it to populate the MAC address table.  
So, let’s say PC1 sends another frame to PC2.  
Once again, it is received by SW1, and it already knows PC1’s MAC address, so it doesn’t have to add it to the MAC address table again.  
However, it still doesn’t know where PC2 is, so it once again floods the frame.  
PC3 drops the frame, and PC2 receives it and processes it normally.  
Now, let’s say PC2 then wants to send some data to PC1, maybe a reply to what PC1 sent to PC2.


![[Pasted image 20261125152948.png]]