# High Availability (HA)

High Availability is a commitment to providing a certain, typically greater than normal, amount of service operation and availability in a given period.

A highly available resource is almost always operational and accessible to clients. [3]

When a system claims to have high availability, it is typically guaranteeing that the amount of downtime it experiences in a year will be kept under a certain (usually very tight) threshold.

High Availability targets may be stipulated in a Service Level Agreement.

High Availability will be closely related to other Availability topics such as: Mean Time To Recover, Recovery Time Objective, Business Continuity Planning, and Disaster Recovery.

High Availability is related to technologies and techniques such as: clustering, RAID, redundancy, failover, replication/back ups.

A failover occurs when a backup components takes over for a failed primary component.

High availability is distinct from fault tolerance; fault tolerant systems are 100% available, 0 downtime systems that can withstand errors, attacks, and/or disasters.

Implementing Highly Available solutions faces challenges in that:

* The system should not be taken down for maintenance
* The system should not be taken down for updates
* The system should not be interrupted due to data corruption
* The system should not be interrupted due to component failures
* The system should not be interrupted by a DoS attack
* The system should not be interrupted during a hacking breach

## Five-Nines Availability

Five-nines availability, or 99.999% availability is a common HA claim or guarantee that assures that a system will be functional, reachable, and operational 99.999% of the time.

Five-nines (99.999%) availability aims to limit system downtime (non-available, or non-functional time) to less than 5 minutes and 15 seconds (0.00001 * 365 days) for the **entire year**.

Availability might also be described by other levels of 'nines', for example four-nines (99.99%, 52 minutes 36 seconds downtime) or three-nines (99.9%, 8 hours and 45 minutes down time). Five-nines is the most common.

## References

[1] https://en.wikipedia.org/wiki/High_availability

[2] https://csrc.nist.gov/glossary/term/high_availability

[3] https://learn.microsoft.com/en-us/previous-versions/windows/desktop/mscs/high-availability

[4] https://www.cisco.com/c/en/us/solutions/hybrid-work/what-is-high-availability.html#~infrastructure-elements