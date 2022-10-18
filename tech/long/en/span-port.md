# Switch Port Analyzer (SPAN) port

Span ports copy ethernet frames from multiple or all switched interfaces onto a single, isolated interface. All the frames are aggregated into a single stream that can be connected to a network monitor and/or intrusion detection/prevention system. 

Span ports will copy all traffic from specified interfaces to the isolated segment, aggregating traffic even across logical segments (VLANs) that typically cannot cross paths.

Span ports are generally synonymous with port mirroring, with the term SPAN being generally more closely associated with Cisco, though the term has entered common vernacular.

Span ports behave in a generally uni-directional manner, meaning that there is no direct response traffic as the copied frames are recorded and analyzed on the span port, but the original frames proceed unobstructed along their original intended path for processing and response.

Span ports are almost always associated with switches (physical OR virtual) and layer two (data link) traffic. Their operation requires switching and so are not considered related to bridges or hubs, which would be more closely associated with Network taps.

Span ports are also commonly associated with IDS systems which passively observe traffic and retroactively analyze network behaviors to generate alerts. For this, they need to be able to see all traffic on the network, even traffic that would typically be logically segmented with VLANs so as to be non-visible to the logically isolated network segments.

Span ports may be associated with IPS systems but the relationship is more complex and case-by-case specific.

Remote span ports are possible, using either 802.1Q and VLAN trunking over layer 2 (data link), or using layer 3 (network) by creating an IP tunnel to a remote destination (only on layer 3 switches). 

## References

[1] https://www.geeksforgeeks.org/switch-port-analyzer-span/