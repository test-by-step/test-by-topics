# Virtual Local Area Network (VLAN)

Virtual Local Area Networks are logically defined segments in a Local Area Network that prevent interfaces on the same layer 2 device from communicating directly, functionally creating separate sub-networks.

VLANs are defined on layer 2 devices; managed switches specifically.

When a managed switch specifies a VLAN for an interface, frames that arrive on that interface can only be switched between interfaces with the same VLAN number. 

Because VLANs prevent a switch interfaces from switching between interfaces of different VLANs (a layer 2 function), in order to communicate between VLANs a layer 3 device is required, such as a router or a layer 3 switch.

VLANs break up broadcast domains.

## Purpose

VLANs are used for:
* improved effeciency
* improved security
* improved scalability
* reduced cost

By being able to logically define new subnetworks using VLANs, new network segments can be created without the need for purchasing expensive hardware, or any complicated rearranging of physical hardware and connections.

VLANs provide an inherent security benefit as it divides the network into segments which cannot communicate directly without being filtered through, at the very least, a layer 3 device. It also prevents a single compromised device from being able to directly observe any other devices beyond its own VLAN.

## Links

While traffic from different VLANs cannot jump between VLANs without a layer 3 device, traffic from the same VLAN can move to different layer 2 devices but requires special link types.

### Access Link

Access links are the links that allow devices to connect and communicate with other links in the same VLAN. It is the type of link that a computer or VOIP phone would be plugged in to in order to access the network. 

Generally only a single VLAN can be defined for this links and no other VLANs will have access to these links. (There is some exception to this, where on some devices an additional VOIP VLAN can be configured to allow for a computer to connect to the network through a jump port on a VOIP phone).

### Trunk Link

In order for VLAN traffic to be shared across multiple layer 2 devices (switches) a special port has to be configured called a trunk port which is allowed to aggregate traffic from various VLANs and pass it along to an adjacent device.

This requires that the layer 2 traffic be given an additional header, generally referred to as 802.1Q header (after the IEEE 802.1Q standard which defines VLAN headers for trunking). This header allows the traffic to be tagged with its VLAN when it is aggregated onto the trunk link and to be parsed back into the appropriate VLAN when it reaches the next switch.

Trunk links also have to specify which VLANs are permitted on their links and are re-separated upon reaching their destination. Even after trunking, traffic tagged with a VLAN will only be switched onto interfaces with the same VLAN tag.

### Hybrid Link

Hybrid links are more complex links which allow both trunked links and access links. Some devices can communicate when they are connected and notify eachother that they are switches and dynamically configure the link for trunking.

## Pitfalls

The virtual in VLAN does not refer to virtual or software defined networking in cloud computing, but rather to the local configuration applied by switches to logically segment interfaces on the same device.

## Related Ideas

* 802.1Q
* lan
* switch

## Refernces

[1] https://www.geeksforgeeks.org/virtual-lan-vlan/