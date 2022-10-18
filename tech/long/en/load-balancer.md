# Load Balancer

Load balancers distribute INCOMING traffic across a back end array of servers or service providers. Load balancing is often referenced when providing high-availability to networked services (as apposed to high-availability for storage, or power).

Load balancers can balance traffic for different types of services including:
* web applications
* network routing
* power systems

Load balancers can automatically integrate new servers or service providers when they come online. Occasionally, they can detect and notify when servers go offline.

Load balancing can occur in hardware or software. Software (layer 7) load balancing can make smarter decisions but requires greater CPU use.

## Goals

1. Provide high availability (also redundancy)
2. Enable scalability

## Load Balancing Strategies

* Round robin: traffic is routed on a rotating basis to each back end service provider in turn.
* Fewest/least connections: traffic is routed to the service provider currently servicing the fewest connections
* Least time: traffic is routed the the service provider with the quickest response time
* Hash: distributes load based on configurable key such as HTTP header, URL, or IP
* IP Hash: See Hash
* Random: routes traffic to service providers through random selection

## Related ideas

* Reverse proxy: reverse proxies and load balancers often appear together, and may be provided by the same application (NGINX) and/or on the same physical hardware. It is possible that load balancers may be mentioned as a feature of some reverse proxies, however they are not synonymous as reverse proxies provide many additional features.
* Failover: a HA (high-availability) term related to provisioning a backup service provider that will take over workloads if the primary service provider fails.
* Active-active: This is the term most commonly associated with load balancing. Two or more service providers are active and traffic is routed to both based on the balancing algorithm chosen.
* Active-passive: Active passive is a high-availability term that it is possible may be referenced in relation to load balancing. Active passive is a failover strategy that a load balancer uses when the active service provider fails, traffic is rerouted to a second, previously idle provider.
* High availability: HA is a term used to reference a guarantee of little to no service down-time. For load balancers, this generally means the service provider is accessible via redundancy (multiple service providers in case one fails) and scalability (add new or spin up idle service providers as demand increases).

## Related tools

NGINX

## Pitfalls

Load balancers do provide high-availability but depending on context, other solutions are more applicable to high availability questions such as RAID (for storage) or UPS (for power).

Load balancers are unlikely to provide disaster recovery unless balancing load across multiple locations.

## Key words

incoming, traffic, high availability, redundancy, scalable

## References
[1] https://www.nginx.com/resources/glossary/load-balancing/
[2] https://www.ibm.com/cloud/learn/load-balancing
[3] https://www.jscape.com/blog/active-active-vs-active-passive-high-availability-cluster