# Network+ Notes
The table of contents will take you right to the section you click on and the links for the headers of each section will take you to the Professor Messer video for that section.

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
