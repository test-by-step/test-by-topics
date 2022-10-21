# Network Access Control Lists (NAC List)

Network Access Control Lists filter network traffic based off of packet features such as source and destination addresses, ports, and protocols.

Access Control Lists are a sequential set of rules that define whether an action is permitted or denied.

Each rule is checked in sequential order until a condition defined in the rule matches a feature of the action or traffic. Once a match is made, the action specified by the rule is followed, and processing of the list ends.

When refering to routers and firewalls, NAC Lists may be abbreviated only as an Access Control List (ACL).

Network Access Control lists (NAC Lists) filter network traffic. Each network packet's source and destination IP address, source and destination port number, and transportation layer protocol is compared against conditions defined in each rule. If any of the packet's features match the rule in the list, the traffic can be permitted (routed to its next interface), or denied (dropped).

A single rule in a NAC List can specify individual IPs, subnets, ranges of ports, or specify 'any'. It can be used to block traffic from a source, or to a destination.

An example: 
> permit tcp 192.168.77.0 0.0.0.255 192.168.77.3 0.0.0.0
explicitly permits TCP traffic from any host in the 192.168.77.0/24 subnet to the device with IP 192.168.77.3.

If the packet being inspected matches this rule, it will permit the packet to continue, and cease checking for further rules, such that even if another rule further down the list would have matched this packet it would not be processed.

Network Access Control Lists function as a packet filter **firewall**.

Network Accesss Control lists are most often associated with IP Networks, routers, and firewalls. 

## Related Ideas

* firewall
* packet filter firewall

## References
