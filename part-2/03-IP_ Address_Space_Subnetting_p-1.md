# IP Address Space & Subnetting
IPv4 standard was created in 1981 via the RFC791 document.

| It occupies IP addresses in a range: | Total of IPv4 addresses |
|:------------------------------------:|:------------------------|
|    `0.0.0.0` => `255.255.255.255`    | **4,294,967,296**       | 

Originally directed by IANA org.

Historically, this range was divided into smaller ranges which are allocated for specific functions.

1. `Class A` address space which starts at `0.0.0.0` and ends at `127.255.255.255`. This range contains 128 networks, each of which has 
   16.7 million addresses. So, these networks take a format as: 
  - `0.anything` (Reserved)
  - `1.anything`  
  - `2.anything`
  - all the way upto `127.anything`  
The first octet denotes the network with the remaining octets available for **hosts** or for **subnetthing**. These were generally used 
    for huge networks (businesses or organizations, such as Apple, US Post, US Military etc.).
2. `Class B` address space starts at `128.0.0.0` and ends at `191.255.255.255`. This range is for regional authorities. So, these 
   networks take a format as:  
  - `127.0.anything`
  - `128.1.anything`
  - `128.2.anything`
  - all the way upto `191.255.anything`  
The first two octets are for the network, and the last two are for the organization to assign to **devices** or to **subnet** into 
    smaller networks. 
3. `Class C` address space starts at `192.0.0.0` and ends at `223.255.255.255`. So, these networks take a format as: 
   - `192.0.1.anything`
   - `192.0.2.anything`
   - `192.0.3.anything`
   - all the way upto `191.255.anything`  
With `Class C` the first three octets denote the **network**, and the remaining is available for **host** or **subnetting**. 
     Historically, `Class C` was used for smaller businesses, which require an IPv4 presence, but were not large enough for `Class A` or 
     `Clas B`, and they are controlled by regional authorities.
4. `Class D` (used for multicast) and `Class E` (is Reserved for private network use and local services –**Cloud Platforms**, such as **AWS**, 
   but they are not routable, and 
   you cannot 
   use them across the public IPv4 internet)

---
<div style="display: flex; justify-content: center; margin: 20px 0">
  <img src="../assets/03-IP_ Address_Space_Subnetting_p-1-1.png" style="width:700px; text-align: center">
</div> 

---

## Private IP addresses
These are defined within a Standard document called **RFC1918** and it defines **three** ranges of IPv4 addresses.

### Single Class A network
- The first private range is a single `Class A` network:  
`10.0.0.0` => `10.255.255.255` (1 x `Class A` Network).  
Total: 16,777,216 IPv4 addresses

This private range is often used with cloud environments, and it's generally chopped up into smaller **subnetworks**. 

- The second private range is:  
`172.16.0.0` => `172.31.255.255` (16 x `Class B` Network).  
Total: 16 x 65,536 IPv4 addresses each  

In AWS one of these private ranges `172.31.anything` is used for the default VPC.

- The third private range is:  
`192.168.0.0` => `192.168.255.255` (256 x `Class C` Network).  
Total: 256 x 256 IPv4 addresses each  

This range is generally used for Home and small Office networks.

## IPv6 vs IPv4
Remember how many of the IPv4 address are there (**4,294,967,296**), and possible devices connected may be times more than that, – IPv6 
was designed to solve this problem. With this IP version 6, we have a thousand times more IP addresses to use than in IPv4.
Number of IPv6 addresses : 
- _670 quadrillion_ per square millimetre of Earth space, or
- _50 octillion_ per human alive, or
- _79,228,163,000,000,000,000,000,000,000_ of IPv4 internets.

> With IPv6 the concept of IP addresses as a valuable commodity just goes away.
