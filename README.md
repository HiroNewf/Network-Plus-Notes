# Network+ Notes
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