# TCP/IP

* **Protocols** are a set of rules or conventions, like a physical handshake for humans , that the world has agreed upon for computers to communicate with.
* **TCP/IP** are two protocols for sending data between two computers. In the real world, we might write an address on an envelope in order to send a letter to someone, along with our own address for a letter in return.
* **IP** stands for internet protocol, a protocol that includes a standard way for computers to address each other. **IP addresses** are unique addresses for computers connected to the internet, such that a packet sent from one computer to another will be passed along routers until it reaches its destination.
  * An IP address might have the format `#.#.#.#`, where each number can have a value from 0 to 255. Each number will be the size of one byte, so the entire address will be 4 bytes, or 32 bits. This means that this version of IP, version 4, can only support a maximum of 4 billion addresses. Another version of IP, version 6, uses 128 bits to support many more possible addresses.
* **TCP**, transmission control protocol, is a protocol for sending and receiving data. TCP allows for a single server, at the same IP address, to provide multiple services through the use of a **port number**, a small integer added to the IP address. For example, HTTP is sent to port number 80, and HTTPS uses port number 443.
  * TCP also allows for a large amount of data, like an image, to be sent in smaller chunks. Each of them might be labeled with a sequence number, as with “part 1 of 4” or “part 2 of 4”. And if one of the parts is lost, the recipient can ask for the missing part again.
  * UDP is another protocol for sending data that does not guarantee delivery like TCP, which might be useful for streaming real-time videos or calls, since we don’t want to wait for all the packets to be redelivered before we get new ones.



#### The 4 layers of the TCP/IP model

TCP/IP functionality is divided into four layers, each of which includes specific protocols:

1. The **application layer** provides applications with standardized data exchange. Its protocols include HTTP, FTP, [Post Office Protocol 3](https://whatis.techtarget.com/definition/POP3-Post-Office-Protocol-3), [Simple Mail Transfer Protocol](https://whatis.techtarget.com/definition/SMTP-Simple-Mail-Transfer-Protocol) and Simple Network Management Protocol. At the application layer, the payload is the actual application data.
2. The **transport layer** is responsible for maintaining end-to-end communications across the network. TCP handles communications between hosts and provides flow control, multiplexing and reliability. The transport protocols include TCP and [User Datagram Protocol](https://www.techtarget.com/searchnetworking/definition/UDP-User-Datagram-Protocol), which is sometimes used instead of TCP for special purposes.
3. The **network layer**, also called the _internet layer_, deals with packets and connects independent networks to transport the packets across network boundaries. The network layer protocols are IP and Internet Control Message Protocol, which is used for error reporting.
4. The **physical layer**, also known as the _network interface layer_ or _data link layer_, consists of protocols that operate only on a link -- the network component that interconnects nodes or hosts in the network. The protocols in this lowest layer include Ethernet for local area networks and [Address Resolution Protocol](https://www.techtarget.com/searchnetworking/definition/Address-Resolution-Protocol-ARP).

#### Uses of TCP/IP

TCP/IP can be used to provide remote login over the network for interactive file transfer to deliver email, to deliver webpages over the network and to remotely access a server host's file system. Most broadly, it is used to represent how information changes form as it travels over a network from the concrete physical layer to the abstract application layer. It details the basic protocols, or methods of communication, at each layer as information passes through.

#### Pros and cons of TCP/IP

The advantages of using the TCP/IP model include the following:

* helps establish a connection between different types of computers;
* works independently of the OS;
* supports many routing protocols;
* uses client-server architecture that is highly scalable;
* can be operated independently;
* supports several routing protocols; and
* is lightweight and doesn't place unnecessary strain on a network or computer.

The disadvantages of TCP/IP include the following:

* is complicated to set up and manage;
* transport layer does not guarantee delivery of packets;
* is not easy to replace protocols in TCP/IP;
* does not clearly separate the concepts of services, interfaces and protocols, so it is not suitable for describing new technologies in new networks; and
* is especially vulnerable to a [synchronization attack](https://www.techtarget.com/searchsecurity/definition/SYN-flooding), which is a type of denial-of-service attack in which a bad actor uses TCP/IP.

{% embed url="https://cs50.harvard.edu/x/2022/notes/8" %}
