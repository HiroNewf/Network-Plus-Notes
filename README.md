# Network+ Notes
The table of contents will take you right to the section you click on and the links for the headers of each section will take you to the Professor Messer video for that section. This probably isn't really going to help anyone else because it is for the 007 version of Network+ but it is here anyways 

## Table of contents
* 1.1 [Introduction to IP](https://github.com/HiroNewf/Network-Notes/blob/main/Network%2B%20Notes.md#introduction-to-ip)
* 1.1 [Common Ports](https://github.com/HiroNewf/Network-Notes/blob/main/Network%2B%20Notes.md#common-ports)
* 1.2 [Understand the OSI Model](https://github.com/HiroNewf/Network-Notes/blob/main/Network%2B%20Notes.md#understanding-the-osi-model)
* 1.3 [Introduction to Ethernet](https://github.com/HiroNewf/Network-Notes/blob/main/Network%2B%20Notes.md#introduction-to-ethernet)
* 1.3 [Network Switching Overview](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#network-switching-overview)
* 1.3 [Broadcast and Collision Domains](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#broadcast-domains-and-collision-domains)
* 1.3 [Unicasts, Broadcasts and Multicasts](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#unicasts-broadcasts-and-multicast)
* 1.3 [Protocol Data Units](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#protocol-data-units)
* 1.3 [Network Segmentation](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#network-segmentation)
* 1.3 [Spanning Tree Protocol](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#spanning-tree-protocol)
* 1.3 [Switch Interface Properties](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#switch-interface-properties)
* 1.3 [Static and Dynamic Routing](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#static-and-dynamic-routing)
* 1.3 [IGP and EGP](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#igp-and-egp)
* 1.3 [Dynamic Routing Protocols](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#dynamic-routing-protocols)
* 1.3 [IPv4 and IPv6 Addressing](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#ipv4-and-ipv6-addressing)
* 1.3 [Configuring IPv6](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#configuring-ipv6)
* 1.3 [Prioritizing Traffic](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#prioritizing-traffic)
* 1.3 [Network Address Translation](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#network-address-translation)
* 1.3 [Access Control Lists](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#access-control-lists)
* 1.3 [Circuit Switching and Packet Switching](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#circuit-switching-and-packet-switching)
* 1.3 [Software Defined Networking](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#software-defined-networking)
* 1.4 [Binary Math](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#binary-math)
* 1.4 [IPv4 Addresses](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#ipv4-addresses)
* 1.4 [Classful Subnetting](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#classful-subnetting)
* 1.4 [IPv4 Subnet Masks](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#ipv4-subnet-masks)
* 1.4 [IPv6 Subnet Masks](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#ipv6-subnet-masks)
* 1.4 [Calculating IPv4 Subnets and Hosts](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#calculating-ipv4-subnets-and-hosts)
* 1.4 [Seven Second Subnetting](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#seven-second-subnetting)
* 1.4 [Assigning IPv4 Addresses](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#assigning-ipv4-addresses)
* 1.4 [Assigning IPv6 Addresses](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#assigning-ipv6-addresses)
* 1.5 [Network Topologies](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#network-topologies)
* 1.5 [Common Network Types](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#common-network-types)
* 1.5 [Internet Of Things Topologies](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#internet-of-things-topologies)
* 1.6 [Wireless Standards](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#wireless-standards)
* 1.6 [Cellular Network Standards](https://github.com/HiroNewf/Network-Notes/blob/main/README.md#cellular-network-standards)
* 

## [Introduction to IP](https://www.youtube.com/watch?v=M5c9HdaQqh0&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=3&ab_channel=ProfessorMesser)

- TCP and UDP for moving data across the network
- Frames have many things inside them including headers and data
- Lots of encapsulation when getting a frame ready to move across the network
- TCP is layer 4
    - Uses the TCP handshake
    - A connection based protocol
    - Good when you need to make sure you get all of the data
- UDP is layer 4
    - Does not verify that data has been received
    - Faster but less reliable (Connection less protocol)
    - Good for real time purposes like voice/video calls, ect
- IP addresses and port numbers is what is used so the routers and other devices know where to direct the frame/data so that the right person may get their information
- Many different applications have their own ports
    - SHH - 22
    - HTTPS 443
    - ect
- All of this routing data like source and destination IP and ports will be stored in the frame
- 0-1023 are permanent port numbers while 1,024-65535 are non permanent port numbers
- TCP ports and UDP ports are different things
- ICMP (Internet Control Message Protocol)
    - Used to check in and see if a device is functioning properly
    - Admin use mainly
    - Also can be used for devices to alert others when they are not working properly
    - Could alert that a packet timed out and did not reach its destination

## [Common Ports](https://www.youtube.com/watch?v=vp_ZxQ0CTJk&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=4&ab_channel=ProfessorMesser)

- Telnet TCP 23
    - Remote login via console
    - Not encrypted so not at all secure
    - Not used often
- SHH TCP 22
    - Encrypted remote login via console
    - Better than Telnet
- DNS UDP 53
    - Converts names of websites to IP addresses
    - Very important, if they aren’t working they whole network will have trouble
- SMTP TCP 25
    - Server to server email transfer
    - Send from a device to a mail server
- SFTP TCP 22
    - Uses SSH to make secure file transfer
    - Full featured file transfer protocol
- FTP TCP 20 (active mode data) TCP 21 (Control)
    - An unencrypted file transfer protocol
    - Username and password needed
    - Full featured
- TFTP TCP 69
    - No authentication or encryption
    - Just read and write files, very basic
- DHCP UDP 67 and UDP 68
    - Automatically configures IP address, default gateway, subnet mask, ect
    - DHCP could be stand alone or more commonly for houses in the router
    - There is a lease time for IP addresses, you only get it for a certain amount of time
    - Reservations can make it so certain devices always get the same IP addresses
- HTTP TCP 80
    - Unencrypted protocol commonly used via a browser
- HTTPS 443
    - Encrypted browser protocol
- SNMP UDP 161
    - Managing network devices, gather logs and statistics from the devices
    - V1 & V2 not encrypted, V3 is encrypted, has integrity, authentication and authorization
- RDP TCP 3389
    - Remotely share a desktop (or just an application)
    - Common for Windows
    - Can use other OS for this as well
- NTP UDP 123
    - Sync all the clocks
    - Very accurate
- SIP TCP 5060-5061
    - Voice over IP
    - Setups up and ends calls
    - Adds features as well
- SMB also called CIFS, TCP 445
    - Used by Windows
    - Files sharing, printer sharing, ect
- POP3 TCP 110
    - Receive emails from a mail server
    - Basic
- IMAP4  TCP 143
    - More common today
    - Receive emails from a mail server
    - More features than POP3
- LDAP TCP 389
    - Directory access protocol
    - Store and retrieve info in a network directory
- LDAPS TCP 636
    - LDAP but over SSL, so secure
- H.323 TCP 1720
    - Another VoIP signaling protocol
    - Call, ring, hangup
    - Early VoIP protocol, but still used quite a lot today

## [Understanding the OSI Model](https://www.youtube.com/watch?v=G7aVKgGUe9c&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=5&ab_channel=ProfessorMesser)

- Open Systems Interconnection Reference Model
- 7 Layers
    - Layer 7 Application (The layer we see, HTTP, FTP, POP3, ect)
    - Layer 6 Presentation (encoding and encryption, often combined with layer 7)
    - Layer 5 Session (Communication management between devices, control protocols and tunneling protocols)
    - Layer 4 Transport (TCP, UDP, ect)
    - Layer 3 Network (Routing layer, routers, IP, Packets, Layer 3 switches, frame fragmentation)
        - Frame fragmentation is when you break a frame into smaller pieces so the data can be sent across the network
    - Layer 2 Data Link (MAC, Frames, Switches, Bridges)
    - Layer 1 Physical (Signaling, cabling, connectors, hubs, bits, ect)
- Certain protocols and processes exists at each layer
- Packet capture tools like Wireshark are where you really start to see OSI model in the real world

## [Introduction to Ethernet](https://www.youtube.com/watch?v=iXfBbs9SSFQ&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=6&ab_channel=ProfessorMesser)

- Enterprise networks have the same base functionality has a home network
    - There is just a ton more data and hardware
    - May even be many building connected to each other
- MAC addresses
    - Physical unique address
    - 48 bits long, displayed in hexadecimal
        - First half is the Organizationally Unique Identifier (the manufacturer)
        - Second half is Network Interface Controller Specific (serial number)
- Half duplex
    - Cannot send and receive at the same time (like hubs or switches if configured as so)
    - Prone to collisions
    - CSMA/CD Can tell when there is a collision and wait a random amount of time before continuing to send data
    - CSMA/CD can see if any data is currently being transmitted or if the case is clear
- Full duplex
    - Can send and receive at the same time
    - Need to make sure the switch and devices support full duplex
    - Much more intelligent in many ways (Knows where the data needs to go instead of just sending it to everyone on the network)
- CSMA/CA
    - Collision Avoidance, like CD but for wireless networks
    - Can’t hear the other devices so they will ask if the network is in the clear before sending data
## [Network Switching Overview](https://www.youtube.com/watch?v=jR3VoKZWJyc&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=7&ab_channel=ProfessorMesser)

- The switch is much smart than the hub
    - Forward or drop frames based on the MAC addresses
    - Has a table MAC addresses
    - Keeping the environment loop free with STP
- Frame switching
    - Has a table of MAC adresses to output interface
    - Only knows the next step, just keeps passing the packet on until it gets to its location or its TTL expires
    - Always adding to its table when it come across something new
        - If it doesn’t know where to send the data it floods the data to all of the devices
            - When the data finds the right person the switch gets a response and adds the information to it’s table
- ARP
    - Determine MAC address based on a IP address
    - Can be captured with a packet capture tool
    - arp -a to view the arp table on your computer
  
## [Broadcast Domains and Collision Domains](https://www.youtube.com/watch?v=SGbtLjIEVeo&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=8&ab_channel=ProfessorMesser)

- Collision domains CSMA/CD
    - Hard to find these days because of full duplex
    - Only one station can talk at a time
    - The collision domains are separated by switches
- Broadcast domains
    - There are some cases where you need to broadcast something (a necessary evil)
    - Broadcasts can go through switches and bridges but they stop at a router

## [Unicasts, Broadcasts, and Multicast](https://www.youtube.com/watch?v=jotgabyT-uI&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=9&ab_channel=ProfessorMesser)

- Unicast = one to one (most common, HTTPS, FTP, IMAP3, ect)
- Multicast = one to many (things like live voice calls with many people, streams, ect)
- Broadcast = one to all (arp requests, routing updates, ect)

## [Protocol Data Units](https://www.youtube.com/watch?v=3RQW9s-aB6k&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=10&ab_channel=ProfessorMesser)

- Unit of transmission (Frame, packet, bits, TCP, UDP, ect)
- Lots of headers are needed so each devices service can see the information they need
    - Frame are encapsulated in headers as they move down the OSI model and de-encapsulated as they move back up the OSI model when they reach their destination
- MTU
    - Maximum size of a IP packet that you can transmit
        - All devices need be able to support the MTU that you have set
        - A high MTU can greatly increase speeds
    - 1500 bytes is the standard MTU for IP packets
        - Some of this packet is the headers not all of it is your payload (only 1472 bytes is the payload)
    - If the DF bit is set it means that the data cannot be fragmented

## [Network Segmentation](https://www.youtube.com/watch?v=9L4qDmvKPjQ&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=11&ab_channel=ProfessorMesser)

- LANs = Local Area Network
- Virtual LANs
    - Separated logically instead of physically
    - Can have many on a single switch (or use many switches)
        - You could run a cable for each VLAN when connecting switches in order to keep the traffic separate or you could use one cable for all of the VLANs with VLAN trunking
            - This is known as a 802.1Q trunk, it adds a header to the frame that notes what VLAN the traffic came from so that it can be routed, once it reaches the end of the trunk the header is removed and the frame is forwarded to the correct VLAN

## [Spanning Tree Protocol](https://www.youtube.com/watch?v=mLCpdsOZM9c&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=12)

- Used to prevent loops in networks
    - Loops will easily overwhelm your network so you need to stop them from happening
- 802.1D standard
- There are a few port states for ports using STP
    - Blocking = not forwarding to prevent a loop
    - Listening = not forwarding and cleaning the MAC table
    - Learning = not forwarding and adding to the MAC table
    - Forwarding = data passes through
    - Disable = admin turned off the port
- Root switch
    - One per network
    - STP will label ports as “root port” if that is the way to get to the root switch
    - The designated ports are the other ports that lead to other spots in the network
    - Blocked ports are well closed port that traffic cannot go through
- STP may make a route to a certain device a little bit longer, but this is worth it
- STP can automatically change the port states if a device fails and you need a new path to get somewhere
- RSTP is 802.1W
    - Faster than STP
    - Backwards compatible

## [Switch Interface Properties](https://www.youtube.com/watch?v=dqQny4UXiX0&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=13)

- Speed and duplex settings
    - The most basic settings you need to config or have config automatically
- IP addresses may also be needed
- Switches need to be assigned a VLAN as well
    - Trunk interfaces need to be config-ed too
- DMZ Demilitarized zone
    - Between the internet and your intranet
    - Security
- POE (802.3af)
    - Ethernet and power in one cable
    - Endspans is what you call a switch with built in POE
    - Midpsans is what you call it when you use a power injector with your switch for POE
    - Mode A = POE on the wires that are used for data
    - Mode B = POE on unused wires
    - 15.4 watts DC power
    - Max current of 350 mA
- POE+ (802.3at)
    - Improved POE
    - 25.5 watts DC power
    - Max current of 600 mA
- Port mirroring
    - Connect a monitoring device so you can copy what is happening on the device (switch) and send a copy to your device
## [Static and Dynamic Routing](https://www.youtube.com/watch?v=YRzr56cwgCg&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=14&ab_channel=ProfessorMesser)

- Each router only knows the next step
    - Routing table tells them where to send packets
- Static routing
    - Manually add the routes
    - Good for small networks / bad for large networks
    - More secure
    - No overhead for routing protocols
    - Easy to mess up and make a loop
    - Have to manually update routes when there is a change
- Dynamic routing
    - Routing tables are updated automatically in almost real time
    - Good for large and complicated networks
    - Has some router overhead
    - Still has some initial configuration that is needed
- Default route
    - The way of last resort
    - Great when there is only one way in and out of the network
    - Can make things a lot simpler depending on your network

## [IGP and EGP](https://www.youtube.com/watch?v=14s-M01m1fQ&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=15&ab_channel=ProfessorMesser)

- AS
    - Autonomous System
    - A network of nearly any size with a single routing policy
    - Within your control
- IGP
    - Used within a single AS
    - IPv4 dynamic routing
        - OSPFv2 (Open shortest path first)
        - RIPv2 (Routing information protocol version 2)
        - EIGRP (Enhanced interior gateway routing protocol)
    - IPv6 dynamic routing
        - OSPFv3
        - EIGRP for IPv6
        - RIPng (RIP next gen)
- EGP
    - Used for routing between AS
    - BGP (Boarder gateway protocol
        - Very common

## [Dynamic Routing Protocols](https://www.youtube.com/watch?v=9390huk39mU&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=16&ab_channel=ProfessorMesser)

- Automatically communicate between routers so they are always updating their routing tables
- Needs a formula to determine the best routes
- Distance vectoring routing protocols
    - How many “hops” (number of routers) away is another network
    - Does not care about the speed of the link only the distance
    - Very little config as it is quite simple
    - Not great for large networks
    - Many different protocols use this
        - RIP
        - RIPv2
        - EIGRP
- Link-state routing protocols
    - Care more for the speed of the link than the distance
    - A ton better for large networks
        - OSPF (very common for large networks)
- Hybrid routing protocols
    - Combining Link state and distance vectoring
    - BGP

## [IPv4 and IPv6 Addressing](https://www.youtube.com/watch?v=U2IxdEYgoEg&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=17&ab_channel=ProfessorMesser)

- Every device needs an IP address
- Subnet mask is also needed
    - Subnet masks tells you which part of the IP address is the network ID and which part is the host ID
- IPv4 address
    - 32 bits / 4 bytes / 4 octets long
    - Lowest number is 0 highest is 255
- IPv6 address
    - 128 bit / 16 bytes / 16 octets long
    - Displayed in hexadecimal
    - Hard to memorize this type of addresses so DNS is even more important
    - IPv6 can be shortened
        - Leading 0’s are optional
        - Groups of 0’s can be replaced with :: (but only once per address)
        - So 2001:0000:0000:CD30:0000:0000:0000:0000
            - is now 2001:0:0:CD30::
## [Configuring IPv6](https://www.youtube.com/watch?v=NhRjwjt2Aog&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=18)

- Duel-stack routing
    - v4 and v6 in one network (Have both types of addresses for a single device)
    - Most modern networks can understand both versions of IP
- Tunneling IPv6
    - 6to4 addressing
        - Can send IPv6 between devices that have a IPv4 connection
        - No NAT support
        - Needs relay routers
    - 4in6 tunneling
        - V4 tunneled in a v6 network
    - Teredo/Miredo tunnel
        - IPv6 through IPv4
        - No special hardware needed
        - Teredo is Microsoft | Miredo is Linux, Mac OS, ect (Open Source)
- NDP (Neighbor Discover Protocol)
    - Sends multicast with ICMPv6
    - Replaced IPv4 ARP
    - Finds other devices MAC addresses
    - SLAAC - automatically config IP address without DHCP servers
    - DAD - No duplicate IPs
    - Discover routers with RS and RA
- NS and NA
    - NS = Neighbor Solicitation
        - Sent as a multicast
        - One workstation searching for the MAC of another workstation
    - NA = Neighbor advertisement
        - The response to a NS with the needed info

## [Prioritizing Traffic](https://www.youtube.com/watch?v=uEKDZqI5osA&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=19)

- Many different apps and devices with many different requirements
- Some types of traffic are more important than others
- Packet Shaping
    - Control bandwidth and data rates
    - Some apps have higher priority
- QoS
    - The process of controlling traffic flows
    - Many different methods
    - CoS
        - Layer 2
        - In a 802.1Q trunk
    - DiffServ
        - Layer 3
        - QoS is set in the IPv4 header

## [Network Address Translation](https://www.youtube.com/watch?v=JAYpfBvGVI8&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=20)

- All of the IPv4 addresses are used up
- Private IP addresses
    - For inside a Intranet only
    - Not rout-able across the internet
    - These are the private addresses range
        - 10.0.0.0-10.255.255.255
        - 172.16.0.0-172.31.255.255
        - 192.169.0.0-192.168.255.255
- NAT changes these private addresses into public addresses (The routers own address with is rout-able across the internet)
    - Each router directly connected to the internet has its own IPv4 address
    - Port numbers are used so the router can tell where on the intranet to send internet traffic (Since it can’t use IP addresses due to the changes being made to them)
- Port forwarding
    - Someone on the outside gets access to the inside of your network
    - Maps External IP and port number to an internal IP and port number
    - Also known as Static NAT or Destination NAT
    - Does not timeout or expire

## [Access Control Lists](https://www.youtube.com/watch?v=6Yj1-pZmHvY&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=21)

- Allow or deny traffic
- Commonly sits on the outer limits of the network where traffic is going in and out
- Can evaluate on many different types of criteria
    - Source IP, Destination IP, Port numbers, ICMP, time of day, application, ect
- Works from top to bottom
    - Looks at first rule to see if there is a match there if not it keeps moving down the list of rules
    - Most specific rules tend to be at the top
    - At the bottom tends to be a implicit deny rule
        - If it matches no other rules than it is denied and can’t come through

## [Circuit Switching and Packet Switching](https://www.youtube.com/watch?v=uBpacYBwYwM&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=22)

- Circuit switching
    - Circuit is established before data passes through
    - Nobody else can use it when it is idle
    - Not an efficient use of resources
    - Connection is always there and it is all yours
    - Examples
        - POTS (Plain Old Telephone Service)
        - T1, T3, E1, and E3
        - ISDN
- Packet Switching
    - Grouping data into packets and sending it across a network
    - The media is shared
        - If you aren’t using it, someone else is
    - More efficient
    - Examples
        - SONET
        - ATM
        - DSL
        - Frame Relay
        - MPLS
        - Cable Modem
        - Satellite
        - Wireless

## [Software-Defined Networking](https://www.youtube.com/watch?v=EdVOeGDYHCU&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=23)

- Control Plane
    - Administration and ongoing servicing
- Data plane
    - Transferring data
- Directly programmable
- Make changes at any time (Dynamically if needed)
- Centrally managed
- Vendor neutral
- Virtualize things with distributed switching
    - Servers can be far away from each other while on the same VLAN
    - Dont need to worry about moving the servers
## [Binary Math](https://www.youtube.com/watch?v=mIbNZzoWE3k&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=24&ab_channel=ProfessorMesser)

- This is kinda hard to write out without any charts or something but here we go
- All 0’s and 1’s
- Each digit is a bit
    - 8 bits is a byte/octet
- Each bit represents a number
    - 0 means that digit is not included in the number while 1 means that digit is included in the number
    - 0     0     0     0     0     0     0     0
    - 128   64   32   16    8     4     2     1
- Every time there is a 0 bring down a 0 every time there is a 1 bring down the number associated with the bit then add them all together
- So for 10010100
    - We have 3 1’s in this binary and they are associated with the numbers 128, 16, and 4
    - So if we simple add all 3 of those numbers together we get 148
- This can be done is reverse so say we have 186 and needed to make it in binary
    - First we ask is there is a 128? if so the first number is a 1 (we also now subtract 128 from 186 to get 58)
    - Now we ask if there is 64 in the remaining number of 58 - there is not so that is a 0
    - Next is 32 which there is so that is 1 and now we have 26 left
    - Next is 16 which there is so that is also a 1 and we have 10 left
    - Next is 8 which there again is so that is 1 and we have 2 left
    - There is no 4 so that is a 0
    - There is a 2 so that is a 1 and now we have 0 Left
    - So this is now 0
    - In the end we have 10111010 = 186

## [IPv4 Addresses](https://www.youtube.com/watch?v=aEMtAFvouNU&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=25&ab_channel=ProfessorMesser)

- Every device needs one | like 182.23.46.2
- Also need a subnet mask like 255.255.0.0 or 255.240.0.0
- Default gateway is needed to talk outside of the local subnet
- Loopback address is a way to send traffic to yourself
    - 127.0.0.1-127.255.255.254
- Reserved addresses are set aside for future use
    - 240.0.0.1-255.255.255.254
- Virtual IP addresses
    - Not for a physical device

## [Classful Subnetting](https://www.youtube.com/watch?v=GxE395bCANM&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=26&ab_channel=ProfessorMesser)

- Class A
    - Leading bits of 1-126
    - 8 network bits and 24 remaining bits
    - like 255.0.0.0
- Class B
    - Leading bits of 128-191
    - 16 network bits and 16 remaining bits
    - 255.255.0.0
- Class C
    - Leading bits of 192-223
    - 24 network bits and 8 remaining bits
- Class D (Multicast)
    - Leading bits of 224-239
    - Nothing else is defined for class D
- Class E (reserved)
    - Leading bits of 240-254
    - Nothing else is defined for class E
- For each subnet there are host addresses, network address and broadcast address
    - The first address in a subnet is the host address
    - The last address in a subnet is the broadcast address
    - All of the other addresses are host addresses
- For actually calculating all of these addresses scroll down to the 7 second subnetting section (I will add it soon)

## [IPv4 Subnet Masks](https://www.youtube.com/watch?v=L3dsWxn5RBU&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=27&ab_channel=ProfessorMesser)

- Subnet masks could be written in binary with ones all lined up on the left and zeros all on the right
    - Something like 11111111.11111111.0.0 or 255.255.0.0 or /16
    - Or 11111111.11100000.00000000.00000000 or 255.224.0.0 or /11
        - These / followed by a number are the CDIR notation, it is a way to display what the subnet mask is
- just simply used Professor Messer’s chart for converting between CDIR notions, binary and decimal for the subnet masks and I am too lazy to make my own chart ATM so nothing goes here

## [IPv6 Subnet Masks](https://www.youtube.com/watch?v=8IqXQ88QXfc&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=28&ab_channel=ProfessorMesser)

- IANA (Internet Assigned Numbers Authority provides addresses to RIRs (Regional Internet Registries
    - RIRs assign smaller blocks to ISps (Internet Service Providers)
    - Then that provider will give you a /48 subnet
- First 48 bits is the Global Routing Prefix
    - The next 16 bits tend to be the different subnets
        - Those 16 bits give you 65,536 total subnets
    - The last 64 bits tend to be Host ID’s on that subnet
        - Those 64 bits give you about 18 million trillion hosts per subnet (So much more than the total IPv4 address range)
- So all in all this is quite similar to how subnet masks for IPv4 work there is just so many more subnets and host addresses to work with

## [Calculating IPv4 Subnets and Hosts](https://www.youtube.com/watch?v=qQEaAb_p8_E&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=29&ab_channel=ProfessorMesser)

- VLSM (Variable Length Subnet Masks)
    - Allows network admins to define their own subnets (not classful)
    - So many more options and flexibility comes from this
- 2 to the power of the number of subnet bits you have would allows you to calculate the total numbers of subnets you have
- 2 to the power of the number of host bits that you have would allow you to calculate the total numbers of hosts you have per subnet (make sure to subtract 2 from that number for the network address and broadcast address)
- Look at the first number of the IPv4 address to see what range it is in (Class A, B, ect) and that will tell you have many bits are the network ID in this case lets say is Class A, so 8 network bits, then you look at your CIDR notation and see it is for example /24 meaning there are still 16 bits left that are not host ID’s but indeed subnet ID’s. The remaining 8 bits are then your hosts ID’s, this is how you get your numbers for the for the equations above
## [Seven Second Subnetting](https://www.youtube.com/watch?v=ZxAwQB8TZsM&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=30&ab_channel=ProfessorMesser)

## [Assigning IPv4 Addresses](https://www.youtube.com/watch?v=Q0Aq_cYBcR0&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=31&ab_channel=ProfessorMesser)

- This used to be completely manual
- BOOTP
    - Automatically define some things but not everything
    - Didn’t know when leases were up
- DHCP
    - Automatically configured most settings and works with nearly every device
    - Your IP will expire and you will get a new one every now and then
        - But you can set it so you always have the same IP if you desire
            - A DHCP reservation where you tie a MAC address to a IP address
- APIPA
    - When you use DHCP but no address is available you can use a link local address to communicate within your subnet
    - 169.254.0.1-169.254.255.254
        - First and last 256 addresses are reserved
    - Your device will pick a link-local address then send an ARP request to make sure that said address is no in use by anyone else, then it assigns it to it’s self if it is available

## [Assigning IPv6 Addresses](https://www.youtube.com/watch?v=lfCFsniHsPk&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=32&ab_channel=ProfessorMesser)
- DHCPv6
    - Every device already has a link-local address without the need for DHCP
        - So your DHCP request can be sent with multicast instead of broadcast
    - Process of getting an address is a lot like IPv4
        - Solicit | Advertise | Request | Reply
- A static IP address with a modified EUI-64 (64 bits)
    - A modified MAC address (48 bits)
    - To make this address first split the MAC address in half
        - Now place FFFE in the middle of the MAC address (the missing 16 bits)
        - Now invert the 7th bit (The U/L bit aka the Universal/local bit)
            - This is the second character in the address and it switches like so (They work both ways to while 1 will become a 3, if you simply started with a 3 that will then be a 1)
            - 0 to 2 | 1 to 3 | 4 to 6 | 5 to 7 | 8 to A | 9 to B | C to E | D to F
    - Examples
        - MAC of 8c:2d:aa:4b:98:a7 to EUI-64 of 8e2d:aaff:fe4b:98a7
        - MAC of a0:21:b7:63:40:3f to EUI-64 of a221:b7ff:fe63:403f
## [Network Topologies](https://www.youtube.com/watch?v=4nPnQVaRj4k&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=33&ab_channel=ProfessorMesser)

- Physical network map
    - All of the physical devices and cable connections
    - Physical maps of the racks and the components inside them
- Logical network map
    - For virtual devices or high level overview of the network
    - Visio, OmniGraffle, [Gliffy.com](http://Gliffy.com)
    - Good for planning and sharing with 3rd parties
- Star network
    - A switch in the middle with everything connected to that switch
- Ring network
    - All of the devices are connected to each other in a ring form
    - Used in MANs and WANs
    - Sometimes you have 2 rings for fault tolerance
- Mesh network
    - Many redundant links, sometimes all of the devices are connected to all of the other devices
    - Redundant, fault tolerant, load balancing
    - Used in WANs
- Bus network
    - Single cable with every device connected to that cable
    - Easy to implement, very horrible for fault tolerance
    - CAN (in your car) is a modern bus network
- Wireless Topologies
    - Infrastructure
        - All devices communicate through an AP
        - Most common
    - Ad hoc networking
        - No preexisting hardware
        - Just configure both devices to communicate directly with each other
    - Mesh
        - Ad hoc devices working together to create a mesh “cloud”
        - Self form and self heal

## [Common Network Types](https://www.youtube.com/watch?v=BrGirZH0FzQ&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=34&ab_channel=ProfessorMesser)

- LAN = local area network
    - A single building, group of buildings, ect
    - High speed and small
- WLAN = Wireless local area network
    - Same thing as LAN but wireless
    - Can be extended with more AP’s
- MAN = metropolitan area network
    - Between the side of a LAN and a WAN
    - Size of like a city or something
    - Often owned by governments
- WAN = Wide area network
    - Spanning around the globe
    - Tends to be slower in speeds
- CAN = Campus Area network
    - Many buildings owned by a company or a college | group of building close to each other
    - LAN technologies so very high speed (many times fiber)
- SAN = Software area network
    - Looks and feels like a local storage device
    - Block level access (More efficient)
- NAS = Network attached storage
    - Remote storage device
    - File level access
- PAN = personal area network
    - Bluetooth, IR, NFC
    - Common inside a house or car (Audio, Mobile phone, workout/health devices, ect)

## [Internet of Things Topologies](https://www.youtube.com/watch?v=g9F5FauEWL4&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=35&ab_channel=ProfessorMesser)

- Wearable tech, home automation, ect
- Z-Wave
    - Mainly for home automation
    - Control lights, locks, garage doors
    - Wireless mesh network
- ANT / ANT+
    - Fitness devices, heart monitors, ect
    - Uses 2.4GHZ so it could be jammed
    - Optional encryption
- Bluetooth
    - Uses PAN
    - Wireless headphones, smart phones, smart watches, tethering, ect
- NFC (near field communication)
    - Common on phones
    - 2 way communication (commonly for payments)
    - Can help with Bluetooth pairing
    - Could also use it as an access token
- IR (Infrared)
    - Included on phones and much more
    - Control entertainment center with your phone (most common use case)
- RFID (Radio-frequency Identification)
    - Tracking, access badges, ect
    - Not usually powered devices
- IEEE 802.11 wireless networks
    - Most common IoT networks
    - Always being updating

## [Wireless Standards](https://www.youtube.com/watch?v=r3pZ0WYSk9g&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=36&ab_channel=ProfessorMesser)

- 802.11a (one of the first standards)
    - 5GHZ range
    - 54Mbit/s
- 802.11b (also one of the first standards)
    - 2.4 GHZ range
    - 11Mbit/s
    - Better range than 802.11a
    - More conflict with other devices
- 802.11g
    - “upgrade of 802.11b”
    - 2.4GHZ range
    - 54Mbit/s
    - Backwards compatible with 802.11b
- 802.11n
    - 5 or 2.4GHZ range
    - Much more bandwidth
    - 600Mbit/s
    - Uses MIMO (Multiple input multiple output)
- 802.11ac
    - 5GHZ range
    - Can use channel bonding for large channel bandwidths
    - 6.8 Gbit/s
    - Uses 8MU-MIMO

## [Cellular Network Standards](https://www.youtube.com/watch?v=GShWfJH6p2c&list=PLG49S3nxzAnmpdmX7RoTOyuNJQAb-r-gd&index=37&ab_channel=ProfessorMesser)

- Separate land into cells
    - One antenna per cell
- 2G networks
    - GSM (Global System for Mobile Communications)
    - CDMA (Code division multiple access)
    - Poor data support
- GSM
    - 90% of the market for a while (AT&T, Tmobile)
    - Could move SIM from phone to phone
    - Uses TDMA (Everyone gets a little slice of time)
        - Streams are combined into a single stream then broken out again when they reach the location
- CDMA
    - Everyone is using the same frequency, but they have their own code
    - Verizon and Sprint used this
- 4G LTE
    - Converged standard
    - Based on GSM and EDGE
    - Downloads of 300Mbit/s for LTE-A (150Mbit/s for normal LTE)
