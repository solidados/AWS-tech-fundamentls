# IP Subnetting
> Subnetting is a process of breaking networks up into smaller and smaller pieces.

Classless Inter-Domain Routing (**CIDR**) lets us take networks and break them down. It defines  a way of expressing the size of a 
network, and this is called a `prefix`.  
(e.g.: `10.16.0.0/16` – range: `10.16.0.0` => `10.16.255.255`)  
`/16` – tells, that the first two octets of IP address `10.16._._` are a Network, and  
`the rest` – are the host part of IPv4 address in a range: `_._.0.0` => `_._.255.255`.

Now, let's say that we were allocated this range within our organization, but we needed to break it down into multiple smaller networks. 
Well, what we can do is to subnet this Network, for instance – break down into two parts.  
So, the single `/16` becomes two `/17` networks.  

The first network starts at the starting point, and ends at the half-way point.  
- `10.16.0.0/17` => `10.16.127.255` 
- `10.16.128.0/17` => `10.16.255.255`  
So, _one_ `/16` network is the same as _two_ `/17` networks.

---
<div style="display: flex; justify-content: center; margin: 20px 0">
  <img src="../assets/04-IP_ Subnetting_p-2-1.png" style="width:700px; text-align: center">
</div> 

---

Detailed:

<div style="display: flex; justify-content: center; margin: 20px 0">
  <img src="../assets/04-IP_ Subnetting_p-2-2.png" style="width:700px; text-align: center">
</div> 

---

