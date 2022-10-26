# Scalability

Scalability is the ability of a system to grow in congress with an increase in demand for system resources.

Scalability provides Availability.

For IT systems, scalability will often need to account for:

* CPU Processing Capacity
* Network Bandwidth Capacity
* Memory / Buffer Capacity
* Data Storage Capacity
* Database transaction capacity
* Capacity for simulatneous connections
* Efficiency of algorithms (latency to scan big data, for example)
* Manageability (human demand for maintenance, provisioning, etc.)

Scalability can be implemented by adding or improving hardware for physical data centers, and can also be implemented logically through virtualization, particularly for cloud services.

Scalability can account for resource demand changes in both growth and recession - when demand goes up, more resoures are provisioned and added to the system; when demand goes down, resources are de-provisioned and released from the system.

Scalable systems often involve an automated process that can be triggered to allocate or de-allocate resources based on load metrics.

Scalability is a key goal for any organization.

Scalability is a key benefit of Cloud Computing.

With cloud computing, scalability can also reduce costs and increase efficiency as cloud service providers often provide *on-demand* resource allocation. With this arrangement, the customer only pays for the resources they use and resources are added or removed automatically to match the specified requirements of the real-time demand.

## Vertical vs Horizontal

Scalability can be achieved by adding resources to existing systems (vertical scaling) or by adding additional systems to share the load (horizontal scaling).

Some systems can make use of both. 

Functions as a Service, for example, will typically be pre-configured with a set amount of RAM to allocate to each running function instance. 

When demand increases, the cloud service provider will create new instances of the function container to process additional requests but each with the same pre-configured amount of RAM (horizontal scaling by adding addtional instances). 

If the developer discovers that the amount of RAM is insufficient to handle the amounts of data it has to process as the system develops over time, the system administrator can increase the amount of RAM allocated to the functions (vertical scaling by improving resources allocated for that instance).

## References

[1] https://en.wikipedia.org/wiki/Scalability