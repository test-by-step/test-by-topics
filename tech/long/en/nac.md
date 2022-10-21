# Network Access Control

Network Access Control is most often related to end-user device (or IoT device) access to a private or corporate network.

Network Access Control will require devices to meet certain criteria to be permitted network access such as: verified approved group policies, no unauthorized softwares, virus free, and/or fully patched and updated.

NAC can also help with inventory management.

NAC may also be useful in incidence response in blocking misbehaving or compromised devices during an incident, and in correlation and investigation during forensics.

NAC allows centralized policy management, enforcing policies on all endpoints.

NAC can either reject a connection for non-compliant devices, quarantine the devices by restricting access to some services or isolating it in a separate VLAN, or put the device into a guest network/VLAN with limited permissions and access.

Abbreviated as NAC.

NAC solutions can be:
* Agent-based
* Agentless

## Agented / Agent-based NAC

Agent based NAC requires an application installed on each end-user device to monitor and report device status to the network service that authorizes access. 

Agented NAC is more invasive and there are difficult ethical considerations when using agented NAC in Bring-Your-Own-Device schemes. The beneift, however, is that there is much greater fidelity and visibility into compromised systems.

## Agentless or Network NAC

Agentless NAC relies on an additional observer on the network observing the behavior of end point devices or remotely scanning open services.

Agentless NACs have a lower overhead and generally lower complexity and are less invasive, however there is reduced control and visibility of the endpoint.

## References

[1] https://www.cisco.com/c/en/us/products/security/what-is-network-access-control-nac.html