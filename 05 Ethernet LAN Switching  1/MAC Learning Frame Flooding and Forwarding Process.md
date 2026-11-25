![[Pasted image 20261125153415.png]]

Let’s look at another example, this time with two switches. Notice the MAC address table of each switch.  
Currently they are empty, so once again we will see the process of MAC address learning and flooding.  
So, PC1 wants to send some information to PC3.  
The source MAC address of the packet is aaaa.aa00.0001, and the destination is aaaa.aa00.0003.  
So, PC1 sends the frame out of its network interface and it arrives at SW1.  
SW1 learns PC1’s MAC address from the source address field of the frame, and associates it with the interface on which it was received, F0/1.  
I’ll just say once more, I’m only writing a short version of the MAC address due to the lack of space here, really the frame and the MAC address table would include the whole MAC address, of course.

![[Pasted image 20261125153446.png]]

Once again, a MAC address learned in this way is called a ‘dynamically learned MAC address, or more often, a ‘dynamic’ mac address.

![[Pasted image 20261125153520.png]]

Now, SW1 has learned that PC1 can be reached via it’s F0/1 interface, but it still doesn’t know where PC3 is.  
Do you remember the name for this kind of frame? It’s called an ‘unknown unicast frame’.  
And what does a switch do with an unknown unicast frame? It floods it out all of its ports, except the one it was received on.  
In this case it will flood the frame out of F0/2 and F0/3, but not F0/1, because it received the frame on F0/1.  
PC2 drops the frame because the destination MAC Address doesn’t match its own MAC address. Now, what will SW2 do?  
Well, the exact same rules apply.  
Just like SW1 did, it uses the source MAC address field of the frame to dynamically learn PC1’s MAC address and the interface it can use to reach PC1.

![[Pasted image 20261125153632.png]]

That’s the meaning of the interface in the MAC address table, it doesn’t mean the device is directly connected to this interface.  
Now, SW2 received a unicast frame, that is a frame destined for a single device, but it doesn’t know how to reach that device, because its not in its MAC address table.  
One last time, what is this kind of frame called? It’s an unknown unicast frame. And what does the switch do with it?

![[Pasted image 20261125160544.png]]


Well, it received the frame on F0/3, so it won’t be flooded out of that interface, but it will be sent out of all other interfaces, F0/1 and F0/2 in this case.  
PC4 drops the frame because the destination MAC address doesn’t match its own.  
PC3, however, receives the frame, as the destination MAC address matches its own MAC address.  
Let’s say that PC3 is going to send a reply back to PC1.  

![[Pasted image 20261125160753.png]]

Notice the destination and source MAC address fields of the frame are reversed. PC3 sends the frame out of its network interface, and it is received by SW2.  
SW2 learns PC3’s MAC address, and enters the MAC address and the corresponding interface in its MAC address table.  

![[Pasted image 20261125160854.png]]

Just so we’re clear, the switch uses the SOURCE MAC ADDRESS field to fill its MAC address table because, if it receives a frame from that source on the interface, it knows that it can reach that MAC address via that interface.

So, lets continue.  
SW2 already has an entry for the destination MAC Address, aaaa.aa00.0001, in its MAC address table, so there is no need to flood the frame.  
Instead, it is forwarded normally out of the corresponding interface in the MAC address table, which is F0/3.  

![[Pasted image 20261125161045.png]]

The frame is received by SW1, which adds an entry for PC3’s MAC address in its MAC address table, with the interface F0/3, since that’s where it received the frame.  
Finally, since SW1 already has an entry for the destination MAC address in its own MAC address table, SW1 forwards the frame out of the corresponding interface, and it reaches its destination, PC1.  

Okay, so that was a lot of information. I was actually planning to cover the Ethernet LAN switching topics in a single video, but I’ve decided to split it up into two videos.


![[Pasted image 20261125161131.png]]