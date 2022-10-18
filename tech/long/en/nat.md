# Network address translation (NAT) gateway

Network Address Transation (NAT) permits bidirection communication from hosts on a network with a private address space (typically unrouteable on the public internet) to public internet addresses.

At its most basic level NAT Gateways maintain a state table of active connections, mapping internal host IP addresses and ports to external addresses and ports as they are requested.

NAT Gateways help remediate the problem of limited IPv4 address space by only requiring a single public IP address for all the internally connected devices.

From a security standpoint, NAT gateways also render internal networks unrouteable directly from the Internet and masks internal IP addresses and port numbers.

NAT is typically only used in IPv4.

## Basic NAT

This configuration is not as likely to be referenced, but can be used to effectively connect two private network address spaces to allow routing between the two over the Internet.

## One-to-many NAT

When referencing NATs it is most likely to be refering to a one-to-many NAT where multiple internal device IP addresses are mapped to a single external, Internet-routable address.

## Key Ideas

Dynamic network address translation, common in home modems and routers, where the translation happens transparently to the user.

DNAT or port-forwarding allows internal servers or services to be accessed from the Internet by providing a static between an external port and address and the internal address and port.

## Other

Some stream based protocols require advanced NAT processing techniques (SIP for example) as there ar multiple UDP streams that may not form a cohesive identifiable session that non-trivial NAT implementations handle well.