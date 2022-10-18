# Intrusion Detection Systems

Intrusion detection systems passively monitor networks or systems for intrusion or malicious behavior then logs, notifies, and/or reports activity.

Intrusion detection systems have several variations with different applications:
1. Network Intrusion Detection Systems (NIDS)
1. Host-based Intrusion Detection Systems (HIDS)
1. Wireless Intrusion Detection Systems (WIDS)

Intrusion Detection Systems are generally NOT placed inline but often attach via a span port or tap to a network segment (for NIDS) to passively monitor network traffic without disrupting its flow through the network.

IDSs are useful for:
* Incident response
* Alerting key personnel to active threats
* Forensics, post-mortem, and AAR for 
* Threat hunting
* Logging activity

## Algorithms

### Anomoly-based 

Anomoly-based detection algorithms must first be trained by observing a sufficient amount of known good activity and watches for activity that diverges significantly from the expected baseline.

Good for detecting novel attacks.

### Behavior-based

Behavior based detection algorithms monitors for activity that exhibits actions that may be indicative of an intrusive behavior and then looks backwards to activity that may correspond to an intrusion.

Behavior based is detection is generally retrospective: that is, the attack has already occured. 

Behavior-based detection may often detect the clean-up/obfuscation of an intrusion permitting a retrospective assessment of behaviors.

Behavior-based detection is good for detecting novel intrusion mechanisms.

### Signature-based

Signature-based detection algorithms rely on a known set of activities that forms a common pattern or signature that indicates an intrusion or attack.

Signature based detection algorithms requires a pre-downloaded and loaded set of signatures and rules in order to effectively identify intrusions.

Signature-based detection does not detect new or nevel intrusion methods.

## Key metrics

Key metric terms to associate with IDSs are:

* False Positives - an alert or trigger was incorrectly tripped indicating an intrusion event that was actually legitimate activity
* False Negatives - an alert or trigger was NOT tripped despite an intrusion event occuring
* True Positives - an alert or trigger is correctly tripped indicating an intrusion even that WAS occuring
* True Negatives - an alert or trigger is not tripped and no intrusion is occuring

Acronyms to associate with IDS metrics can include: FPR (false positive rate), FNR (false negative rate), TPR (true positive rate), TNR (true negative rate).

Also FP, FN, TP, TN

FRR and FAR are generally NOT associated with IDS - these terms are more often used in access control and authentication such as biometric authentication methods.

## Network Intrusion Detection Systems

NIDS are implemented as a service in the network (real or virtual) and can be implemented on a stand-alone device, VM, or application. Generally, NIDS are connected to a network segment tap or span port so that traffic can be monitored without disrupting network traffic or adding additional hops or latency in the topology.

## Host-based Intrusion Detection Systems

HIDS are applications installed on end-user devices that monitor activity on user accounts, systems, and operating systems. HIDS can have a wide array of implementations and purposes.

Some features that HIDS may include:
* File Integrity Monitoring (FIM)
* Log system and user activity
* Block external media connections (block USB)
* Track critical services or detect rogue/malicous services
* Report logs to central server or SIEM

Generally, HIDS will NOT be referred to as virus scanners or anti-malware, though it is not impossible that a HIDS solution vender may offer all services in a single package.

It is possible for HIDS to be referenced related to NAC (network access control) as a HIDS solution may participate as an agent, though the concepts are not synonymous.

## Wireless Intrusion Detection Systems

Wireless Intrusion Detection Systems work like NIDS except that they monitor wireless connections. 

WIDS may additionally look for attacks against the wireless protocols in particular, for example deauthentication attacks, downgrade attacks, rogue access points, or unauthorized devices (MAC addresses, e.g.).

Wireless systems have additional challenges since individual connections (in newer wireless standards) are encrypted individually making passive scanning of packets difficult or impractical.

## Advantages

NIDS do not interfere with network activity, preserving latency. That is, the real-time network activity performance is not reduced.

## Limitations and Pitfalls

IDS applications cannot intervene in an intrusion nor prevent malcious activity. It will only log, notify, and/or report.

Generally IDS solutions do not correlate events - a SIEM solution is typically required for correlation.

Firewalls and IDS are generally considered distinct when constructed into test questions. They are unlikely to be conflated.

## Related ideas

* Passive: IDSs do not intervene in network activity, even if an intrusion is detected
* Span port: Span ports are often related to network intrusion detection as they are used to copy all network traffic on switch ports to a single interface for routing to an IDS interface.
* SIEM: An IDS will often report its significant logs to a SIEM which (the SIEM) is used for correlation of events and incidents.

## Keywords

passive, span port, detection, tap, nac, network access control

## References

[1] https://cybersecurity.att.com/solutions/host-intrusion-detection-system
[2] https://stackoverflow.com/questions/9228383/difference-between-anomaly-detection-and-behaviour-detection
[3] https://www.geeksforgeeks.org/intrusion-detection-system-ids/