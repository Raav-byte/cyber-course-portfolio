U1-03f Subnetting Basics
Task 1 - Binary ↔ decimal for a single octet
1.1 - Decimal to binary
Decimal	Binary
10	00001010
210	11010010
168	10101000
16	00010000
255	11111111
128	10000000
192	11000000
248	11111000
0	00000000

Work:

210 = 128 + 64 + 16 + 2 = 210
So 210 = 11010010

168 = 128 + 32 + 8 = 168
So 168 = 10101000

248 = 128 + 64 + 32 + 16 + 8 = 248
So 248 = 11111000

1.2 - Binary to decimal
Binary	Decimal
11000000	192
11111111	255
10101000	168
00010000	16
11111000	248
11010010	210

1.3 - Full-address conversion
10.210.168.16 →

00001010.11010010.10101000.00010000

192.168.0.1 →

11000000.10101000.00000000.00000001

172.16.5.100 →

10101100.00010000.00000101.01100100

11000000.10101000.00000001.00000001 →

192.168.1.1

00001010.00001010.00000000.01001011 →

10.10.0.75

Task 2 - Recognize the class and CIDR
2.1 - What class is it?
Address	Class	Default mask (dotted)	Default mask (CIDR)
10.0.0.5	A	255.0.0.0	/8
192.168.1.1	C	255.255.255.0	/24
172.16.4.20	B	255.255.0.0	/16
8.8.8.8	A	255.0.0.0	/8
200.100.50.25	C	255.255.255.0	/24

2.2 - Mask ↔ CIDR ↔ binary
Dotted-decimal	CIDR	Binary
255.255.255.0	/24	11111111.11111111.11111111.00000000
255.255.0.0	/16	11111111.11111111.00000000.00000000
255.0.0.0	/8	11111111.00000000.00000000.00000000
255.255.255.192	/26	11111111.11111111.11111111.11000000
255.255.248.0	/21	11111111.11111111.11111000.00000000
255.255.255.128	/25	11111111.11111111.11111111.10000000

2.3 - Networks and hosts per class
Class	Default CIDR	Number of possible networks	Number of hosts per network
A	/8	128 nets	16,777,214 hosts
B	/16	16,384 nets	65,534 hosts
C	/24	2,097,152 nets	254 hosts

Task 3 - The five key values
3.1 - 172.16.0.0/16
subnet mask:       255.255.0.0
network address:   172.16.0.0
default gateway:   172.16.0.1
host range start:  172.16.0.2
host range end:    172.16.255.254
broadcast:         172.16.255.255

3.2 - 10.10.0.0/26
subnet mask:       255.255.255.192
network address:   10.10.0.0
default gateway:   10.10.0.1
host range start:  10.10.0.2
host range end:    10.10.0.62
broadcast:         10.10.0.63

Work:

256 - 192 = 64, so the block is .0 to .63.

3.3 - 192.168.5.0/28
subnet mask:       255.255.255.240
network address:   192.168.5.0
default gateway:   192.168.5.1
host range start:  192.168.5.2
host range end:    192.168.5.14
broadcast:         192.168.5.15

Work:

256 - 240 = 16

16 - 2 = 14 usable hosts

3.4 - 10.0.0.0/30
subnet mask:       255.255.255.252
network address:   10.0.0.0
default gateway:   10.0.0.1
host range start:  10.0.0.2
host range end:    10.0.0.2
broadcast:         10.0.0.3

Work:

256 - 252 = 4

4 - 2 = 2 usable hosts

A /30 is useful for a point-to-point link because it gives 2 usable addresses.

3.5 - 192.168.100.128/25
subnet mask:       255.255.255.128
network address:   192.168.100.128
default gateway:   192.168.100.129
host range start:  192.168.100.130
host range end:    192.168.100.254
broadcast:         192.168.100.255

Work:

256 - 128 = 128

.128 + 128 - 1 = .255

Task 4 - Which subnet does this host belong to?
4.1 - 10.10.0.75/26
Network address of this subnet:

10.10.0.64

Broadcast of this subnet:

10.10.0.127

Valid host?

Yes.

The /26 blocks are 0-63, 64-127, 128-191 and 192-255.
75 is between 64 and 127, so it is a valid host.

4.2 - 192.168.1.200/26
Network address:

192.168.1.192

Broadcast:

192.168.1.255

Valid host?

Yes.

200 is between 192 and 255, so it is a valid host.

4.3 - 172.16.5.130/25
Network address:

172.16.5.128

Broadcast:

172.16.5.255

Valid host?

Yes.

The /25 blocks are 0-127 and 128-255.
130 is inside the second block and is not the network or broadcast address.

4.4 - 10.0.0.0/30
Network address:

10.0.0.0

Broadcast:

10.0.0.3

Valid host?

No.

10.0.0.0 is the network address. The usable hosts are 10.0.0.1 and 10.0.0.2.

Task 5 - Slicing up a /24
5.1 - Four equal /26 subnets
Original network:

192.168.10.0/24

Subnet 1
Network address: 192.168.10.0
Default gateway: 192.168.10.1
Host range:      192.168.10.2 - 192.168.10.62
Broadcast:       192.168.10.63

Subnet 2
Network address: 192.168.10.64
Default gateway: 192.168.10.65
Host range:      192.168.10.66 - 192.168.10.126
Broadcast:       192.168.10.127

Subnet 3
Network address: 192.168.10.128
Default gateway: 192.168.10.129
Host range:      192.168.10.130 - 192.168.10.190
Broadcast:       192.168.10.191

Subnet 4
Network address: 192.168.10.192
Default gateway: 192.168.10.193
Host range:      192.168.10.194 - 192.168.10.254
Broadcast:       192.168.10.255

5.2 - Enough hosts?
CIDR	Total addresses	Usable hosts
/24	256	254
/25	128	126
/26	64	62
/27	32	30
/28	16	14
/29	8	6
/30	4	2

A /26 would fit all four departments, but it would waste addresses for the smaller departments.

Department	Hosts needed	Suggested CIDR	Usable hosts
A	50	/26	62
B	25	/27	30
C	10	/28	14
D	2	/30	2

A needs /26 because /27 only has 30 usable hosts.

B can use /27 because it has 30 usable hosts.

C can use /28 because it has 14 usable hosts.

D can use /30 because it has exactly 2 usable hosts.

Task 6 - IPv6, briefly
6.1 - Hex ↔ decimal ↔ binary refresher
Hex	Decimal	Binary
0	0	0000
5	5	0101
a	10	1010
f	15	1111

6.2 - Compress these IPv6 addresses
2001:0df8:23f2:0000:0000:0000:0000:0f11

→ 2001:df8:23f2::f11

2001:0000:00d0:00f2:0000:0000:0000:0f11

→ 2001:0:d0:f2::f11

fe80:0000:0000:0000:0000:0000:0000:0001

→ fe80::1

6.3 - Why do we need IPv6?
We need IPv6 because IPv4 does not have enough addresses for all the devices connected to networks today. IPv6 uses 128-bit addresses, which gives us a much larger number of possible addresses.
