# Virtual Private Cloud (VPC)

Virtual Private Clouds are computational networks that host a suite of remotely administered services; most noteably: cloud networks, virtual machines and servers, databases, security appliances, gateways, and other specialized computing services.

VPCs are virtual networks, configured and defined to meet customer specifications.

VPCs are **public**ly provided cloud services to private organizations; this is different than a pre-assembled public Software or Platform as a Service or a self-hosted private cloud.

Virtual Private Clouds take advantage of economies of scale to cheaply provide vast amounts of computational and networking resources that are administered remotely (note that this can be provided by a third part, e.g. AWS or Azure or self hosted, though third party has become much more popular and expected).

Virtual Private Clouds allow the client organization to remotely provision and define a wide array of networked services through which all the traffic in the organization is routed through, albeit from a remote location.

## Common Operations for VPCs

* Storage - file storage for personal/indivual files, shared files, and archiving
* Databases - key-value or relational data stored for common / quick access
* Computation - services, functions, virtual machines, and other servers can be hosted, provisioned, and deprovisioned for exclusive use within the organization
* Networking - entire networks can be logically defined to specify subnets, VLANs, and routes to match the structure of the organization

## Benefits

* Reduced costs, taking advantage of economies of scale
* Scalable, can provision or deprovision resources as demand changes
* Risk management 
* Efficiently implement security controls
* Less management overhead

## Software Defined Networking

VPCs make use of Software Defined Networking (SDN) to create a virtual network that can be configured to behave in a multitude of logical arrangements, while allowing the underlying hardware to remain in a static configuration.

SDN can specify virtual routers and switches along with corresponding networks, subnets, VLANs, segments, trunks, and virtualized links that connect it all.

With software defined networking, network devices and security devices can be provisioned and connected dynamically.

### Traffic Mirroring

Port mirroring (Span Ports) can be effortlessly defined to mirror traffic to monitoring and IDS instances and events logged to SIEM solutions.

## Security Controls

VPCs offer many efficient security controls. 

Traffic mirroring can be used to copy traffic to a monitoring or IDS interface.

Software Defined Networking can be used to dynamically isolate networks when compromise is detected, disconnecting network segments in real time to prevent proliferation.

## Infrastructure as Code

Through the use of configuration files and exhaustive structural definitions, the shape and function of virtual private clouds can be defined via code.

These definitions are typically structured as YAML, XML, or JSON files that are processed via command line tools and cloud provisioning handled by the VPC providers back end.

## Pitfalls

Virtual Private Clouds and Private Clouds are not the same. VPCs are, typically, a public cloud service that provides a self-contained cloud infrastructure for a private organization, that is not publicly accessible. Private clouds are cloud services that are self-hosted by the organization.

## Related Ideas

* Software Defined Networking (SDN)
* Infrastructure as Code
* Infrastructure as a Service

## References

[1] https://www.ibm.com/cloud/learn/vpc