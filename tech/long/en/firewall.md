# Firewall/unified threat management (UTM)/next-generation firewall (NGFW)

Firewalls are a network security mitigation tool that filter traffic into and out of protected networks. Basic firewalls are most active at layer 3 (network, IP) and layer 4 (transport, TCP/UDP/port number) of the OSI model; NGFWs and UTMs have an increased focus on additional layers.

Firewalls can create rules for each network interface (physical or virtual) for both inbound and outbound traffic. The most basic operations the rules can define for various traffic rules are 'permit' or 'deny'.

Firewalls work by checking all traffic against a list of pre-defined rules in sequential order, and executes which ever rule first matches the traffic pattern detected.

Firewalls can be hardware or software, can be standalone devices, VMs, and most operating systems (desktop and server) have host-based firewalls.

Firewalls can be stateful or stateless.

### Stateless Firewalls

Also referred to as *packet-filter*s or packet-filter firewalls.

Stateless firewalls do not keep track of sessions or traffic flows. They only evaluate each packet on its own merit and apply the defined traffic rules individually.

Stateless firewalls require less procesing power and less memory to operate, making them cheaper, more efficient, and less disruptive to legitimate network traffic. However, they are not able to assist in filtering session or flow based attacks such as Syn Floods or other DoS attacks.

### Stateful Firewalls

Stateful firewalls are able to keep track of sessions and data flows in order to apply rules based on the state of connections. 

This can be useful, for example, to prevent a single source from establishing too many connections or for too many TCP Syn requests to be initiated (requiring resources to be allocated but not used on the server) without the three-way handshake completing the connection.

The downside is an increased resource and memory requirement to maintain state information. It is possible to attack this by overwhelming the state table with enough legitimate traffic that the bad traffic states are either dropped or not recorded.

## Next Generation Firewall

Next generation firewalls (NGFW) have all the same functions as a standard firewall, but aims to operate up through layer 7 (application) of the OSI model. This allows for deeper packet inspection, inspecting payloads where possible. Next generation firewalls cannot inspect encrypted traffic payloads such as HTTPS unless the network uses a break-and-inspect process to de-encrypt and re-encrypted.

NGFWs operating at the application layer allows them to provide additional security services not found in common firewalls, which make them very similar to UTM solutions and the term may be used interchangeably.

## Unified Threat Management

Unified Threat Management (UTM) combines multiple security and mitigation services into a single device. 

Possible services to host on a UTM:
* Anti-virus
* Anti-malware
* Firewall
* Data-loss prevention
* IPS
* web-filters

The downside to UTM is a single point of failure, meaning that if the UTM device fails or is overwhelmed, all of the supported security services are interrupted.

Possible upsides are reduced cost of hardware, easier to maintain and update, 

A commercial UTM product may ship with a suite of security solutions, more possibly than required for the organization. If a distinction is to be made between NGFWs and UTMs, this is where it is most likely to be seen.

## Key Ideas

In most cases, a firewall configuration should conclude with a 'deny all' rule. Because rules are evaluated in order, this will allow only traffic that has been explicitly permitted.

Firewalls can be stateful or stateless.

NGFWs allow deeper packet inspection by operating at more levels of the OSI model, allowing the firewall to provide additional security features in parallel, such as virus and malware scanning of traffic.

## Keywords

Packet filter

## Related Ideas

* Break and inspect

## References

[1] https://en.wikipedia.org/wiki/Next-generation_firewall
[2] https://www.fortinet.com/resources/cyberglossary/unified-threat-management