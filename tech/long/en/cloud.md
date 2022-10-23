# Cloud

Cloud computing, or the Cloud, is a commercial networking strategy that takes advantage of economies of scale to provide scalable, highly reliable, highly available, and affordable computing and networking resources hosted on a remotely accessible data center.

The cloud can provide almost any computational or networking product that traditionally was provided by self-hosted or self-managed services.

Cloud Services are provided by Cloud Service Providers (CSPs).

Services may include:
* Computational power, such as Virtual Machines, Virtual Servers, or Virtual Functions
* Data Storage
* Databases
* Virtual Networks

Cloud service are useful for providing scalable back ups and recovery for Disaster Recovery.

**No matter what type of cloud service is chosen, the client is always responsible for their own data and data governance.** Responsibility for handling, processing, and release of data cannot be delegated to a CSP, though the CSP may be responsible for the physical storage, and in some specific cases some guarantees to the secure storage and transfer of data.

## Public and Private Clouds

Cloud services are often broadly categorized as Public or Private Clouds.

### Public

Public Clouds are commercial services that provide cloud services for paying or subscribing customers, clients, or tenents. 

Public refers to the commercial availability of the cloud resources for purchase, not to the after-market availability of services that are purchased by the client.

For example, a Virtual Private Cloud is a private virtual network that is used by and is accessible only to the client organization that purchased the VPC, but the VPC offering is a Public Cloud service provided by many Cloud Service Providers.

### Private

Private Clouds are non-commercial cloud services that are hosted internally by the managing organization.

With private clouds, the infrastructure, hardware, software, and all accompanying parts, products, and maintenance is handled by the organization that is using the cloud services internally.

Private Cloud services are generally not available for public purchase using the infrastructure of the private clouds host.

### Hybrid

In some cases, an organization may self-host some portion of the cloud services the use, but also purchase services from a public cloud service provider.

This situation is a hybrid cloud.

## Services

Clouds offer a huge variety of services such as:

### Virtual Private Cloud (VPC)

A Virtual Private Cloud is a public cloud offering that allows a private organization operate a cloud based virtual network.

VPCs allow an organization to use Software Defined Networking to dynamically segment and organize services and resources for different business units.

## X-as-a-Service

Cloud providers can provide a varying array of services, anywhere from an un-configured package of alloted hardware resources (IaaS) to a web-based application (SaaS).

### Software-as-a-Service (SaaS)

Software as a service is a cloud service offering that sells or offers a fully functional, typically web-based application.

Applications are typically licensed on a subscription basis; the application is often not sold as a an individual version or package, but as an authorization to use all versions of the application for the duration of the subscription license even as new versions are released.

With Software as a Service the client manages no part of the cloud service; the CSP is responsible for managing all aspects.

Examples of very popular SaaS offerings:
* Google Mail
* Dropbox
* Office365

Downsides to SaaS involve the lack of data privacy, as all data is ultimately controlled by the cloud, and a lack of resource ownership: if the license changes, the subscriber is not entitled to keep or use any executable part of the application they paid for.

### Platform-as-a-Service (PaaS)

A Platform-as-a-Service offering provides a fully configured computational network and environment for the client, that may include a network, virtual machines, servers, databases, operating systems, and applications.

Most commonly this is used to provide the environment and tools in a single package for developers to build applications, ran over the internet. 

These packages will typically come pre-installed and configured with the requisite development tools and build chains required for the developers to write or publish code that will be automatically built, published, or deployed by the platform systems.

With PaaS the CSP provides the backend hardware and infrastrucutre, including networking, the data storage and databases, the servers and VMs, the operating systems, firmwares, and tools. The handling of data and operation of applications is the responsibility of the client.

PaaS can be exceptionally convenient for developers as it provides a scalable, shared environment to push updates to review, integrate, or build, rather than building or testing on individual non-collaborative machines.

### Infrastructure-as-a-Service (IaaS)

Infrastructure-as-a-Service provides only a guaranteed amount of physical resources and some virtualization tools for the client to use to deploy their own VMs, servers, applications, and services.

With IaaS, a client purchases an amount of network resources, such as CPU power, RAM, network bandwidth, and data storage. The CSP then provisions and/or virtualizes the resources on their hardware, and provides an interface for the client to connect to the virtualized environment.

With IaaS, the CSP provides the back end hardware, the physical storage and servers, and the virtualization software that supports the clients purchase. The client is responsible for installing all operating systems, tools, software and managing and securing all the data and applications that are installed and run in the environment.

### Function-as-a-Service (Faas)

Function-as-a-Service is a cloud service offering that allows a client to purchase processing time for a single function or action that runs on demand and is billed only by the resources used, rather than running indefinitely.

With FaaS, the client writes their own function, a peice of software that performs a single task rather than an entire application, and the CSP provisions the needed resources and executes the function on demand.

Demand is often triggered manually by the client through a CSP provided interface, on a schedule defined by the client, or asynchronously such as when accessed through an API gateway by another application.

FaaS is often called 'serverless' computing, as the servers that run the function are not managed, configured, or generally visible to the client and maintained entirely transparently by the CSP. 

## References

https://en.wikipedia.org/wiki/Cloud_computing