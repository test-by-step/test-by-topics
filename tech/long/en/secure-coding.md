# Secure Coding Standards

Secure Coding Standards are principles, procedures, and expectations that a development team is expected to follow and regularly asses when developing an application. Secure Coding Standards helps to ensure that the application under devlopment is protected against common or severe flaws that expose the application to attack.

Secure Coding Standards are related to the principle of Secure By Design.

Security coding standards require that the security requirements of the application be considered and planned for up front and incorporated into every step of the software development life cycle.

Secure Coding Standards cannot protect an application that has a flaw in its design. That is, even with perfect implementation and otherwise secure code, if the design contains a security flaw, the application will be insecure.

Secure Coding Standards are closely related to the Software Development Lifecycle.

Common standards to consider:

* Routines should fail securely
* Critical and sensitive functions should be handled server side
* Use standard routines and libraries where possible
* Deny by default wherever possible

## OWASP Secure Coding Guidelines

The Open Web Application Security Project maintains a list of 10 secure coding guidelines.

### Input Validation

* All data validation should happen on the server side, on a trusted server.
* Data validation should be handled by a centralized routine.
* Check proper character sets
* Check data length
* Check data range
* Use a 'white-list' of characters whenever possible; that is deny all characters that aren't explicitly permitted.
* Check for null bytes, new lines, and '../' (including encoded versions like %c0%ae%c0%ae/)

### Output Encoding

* Encode the output on the server side
* Use standard libraries or routines
* Sanitize all data for output to database queries like SQL
* Sanitize all data for output to system commands
* Sanitize all data for output back to clients that originate outside of a trusted source; for example, HTML entity encoding

### Authentication and Password Management

* Require authentication for all pages, unless the page is explicitly intended for public consumption
* Authentication controls must be enforced on the server side
* Use standard libraries or routines
* Use centralized routines for authentication
* Authentication should fail securely
* If using passwords, only store strong, salted, one-way hashes
* Password store should be writable by the application only
* Validate authentication only on input completion
* Authentication responses should not indicate which auth factor was incorrect
* Source code is NOT a secure location
* Use only POST requests to transmit auth data and encrypt connection (HTTPS e.g.)
* Enforce secure password policies if using passwords
* Use multi-factor authentication where possible
* Change all default passwords or disable accounts

### Session Management

* Manage the session only on the server
* Do not include session identifiers in URLs
* Session identifiers should exist only in cookie headers
* Logout should fully terminate session
* Use strong per-session random tokens as identifiers
* Set cookies with HTTP only attribute

### Access Control

* Use only server side objects for making access control decisions
* Check access control using a centralized routine
* Access control should fail securely
* Enforce access control on every request, including server side requests
* Segregate privileged logic from other application logic
* Restrict access to urls, functions, objects, data, etc. to only authorized users by default
* Limit the number of transactions a single user can perform per time period
* Support account disabling and session termination

### Cryptographic Practices

* Apply cryptography only on the server side
* Protect master secrets
* Source code is not a secure location
* Cryptographic routines should fail securely
* Random numbers should be generated with an approved Cryptographic Random Number Generator

### Error Handling and Logging

* Do not disclose sensitive information in error responses
* Do not display debugging information
* Free allocated memory when errors occur
* Implement generic error messages as a default error response
* Ensure untrusted log data will not execute code in a log viewer
* Do not store unecessary details in logs, including sensitive system information
* Error handling logic for security controls should deny by default

###  Data Protection

* Implement least-privilege
* Grant only sufficent access to data in order for user or system to perform its task
* Protect cached sensitive data
* Encrypt sensitive data even on the server side
* Don't store passwords or authenticating data in clear text
* Do not include sensitive information in GET requests / URL parameters
* Disable client side cachine on pages with sensitive information

### Communication Security

* Encrypt all transmissions of sensitive information, including authentication information
* Failed TLS connections should not fail back to a less secure connection
* Specify character encoding for all connections
* Filter sensitive information from HTTP referer

### System Configuration

* Ensure all systems are running latest approved version
* Ensure all systems have up to date patches
* Fail securely when exceptions occur
* Disable unnecessary HTTP methods
* Remove unnecessary information from HTTP headers (OS version, server version, etc.)
* Implement a change control and management system

### Database Security

* Use parameterized queries (queries that distinguish between code input and data input)
* Use input validation on both query input and output
* Use least privilege
* Do not use hard coded connection strings; store connection strings on a separate, secured configuration file
* Close connection as soon as possible
* Application should have distinct credentials for different levels of access (e.g. read-only, guest, admin)

### File Management

* Require authentication before uplaod
* Limit types of files that can be uploaded
* Check file headers and validate file
* Turn of execution privileges of upload folder
* Do not pass directory paths, index a pre defined path list
* Do not send absolute paths to clients
* Set application files and resources to read only
* Scan for viruses and malware

### Memory Management

* Double check buffer sizes
* Check buffer boundaries and input lengths before copying
* Truncate input strings to a reasonable length
* Specifically close resources; don't rely on garbage collection
* Use non-executeable stacks
* Avoid vulnerable functions (printf, strcat, strcpy)
* Free allocated memory upon use completion

### General

* Use (and/or reuse) tested and approved code rather than creating new code where possible
* Use mutexes and locking to prevent race conditions
* Review all secondary applications and third party code

## References

[1] https://owasp.org/www-pdf-archive/OWASP_SCP_Quick_Reference_Guide_v2.pdf