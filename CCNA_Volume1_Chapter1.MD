# Chapter 1: Internetworking

## Internetworking Basics

- Things that commonly cause LAN traffic congestion: 

  - Too many hosts in a collision or broadcast domain  

  - Broadcast storms  

  - Too much multi-cast traffic 

  - Low bandwidth  

  - Adding hubs for connectivity to the network 

   - A bunch of ARP broadcasts 

 
- Network Segmentation: The process of breaking up a massive network into a number of smaller ones 

- Infrastructure is managed by devices like routers, switches, hubs, etc 

- Switch's can break up collision domains. 

- Hubs don't segment a network, they just connect network segments. It's an inexpensive way to connect a coupe of PC's.  

- By default, routers are basically employed to efficiently break up a broadcast domain. 

- Routers, provide connections to Wide Area Networks (WAN) services as well as via a serial interface for WAN connections, specifically, a V.35 physical interface on a CISCO router.  

- Breaking up a broadcast domain is super important. When a host or server sends a network broadcast, every device on the network will read it and process that broadcast--unless you have a router.  

- When the router's interface receives this broadcast, it can say "no thanks" and discard the broadcast without forwarding it to other networks.  
 
- Even though routers are known for breaking up broadcast domains by default, its important to remember that they break up collision domains as well.  
 
- There are 2 advantages for using routers in your network: 

    - They don't forward broadcasts by default 

    - They can filter the network based on layer 3 (network layer) information such as IP address. 

- Here are four ways a router functions in your network: 
    - Packet switching 

    - Packet filtering 

    - Internetwork communication 

    - Path selection  

- Switches create separate collision domains within a single broadcast domain.  
 
- Routers provide a separate broadcast domain for each interface.  

- Each port on a switch is a separate collision domain.  

- Each VLAN is a separate broadcast domain.  

- Routers use logical addressing and provide an important capacity called packet switching.  
 
- Routers can also provide packet filtering via access lists.  

- When routers connect two or more networks together and use logical addressing (IPv4/IPv6), you then have an "internetwork" 

- We don't use switches to create internetworks because they don't break up broadcast domains by default. Instead, they are employed to add functionality to a network LAN,  

- The main purpose of these switches is to make a LAN work better--to optimize performance--providing more bandwidth to the LAN's users.  

- Switches also don't forward packets to other networks like routers do. Instead, they only "switch" frames from one port to another within the switched network.  

- IMPORTANT: Switches and Hubs are used to segment networks, but they will not isolate broadcast or multi-cast packets. 

- It's pretty common to hear people referring to switches as bridges. This is because bridges and switches both basically do the same thing--break up collision domains of a LAN.  
 
- You can not buy a physical bridge these days, only LAN switches that use bridging technologies.  
 
- Cisco and others will commonly refer to LAN switches as multi-port bridges now and then.  

- It's important to remember that even in a switched network environment, you still need a router to provide communication between VLANS.  
 
- VLAN (Virtual Local Area Network) is when you logically break up broadcast domains in a switched network.  

- The best network design is the one that's perfectly configured to meet business requirements of the specific company or client it serves.  

- WLAN Devices: Devices that connect wireless devices such as computers, printers, tablets to the network.  

- Since pretty much every device today has a Wireless NIC, you just need to configure a basic access point (AP) to connect to a traditional wired network.  
 
- Access Point (AP) :  Devices that allow wireless devices to connect to a wired network and extend a collision domain from a switch. They're typically in their own broadcast domain or what we'll refer to as a VLAN. 

- An AP can be simple stand-alone device, but today they are usually managed by wireless controllers, either in house or through the internet. 

- WLAN Controllers: These are devices that network administrators or network operation centers use to manage access points in medium to large to extremely large quantities. It automatically handles the configuration of wireless AP's and was typically used only in larger enterprise systems. 

- Since Cisco acquired Meraki, you can easily manage a small-medium sized wireless network via the cloud using their simple to configure web controller system.  

- Firewalls: These devices are network security systems that monitor and control incoming and outgoing network traffic based on security rules--usually an IPS(Intrusion Protection System) 

- Cisco Adaptive Security Appliance (ASA) firewall typically established a barrier between a trust, secure internal network and the Internet (which is not secure or trusted).  

