
# OSI Model and TCP/IP

## Purpose
Networking models are useful because they breakdown the complex and mostly intangible process behind data communication into a standardized sturcture. This is useful for communication between different positions and levels of expertise in the IT and the wider tech field. Assists in the structured troubleshooting, security and isolation of the issue or vulnerability to a specific layer. Adds modularity allowing for simpler updates and interchange for hardware and software. It also makes training and documentation easier to visualize and describe. 
## The Seven OSI Layers
| Layer | Name     | Main Responsibility                     |         Examples |
|---|---           |---                                      |               ---|
| 7 | Application  |Request Content in Required Format       |Gmail or Outlook  |
| 6 | Presentation |Encryption, Compression, and Translation |SSL encryption    |
| 5 | Session      |Session of Comunication                  |Links presentation|
|---|---           |---                                      |to Transport      |
| 4 | Transport    |Segmentation, Transport, and Reassembly  |TCP/UDP           |
| 3 | Network      |Packet Creation, Routing, Packet Assembly|IP encapsulation, |
|---|---           |---                                      |or Subnetting     |
| 2 | Data Link    |Frame Creation, Local Network Delivery,  |Ethernet and MAC  |
|---|---           |and Transport Frames between Net         |addresses         |
| 1 | Physical     |Data transfer over physical medium       |electrical or     | 
|---|---           |---                                      |optical signals   |

## TCP/IP Model
The TCP/IP model is a four-layer architecture consisting of Application, Transport, Internet, and Network Access layers. 
    - The Application layer is where applications like web browsers, email clients, and file-sharing tools interact with the network. It includes functionality like data formatting, encyption and session management. This layer covers layers 5, the session layer, 6, the presentation layer, and 7, the application layer from the OSI model. 
    - The Transport layer ensures reliable and efficient delivery of data between devices, managing segmentation, ordering, and retransmission as needed. TCP checks for errors, and resends lost data ensuring correct order. UDP on the other hand provides low-latency, connectionless delivery without error checking. This layer prevents the reciever from being overwhelmed by regulating data flow and uses port number to allow multiple applications to share the network simultaneously. This layer corresponds to layer 4, also the transport layer, in the OSI model.
    - The Internet Layer is responsible for addressing, packaging, and routing data packers so they can travel across networks and reach the correct destination device. This layer has to do with assigning IP addresses to ID source and destination devices. It determines the best route for data to travel across networks. This layer is primarily associated with the use of Internet Protocol (IP) along with supporting protocols like ICMP for error reporting and ARP for address resolution. This layer is comparable to layer 3, the Network layer of the OSI model.
    - The Network Access layer is responsible for physically transmitting data over network hardware, including cables switches, and wireless connections. It handles how data is formatted for the network medium and ensures it reaches the next device on the path. It organizes data into frames for proper transmission and recognition by devices, and detects transmisison errors using checksums or CRC. Uses MAC addresses to ID devices within the same network segment and determines how multiple devices share the same physical medium, avoiding collisions. This layer can associated with the Data Link and Physical Layers 6 and 7. 
    - TCP/IP is preferred over the OSI model because it is simpler, practical and widely implemented in real-world networks and the Internet. TCP/IP is protocol driven and focuses on actual communication needs.

## Example: Opening a Website
• Application Layer: The browser initiates the process by using DNS (like a phonebook) to translate the website's URL into an IP address and then generates an HTTP/HTTPS request for the page content.
• Transport Layer: This layer establishes a reliable connection between the client and the web server via a TCP three-way handshake, breaking the application data down into manageable segments. The three-way handshake has to do with the client and server comunicating with a SYNchronize step, a SYNchronize-ACKnoledge step and a final ACKnoledge step.
• Internet Layer: The segments are packaged into IP packets with the source and destination IP addresses so routers can direct them across the internet.
• Network Access Layer: Packets are converted into network frames containing physical MAC addresses and converted into electrical, radio, or optical signals for physical transmission over hardware.

## Common Confusions
- MAC address versus IP address: MAC addresses are physical taged to the NIC (network interface card) and is associated with the physical device capable of connecting to a network. The IP address is a logical address given to each device on a computer network allowing devices on the network to identify and communicate.
- Switch versus router: A switch is a physical connection within a LAN that connects multiple devices. A router is a device that connects the local network to the outside internet.
- TCP versus UDP: TCP is used when reliability and accuracy are important with TCP resending any lost or corrupted data and UDP is used when speed is more important than perfect accuracy

## Self-Test
-Which protocols are examples of TCP/IP transport layer protocols? TCP UDP
-The process of HTTP asking TCP to send some data and making sure that it is received correctly is an example of what? Adjacent-Layer interaction
-The process of TCP on one computer marking a TCP segment as segment 1, and the receiving computer then acknowledging the receipt of TCP segment 1 is an example of what? Same-Layer Interaction
-The process of a web server adding a TCP header to the contents of a web page, followed by adding an IP header and then adding a data link header and trailer is an example of what? Data Encapsulation
-Which of the following terms is used specifically to identify the entity created when encapsulating data inside data link layer headers and trailers? Frame
-Which OSI layer defines the functions of logical network-wide addressing and routing? Layer 3, the Network Layer
-Which OSI layer defines the standards for cabling and connectors? Layer 1, the Physical Layer


## References
https://www.geeksforgeeks.org/computer-networks/tcp-ip-model/
https://www.geeksforgeeks.org/computer-networks/open-systems-interconnection-model-osi/
https://www.youtube.com/watch?v=AYgXr1dynKU&t=434s - Proffesor Messer OSI Model
