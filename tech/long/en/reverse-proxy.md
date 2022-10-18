# Reverse Proxy

Reverse proxies are placed in front of servers in order to filter, inspect, and pre-process connections before forwarding to the server.

Reverse proxies can perform many functions:
* SSL acceleration
* Load balancing
* Cache frequently requested content
* Compression
* Inspection and filtering

Reverse proxies are used to improve scalability, availability, assist in redundancy, and can provide mitigation through inspection and filtering.

Reverse proxies can be a double-edged blade from a security perspective: on one hand it is easier to secure a single device (the reverse proxy) that handles external connections on behalf of the internal servers; on the other hand, it becomes a single point of failure.

## Functions

### SSL Acceleration

Some physical reverse proxies are equipped with specialized hardware which efficiently decrypts secure encrypted sessions, this both speeds up the process as well as lightens the processing burden on the servers.

### Load balancing

Reverse proxies can be configured to manage back-end server clusters and distribute connections accross servers based on an algorithm to balance connection requirements so that no one device becomes overloaded, and to shift load if a server fails.

Load balancing is part of enabling high-availability.

### Caching

Some web resources are static and frequently requested. Rather than burdening the back end servers with fetching and returning these requests individually, the reverse proxy can immediately serve the request from cached content.

### Compression

The reverse proxy can compress and decompress content in order to improve load times over the network and reduce network bandwidth useage.

### Inspection and filtering

The reverse proxy can also inspect and filter traffic before it reaches the server. This would be commonly implemented or paired with a web application firewall (WAF).

Filtering and inspection will look for malicous or malformed activity and drop or block it before it reaches the servers for processing.

## Key Ideas

* Reverse proxies are set in front of servers or server clusters
* With a WAF are often on a reverse proxy in order to inspect and filter traffic before being passed to the back end service
* Load-balancers are also often installed on the reverse proxy
* Physical hardware on reverse proxy devices can efficiently decrypt SSL conections for SSL acceleration

## References

[1] https://en.wikipedia.org/wiki/Reverse_proxy