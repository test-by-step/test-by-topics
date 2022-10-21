# Network Tap

A network tap is an interface or physical connection to an existing network link that allows the tap to view all the network traffic along that link without interrupting its flow.

Classicly, taps were attached shared network buses such as coaxial cables, and every device interface connected to the bus via a tap had to contend for bandwidth on the shared bus.

Network taps in a modern context function in the same conceptual way, though may be implemented on different physical mediums such as twisted pair links or virtualized in a VPC.

Network taps are typically distinct from span ports or port mirroring in that taps do not involve any packet switching or dynamic copying of packets onto a specific port but rather observes all of the traffic as it moves organically over a link.

Conceptually, a network tap attaches to a link rather than an interface (as it interacts with the link as if it were a shared medium) and spies on all of the traffic across that link. 

A network tap can be used to passively pass on data from the link to network monitoring devices or Intrusion Detection Systems.

## Related Ideas

Simple layer two devices like hubs may be related to network taps as all traffic is reflected onto every interface blindly.

Network taps may also be related to coax ethernet connections, as taps are how new devices could join the shared bus.

## References

