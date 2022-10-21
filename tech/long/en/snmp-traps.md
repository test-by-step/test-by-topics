# Simple Network Management Protocol (SNMP) Traps

SNMP traps are triggers defined on the network device (typically router) that asynchronously notify the network management station of events. 

Other SNMP operations (not traps) are synchronous communication, with the network management station (NMS) initiating with a message to the network device and the network device responding.

With SNMP traps, a trigger based on some observed network conditions causes the network device (agent, in SNMP terms) to initiate a message to the manager.

SNMP traps operate on port 162 (or 10162 for secure SNMP).

SNMP traps require a management information database (MIB) on the manager in order to interpret the trap message, since each trap is associated with an object ID defined in the MIB - this is particularly important for enterprise specific traps which are not specified in the SNMP RFC.

## Types of SNMP Traps

### Generic Traps

Generic traps are defined in the SNMP RFC (RFC 1215).

* coldStart
* warmStart
* linkDown
* linkUp
* authenticationFailure
* egpNeighborLoss

### Enterprise Specific Traps

Enterprise specific traps are custom traps defined by the vendor or manufacturer.

## References

[1] https://www.solarwinds.com/resources/it-glossary/snmp-traps