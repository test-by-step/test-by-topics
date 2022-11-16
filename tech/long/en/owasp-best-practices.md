# OWASP Best Practices

The Open Web Application Security Project Publishes a list of best practices for secure coding standards.

The main categories addressed are:

* Input Validation
* Output Encoding
* Authentication and Password Management
* Session Management
* Access Control
* Cryptographic Practices
* Error Handling and Logging
* Data Protection
* Communication Security
* System Configuration
* Database Security
* File Management
* Memory Management
* General

Common to all categories:
* Fail securely (deny by default, do not report error details, do not expose credentials)
* Perform sensitive actions on the trusted system (server side)

## Input Validation

Input from users should be treated as un-trusted and stripped of any possibly harmful characters or structures.

Data length, range, and type of data should be checked to be within bounds.

Data validation failures should reject input by default.

Data should be validated on the server side, not client side.

## Output Encoding

Output should be encoded server side, not client side.

Sanitize untrusted outputs prior to passing to other processes (database query, e.g.).

Explicitly validate or encode all output characters.

## Authentication and Password Management

Require authentication to all resources not explicitly designated as public.

Authentication only performed server side, not client side.

Credentials should only be stored as cryptographically secure one way salted hash.

Keys should only be writable by the application.

Authentication credentials should not be stored in the source code (closed source or otherwise).

Use multi-factor authentication.

## Session Management

Do not expose session identifiers in URLs, errors, or logs.

Session identifiers should only be in HTTP cookie headers.

Use HTTPS for authentication and authenticated sessions.

Use secure attribute and HTTPOnly attribute for cookies.

## Access Control

Deny access by default, unless access permission can be verified.

Periodically revalidate users authorization to ensure privileges haven't changed.

Service accounts should have the least privileges possible.

## Cryptographic Practices

Protect master secrets from unauthorized access.

Use standard, well-vetted, and approved cryptographic modules.

Use cyptographic modules approved random number generator for random numbers.

## Error Handling and Logging

Give only a generic response - do not disclose sensitive information in error message.

Free allocated memory when an error occurs.

Logging should include success and failure of security events.

## Data Protection

Implement least privilege.

Encrypt sensitive data.

## Communication Security

Implement encryption for transmissions with sensitive information. HTTPS with TLS, e.g.

TLS Certificates must be valid for the given domain.

TLS connections should not be downgraded, and failed connections should not fall back to unencrypted.

## System Configuration

Remove unnecessary functionality, services, and files from the server.

Restrict web server accounts to least privilege.

Turn off directory listings.

Restrict access to only the application directory (no directory traversal).

Isolate development from production environment.

Implement change control systems.

Disable unnecessary HTTP methods.

## Database Security

Use parameterized queries (queries that distinguish between untrusted, typed user-inputs and they query instruction string).

Ensure variables are strongly typed.

Use secure credentials for databse access.

Application should have the lowest necessary privilege for database access.

Close connection as soon as possible.

Connection strings should not be hard coded.

Change all default database passwords or disable default accounts.

## File Management

Do not pass user input directly to include files in the application.

Limit type of files that can be uploaded.

Do not save files on the same system as server.

Turn of execution privileges on upload directories.

Do not pass user supplied directories or file paths; use a predifined list of white listed file paths.

## Memory Management

Double check buffer is large enough or large as specified.

Truncate input strings to reasonable length before passing to copy or concatenate.

Close resources after use.

Avoid the use of vulnerable functions (strcpy, strcat, printf).

Free allocated memory upon completion of function.

## General

Use tested and approved managed code rather than creating new unmanaged code for common tasks.

Use locking to prevent race conditions.

Do not pass user supplied data to dynamic execution functions.

## References

[1] https://owasp.org/www-pdf-archive/OWASP_SCP_Quick_Reference_Guide_v2.pdf