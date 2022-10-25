# Cloud to on-premises

With hybrid cloud systems, in which business functions happen both on-premises, or on the corporate campus, and on cloud services, the link between the two disparate systems must be properly configured and secured.

Often, the crucial link between cloud and premises services involves authentication and verification of user identities and the actions they are authorized to make.

Access and interaction betwen cloud services and on-premises services should always take place over a secured connection, either HTTPS, SSH, or other secure protocols.

In many cases, it is also beneficial to require users to connect to the cloud based systems from within the corporate network, which can be accomplished for remote workers through the use of VPNs.

## Federated Identities

With hybrid cloud systems, user identities and authorizations must somehow be shared between the on-premises services and the cloud services.

Often identity and credential management can be a complex process, with user accounts and privileged managed independent from PKI (such as smart cards). Identity and credential management can happen on-premises, on the cloud, or both.

SAML (Security Assertions Markup Language) is the process typically used to communicate identity and authentication information between two collaborating systems. Each SAML exchange will include a token which either system can use to verify the authenticity of an entity and/or the authorization of that entity to perform an action.

### Federated Identity Security

If a SAML token is compromised, a malicious user can execute actions as if they were the user whose token was comprimised.

Worse, if the token signing key is compromised (at an organizational level) a malicious user can create fraudulant tokens and execute arbitrary actions on the cloud as any user.

## Securing Cloud to Premises

Administrative accounts and user accounts should be isolated from one another and, if possible, signed with separate token signing keys. 

It may be pertinent to ensure on-premises administrative accounts do not have administrative access to manage cloud services. (Cloud only accounts manage cloud services)

User accounts do not get administrative privileges.

Administrator accounts are independant accounts, provisioned and secured separately from primary user accounts.

Administrative accounts adhere to least-privelege principle, and get access to only the features they are authorized to configure (elevated or otherwise).

Use strong authentication and Multi-factor authentication to verify user identities.

## References

[1] https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/protect-m365-from-on-premises-attacks