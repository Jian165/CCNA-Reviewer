![[Pasted image 20261125151440.png]]

As I mentioned before, a MAC address is a 6-byte, or 48-bit, physical address assigned to the device when it is made.  
This is different than an IP address, which you assign in the CLI when you configure the device.  
You might also hear the term ‘burned in address', or BIA, to refer to a MAC address.  
This is because the address is ‘burned-in’ to the device as it is made.  
The MAC address is globally unique, no two devices in the world should have the same MAC address.  
Although, there are MAC addresses known as ‘locally-unique’ MAC address, which don’t have to be globally unique throughout the world, however in almost all cases MAC addresses are globally unique.  
The first 3 bytes of the MAC address are the OUI, which stands for organizationally unique identifier, and it's assigned to the company making the device.  
So Cisco, for example, will have various OUIs which only Cisco can use, and other makers will have their own OUIs which only they can use.  
The last 3 bytes, the second half of the address, are unique to the device itself.  
MAC addresses are written as a series of 12 hexadecimal characters.  
For those of you who aren’t sure what hexadecimal is, let’s check it out a little bit.

![[Pasted image 20261125152011.png]]

So here’s a simple network, just three PCs connected to a switch.  
Notice the interface names for the switch, F0/1, F0/2, and F0/3.  
F means fastethernet, so these are 100 megabit per second interfaces. I’ve also written the MAC address for each PC.  
You’re probably not going to see any MAC addresses like these, I’ve just simplified them for this demonstration.  
Notice each MAC address is a series of 12 hexadecimal digits, separated by periods.  
You may also see periods after every other digit, so for example PC1’s MAC address would be AA dot AA dot AA dot 00 dot 00 dot 01. But I tend to write them after every fourth character.  
The OUI, or organizationally unique identifier, which is the first half of the MAC address, is AAAAAA for each device, so we know that these PCs are all from the same maker.  
The second half of the MAC address of each device, however, is different for each PC, as the second half identifies the device itself.  
Now, let’s say PC1 wants to send some data to PC2.

