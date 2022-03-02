# TCP/IP



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
