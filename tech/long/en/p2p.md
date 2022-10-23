# Peer-to-peer (P2P)

Peer-to-peer networks and connections are decentralized services and applications that function by sharing or linking directly between two or more participating client nodes in the network rather than connecting to a dedicated server.

In contrast, traditional networking operates on client-server model in which a client reaches out to a central server, the server does the computational processing of the request and responds, as well as forwards any requisite messages to any other connected clients.

In peer-to-peer applications, all of the data and computational power is hosted on the client machines who communicate directly with each other. 

P2P is almost always built on an Application layer protocol.

Most Peer-to-Peer networks operate on the principle that each node (client) in the network is equally privileged. However, resources can be apportioned according to network participation, in BitTorrent for example, download bandwidth is alloted in greater portion to clients that provide greater amounts of upload bandwidth. When there is no competition for bandwidth, there is typically no restriction.

Several P2P protocols can operate over the Internet, such as BitTorrent and Skype, but there are some local protocol that are functionally peer-to-peer networks and protcols. Local file shares such as Windows file shares allowed Windows machines on a local network to discover other Windows machines and share files (and printers) by downloading directly from the endpoint. Originally this was done using NetBIOS in Windows, which still exists for discovery and other purposes; currently file sharing in windows happens over SMB.

P2P networks are useful in filesharing and internet voice and video application where client nodes host the file data, do all the application processing, respond to connections, and provide the network bandwidth required for the connections.

## Organization

P2P networks are typically constructed via a virtual overlay, where network traffic is still routed over TCP/IP or other Internet protocols, but nodes logically connect themselves at the application layer.

### Unstructured networks

Unstructured P2P networks do not have a particular arrangement or requirements for participating nodes; nodes can easily enter and leave the network making it highly dynamic.

The downside is that when a query is made in the network, to search for a particular file for example, the query must be flooded throughout the entire network, incurring large overhead costs for individual actions.

### Structured networks

In structured networks, each node upon entering the network joins a specific topology. Network resources are tracked via Distributed Hash Tables (DHT).

Looking up resource owners and locations with DHT is a simple key-value look up that doesn't require a network flood, but joining and leaving the network is more difficult as the participating nodes need to synchronize their place in the topology and the DHT.

## Securing P2P

A network administrator seeking to prevent some P2P activity can block common P2P ports from the network:

* 411-412 Direct Connect
* 1214 KAZAA
* 1337 Waste
* 4627 EMule
* 6257 WINMX
* 6346-6347 Gnutella
* 6699 Napster
* 6881-6999 BitTorrent

Some protocols are trickier to block without interrupting legitimate network operations such as SMB (port 445) and NetBIOS (ports 137, 138, 139) as these are commonly used in Windows for discovering neighboring devices, sharing printers, and sharing files locally. Careful consideration should be taken to decide when, how, and if SMB or NetBIOS traffic should be allowed on the network.

Early versions of SMB were vulnerable to an attack known as EternalBlue which allows arbitrary code execution on attacked devices where vulnerable. If SMB is required for legitimate operations, SMB should always be SMBv3.

## Getting around NATs

A non-trivial problem in P2P networks is the abundance of client devices that are hosted within a network behind a NAT, typically rendering the device unroutable from the Internet and therefor not directly acessible from other P2P clients. 

To solve this, volunteer relay nodes (or sometimes, as in the case of Skype, commercially hosted relay nodes) act as intermediaries that can host a persistent connection allowing traffic to flow back through the NAT gateway even if a remote connection initiates a new unique session.

With these relay nodes, traffic is still routed from client to client, rather than through a server and all application processing is still handled by the client endpoints.

## Examples

* BitTorrent
* Skype
* Windows File Shares

Many cryptocurrencies such as Bitcoin and Ether are classed as Peer-to-peer networks as there is no central server and each node acts as a client and as a server.

## References

[1] https://en.wikipedia.org/wiki/Peer-to-peer