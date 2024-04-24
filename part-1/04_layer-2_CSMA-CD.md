# Layer-2 CSMA/CD
**L2** provides Controlled Access to the Physical medium.

Let's see what happens when one computer on the left wants to send data to the computer on the right:  
- The computer on the left (CoL) knows MAC-address of the computer on the right (CoR).
- CoL uses L2 (Ethernet) and intends to send data to `3e:22:fb:b9:5b:76`
- L2 creates an Ethernet Frame (F1) containing the data that is desired to be sent in the `Payload` component of the Frame.
- So, the F1 has a destination (MAC-address) and the `Payload` data to be sent.

L2 can look for a `carrier` signal. If any other device on the network were transmitting on this point you would see the signal on L1 
network. So it's looking to sense a carrier. And this is a job of `CSMA`.

> `CSMA` – Carrier Sense Multiple Access

If a carrier were not detected, L2 passes a Frame to L1.  
L1 doesn't understand the Frame as anything beyond a _block of data_, and so it transmits this _block of data_ on to `shared medium`.  

The CoR receives a raw bit stream, and it passes it up to its L2.  
L2 reviews the destination MAC-address of the Frame and sees that the Frame destined to itself and so it can pass that `Payload` data to 
the Application.

## Media Access Control
If we assume that at the same time that the CoL was transmitting, the CoR attempted to do the same. If the carrier is detected, so the 
opposite machine shall wait, until the carrier is not detected and the other transmission is free to go.  

## Encapsulation
Now, I want to reiterate a term again, and that term is **encapsulation**.
> Encapsulation - is a process of taking some data and wrapping it in something else.

In our case the data is encapsulated inside a `Frame` at each side before giving it back its intended data, the data is de-encapsulated, 
the `Payload` is extracted from the `Frame`.  
As data passes down the OSI model, it's encapsulated in more and more different components.

## CSMA/CD
> CD - Collision Detection

If a Collision is detected, then a jam signal is sent by all devices which detect it, and then a random `back-off` occurs.  
The `back-off` is a period of time during which no device will attempt a transmission. So after this `back-off` period occurs, the 
transmission is retried.

## SWITCH
As it was said before, the HUB is very dumb, more L1 alike device, and it transmits Frames to all devices which are connected with.

This is where comes a **SWITCH**.  
SWITCH is L2's intelligent device, it works in the same way physically as a HUB, but it understands L2, has a L2 software running, and so 
provides 
significant advantages.  
It has a MAC-addresses table, which is empty by default.  
Over time it learn what's connected to each port, so it gets each MAC-address and populate it to a table under specific Port.  
Therefore it can see the Source's and Destination's MAC-address and ports they are connected to.

If the SWITCH does not receive the Destination MAC-address, so it will transfer the Frame to all the ports.

Because each Port is a separate Collision Domain, the only two things which can be transmitted at the same time are the device and the 
port it is connected to. So if there is a collision, it will be limited to that one port only.

## Summary
**Layer 2 DataLink** has:
- Identifiable devices (by MACs)
- Media Access Control (sharing)
- Collision Detection
- Unicast communication `1:1`
- Broadcast communication `1:ALL`
- Switches - Hubs alike, but with super powers of L2, and they help to avoid collisions.