- Cisco's acquisition of Sourcefire put them in the top of the market with Next Generation Firewalls (NGFW) and Next Generation IPS (NGIPS), which Cisco calls "Firepower". 

- "Firepower" runs on dedicated appliances: Cisco's ASA's, ISR routers and even on Meraki products.  

<hr/>

## OSI Model 

- When networks first came into being, computers could only typically communicate with computers from the same manufacturer. Companies either ran DECnet solution or an IBM solution, never both together. 

- In the late 1970's, the OSI (Open Systems Interconnections) Reference Model was created by the International Organization for Standardization to break through this barrier.  

- The OSI Model was meant to help vendors create interoperable network devices and software in the form of protocols. This was so different vendor networks work with each other.  

- The OSI Model describes how data and network information are communicated. 

- The OSI Model has 7 layers and is a "reference" model. It is a blueprint of how communications SHOULD take place.  

- The OSI Model is hierarchical and there are many advantages that can be applied to any layered model.  


 
Here are some important benefits of using the OSI Layered Model: 

1) It divides the network communication process into smaller and simpler components.  

2) It allows multiple-vendor development through the standardization of network components.  

3) It encourages industry standardization by clearly defining what functions occur at each layer of the model.  

4) It allows various types of network hardware and software to communicate.  

5) It prevents changes in one layer from impacting other layers.  

6) The OSI Model is broke up into two groups: <b>Upper Layers</b> and <b>Lower Layers</b> 

## Upper Layers 

Layer 7 (Application) :  

- Provides a user interface 

Layer 6 (Presentation): 

- Presents data in the proper format 

- Handles processing such as encryption, compression, translation services 

Layer 5 (Session): 

- Keeps different application' data separate 

- Dialog control 

Lower Layers 

Layer 4 (Transport)  

- Provides reliable/unreliable delivery 

- Performs error correction before retransmit 

- End to end connection 

Layer 3 (Network) 

- Provides logical addressing, which routers use for path determination 

Layer 2 (Data Link) 

- Combines packets into bytes, then bytes into frames 

- Provides access to media using MAC Addresses 

- Performs error detection not correction 

Layer 1 (Physical) 

- Move bits between devices 

- Specifies voltages, wire speed, and pinout of cables 



The following network devices operate at all 7 layers: 

- Network Management Stations (NMS) 

- Web and Applications Servers 

- Gateways (not default gateways) 

- Servers 

- Network Hosts 

<hr/>

## The Application Layer 

- The Application Layer is where users actually communicate to the computer 

- The Application Layer works as the interface between actual application programs. This means end-user programs like Microsoft Word don't reside at the Application Layer, they interface with this layer's protocols.  

- Examples: Web Browsing, File Transfers, Email, Enable Remote Access, Client/Server Processes, Information Location, Network Management Activities  

- Identifying and confirming the communication partner's availability and verifying the required resources to permit the specified type of communication to take place also occurs at this layer. 

 

## The Presentation Layer 

- This layer presents data to the application layer and is responsible for data translation and code formatting.  
     
- Think of this as the OSI Model's translator, providing coding and conversion services.  
     
- One very effective  way of ensuring a successful data transfer is to convert the data into a standard format before transmission.  
     
- Data compressions, decompression, encryption, decryption are also associated at this layer.  

 
## The Session Layer 

- This layer is responsible for setting up, managing and dismantling sessions between Presentation Layer entities and keeping user data separate.  
     
- Dialog control between devices also occur at this layer. 

- Communication between hosts' various applications at this layer is coordinated/organized via three modes: Simples, Half-Duplex, and Full-Duplex 
     
- Simplex: One way communication--sending a message and not getting a reply 
     
- Half-Duplex: Two way communication, but it can take place in only one direction at a time.  
     
- Full Duplex: Two way communication where devices and transmit and receive at the same time.  

## The Transport Layer  

- This layer segments and reassembles data into a single data stream 

- Services at this layer take all the various data received from the upper layer applications, then combine it into the same, concise data stream. 

- TCP and UDP are at this layer 

- TCP is reliable and UDP is not. 

- TCP is connection-oriented. It must establish a connection first, by using a "three-way handshake" 

- TCP sets up "virtual circuits" between endpoints. Once a session is established, you can drop data into one side and know that it will emerge on the other side intact. 

- Once this process is complete, a call termination takes place to tear down the virtual circuit. 

