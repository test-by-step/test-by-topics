# Zero Trust Model

Zero Trust is a key concept with Deperimiterization which implies that no connection, device, or user is implicitly trustworth, and should treat each endpoint and connection as a potential threat.

With the Zero Trust model, all users, devices, and connections, as well as each action taken by those entities, is thoroughly authenticated, even those connections from inside the organizations firewall, as if it were form an open network before being permitted to proceed.

Even after a connection is established, it is still treated as a potential threat and all activity should be logged, scrutinized, and continuously authenticated.

Zero Trust for deperimiterization may be conceptually paired with agent-based NAC solutions as the NAC enforces certain endpoint policies such as end-to-end encryption and performs various system security verifications before a connection is authorized.

Zero Trust is also conceptually linked to strong authentication and concepts like multi-factor authentication to guarantee that the connecting entity is who or what it claims to be.

## Key Ideas

All internal resources, under a Zero Trust model, should be inaccessible by default.

Each action, request, or permission needs to be explicitly verified and permitted.

Assume a breach for every connection - proper segmentation and isolation is important.

All requests are strongly authenticated as if they came from an open network, regardless of if they originated from inside the firewall or not.

## References

[1] https://www.ibm.com/topics/zero-trust
[2] https://www.microsoft.com/en-us/security/business/zero-trust