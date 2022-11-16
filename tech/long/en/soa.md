# Service Oriented Architecture (SOA)

Service Oriented Architecture (SOA) is an application/system design idea which breaks components of multiple applications functions into discrete services, rather than as a single monolithic applications.

Service Oriented Architecture is an integrating feature, spanning an entire organization. It allows the reuse of functionality of multiple applications that service multiple facets of an organization, rather than functioning as a single application.

SOA is somewhat distinct from microservices as SOA allows reuse of specific application functions across multiple organizational applications. Microservices are typically most associated with serving the requested functions of distributed applications, rather than integrating or communicating across applications.

SOA can be said to loosely couple organizational applications. An enterprise service bus (ESB) can be used to connect services by providing an abstraction between the services rather than having them trying to communicate directly.

SOA is often highly related to an ESB.

SOA services typically serve a discrete function, and in order to perform multiple functions other services must be invoked through a service interface.

SOA can be useful to break down application features and functions into multiple components which may also be reused across multiple applications and interfaces without the need for service duplication.

Service Oriented Architecture can also assist in dividing access, or providing tiered access, to other departments, clients, partners, and customers. For example, rather than providing full application access to a connected partner, only the necessary services need to be exposed or access granted.

## Service features

1. A single, repeatable function
1. Self-contained 
1. Black-box; only input and output needs to be known, not internal operation
1. May invoke multiple other services

* Services are stateless, dependent only on the input of each invokation
* 

## References

[1] https://www.ibm.com/cloud/learn/soa

[2] https://en.wikipedia.org/wiki/Service-oriented_architecture