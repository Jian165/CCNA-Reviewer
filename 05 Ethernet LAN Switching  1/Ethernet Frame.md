![[Pasted image 20261125145730.png]]

Note that I put the header on the left and the trailer on the right, opposite of the previous slide. Let’s look at the header. Don’t worry, I’ll cover these in more detail, but here’s a quick rundown. There are five fields in the header. First, the preamble and SFD, which means start frame delimiter. These are used for synchronization and to allow the receiving device to be prepared to receive the rest of the data in the frame. Next is the destination, the Layer 2 address to which the frame is being sent. Next, there is the source, the Layer 2 address of the device which sent the frame. The final field in the Ethernet header is the type. It indicates the Layer 3 protocol used in the encapsulated Packet, which is almost always Internet Protocol, or IP, version 4, or IP version 6. However, sometimes this is a length field, indicating the length of the encapsulated data, depending on the version of Ethernet. Now, the Ethernet trailer has only one field. That’s the FCS, which stands for frame check sequence. It’s used by the receiving device to detect any errors that might have occurred in transmission. Okay, now let’s take a look at these fields in more detail, starting with the preamble and start frame delimiter.

## Preamble & SFD

![[Pasted image 20261125150155.png]]

Here are the first two fields, the Preamble and SFD, which I like to think of as a set. Let’s look at the preamble first. It’s 7 bytes long. How many bits is that? If you remember, there are 8 bits in 1 byte, so, 7 times 8 is equal to... 56 bits. It’s a series of alternating 1s and 0s. Like this 10101010, which is one byte, seven times. The purpose of this is that it allows devices to synchronize their receiver clocks, to make sure they’re ready to receive the rest of the frame and the data inside. Okay, that’s the preamble, now the SFD. SFD stands for ‘start frame delimiter’. It’s length is 1 byte, or 8 bits. It’s bit pattern is 10101011, similar to each byte of the preamble but the last bit is a 1, not a 0. It indicates the end of the preamble and the beginning of the rest of the frame.

## Destination & Source

![[Pasted image 20261125150416.png]]

Now let’s look at the next two fields, the destination and source fields. They indicate the devices sending and receiving the frame, like when you send an email both the destination and source email addresses are included in the email, or when you send a letter in the mail, although that’s getting less and less common these days. The addresses used in Ethernet are the destination and source ‘MAC addresses’. MAC stands for media access control. The MAC address is a 6-byte, or 48-bit, address of the physical device. This is separate from a logical address like an IP address, the MAC address is actually assigned to the device when it is made. I’ll talk more about MAC addresses in a few slides, but let’s move on to the remaining fields of the Ethernet frame.

## Type/Length

![[Pasted image 20261125151021.png]]

The last field of the Ethernet header is the Type or Length field.  
It is 2-bytes, or 16-bits, in length.  
It can be used to represent either the type of the encapsulated packet, or the length of the encapsulated packet. What do I mean by that?  
Well, if the value in the field is 1500 or less, that means it is indicating the LENGTH of the encapsulated packet in bytes.  
For example, if the value in this field is 1,400, it means that the encapsulated packet is 1,400 bytes in length.  
However, a value of 1,536 or greater in this field indicates the TYPE of the encapsulated packet, which is usually internet protocol version 4 or version 6, and then the length is determined via other methods.  
For example, a value of 0x0800, which is written in hexadecimal, and is equal to 2048 in decimal.  
The 0x in front of 0800 is used to indicate hexadecimal, by the way.  
I’ll talk more about hexadecimal in a few slides when I talk in detail about MAC addresses.  
2048 is greater than 1536, of course, and its used to identify that the encapsulated packet is an IPv4 packet.  
0x86DD, which is equal to 34525 in decimal, is used to indicate that the encapsulated packet is an IPv6 packet.  
Okay, so those are all of the fields in an Ethernet header. Try to remember the lengths of each field...  
The preamble is 7 bytes long, the start frame delimiter is 1 byte, the destination is 6 bytes, as is the source, as both are MAC addresses, and the Type, or length, field is 2 bytes.  
Now let’s take a brief look at the only field of the Ethernet trailer, the FCS, or frame check sequence.

## FCS

The only field of the Ethernet trailer is the FCS, which as I mentioned stands for frame check sequence.

It is 4 bytes, or 32-bits in length.

It’s purpose is to detect corrupted data by running a ‘CRC’ algorithm over the received data.

CRC means cyclic redundancy check.

Cyclic refers to something called ‘cyclic codes', ‘redundancy’ refers to the fact that these 4 bytes at the end of the message enlarge the message without adding any new information, so they are redundant, and check refers to the fact that is CHECKS, or verifies, the data for errors.

Don’t worry about the details of CRC too much, just be aware of the term, and remember that the Ethernet frame’s Frame Check Sequence is a Cyclic Redundancy Check.

If you remember that, you should be good for the CCNA.

Feel free to read around on Wikipedia if you’re curious to learn more about Cyclic Redundancy Checks.

![[Pasted image 20261125151308.png]]


Okay, now we know all of the fields of an Ethernet frame, both the header and the trailer.

Try to recall the length of each field again…. The Preamble is 7 bytes….

The Start-frame delimiter is 1 byte….

The destination is 6 bytes... the source is 6 bytes also... the type, or length, field is 2 bytes...How about the trailer, what’s the length of the frame check sequence?

It is 4 bytes. This brings the total size, including header and trailer, to 26 bytes.

So, there’s an overview of each field of an Ethernet frame.

However, the fields I really want to focus on in this video are the source and destination MAC address fields.

I mentioned a little bit about MAC addresses, but let’s dig a little deeper. So let’s spend a few slides looking into MAC addresses.