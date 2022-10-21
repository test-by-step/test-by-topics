# File Integrity Monitoring (FIM)

File integrity monitoring inspects files for changes and triggers events or alerts when a discrepency is found.

File Integrity Monitoring will typically operate by hashing the contents of a file, recording the expected hash value as a baseline and comparing subsequent scans of the file, directory, or filesystem with the expected baseline hash value.

Using a good hashing algorithm neans that any change, no matter how small, to a file will result in a radically different hash value.

FIM can be particularly useful in protecting critical system components that are expected to be generally static or immutable such as binaries used for boot up and kernel processes. If FIM detects a change in some sensitive system component, it might indicate a compromise of the system.

## Related Ideas

* Hashing

## References

https://www.crowdstrike.com/cybersecurity-101/file-integrity-monitoring/