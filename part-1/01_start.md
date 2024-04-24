# OSI Model Introduction
> The OSI (Open Systems Interconnection) model is a conceptual framework that describes the communication functions of a telecommunication or computer system.

## Local Networking (Ethernet)
This is about how data moves between devices in your local network.  
This is foundational to everything; it's the Starting point or Ending point of data which moves across the Internet.

## Routing
This article will cover the topics of how data moves across the internet from your network through to e.g. Netflix, or AWS.  
When data moves across the internet, it moves across many interconnected networks, so that's why a local networking matters.  
## Reliable transit
- Segmenting, 
- Ports,
- Sessions

## Applications

## OSI (Open Systems Interconnection)
This is a concept framework that describes the communication functions of telecommunication or computer systems.  

### 7-Layer Model
So, let's start with how does this Model look:  

Table: **Networking Stack**

|  Layer  | Name           |
|:-------:|:---------------|  
| Layer-7 | `Application`  |  
| Layer-6 | `Presentation` |  
| Layer-5 | `Session`      |  
| Layer-4 | `Transport`    |  
| Layer-3 | `Network`      |  
| Layer-2 | `Data Link`    |  
| Layer-1 | `Physical`     |  

Table: **OSI Groupings**

| Media Layers   | Host Layers       |
|----------------|-------------------|
| L3 `Network`   | L7 `Application`  |
| L2 `Data Link` | L6 `Presentation` |
| L1 `Physical`  | L5 `Session`      |
|                | L4 `Transport`    |

- **Media Layers** is dealing with how data move between point **A** and point **B**. This could be in the same Local Network, or on the 
  opposite side of the Planet.
- **Host Layers** is dealing with how data chop-top and re-assembled for transport, and how it's formatted so, it is understandable by both 
  sides of the network.

On the Layer-7 there may be a Web Browser or a Server. So, the data flows down through the Layers at one side to the bottom one (Layer-1)
, then it arrives to the other side of Layer-1 and flows back up through the Layers to the Server on Level-7.
