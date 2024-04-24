# Layer-1 Physical
`Layer 1`, also known as the `Physical` layer, is the first and lowest layer in the OSI model.  

It is responsible for the physical transmission of data over a communication channel, such as a:
- wire, 
- cable, or 
- wireless signal.  

This layer defines the physical characteristics of the _communication medium_, including _voltage levels_, _cable types_, and _signaling 
methods_, to ensure that data is transmitted accurately and reliably between devices. 

In this lesson, you will explore the functions and protocols of Layer 1 in detail to understand how it enables communication between 
devices in a network.

## Copper cable
For copper cable electrical signals are used.  
So a certain voltage is defined as binary one (1), say one volt, and a certain voltage is binary zero (0), say -1 volt.

## Physical - HUB
If you need to add more than two devices, you may use HUB to connect them.  
Anything received on any Port, is transmitted on every other Port of the HUB, including any `Errors` or `Collisions`.  

Conceptually a HUB creates a four connector network cable; one single piece of physical medium which four devices can be connected to.

### Remember
- on Layer-1 there are no `device addressing` – all data is processed by all devices, but it is fixed by Layer-2
- if all devices transmit at once, a collision occurs. This corrupts any transmissions on a `shared medium`. Only one thing can 
transmit at once on a `shared medium` and be legible to everything else
- Layer-1 has no `media control` and no `collision detection`
- Layer-1 is not able to detect when collisions occur.