Three-Way Handshake  

- The first connection agreement segment is a request for synchronizations (SYN) 

- The next segments acknowledge (SYN/ACK) the request and establish connection parameters--rules between hosts. These segments request that the receiver's sequencing is synchronized here as well so that a bidirectional connection can be formed. 

- The final segment is also an acknowledgment, which notifies the destination host that the connection agreement has been accepted and the actual connection is established. Data transfer can now begin.  

- When a machine receives a flood of datagrams too quickly for it to process, it stores them in a memory section called a buffer.  

- This solution is only good for a small burst of datagrams. If this continues, eventually exhausting the device's memory, its flood capacity will be exceeded and it will dump any and all additional datagrams it receives.  

- Flow control is a way to ensure data integrity at the Transport Layer by allowing applications to request reliable data transport between systems.  

- Flow control prevents a sending host on one side of the connection from overflowing the buffers in the receiving host.  

- Reliable data transport employs a connection-oriented communication session between systems and the protocols involved ensure that the following will be achieved: 

    - The segments delivered are acknowledged back to the sender upon the reception. 

    - Any segments not acknowledged are retransmitted. 

    - Segments are sequenced back into their proper order upon arrival at their destination.  

    - Data flow is maintained in order to avoid congestion, overloading, or worse, data loss.  

- Because of the transport function, network flood control systems really work well. Instead of dumping data and losing it, the Transport Layer can issue a "not ready" indicator to the sender, signaling the sender to stop transmitting network traffic until it is ready.  

- A Service is considered "connection-oriented" if it has the following characteristics: 

    - A "virtual circuit" or "three-way handshake" is set up 

    - It uses sequencing 

    - It uses acknowledgements 

    - It uses flow control 

- There are three types of flow control: Buffering, Windowing and Congestion Avoidance 

- Window: The quantity of data segments, measured in bytes, that the transmitting machine is allowed to send without receiving an acknowledgment.  

- Windows are used to control the amount of outstanding, unacknowledged data segments.  

- The size of the windows controls how much information is transferred from one end to the other before an acknowledgement is required.  

- While some protocols quantify information depending on the packets, TCP/IP measure it by counting the number of bytes.  

- Reliable data delivery ensures the integrity of a stream of data sent from one machine to another through a fully functional data link.  
 
- This is achieved through "Positive Acknowledgment With Retransmission"--a technique that requires a receiving machine to communicate with the transmitting source by sending an acknowledgement message back to the sender when it receives data.  

- The Transport Layer, working in tandem with the Session Layer also separates data from different applications--an activity known as session multiplexing. 

- Session multiplexing occurs when a client connects to a server with multiple browser sessions open. The client data from each browser session must be separate when the server application receives it.  

## The Network Layer 

- This layer manages device addressing, tracks the location of devices on the network, and determines the best way to move data.  

- This means it up to the Network Layer to transport traffic between devices that aren't locally attached.  
     
- Routers, which are layer 3 devices, are specified at this layer and provide the routing services within an internetwork.  

Here's how that works: 

- First, when a packet is received on a router interface, the destination IP Address is checked.  

- If the packet isn't destined for that particular router, it will look up the destination network address in the routing table.  

- Once the router chooses an exit interface, the packet will be sent to that interface to be framed and sent out on the local network.  

- If the router can't find an entry for the packet's destination network in the routing table, the router drops the packet.  
     
     
There are 2 types of packets used at the Network Layer: 

- Data Packets 
    - These are used to transport user data through the internetwork.  
    - Protocols used to support data traffic are called "routed protocols". 
    - IPv4/IPv6 are key examples.  

Route Update Packets:  
    - These packets are used to update neighboring routers about the network connected to all routers within the internetwork. 
    - Protocols that send our route update protocols are called "routing protocols".  
    - Most critical ones for CCNA are Static Routing and OSPF Single Area 
    - Routing Update Packets are used to help build and maintain routing tables.  


- Routing Information Protocol (RIP) uses hop counts, which refers to the number of routers a packet passes through en-route to a network.  

- Others use bandwidth, delay of the line, or even tick count (1/18 of  second) to determine the best path for data to get to a given destination.  

