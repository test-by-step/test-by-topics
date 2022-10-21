# Screened Subnet

Screened subnets are semi-trusted subnets that are placed betwen the outside Internet or WAN and the internal organizational network.

Screened subnets will involve at least two firewalls: one, less-strict firewall which filters traffic coming from the WAN into the screened subnet where public traffic from the WAN might have some legitimate business, such as accessing public web servers or mail servers; and a second, more-strict firewall which will filter all untrusted traffic.

The screened subnet is sometimes called a DMZ, demilitarized zone, perimiter network, or bastion hosts.

A screened subnet provides an area where an organization can provide access to services for legitimate use public traffic, while still protecting their services from common attacks. The second router is intended to prevent public access entirely and only provide access for outgoing connections and for authorized incoming remote traffic.

Typical devices in the screened subnet are:
* public web servers
* mail servers

It is possible for a screened subnet to be implemented with only one router and three interfaces. It is most common to see a screened subnet referenced as at least two distinct routers.

## Pitfalls

Screened subnets are different from screened host firewalls. Screened host firewalls are a single firewall solution that only separates two networks: external and internal. Screened subnets require two or more firewalls and separate three or more networks.

## References

[1] https://en.wikipedia.org/wiki/Screened_subnet