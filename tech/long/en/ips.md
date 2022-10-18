# Intrusion Prevention Systems

Intrusion prevention systems actively monitor networks or systems for intrusion or malicious behavior then logs, notifies, and/or reports activity AND *can intervene* to interrupt or disrupt an active intrusion or attack.

IPS solutions can do everything that an IDS can do, with the addition of actively interact and mitigate an intrusion in real time.

A key understanding in IPSs vs. IDSs is that a false positive for IPS solutions will cause a disruption to legitimate activity, self imposing a Denial-of-Service (DOS).

Intrusion prevention systems have several variations with different applications:
1. Network Intrusion Prevention Systems (NIPS)
1. Host-based Intrusion Prevention Systems (HIPS)
1. Wireless Intrusion Prevention Systems (WIPS)

Intrusion Prevention Systems are generally placed inline with the traffic flow to actively monitor that network traffic which may disrupt its flow through the network.

IPSs are useful for:
* Mitigation
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

Key metric terms to associate with IPSs are:

* False Positives - an alert or trigger was incorrectly tripped indicating an intrusion event that was actually legitimate activity
* False Negatives - an alert or trigger was NOT tripped despite an intrusion event occuring
* True Positives - an alert or trigger is correctly tripped indicating an intrusion even that WAS occuring
* True Negatives - an alert or trigger is not tripped and no intrusion is occuring

Acronyms to associate with IPS metrics can include: FPR (false positive rate), FNR (false negative rate), TPR (true positive rate), TNR (true negative rate).

Also FP, FN, TP, TN

FRR and FAR are generally NOT associated with IDS - these terms are more often used in access control and authentication such as biometric authentication methods.

## Network Intrusion Prevention Systems

NIPS are implemented as a service in the network (real or virtual) and can be implemented on a stand-alone device, VM, or application. Generally, NIPS are connected directly to the network on-path so that traffic can be monitored and interacted with, which may add additional hops or latency in the topology.

## Host-based Intrusion Prevention Systems

HIPS are applications installed on end-user devices that monitor activity on user accounts, systems, and operating systems. HIPS can have a wide array of implementations and purposes.

Some features that HIDS may include:
* File Integrity Monitoring (FIM)
* Log system and user activity
* Block external media connections (block USB)
* Track critical services or detect rogue/malicous services
* Report logs to central server or SIEM
* Interrupt or block malicious connections
* Block compromising or intrusive system or user activity

Generally, HIPS will NOT be referred to as virus scanners or anti-malware, though it is not impossible that a HIPS solution vender may offer all services in a single package.

It is possible for HIPS to be referenced related to NAC (network access control) as a HIPS solution may participate as an agent, though the concepts are not synonymous.

## Wireless Intrusion Prevention Systems

Wireless Intrusion Prevention Systems work like NIPS except that they monitor wireless connections. 

WIPS may additionally look for attacks against the wireless protocols in particular, for example deauthentication attacks, downgrade attacks, rogue access points, or unauthorized devices (MAC addresses, e.g.).

Wireless systems have additional challenges since individual connections (in newer wireless standards) are encrypted individually making passive scanning of packets difficult or impractical.

Wireless Intrusion Prevention systems may use their own deauthentication attacks to interrupt malcious connections.

## Advantages

IPS can interfere with network activity, preventing an active attack without requiring manual administrative interaction.

## Limitations and Pitfalls

IPS inherently have a processing requirement, adding additional latency to even legitimate network traffic.

Generally IPS solutions do not correlate events - a SIEM solution is typically required for correlation.

Firewalls and IPS are generally considered distinct, though depending on firewall type they may appear similar function. When distinguishing context between the two, firewalls will typically rely on a set of simple pre-defined access rules based on routing information; IPSs will rely on complex rules at multiple levels of the OSI model. NGFW and and Layer 7 firewalls will typically be distinguished from IPSs as inspecting and filtering protocols and packet contents rather than behaviors, activity, or signatures.

## Related ideas

* Active: IPSs intervene in network activity if an intrusion is detected
* SIEM: An IDS will often report its significant logs to a SIEM which (the SIEM) is used for correlation of events and incidents.

## Keywords

active, prevent, nac, network access control

## References

[1] https://stackoverflow.com/questions/9228383/difference-between-anomaly-detection-and-behaviour-detection