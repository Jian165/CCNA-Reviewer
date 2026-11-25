
![[Pasted image 20261125153158.png]]

This time, however, it doesn’t flood the frame.  
This is known as a KNOWN UNICAST frame, because the destination is already in its MAC address table.  
Whereas UNKNOWN unicast frames are flooded, known unicast frames are simply forwarded to the destination, like this.  
And PC1 then processes the frame up the OSI stack, through the de-encapsulation process which we learned about in day 3’s video.  
One more point about these dynamic MAC addresses.  
On Cisco switches, these MAC addresses are removed from the MAC address table after 5 minutes of inactivity.  
So, if PC1 didn’t send any traffic for over 5 minutes, SW1 would remove the MAC address to clean out the MAC address table.  
Of course, if PC1 sent traffic again, SW1 would dynamically learn its MAC address again.