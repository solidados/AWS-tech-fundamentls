# Layer-2 DataLink
This is the most critical layer in the entire OSI seven-layer model.  
Everything above this Layer relies on device-to-device communication which the `DataLink` provide.

The DataLink layer runs above Layer-1 and supports the transfer of data.

## Frame
> Frame is a format for sending information over a `Layer-2` network.

L2 also introduces a unique hardware address, called MAC-address for every device on a network.

This hardware address is a hax-decimal address, which is 48-bits<sup>*</sup> long, and it looks like: `3e:22:fb:b9:5b:75`.  
The MAC-address is formed of two parts which make it _globally_ unique:  
- OUI (organizationally unique identifier) from manufacturer;
- NIC (network interface controller)

> <sup>*</sup> 1 byte === 8 bits  

So, it works this:
- L2 provides frames, and
- L1 handles the physical transmission and reception from the physical shared medium.

## Frame Components
Now a Frame, that L2 uses for communication is a "container" of sorts and has a few different Components.

**Frame Starter**:
1. `Preamble` (56 Bits | SFD - 8 Bits) - it is a start frame delimiter. It allows devices to know that it's a start of the Frame 
   transmitting.  

**MAC-header**:  
2. `Destination MAC-address` - a frame can be sent to a specific device on a network by putting its MAC-address in a `Destination` field,
   or you can put `All Fs` if you want to send a frame on every device on the local network—aka **Broadcast**.
3. `Source MAC-address` - is set to the device that is transmitting the frame, and this allows it to receive replies.
4. `ET (EtherType)` (16 Bits) - commonly used to specify which **L3 Protocol** is putting its data inside a Frame (e.g. IP or the 
   internet protocol).
5. `Payload` (46 - 1500 Bytes in size for standard frames) - is the data the Frame carries from source to destination. It is generally 
   provided by **L3**, and the **ET** attribute defines which **L3** protocol is used (e.g. IP).  

This process is called `encapsulation`. You have something which **L3** generates, often it is an `IP-packet` and this is put inside an 
ethernet frame (encapsulated in it).

6. `FCS` (Frame Check Sequence = 32 Bits) - used to identify any `errors` in the Frame. It's a simple `CRC` check, and it allows the 
   destination to check if corruption has occurred or not.
