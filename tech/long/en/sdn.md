# Software Defined Networking (SDN) / Open SDN

Software Defined Networking (SDN) is the dynamic, logical routing and switching of network traffic based on configurations arranged in software and overlayed on a static network hardware infrastructure.

Software Defined Networking decouples the network control logic from the physical hardware that performs the function, such as routers and switches. This is often expressed as a separating of control plane and data or forwarding plane functions. This means that the hardware is now only responsible for forwarding data, the control (routing control, switching information, and other logical network arrangements) is all managed by an application layer.

With SDN, the network hardware configuration and infrastructure is largely static, remaining unchanged. Instead, when a new network configuration is required, an software controller logically configures the network behavior and translates the requirements to the appropriate actions for servicing by the underlying hardware.

This arrangement allows for flexible, dynamic, and responsive network design. 

A key benefit of software defined networking is the centralized nature of configuration - the SDN controller can view and control all traffic on the network. This is especially beneficial for network monitoring for performance as well as for security.

Benefits:

* Centralized control can view, monitor, and control all traffic
* Cheaper to update and maintain
* Dynamically isolate internal threats by programatically severing connections
* Vendor-neutral (doesn't depend on vendor specific features or configurations)
* Better security as controller can monitor all traffic

Software Defined Networking may rely heavily on virtualization, particularly for application layer appliances which can be more easily abstracted into the SDN network definitions as VMs.

## Open SDN

Open SDN is a broad, and not very well agreed upon, concept of the open availability and licensing of software defined networking implementations for use across the contributing body.

Generally Open SDN implies that software defined networking should be vendor agnostic and any implementation should not rely on some vendor-locked feature of the underlying hardware or software implementation, and that use of the SDN implementation is free to use without restriction for any contributing member.

This includes:
* Open source standards
* Open source software
* Open source APIs and SDKs
* Open source hardware

More broadly, it may imply that access to development and contribution is open to all interested parties, however this is not a core tenent.

SDN was created with openness intended as a core feature. References to Open SDN are typically a reference to SDN in general.

## Components

### Application Layer

The application layer consists of network appliances such as firewalls, IDSs, load balancers, proxies, servers, and any other network appliance or device that has a network requirement within the SDN network.

Rather than communicating their network requirements directly to a hardware device interface, SDN network applications notify the **SDN Controller** of their requirements via a **North Bound Interface** (NBI).

The **North Bound Interface** is the communication path between the Application and the Controller, or the Application Layer to the Control Layer.

### Control Layer

An SDN Controller is responsible for the operations of the Control Layer. The controller is responsible for receiving the application network requirements and information from the Application layer via the North-bound interface (NBI) and translating those requirements into a Datapath.

The control layer translates that Datapath into instructions for the underlying hardware in the Infrastructre to properly forward the traffic along its physical interfaces.

The Datapath instructions are communicated to the infrastructe via the **South Bound Interface** (SBI).

### Infrastructure Layer

The infrastructure layer consists of the physical hardware which receives the datapath information from the South-bound Interface and performs the physical switching and forwarding of data packets across hardware.

## Control Plane

The control plane is the part of the network's traffic and activity that is active and collaborative. As an active plane, it is constantly scanning, updating, monitoring, and adjusting behaviors based on observations.

The control plane is responsible for:
* creating routing tables
* packet handling policies
* access control
* quality of service

With SDN, the control plane operations are taken over by a separate software, rather than by the hardware devices independantly.

## Data Plane

The data plane is responsible for the movement of/ the useful information and (or the information that a user or application is interested in receiving after it has arrived across the network) that is transmitted across the network.

The data plane is largely responsive, not active, meaning that it receives and moves packets according to configured instructions from other planes.

This plane includes:
* fragmenting and reassembling packets
* forwarding of packets
* copying of packets across interfaces

With SDN, the data plane is still handled by the underlying hardware devices.

## References

[1] https://www.geeksforgeeks.org/software-defined-networking/
[2] https://en.wikipedia.org/wiki/Software-defined_networking
[3] https://www.ibm.com/cloud/blog/software-defined-networking