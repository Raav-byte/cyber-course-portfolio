# Network Profile — My Machine

## Identity

* IPv4 address:
* Subnet mask / CIDR:
* MAC address:
* Network address:
* Broadcast address:

### Q1

My IPv4 address is:

My MAC address is:

### Q2

A private IP address is used inside a local network and is not directly routable on the public internet. A public IP address is used for communication over the internet. Routers use private IP addresses inside local networks so multiple devices can share an internet connection.

### Q3

An IP address operates at OSI Layer 3 (Network) and can change. A MAC address operates at OSI Layer 2 (Data Link) and is normally associated with the network interface hardware, although it can be changed or spoofed in software.

### Q4

A /24 subnet contains 256 total addresses and 254 usable host addresses.

My network address is:

My broadcast address is:

## Gateway and Reachability

* Default gateway:
* Ping to gateway (average):
* Ping to 1.1.1.1 (average):

### Q5

My default gateway is:

It is on the same subnet as my machine because:

### Q6

The average ping to my gateway was:

The average ping to 1.1.1.1 was:

The gateway was faster because it is on my local network, while 1.1.1.1 is reached through the internet.

### Q7

DNS made it possible to use example.com instead of an IP address because DNS translates domain names into IP addresses.

## DNS

* Configured DNS server(s):
* example.com resolves to:
* google.com resolves to:
* github.com resolves to:

### Q8

My computer is configured to use:

### Q9

My DNS lookup results were:

Large websites may have multiple IP addresses to distribute traffic, provide redundancy, and improve performance.

### Q10

Someone monitoring DNS traffic could see which domain names I look up. This could reveal information about the websites and services I use even when the actual website traffic is protected by HTTPS.

## Path to the Internet

* Hops to example.com:
* First hop:

### Q11

It took approximately:

The first hop was:

### Q12

A `* * *` result does not necessarily mean the connection is broken. Some routers or network devices do not respond to traceroute packets or may filter those responses while still forwarding normal traffic.

## Listening Ports

| Port | Protocol | Interface (localhost / all) | Common use |
| ---- | -------- | --------------------------- | ---------- |
|      |          |                             |            |
|      |          |                             |            |
|      |          |                             |            |

### Q13

The listening ports on my machine are listed above. Ports listening on localhost are generally only reachable from my own computer, while ports listening on all interfaces may be reachable from other devices on the network.

### Q14

A port listening only on localhost has a smaller attack surface because other devices cannot normally connect directly to it. A port listening on all interfaces can accept network connections and therefore requires more attention from a security perspective.

### Q15

My machine is exposing:

## Reflection

This exercise helped me understand how the networking concepts from the course appear on my own computer. One thing that surprised me was:

I noticed that:

The open port I would most want to investigate is:

I would investigate it because:

The command I think I will use most often is:

I would use it because:

Overall, this exercise showed me that understanding IP addresses, gateways, DNS, routing, and listening ports is useful for understanding the security of a computer and network.
