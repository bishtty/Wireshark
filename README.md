# Wireshark
In this project I am using Wireshark to find any anomalies or intrusion in the network.

# Wireshark

************************Introduction************************

Wireshark is tool for creating  and analyzing PCAPs(network packet capture files)

### Collection Methods

Network taps; 

MAC Floods way of actively sniffing packets, is intended to stress the switch  and fill the CAM table(Content Addressable Memory is a system memory crontruct used by ethernet switch logic), Once the CAM table is filled the switch will no longer accept new MAC addresses and to keep network alive, the switch will send out packets to all the port.

ARP poisoinning- can redirect traffic from host to machine you are monitoring from.

### Filtering Captures

few operator that are used in wireshark

- and - operator: and / &&
- or - operator: or / ||
- equals - operator: eq / ==
- not equal - operator: ne / !=
- greater than - operator: gt / >
- less than - operator: lt / <

Note: few other operator that work beyond normal logical operator- contains, matches and bitwise_and operator.

Filtering by ip: `ip.addr == <IP Address>`

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/872d9749-e859-4476-b810-650706cd242f/aeac0038-cd9f-47a8-864c-8becf6d7ed23/Untitled.png)

filtering by SRC and DST: `ip.src == <SRC IP Address> and ip.dst == <DST IP Address>`

![10.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/872d9749-e859-4476-b810-650706cd242f/5fcfd0c5-0789-416d-95e9-182f607c5787/10.png)

filtering by TCP Protocols: `tcp.port eq <port #> or <Protocol Name>` 

![11.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/872d9749-e859-4476-b810-650706cd242f/b2699cf3-ae83-46b2-a208-eb3a5d6c19dd/11.png)

filtering by UDP protocols: `udp.port eq <Port #> or <protocol Name>`

### Packet Dissection
