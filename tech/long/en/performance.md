# Performance

Performance of a system measures the amount of useful work it can do at any time, or over a measurable period.

Aspects of performance:

* Availability: how often the application is reachable
* Response time: how quickly a request is processed and response returned
    * Service time: how long to process
    * wait time: how long from message received until service time begins
    * transmission: time on the wire to send and receive data
* Bandwidth: how much information can be moved per unit of time
* Throughput: how many processes can be completed per unit of time (for networks, bandwidth and throughput are used interchangeably)
* Power: how much power a system requires to run (often throughput per watt)

## Performance Tuning

1. Assess problem
1. Measure performance
1. Identify bottleneck
1. Remove bottleneck
1. Measure performance
1. Repeat or Adopt 

## Network Performance

Network performance is typically measured in bandwidth.

Ways to improve network performance:

* Break up broadcast domains with VLANs, subnets, and routers.
* Break up collision domains with switches
* Use spanning tree protocol to prevent broadcast storms in layer 2 network loops
* Fix damaged physical connects
* Fix damaged wires/cables
* Purchase additional bandwidth for WAN links
* Reduce number of inline devices that increase latency
* Use quality of service rules to prioritize latency-sensitive traffic such as VoIP and video traffic
* Block or filter unwanted or misbehaving protocols

### Routing

* Ensure there are sufficient IP addresses and no duplicate IP addresses in the subnet 
* Ensure routers are advertising the appropriate networks
* Choose the right routing protocol
* Distance Vector protocols can have loops that never go away
* Distance Vector protocols, broken routes are transmitted slowly
* Link State protocols flood the network to advertise
* Link State protocols can have infinite routing loops that can be eliminated with TTL

## Wireless Performance

Wireless performance is often measured in bandwidth.

* Choose channels that don't interfere.
* Use wireless site survey to identify optimal placement for APs
* Reduce noise by removing or moving other emitters
* Increase signal strength (if RSSI is low)
* Choose a protocol with lower frequency (2.4GHz: .11b, .11g, .11n, ax, be) if devices are farther away
* Choose a protocol with higher frequency (5GHz: .11a, .11n, .11ac, ax, be)

## Server Performance

* Use SSL accelerators to hardware decrypt encrypted connections
* Use load-balancers to distribute requests across multiple servers
* Use content delivery networks to load static content geographically close to client
* Increase caches for commonly/frequently/repeatedly accessed requests
* Increase buffer sizes where too many connections/processes

## Security Performance

* Reduce the number of inline appliances
* Eliminate single points of failure or congestion

## References

[1] https://en.wikipedia.org/wiki/Computer_performance