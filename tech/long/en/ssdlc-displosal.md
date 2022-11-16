# Disposal and Reuse (SSDLC)

When a secure software Secure software comes to end of life, or when a software is to be reused in other contexts, protected artifacts need to be sanitized and properly disposed of.

Cryptographic keys must be securely destroyed.

Secret or protected data must be securely destroyed; the requirements for safe destruction of data may be governed by policy, industry standards / comliance requirements, or regulation.

Regulation may also require the retention of some key data, which has to be protected and securely stored rather than expunged.

Access keys and authentication or identity credentials must be securely cleared and sanitized.

Reuse Existing, Well-Secured Software When Feasible may be preferred to Duplicating Functionality. 

Reuse of secure assets lowers the costs of software development, expedite software development, and decrease the likelihood of introducing additional security vulnerabilities into the software by reusing software modules and services that have already had their security posture checked. 

This is particularly important for software that implements security functionality, such as cryptographic modules and protocols.

When software is reused across trust domains or between distinct entities or departments, sanitization still needs to occur to protect data, keys, and credentials.

## References

[1] https://csrc.nist.gov/publications/detail/sp/800-218/final

[2] https://defenselead.com/secure-sdlc-procedure/#ssdlcsanitizationdisposal