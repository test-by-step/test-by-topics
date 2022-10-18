# Distributed Denial-of-Service (DDoS) Protection

A Distributed Denial-of-Service attack involves the use of many supplicant client devices, very often controlled via a botnet, to overwhelm the target system or network and cause it to be inaccessible to legitimate traffic.

A DDoS attack aims to deny availability, as such DDoS protection aims to ensure availability.

The simplest method to protect against DDoS is source address filtering - however several attack techniques make filtering based on source address or prefix alone.

Ideally, DDoS protection will occur at the edge network, before the attack reaches internal systems. Orchestrating a DDoS response to the edge network once an attack is discovered is complex and requires will configured Security Architecture Orchestration and Response (SOAR).

Reflection and Amplification attacks such as DNS or NTP reflecton are especially problematic as the traffic may come from an otherwise legitimate source, making it difficult to filter without disrupting some legitimate service.

Similarly, reflection and other spoofing techniques require planning so as not to self impose a denial of service by filtering legitimate traffic.

## Techniques for DDoS protection

### Blackhole filtering

Blackhole filtering involves routing traffic to a null interface to silently drop the connection.

If a the DDoS attack can be detected at a routing device traffic from offending sources can be routed to a null interface effectively killing the stream.

Detecting the attack and then triggering edge network interfaces to route offending traffic to a null or blackhole interface is Remote Triggered Black Hole filtering (RTBH).

By routing to a null interface, the traffic does not clog up internal or any single interface, reducing the impact of the attack. The attack instead is only limited to external interfaces and will ideally be much more distributed.

This method requires careful orchestration and effective detection.

### Load Balancers

Load balancers can be used to distribute connections to a pool of servers to share the load of the requests and scale to meet the increased demand.

### Content Delivery Networks

Content Delivery Networks (CDNs) are a distrubuted network of servers capable of service static and cached content from servers located geographically close to the destination.

Using content deliver networks can reduce the congestion caused by DDoS attacks by causing as much of the requests as possible to be routed to multiple geographically distributed content servers rather than a centralized resource.

### Plan to Scale

Some cloud providers allow for dynamic provisioning and scaling based on demand. Allowing for new resources to be provisioned and scaled on the fly can potentially rise to meet the demand of the DDoS botnet.

### Firewalls

Stateful firewalls especially can detect certain types of Denial of Service attacks such as attacks that iniate but never close TCP connections and mitigate them. 

Limiting TCP connections and dropping unresponsive connections may also help in mitigating DoS attacks that use IP address source spoofing to avoid detection.

Web Application Firewalls also apply here.

Typically DDoS attacks rely more on overwhelming numbers of zombie devices rather than strictly on protocol attacks. Firewalls and typical DoS mitigation is certainly helpful for DDoS, but may not be the best solution if presented with a DDoS context.

## Related Ideas

* DDoS
* Botnet

## Pitfalls

It is worth keeping in mind the distinction between DoS and DDoS attacks when detirmining the best solution to a problem. For example, while stateful firewalls can help with some denial of service attacks such as SYN Floods, a SYN Flood doesn't usually require a large zombie network to carry out, so another answer for DDoS might be more effective.

## References

[1] https://www.nist.gov/programs-projects/advanced-ddos-mitigation-techniques