- Routers are a layer 3 or Network Layer Device. Here are some router characteristics that you should never forget: 

    -  Routers, by default, will not forward any broadcast or multicast packets. 

    - Routers can provide QoS (Quality of Service) for specific types of network traffic.  

    - Routers can provide Layer 2 bridging functions if needed and can simultaneously route through the same interface.  

    - Routers can use access lists, created by the administrator, to control security based on the types of packets allowed to enter or exit an interface.  

    - Routers use the logical address (IP Address) in a Network Layer header to determine the next-hop router to forward the packet to.  

## The Data Link Layer 

- The Data Link Layer provides for the physical transmission of data and handles error notification, network topology, and flow control.  

- This means that this layer will ensure that messages are delivered to the proper device on a LAN using hardware addresses (MAC Addresses) and will translate messages from the Network Layer into bits for the Physical Layer to transmit.  

- This layer formats the messages, each called a "data frame", and adds a customized header containing the hardware destination and source address (MAC Addresses) 

- The IEEE Ethernet Data Link Layer has 2 sublayers: Media Access Control & Logical Link Control 

 
- Media Access Control (MAC) :  

    - Physical addressing is defined here (MAC Addresses)  

    - The method of data transmission is defined here (CSMA/CD)

    - The logical topology being used is defined here as well     

- Logical Link Control (LLC) :  

    - Synchronizes transmission

    - Provides error control and flow control

    - Uses CRC in FCS to check for frame errors


- Switches and Bridges work at the Data Link Layer 

- Layer 2 Switching is considered hardware-based bridging because it uses specialized hardware called "Application-Specific Integrated Circuit" (ASIC).  

- ASIC's can run up to high gigabit speeds with low latency rates.  

- Latency: The time measured from when a frame enters a port to when it exits a port 

- Bridges and Switches read each frame as it passes through the network. Then, it puts the source MAC Address in a filter table and keeps track of which port the frame was received on.  
 
- This information--logged in the bridges or switches filter table--is what helps the machine determine the location of the specific sending device.  

- A transparent bridge is a common type of bridge that observes incoming network traffic to identify media access control (MAC) addresses. 

- Every switch port is its own collision domain.  

- A broadcast storm is an abnormally high number of broadcast packets within a short period of time. 

- When a switch interface receives a frame witha destination MAC address that isnt found in the table, it will forward the frame to all ports except where it came from. Then, when the unknown device accepts the frame, the table will be updated for future reference. 

## The Physical Layer 

- This layer sends and receives bits.  

- Bits come in values of only 0's and 1's.  

- The Physical Layer communicates directly with the varous types of actual communication media.  

- Different kinds of media represent these bit values in different ways.  

    - Some use audio tones. 

    - Others employ "state transmissions" -- changes in voltages from high to low and low to high 

- This layer specifies the electrical, mechanical, procedural, and functional requirements for activating, maintaining, and deactivating a physical link between end systems.  

- This layer is also where you identify the interface between the Data Terminal Equipment and the Data Communication Equipment. 

- DCE is usually located at the service provider, while the DTE is the attached device.  

- Hubs are used at this layer.  

- A Hub is a multi-port repeater.  

- A Repeater receives a digital signal, reamplifies or regenerates that signal, then forwards the signal out the other without looking at any data.  

- All devices plugged into a hub are in the same collision domain as well as the same broadcast domain.  

- Hubs don’t examine any traffic as it enters or before its transmitted out to the other ports.  
 
- A Hub creates a physical star network topology 

## Topologies at the Physical Layer: 

- The physical topology of a network refers to the physical layout of devices, but mostly the cabling and cabling layout 
     
- The logical topology defines the logical path on which the signal will travel on the physical topology.  

Topology Types: 

- Bus: In a bus topology, every workstation is connected to a single cable, meaning every host is directly connected to every other workstation in the network  
     
- Ring: In a ring topology, computers and other network devices are cabled together in a way that the last device is connected to the first for form a circle or ring.  
     

- Star: The most common physical topology is a star topology, which is your Ethernet Switching Physical Layout. A central cabling device (Switch) connects the computers and other network devices together. Physical connection is commonly made using twisted-pair wiring.  
     

- Mesh: In a mesh topology, every network device is cabled together with connection to each other. Redundant links increase reliability and self-healing. The physical connection is commonly made using fiber or twisted pair wiring.  
     

- Hybrid: Ethernet uses a physical star layout and the signal travels end-to-end, like a bus route.  

 