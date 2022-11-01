# Secure Design Patterns

Secure design patterns incorporate software and system security into the development process from the beginning of the development lifecycle through a rigorous planning process and the implementation of best practices and procedures.

Secure Design Patterns is closely associated with Secure by Design principles.

Security in application development should be planned for from the beginning and implemented at every stage of software development.

Secure Design Patterns is closely associated with the Software Development Lifecycle (SDLC).

Open Web Application Security Project (OWASP) Secure Design Patterns:

* Remove logging output 
* Validate Inputs
* Clear sensitive information
* Handle exceptions (don't pass, wrap and sanitize)

Additional

* Know and use tested libraries
* Consistent use of coding standards
* Develop unit test cases
* Perform code reviews
* Security training for developers

## Secure Coding Practices

OWASP Top 10 secure coding practices

1. Minimize Attack Surface
1. Establish Secure Defaults
1. Principle of Least Privilege
1. Principle of Defense in Depth
1. Fail Securely
1. Don’t Trust Services
1. Separation of Duties
1. Keep Security Simple
1. Fix Security Issues Correctly

CERT Top 10 Secure Coding Practices

1. Validate Input
1. Heed Compiler Warnings
1. Architect and Design for Security Policies
1. Keep It Simple
1. Default Deny
1. Least Privilege
1. Sanitize Data
1. Defense In-Depth
1. Effective Quality Assurance
1. Secure Coding Standard


## OWASP Top 10

OWASP Top 10 are the top 10 most common and/or dangerous vulnerabilities in web applications:

1. A01:2021-Broken Access Control
1. A02:2021-Cryptographic Failures - This category often leads to sensitive data exposure or system compromise.
1. A03:2021-Injection (including cross site scripting)
1. A04:2021-Insecure Design - An insecure design cannot be fixed by a perfect implementation as by definition, needed security controls were never created to defend against specific attacks.
1. A05:2021-Security Misconfiguration 
1. A06:2021-Vulnerable and Outdated Components
1. A07:2021-Identification and Authentication Failures
1. A08:2021-Software and Data Integrity Failures
1. A09:2021-Security Logging and Monitoring Failures
1. A10:2021-Server-Side Request Forgery

## References

[1] http://www.owasp.org/index.php/Secure_Coding_Principles

[2] https://www.securecoding.cert.org/confluence/display/seccode/Top+10+Secure+Coding+Practices

[3] https://owasp.org/Top10/

[4] https://owasp.org/www-pdf-archive/Secure_Application_Development.pdf