# Mobile

Mobile devices are a concern for an organization's network and a key concept in deperimiterization.

Mobile devices are any device that is designed to be moved to and used in a remote location or away from a statick, controlled location, such as in the cases of: during field work, while traveling, remote work/work from home, or for business communications such as company enabled smartphones.

Organizations have to be concerned with how mobile devices are used within their networks, in some high security cases how they are used on their premesis, and also how they are allowed to connect to and access organizational resources while connected outside of the corporate network.

## Mobile device deployment methods

If an organization allows mobile devices to connect to resources on their intranet, they will typically choose between several broad arrangements for how to authorize which devices are permitted access.

### Bring Your Own Device (BYOD)

Bring Your Own Device allows or requires employees or members of the organization to use their own mobile devices to connect to intranet resources.

Bring Your Own Device (BYOD) is the cheapest option from the organiztions perspective. Organizations may often subsidize device purchases, cost of internet access, and/or cellular bill, but in any case the organization does not outright purchase equipment or services for each mobile connected user.

BYOD is generally considered the least secure arrangement, as the organization has much less fidelity over the policies installed on the device, and the user may use the device, unrestricted, for personal purposes that may incur a risk to the organization.

BYOD devices may also have inherently insecure or dated hardware and software that is vulnerable to attack if the user is allowed to use old devices or devices from compromisable vendors. If the underlying system itself is insecure, no policies can protect the device. 

Furthermore, if the device is lost or stolen, the organization may have no way of protecting or wiping any sensitive data that may have been loaded on the device.

### Company Owned Business Only (COBO)

Company Owned Business Only devices are devices which are purchased, configured, managed, and maintained by the company/organizations which are used exclusively for business functions.

COBO is the most secure arrangement for mobile device deployment as the company exercises full control over device configuration, management, security policies, and can fully restrict what the user is able to install or access on the internet that can be enforced through Mobile Device Management.

Users are generally not permitted or able, via policies pre-configured or configured via MDM on the device, to perform actions that could compromise the device or leak data.

COBO is the most expensive deployment model to maintain as the device as well as any required cellular access bills are paid for by the organization.

### Company Owned Personally Enabled (COPE)

Company Owned Personally Enabled Devices are devices which are purchased, configured, managed, and maintained by the company/organization, but which the user who is issued the device is allowed to use for personal purposes.

COPE is significantly more secure than BYOD, as the company is able to initially configure security policies that may be enforced through Mobile Device Management (MDM).

COPE may still be less secure than COBO as the user is allowed personal use of the device, which may lead to accidental data leaks, or for otherwise insecure actions that compromise the device. 

COPE is also more expensive for the organization (though likely equally as expensive as COBO) as the device is purchased and maintained by the organization; in the case of smartphones and cell phones, they will also typically cover the cellular service/data bill.

### Choose Your Own Device (CYOD)

CYOD is similar to BYOD, except that the organization allows the user to select from a cleared list of pre-screened and secure devices that are permitted. The organization will typically subsidize this purchase.

CYOD is more secure than BYOD because it provides addtional guarantees that at least the hardware and software are sufficiently secure and from a trusted vendor.

CYOD otherwise suffers many of the same drawbacks as BYOD, where the company does not have explicit control over all aspects of the device after purchase, as the device is maintained by the user for personal use as well.

CYOD is still cheaper than COBO and COPE.

## Mobile Security

### Mobility Managed Services

Mobility Manged Services (MMS) is a commercial service by some device vendors or third party provisioning companies in which the process of pre-configuring a device is automated on behalf of the company.

For example, a cellphone service company (for example, AT&T, Verizon, Telekom, Vodafone), in partnership with a device manufacturer (Apple, Samsung, e.g.) provides a service where devices sold to a company are registered by serial number, IMEI, or other at the time of sale.

Upon the first boot of one of these devices, it connects to a server hosted by the device vendor which automatically identifies the device as belonging to the organization and begins downloading the organizations security policies directly and requires the device to be authorized for the end user, before permitting the devices use.

This has the added benefit of preventing the devices general use by unauthorized parties if it has been lost or stolen.

### Mobile Device Management (MDM)

Mobile Device Management is an application that runs on mobile devices, it can be part of the operating itself but often is provided by a third-party application, which enforces security policies specified by the organization for its use for corporate/organizational business.

MDM is a key enabler for **scalability** with regards to mobile devices and large organizations. MDM is essential for securing large numbers of mobile devices for large organizations, where the individual management of devices would be prohibitive.

MDM can automatically install and configure required applications, apply security policies and restrictions, configure certificates and VPNs, configuring and enforcing device encryption and compartmentalization, and many more security features.

Policies and configurations for MDM enabled devices can be delivered and downloaded 'over-the-air' such that the device can be configured remotely or without direct IT intervention. Policies can also be updated dynamically, after initial configuration.

MDM is the most common broad-scope security concept to be related to mobile devices.

MDM can be used to track inventory both by logging activity and physically tracking using GPS/location services, and can be used to configure a device to remotely wipe aall data if it is lost or stolen.

MDM is related to NAC and serve similar functions, however NAC does not inherently enforce device policies, it restricts network access based on evaluated adherence to policies. MDM fully enforces defined policies.

### Compartmentalization

Compartmentalization is an important mobile device security aspect in which business data, apps, and traffic is logically isolated and secured from personal or non-business functions on a mobile device.

Data and apps are kept separately encrypted with a separate key, and applications are not permitted to communicate between one compartment and another.

Generally, this is often provded through a third party app or service such as Blackberry.

This compartmentalization may allow personally enabled devices to switch seamlessly between business and personal mode, without any action between the two systems.

It also allows for greater protection for the organizations protected data if there is some compromise or malicious application on the personal side.

### Encryption

Mobile device encryption is extremely important, bordering on mandatory for business devices. Encyryption is essential to prevent sensitive data from being accessed on the device if it is lost or stolen.

Most mobile operating systems allow full-drive encryption and in some cases are enabled with some level or hardware security modules that protect device encryption keys.

Encryption is also important for security network activity, and MDM may enforce VPN connections while disconnected from corporate networks.

### Data Wipe

When a device leaves the ownership of any one user, all of the data should be completely wiped.

This means a complete data wipe and factory reset if a company owned device is transfered to a new user, and also means remote wipe if the device is lost or stolen.

If a device is lost or stolen and cannot be recovered, the should be configured to be able to be wiped remotely by the organizations IT services to protect sensitive data and prevent the devices use by anyone who finds it.

Data wipe signals may be defeated by advanced threats who put the device in special radio frequency blocking containers or Farraday cages.

### Geofencing

Geofencing is the blocking of actions based on geographic location.

Geographic location on mobile devices is provided primarily by an advanced algorithm that tracks Wi-Fi signals and Wi-Fi Basic Service Set IDs (BSSIDs), but is also supported by GPS.

Geofencing may prohibit certain actions outside of a certain geographic region, or only permit certain actions inside of a geographic region.

A simple example of geofencing is in commercial drones, whose firmware is often included with code that prevents a drone from taking off in, or flying into, protected (by law or custom) air-zones such as around airfields, government sites, and power facilities. 

It is possible to spoof location information, but typically requires an advanced attacker.

## Key Ideas



## Related Ideas

* mdm

## References

[1] https://en.wikipedia.org/wiki/Mobile_device_management
[2] https://en.wikipedia.org/wiki/Geo-fence