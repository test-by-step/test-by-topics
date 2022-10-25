# Directory Services

Directory Services are databases which are used to store, describe, and manage information on network resources and entities such as users, computers, printers, network volumes, groups.

Directory Services are most often associated with LDAP and Active Directory, but many other service providers implement Directory Services as well.

The **X.500** specification is the most common format for access directory services.

**LDAP**, based on the X.500 specification, is the most often used protocol to access directory services information over TCP/IP.

LDAP operates on port 389 for unencrypted connections, and port 636 for encrypted connections over TLS (LDAPS).

The Domain Name System (DNS) is considered to be a directory service.

Directory Services is often used in conjunction with identity and access management (IAM), identity federation, single sign-on, and device and account management.

## Common Directory Service entities

### Accounts

A user network account may be specified in domain services which can describe such things as: 

* the users unit within the organization
* the identity associated with the account
* groups or roles the user belongs to
* custom permissions granted to the user
* group or user policies associated with the account
* scripts to run on login
* multi-factor authentication information and policies
* password policies
* other logon policies (such as smart card)

Administrative accounts can also be specified within the directory service but should always be distinct from user accounts, and should have by default no permissions. Administrative access, or even standard access, is only granted to resources the account is provisioned with the purpose of managing. 

### Computers

A computer may be specified in the directory service which can describe:

* organization and unit the device belongs to
* device and group policies the device must have configured
* VLAN the device should be assigned to
* IP address associated with the device
* device encryption information (for recovering an encryption key from escrow)

### Printers

Shared printers are often listed in directory services that can be easily configured for access by users or computers.

### Groups

Groups can be defined in the directory services which can be associated with such things as:

* Policies to adjust for members of the group
* Permissions to apply for members of the gorup
* Volume mapping for members

## References

[1] https://en.wikipedia.org/wiki/Directory_service