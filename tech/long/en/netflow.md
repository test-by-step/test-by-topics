# Netflow

Netflow is allows network devices to gather analytics data and metrics about network activity related to that device and export it to a centralized location for aggregation and analyzation.

Netflow was originally introduced by Cisco but is now has an implementation on most routers.

Netflow collects then exports for analysis statistics on IP traffic based on flows.

A flow represents a unique connection or stream of data to-and-from two endpoint services; an example is a single HTTP connection from a browser to a website server serving a single static page. Statistics are collected and accumulated and reported for each flow flows.

Each flow is defined uniquely by:
* ingress interface
* source and destination IP
* IP protocol used
* source and destination TCP/UDP ports
* IP type of service information

Netflow components include:
* Flow exporter - network device that gathers data and sends it to central location
* Flow collector - the repository that receives exporter data and aggregates it
* Analysis application - application that parses netflow data and analyzes it for network administrators


## References

[1] https://en.wikipedia.org/wiki/NetFlow