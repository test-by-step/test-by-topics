# Code Signing

Code signing is the process used by a development team or vendor to digitally sign an executable binary or a packged/bundled peice of code or software, verifying that it is the unaltered version of the software as published by the trusted vendor.

Code signing provides Integrity verification for code packages.

Code signing is highly related to digital signatures.

Code signing uses a cryptographic hash of the software bundle or binary to generate a signature.

Once a signature is verified, the verifier can be reasonably certain that the package is uncorrupted or unaltered from its published/released state. 

Security of code signing relies on the security of the signing keys. It is susceptible to all the benefits and caveats of other public-key infrastructure systems. 

Verifying the code signature requires that the public key used to verify the signature is also trusted. It is possible to achieve this through an centralized system, such as using signed certificates (such as X.509), by verifying public keys signed by a trusted party (such as may be done with PGP / GPG) or by distributing the key through a trusted distribution source (copied from a known-trusted HTTPS domain may be an option).

Trust on first use is another trust model in which the first time the key is encountered and accepted by the user, the fingerprint is registered and used to validate future releases of the same software.

## Extended Validation (EV)

Extended Validation (EV) code signing subjects code signing certificates to additional security and technical requirements. Generally this means that the private keys are completely isolated in a compliant hardware security module (HSM) through its entire lifespan, from generation, use, and storage.

## References

[1] https://en.wikipedia.org/wiki/Code_signing