# Network Profile — My Machine

## Identity

* IPv4 address: `172.20.XX.X`
* Subnet mask / CIDR: `255.255.255.240` (`/28`)
* MAC address: `70-08-94-DA-xx-xx`
* Network address: `172.20.xx.x
* Broadcast address: `172.20.xx.xx`

**Q1:** My IPv4 address is `172.20.XX.X` and my MAC address is `70-08-94-DA-xx-xx`.

**Q2:** A private IP is used inside a local network, while a public IP is used on the internet. Private IPs let multiple devices use the same internet connection.

**Q3:** An IP address works at Layer 3 and can change. A MAC address works at Layer 2 and is normally connected to the network hardware.

**Q4:** A `/28` has 16 total addresses and 14 usable addresses. My network address is `172.20.10.0` and my broadcast address is `172.20.10.15`.

## Gateway and reachability

* Default gateway: `172.20.xx.x`
* Ping to gateway (avg): `12 ms`
* Ping to 1.1.1.1 (avg): `49 ms`

**Q5:** My gateway is `172.20.xx.x`. It is on the same subnet as my computer.

**Q6:** The gateway was faster because it is on my local network. `1.1.1.1` is reached through the internet.

**Q7:** DNS allowed me to use `example.com` instead of an IP address.

## DNS

* Configured DNS server(s): `172.20.10.1`, `fe80::f8e5:ceff:fed0:5964`
* example.com resolves to: `2606:4700:10::ac42:93f3`, `2606:4700:10::6814:179a`

**Q8:** My computer uses `172.20.xx.x` and an IPv6 DNS server.

**Q9:** `google.com` resolved to `2a00:1450:4026:808::200e` and `github.com` resolved to `140.82.121.4`. Large websites can have multiple IPs for performance and reliability.

**Q10:** Someone watching DNS could see which websites I look up, even if the websites use HTTPS.

## Path to the internet

* Hops to example.com: `9`
* First hop: `172.20.10.1`

**Q11:** It took 9 hops to reach example.com. The first hop was my gateway.

**Q12:** `* * *` usually means a router did not respond to the traceroute request. It does not necessarily mean the connection is broken.

## Listening ports

| Port        | Protocol | Interface | Common use          |
| ----------- | -------- | --------- | ------------------- |
| 135         | TCP      | All       | Windows RPC         |
| 139         | TCP      | All       | NetBIOS             |
| 445         | TCP      | All       | SMB/file sharing    |
| 5040        | TCP      | All       | Application/service |
| 6463        | TCP      | Localhost | Application         |
| 42050       | TCP      | Localhost | Application         |
| 49664–49670 | TCP      | All       | Windows RPC         |

**Q13:** My computer has several ports listening on all interfaces and a few that are localhost-only.

**Q14:** Port 445 is commonly used for SMB/file sharing. A localhost-only port is less exposed because other devices normally cannot connect to it. A port listening on all interfaces has more exposure.

**Q15:** I was surprised that my computer had several network-facing ports open. I would investigate ports 139 and 445 because they are related to Windows network/file sharing.

## Reflection

I was surprised by how many ports were listening on my computer. I expected there to be fewer. The ports I would investigate most are 139 and 445 because they are used for Windows network and file sharing .The command I think I will use most is `ipconfig /all`. This task also made it easier to understand how IP addresses, DNS, gateways and ports work together. Before doing this, these felt more difficult, but checking my own computer made them much easier to understand.
