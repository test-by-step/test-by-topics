# Wireless Networks

Wireless networks are networks which communicate using radio frequencies to pass network traffic.

The most popular wireless network method is Wi-Fi (IEEE 802.11), however there are many other popular wireless network protocols such as WiMAX, IEEE 802.15.4 and Zigbee, Bluetooth, Z-Wave.

Wireless networks are both a great enabler of networking, as wireless devices can be easily configured and deployed, but also a security risk.

Wireless networks allow a larger number of devices to be quickly deployed in arbitrary configurations without the need for complex and expensive wiring. Wireless networks greatly reduce costs, but also greatly increase attack surface area by exposing network traffic to the airwaves.

## Wirelass Personal Area Network (PAN)

Personal Area Networks are limited to the immediate surroundings of the radio and are used for connecting power constrained devices such as wearable smartwatches to more powerful devices.

Typically these networks use protocols such as IEEE 802.15.4, Zigbee, or Bluetooth.

## Wireless Local Area Network (LAN)

Wireless Local Area Networks function the same as a wired LAN, and is typically implemented using Wi-Fi (802.11).

## Cellular Networks

Cellular networks provide wide geographic coverage for mobile phones and can provide voice, text, and data services to endpoint devices.

## Site Surveys

Wireless site surveys are often conducted in order to establish the optimal placement of wireless transceivers such as Wi-Fi access points, to maximize the signal coverage for the smallest amount of hardware and resources.

Site Surveys are also important for ensuring signal does not leak outside of the protected area - signal should be contained within the organizational campus.

Site surveys may also look for malicious access points such as evil twins or other rogue access points that are not authorized on the network or campus.

## Wireless Security

Wireless security can be difficult, because the signal is broadly available to any observing device in range.

Wi-Fi has gone through several security implementations, including: WEP, WPA1-3, and WPS.

### Wired Equivalent Privacy (WEP)

Wired Equivalent Privacy was an early attempt at wireless security for Wi-Fi connections. It is considered insecure and should not be used.

WEP uses the RC4 stream cipher encryption algorithm and a 40 bit key with a 24 bit initialization vector (for 64 total bits).

The 24 bit initialization vector was not long enough to ensure that a unique key would be used on every network transaction for a busy network, and therefor the RC4 algorithm could be cracked with sufficient traffic observed.

Wireless Protected Setup (WPS) allows a router to automatically configure a new connection to an endpoint device by pressing a physical button on the wireless router or access point. Avoid using this feature.

### Wi-Fi Protected Access (WPA)

Wi-Fi Protected Access (WPA) was the next iteration of security for wireless connections.

The most current version of WPA is WPA3 and is the most secure.

WPA1's Temporal Key Integrity Protocol (WPA-TKIP) is susceptible to packet spoofing and injection and can be considered generally insecure.

WPA2 and 3 use Counter Mode Cipher Block Chaining (CCMP) with the AES encryption algorithm which is more secure than WEP or WPA-TKIP.

WPA uses the SHA hash algorithm to generate hash-based message authentication codes (HMAC) in order to verify integrity of the frames.

#### WPA3

WPA3 improves WPA2 by providing perfect forward secrecy, in which compromise of single transmission will not compromise any other transaction.

WPA3 uses Simultaneous Authentication of Equals (SAE) to mutually authenticate Access Point and endpoint, replacing the direct use of the pre-shared key (PSK, or password).

WPA3 uses CCMP-256 (256 bit key, 192 bit effective protection) for enterprise mode and CCMP-128 for personal mode.

#### WPA-Personal or WPA-PSK

WPA personal is most often used for home use, or for small office use (such as coffee shops, libraries, etc).

Uses a pre-shared key (PSK) or password to derive the transmission encryption key.

#### WPA-Enterprise

WPA-Enterprise uses IEEE 802.1x and the Extensible Authentication Protocol (EAP) to authenticate wireless access.

WPA-Enterprise can use any manner of RADIUS, TACACS, or other 802.1x authentication mechanisms to authenticate access to the network.

### Rogue Access Points / Evil Twin

A rogue access point is an unauthorized wireless access point operating in or around the organizational campus. 

Rogue APs may pose as a legitimate access point by advertising on an innocuous, or fraudulant BSSID and convinces devices to connect to it instead of the secure network. This is often operated as an Evil Twin, when pretending to be a legitimate business AP, but is actually a malicious clone.

Rogue APs may also be generally non-malicous devices that trusted insiders set up either ignorantly or as a means to circumvent other network restrictions such as social media blocks, violating company policy.

### Signal Leakage and DLP

Wireless signals can leak outside of the organizational campus boundaries making them more difficult to protect.

Good shielding on the exterior of buildings can prevent signals from leaking outside of the organizational boundary.

### Wireless Intrusion Detection Ssytems (WIDS)

Wireless Intrusion Detection Systems (WIDS) and WIPS are network devices which specifically monitor wireless traffic, otherwise performing many of the same functions of other IDPS appliances.

WIDS and WIPS will be configured and capable of watching for wireless specific attacks such as rogue access points, de-authentication attacks, and jamming.

## Internet of Things

Low-frequency, low-power signals are popular for many internet-of-things devices that only need to communicate at a low-bandwidth/data rate and do not want to interfere with other wireless signals.

Zigbee and Z-wave are a popular choice for sensors, lightbulbs, and switches. 

Many Internet of Things appliances will still use Wi-Fi for its ease of use, configuration, and high data rates.

Internet of Things devices connected over Wi-Fi in particular represent a large attack surface area for wireless network security, as their software is typically maintained by the vendor and not the user or corporate IT, making them black boxes for security.

## Wireless Sensor Networks

Many low-frequency, low-power signals are used in wireless sensor networks which operate in resource and power constrained environments. Many sensor networks use cheap devices that do not have encryption hardware and so do not have any inherent confidentiality or protection built in to their design.

## References

[1] https://en.wikipedia.org/wiki/Wired_Equivalent_Privacy
[2] https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access