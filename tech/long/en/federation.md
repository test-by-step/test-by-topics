# Identity Federation

Identity Federation, or Federation, allows for the sharing of authentication information between multiple domains, systems, applications, and/or environments which have been configured to trust an identity provider of one or more domains.

It is common for a federated identity to have multiple attributes stored across multiple identity systems which can be associated with authenticated identity information provided from a centralized identity provider.

Identity Federation is often closely associated with Single Sign On (SSO).

When two systems are federated, they agree to accept authenticating information, typically in the form of authentication tokens, from one or more federated systems' respective domains. 

Often, federation may involve delegating the authentication responsibility to a trusted third party, which all entities have agreed to trust. 

Within federated systems, there must be a system that authenticates identities, usually called an Identity Provider, and other systems that provide services, typically Service Providers.

Even after an Identity Provider has authenticated a user and provided a token, the token is not a guarantee of authorization to use a service. Service Providers must still verify that the authenticated user/entity has permissions and is authorized to use their service.

Federation is often seen in context with cloud service providers, and especially hybrid cloud or cloud-to-premises environments. Federated Identity allows a member of an organization or employee of a business to verify their identity with a centralized, organization-controlled server, receive a token attesting to their identity from the organization itself, which is then shared with the external service provide for access to that service.

Federation may also be used between organizations, where two organizations wish to share some IT or network resources between their users. Each organizations users can authenticate with their own organization, and the federated systems are configured to trust that identity. 

## Tokens

Tokens are a structured and digitally signed object which attests the to identity and authenticity of the token holder, and may also describe:
* duration of validity of token (expiration time)
* roles and/or permissions associated with the token
* administrative information related to the token holder
* usernames
* unique subject identifiers (sometimes referred to as 'sub') that identifies the unique entity (more specific than a username, closer to a randomly assigned serial number)

When using tokens, a trusted federated domain can sign the token using its private token signing key, which any system that has agreed to trust the federated domain can easily verify using the federated domain's public key. 

## References

[1] https://learn.microsoft.com/en-us/previous-versions/office/developer/sharepoint-2010/ee535902(v=office.14)
[2] https://en.wikipedia.org/wiki/Federated_identity