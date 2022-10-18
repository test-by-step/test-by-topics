# Domain Name System Security

DNSSEC protects against DNS cache poisoning and forged or manipulated DNS data.

DNSSEC protected answers are signed with a digital signature, while the payload remains unencrypted. The DNS resolver is responsible for verifying the certificate and signature is valid. 

The digital signature is used to verify the DNS answer is unmodified.

Multiple new record types were created to support and/or enable DNSSEC including records to specify signing algorithms, public keys, and secure record identification.

## Key ideas

For DNSSEC DNS resolvers must have a 'Trusted Anchor,' atleast one known and trusted public key or delegated signer. These are likely included with the operating system or deployed from a trusted source.

## Pitfalls

* DNSSEC does NOT provide confidentiality or availability. DNSSEC only provides integrity, and that the record is authentic.

## Related Ideas

* Digital signatures
* PKI

## Reference

[1] https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions