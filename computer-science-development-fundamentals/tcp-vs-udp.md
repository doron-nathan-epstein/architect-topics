# TCP vs UDP

![TCP vs UDP](https://media.geeksforgeeks.org/wp-content/uploads/20230406112559/TCP-3.png)

## TCP

### TCP Features

- TCP keeps track of the segments being transmitted or received by assigning numbers to every single one of them.
- Flow control limits the rate at which a sender transfers data. This is done to ensure reliable delivery.
- TCP implements an error control mechanism for reliable data transfer.
- TCP takes into account the level of congestion in the network.
- Used for:
  - Sending Emails
  - Transferring Files
  - Web Browsing

### TCP Advantages vs Disadvantages

| Advantages | Disadvantages |
| ---------- | ------------- |
| It is reliable for maintaining a connection between Sender and Receiver. | It is slower than UDP and it takes more bandwidth. |
| It is responsible for sending data in a particular sequence. | Slower upon starting of transfer of a file. |
| Its' operations are not dependent on OS. | Not suitable for LAN and PAN Networks. |
| It allows and supports many routing protocols. | It does not have a multicast or broadcast category. |
| It can reduce the speed of data based on the speed of the receiver. | It does not load the whole page if a single data of the page is missing. |

## UDP

### UDP Features

- Used for simple request-response communication when the size of data is less and hence there is lesser concern about flow and error control.
- It is a suitable protocol for multicasting as UDP supports packet switching.
- UDP is used for some routing update protocols like RIP(Routing Information Protocol).
- Normally used for real-time applications which can not tolerate uneven delays between sections of a received message.
- Used for:
  - Gaming
  - Video Streaming
  - Online Video Chats

### UDP Advantages vs Disadvantages

| Advantages | Disadvantages |
| ---------- | ------------- |
| It does not require any connection for sending or receiving data. | We can not have any way to acknowledge the successful transfer of data. |
| Broadcast and Multicast are available in UDP. | UDP cannot have the mechanism to track the sequence of data. |
| UDP can operate on a large range of networks. | UDP is connectionless, and due to this, it is unreliable to transfer data. |
| UDP has live and real-time data. | In case of a Collision, UDP packets are dropped by Routers in comparison to TCP. |
| UDP can deliver data if all the components of the data are not complete. | UDP can drop packets in case of detection of errors. |

## Differences between TCP and UDP

| Basis | Transmission Control Protocol (TCP) | User Datagram Protocol (UDP) |
| ----- | ----------------------------------- | ---------------------------- |
| Type of Serivce | TCP is a connection-oriented protocol. | UDP is a connectionless protocol. |
|Reliability | TCP is a reliable protocol as it guarantees the delivery of data to the destination router. | UDP is an unreliable protocol as it does not guarantee the delivery of data to the destination. |
| Error Checking | TCP has a mechanism for error checking and error recovery. | UDP has no mechanism for error checking and error recovery. |
| Acknowledgement | TCP uses the acknowledgment technique. | UDP does not use the acknowledgment technique. |
| Sequence of Data | TCP rearranges the data packets in the receiver's side based on the sequence number. | UDP does not rearrange the data packets in the receiver's side. |
| Speed | TCP is slower than UDP. | UDP is faster than TCP. |
| Retransmission of Packets | TCP retransmits the lost packets. | UDP does not retransmit the lost packets. |
| Header Length | TCP header is of 20-60 bytes. | UDP header is of 8 bytes. |
| Weight | TCP is a heavy-weight protocol. | UDP is a lightweight protocol. |
| Handshake Technique | TCP uses a three-way handshake technique to establish a connection. | UDP does not establish a connection before sending data. |
| Broadcasting | TCP does not support Broadcasting. | UDP supports Broadcasting. |
| Protocols | TCP is used for HTTP, HTTPs, FTP, SMTP, Telnet. | UDP is used for DNS, DHCP, TFTP, SNMP, RIP, VOIP. |
| Stream Type | TCP is a stream-oriented protocol. | UDP is a message-oriented protocol. |
| Overhead | TCP has more overhead. | UDP has less overhead. |
| Applications | TCP is used for applications that require high reliability. | UDP is used for applications that do not require high reliability. |

## Sources

- <https://www.geeksforgeeks.org/differences-between-tcp-and-udp/>