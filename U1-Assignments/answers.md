# Packet Tracer - Identify MAC and IP Addresses

## Reflection Questions

### 1. What different types of cables/media were used to connect devices?

Ethernet cables and wireless connections were used.

### 2. Did the cables change the handling of the PDU in any way?

No, the cables did not change the PDU.

### 3. Did the wireless Access Point do anything to the PDUs that it received?

It forwarded the PDUs to the correct device.

### 4. Was PDU addressing changed by the access point?

No, the addressing did not change.

### 5. What was the highest OSI layer that the Access Point used?

Layer 2, the Data Link layer.

### 6. At what Layer of the OSI model do cables and access points operate?

Layer 1 for cables and Layer 2 for access points.

### 7. When examining the PDU Details tab, which MAC address appeared first, the source or the destination?

The source MAC address appeared first.

### 8. Sometimes PDUs were marked with red Xs while others had green check marks. What is the significance of these markings?

A green check means the PDU was successful. A red X means the PDU failed or was dropped.

### 9. Every time that the PDU was sent between the 10 network and the 172 network, there was a point where the MAC addresses suddenly changed. Where did that occur?

The MAC addresses changed at the router.

### 10. Which device uses MAC addresses that start with 00D0:BA?

The router uses MAC addresses starting with 00D0:BA.

### 11. What devices did the other MAC addresses belong to?

They belonged to the PCs, switches, and other network devices.

### 12. Did the sending and receiving IPv4 addresses change in any of the PDUs?

No, the IPv4 addresses stayed the same from source to destination.

### 13. When you follow the reply to a ping, sometimes called a pong, what happens to the source and destination addresses?

The source and destination addresses switch around.

### 14. Why do you think the interfaces of the router are part of two different IP networks?

Because the router connects two different networks.

### 15. Which IP networks are connected by the router?

The 172.16.31.0 network and the 10.10.10.0 network.

# Packet Tracer - Use Telnet and SSH

## Part 1: Verify Connectivity

### Step 1: Verify IP Address on a PC

**Question: What command did you use to verify the IP address from DHCP?**

I used the `ipconfig` command.

## Part 2: Access a Remote Device

### Step 1: Telnet to HQ

**Question: Were you successful? What was the output?**

No. Telnet was not successful. The connection was refused because Telnet is disabled on the router.

### Step 2: SSH to HQ

**Question: What is the prompt after accessing the router successfully via SSH?**

The prompt is:

`HQ>`

