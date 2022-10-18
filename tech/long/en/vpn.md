# Virtual Private Network

VPNs create an ecrypted connection from a local or public network to a (typically remote) private network through which traffic can be routed. This connection is usually referred to as a tunnel as the traffic routed through it is entirely encapsulated and protected in the secure connection that crosses an insecure or open network.

In the context of test questions, VPNs are most likely to be referenced for creating a secure connection from either a remote device or a remote site to a more secure or sensitive internal corporate network.

Traffic routed through VPNs is granted confidentiality via encryption while in transit between the VPN supplicants and servers.

While inside the VPN tunnel traffic information is protected along with payload, such as final destination IP address; the only exposed IP address is that of the VPN server and client.

VPNs are used to allow remote access to networks and internal services and assets that are otherwise unavailable to a public internet connection. Connecting via VPN to the internal network may require Network Access Control (NAC).

## VPN Concepts

### Client-to-site VPN

In a client-to-site VPN an application is installed on the end-user device which is responsible for establishing a connection to the VPN server and passing traffic to the VPN for routing.

### Site-to-site VPN

In a site-to-site VPN one private network is connected remotely to another private network by creating a VPN tunnel between two routing devices. 

### VPN Concentrator

VPN concentrators are physical devices with specialized hardware for efficiently managing, encrypting, and decrypting multiple VPN connections before passing the traffic along to the respective network.

### Split tunneling

Split tunneling is a configuration in which only some of the network traffic is routed through the VPN tunnel and the rest is allowed to pass to the standard internet connection. For example, all traffic for private address space 10.0.10.0/16 may be routed over the VPN to the private corporate network, and all other requests are serviced by the local ISP.

## Protocols

* IPSec: IPSec is the most typical protocol to be associated with VPNs. IPSec is used to create the secure tunnel over which the VPN traffic is routed.
* Wireguard: Wireguard is a newer protocol that aims to provide faster, more efficient encryption and processing
* SSH: It is possible to create a VPN connection using SSH, but unlikely in test context.

## Pitfalls



## Related Ideas

* IPSEC
* Wireguard

## Reference

[1] https://www.kaspersky.com/resource-center/definitions/what-is-a-vpn