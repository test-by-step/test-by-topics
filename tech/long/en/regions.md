# Regions

Regions are geographically distributed areas in cloud computing that provide broad physical segmentation of cloud resources. Regions generally represent the physical location of a cloud service providers data center.

Regions are the physical locations where servers and data are located.

Regions can be used to:

Provide services closer to clients by choosing regions in the same geographic area, reducing latency and improving cloud service responsiveness.

Aid in disaster recovery / increase availability by spreading services over a wider geographic area. If services in one geographic area is affected, traffic can be redirected to a new geographic area (if it is already provisioned).

Comply with regulations when laws (GDPR, e.g.) or industry standards (PCI-DSS) mandate where and how data is stored and transfered. Some standards may require that data be stored in certain locations, or not stored in others - using regions allows clients to select exactly where in the world their data and services are physically located.

Regions are distinct from availability zones in that regions represent an entire geographic area, typically a single data center whereas availability zones are physical blocks or segments within the region / data center.

## Key Ideas

Regions are geographicly distributed data centers.

Regions are most associated with cloud computing.

Different regions can be used to provide:
* Availability (through redundancy)
* Disaster recovery, as hot/cold/warm sites
* Comply with regulations, where data sovereignty or privacy laws apply geographically

## Related Ideas

* Availability Zones
* Cloud Service Provider

## References

[1] https://www.tomsguide.com/features/why-regional-cloud-hosting-matters