![[Pasted image 20261125152415.png]]

After SW1 receives the frame, it looks at the source MAC address field of the frame and then uses that information to LEARN where PC1 is.  
As you can see here, it adds the MAC address AAAA.AA00.0001 to it’s MAC Address table, and it associates that MAC address with its F0/1 interface.

![[Pasted image 20261125152547.png]]

Every switch will keep a MAC address table like this, and they fill the MAC address table dynamically by looking at the source MAC address of frames it receives.  
Since SW1 received a frame from source MAC Address AAAA.AA00.0001 on it’s F0/1 interface, it knows that I can reach that MAC address on that interface, and adds it to the MAC address table.  
This is a very important concept, so I’ll probably repeat it multiple times.  
This is how switches dynamically learn where each device on the network is, by looking at the source MAC address of the frame.  
Now, there is one problem.
