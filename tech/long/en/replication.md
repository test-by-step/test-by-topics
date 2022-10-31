# Replication

Replication involves the duplication of components or devices with a continual synchronization of the system state between nodes to maintain the consistency of state across the system and improve reliability.

Replicated systems are usually also redundant systems.

The goal of replication is consistency across the system or application.

Replication improves consistency, resiliency, reliability, and fault tolerance.

Replication can be active, in which data and requests are duplicated and processed by all nodes at the time of the request.

Replication can be passive, in which data and requests are processed by a single node and then copied and transfered to other nodes.

Typically back-ups are not considered replications; back ups create point in time views of a system state, where as replication continuously syncrhonizes state across independant nodes in the system.

Examples of replication:
* RAID
* Distributed database
* Some aspects of CDNs
* Hot sites

## Redundancy vs. Replication

Replication may be an aspect of redundancy but the purpose of each is often slightly different. 

With any **redundant** system, the two systems should perform identical or nearly identical functions; the system is either stateless, or the state of the system is detirmined at the time of provisioning and remains identical for each redundant system throughout its operation.

The goal of redundancy is to improve **reliability**.

Replicated systems must synchronize the system/application state between nodes. Systems that require replication operate in an environment where the state is constantly changing, requiring copying or synchronization to a secondary system, i.e. replication.

The goal of replication is to improve **consistency**.

An example of a redundant-only system is a server cluster in which each server in the cluster performs the same function (e.g. serves the exact same web page). The logic for performing this function does not frequently change and so the servers do not need to be synchronized after provisioning to remain redundant.

An example of a replicated system is a primary database and a back up database; data must be either written to both at the same time (active) to keep them consistent with each other, or the primary must be periodically backed up (passive) to the secondary to remain consistent.

Replicated systems are most often redundant systems.

## References

[1] https://en.wikipedia.org/wiki/Replication_(computing)