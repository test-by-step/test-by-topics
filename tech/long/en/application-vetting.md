# Application Vetting Process

An application vetting process rigorously investigates, assesses, and tests an application before it is released or deployed into a production environment.

The application vetting process ensures that an application meets the organizations security requirements and accepts the application for integration or deployment or rejects the application.

Organizations should have an application vetting process in place, ideally a formal, documented process, that vetts and verifies each application before deploying to the organization. 

In order for an application to be vetted, the organization must first identify the application security requirements, as well as the app and version that is to be vetted.

If an application is rejected, it may sometimes be allowed to be resubmitted for testing after remediating the flaws.

## White vs Blacklisting

Whitelisting is an organizational policy in which applications are NOT permitted by default unless explicitly accepted.

Blacklisting is an organizational policy in which applications are permitted by default unless explicitly rejected or denied.

The most secure option is whitelisting.

## Testing

Testing may include an automated tool that checks requirements in a consistent and rigorous manner.

Application may be fuzz tested to validate input handling.

Application may be subject to static code review.

A dynamic test tool may check the run time behavior of the app.

A static test tool may attempt to decode and analyze the app binary.

The test should run the application in a sandbox in order to observe its behavior.

### Correctness Testing

Correctness testing verifies the application produces proper outputs given set inputs and detects errors.

Correctness testing can use an automated tool such as a fuzzer or unit tests.

### Source and Binary Code Testing

Source and binary testing analyzes the source code and binary instructions for non-compliant patterns or security flaws.

Source and binary code testing are often static.

### Static Testing

Static tests observe components of the application without running the application. Static tests can look at the source code for flaws, errors, or bad practices. Static tests can also look at the application binary for flawed or insecure execution paradigms.

### Dynamic Testing

Dynamic tests are conducted when the application is running. Dynamic tests may observe inputs and outputs of the application, what is loaded into memory by the application, where and how the application jumps in its instructions.

## Phases of a vetting process

1. Intake: Possible applications are submitted or considered for use
1. Testing: Applications are tested against the security standards
1. Approval/Rejection: The application is accepted or rejected based on its test results
    * Additional Requirements may be added
    * Recommendations may be made
    * Application may be resubmitted to testing after remediation
1. Results: Approval or rejection is documented 


## References

[1] https://csrc.nist.gov/glossary/term/App_Vetting_Process

[2] https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-163r1.pdf