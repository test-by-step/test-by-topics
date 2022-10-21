# Jump Box

Jump boxes are security hardened devices that are provisioned with the specific purpose of being the only device that has access to devices, services, and appliances on a secured subnet or security zone.

The jump box, then, is the only device that bridges an untrusted and trusted/secured network area.

By definition, it should be the only device connected to the security zone that has an interface connecting to another network.

Jump boxes will be preferred over firewalls or routers for cases when an operating system is required, such as to run some specialized system tools or appliances that interact directly with the security zone.

A jump box may be used connect between an IT network and a configuration subnet/VLAN; the jump box in this case is the only system with access to the configuration interfaces on a security zone. The jump box can then be shut down when not in use, and/or in order to configure the devices in the configuration zone, administrators need to log in to the jump box.

Jump boxes are a convenient security feature as it allows administrators to both reduce attack surfaces and apply principles of least privilege. With a jump box, only one device needs to be significantly hardened, and no other devices need to be given permissions to access services the security zone. 

In some special cases, the jump box may be able to be shut down when it is not needed and started or provisioned only when some changes need to be made, greatly reducing the attack surface over time. 

## References

[1] https://www.techrepublic.com/article/jump-boxes-vs-firewalls/
[2] https://www.csoonline.com/article/2612700/security-jump-boxes-improve-security-if-you-set-them-up-right.html
[3] https://en.wikipedia.org/wiki/Jump_server