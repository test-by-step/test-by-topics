# Segmentation

Segmentation is the concept of dividing networks into generally isolated, protected subnets and systems that are not able to interact or be accessed unless explicitly permitted to do so.

Segments generally expect a zero-trust model between segments. This means that traffic and services have to be explictly configured to be permitted, or even routed, between segments.

Segmentation also improves performance by limiting the scope and propogation of broadcast packets, reducing network load as a whole.

## Segmenting

Several techniques can be used to segment networks and systems at various levels of the OSI model.

### Physical Segmentation

Switches and routers are physical devices that provide some Physical Laye (layer 1) segmentation through physical wiring.

### Logical Segmentation

VLANs segment Local Area Networks at the Data Link Layer (Layer 2).

Subnets segment LANs at the network layer (layer 3), usually via IP subnetting.

Firewalls and Next Generation Firewalls are capable of segmenting networks all the way up through the application (7) layer.