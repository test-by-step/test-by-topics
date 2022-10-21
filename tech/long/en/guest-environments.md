# Guest Environments

Guest environments are a logical segmentation technique which are used to grant limited network and/or system access on the organizational network to untrusted or un-credentialed users or applications who have a legitimate use for network resources but who are not authorized access to other organizational resources.

Guest Environments (or sometimes guest sharing environments) are often used to permit limited access for business partners or contractors to organizational network resources. Guest Environments need to be properly segmented so that they do not have access to the larger organizational back end but only access to the minimum resources needed to accomplish the goals identified in the BPA, ISA, and/or SLA. In this case, access to the guest environment is very often granted by authorization through identity federation between organizations.

Guest environments can, in some cases, be used to grant limited network or desktop access to users that do not have a provisioned network account but have some legitimate use. Resources are granted temporarily and all session data is completely cleared after the session ends. Consider the example of a shared desktop in a hotel business room.

Guest Environments may occaisionally refer to the isolated system resouce space allocated by a hypervisor to a guest operating system with virtual machines.

Guest environments are largely logically isolated, given access to only a minimum standard set of resources and are not associated with internally provisioned organizational network accounts. 

## Related Ideas

* Identity Federation

## References

[1] https://learn.microsoft.com/en-us/microsoft-365/solutions/create-secure-guest-sharing-environment?view=o365-worldwide