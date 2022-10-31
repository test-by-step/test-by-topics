# Redundancy

Redundancy is the duplication of functions, systems, and equipment in order to increase reliability or improve performance.

Redundancy improves reliability by providing failover, back up, or alternative options for systems and components.

Redundancy can improve performance by providing additional network paths or parallel processing power.

Generally, redundancy provides resiliency, fault-tollerance, and availability; systems can either withstand individual system failures/interruptions or automatically cover an individual malfunction with redundant systems.

Redundancy can be active, in which traffic or service requests are sent to all redundant systems in roughly equal measure or at the same time.

Redundancy can be passive, in which traffic is sent primarily to a primary system until that system becomes overwhelmed or fails. Traffic or service requests are then switched to the redundant system.

Failover occurs when a primary system fails and a backup or redundant system takes over as the primary servicer.

Examples of providing redundancy:
* Multiple Routers/routes that lead to the same network
* Multiple power supply inputs
* Clustering (active-active & active passive)
* Some aspects of Content Delivery Networks

Redundancy is strongly related to fault-tolerant systems as well as high availability systems.

Redundancy can also be used for error detection; that is, with identical systems one system can be used to check the other, or both can check each other for errors.

Redundancy can be distributed geographically.

## Dissimilar Redundancy

Though uncommon, some contexts might call for dissimilar redundancy in which two different types of systems or equipment are used to provide the same function, with the expectation that both will be unlikely to develop or exhibit the same flaw.

E.g. processors from two separate vendors, or two different softwares built for the same purpose or function.

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

[1] https://en.wikipedia.org/wiki/Redundancy_(engineering)