# Antivirus

Antivirus is/are softwares that detect and protect against computer viruses.

Antivirus is typically a software installed on endpoints and at critical network junctures (such as perimiter security devices/firewalls and mail servers) to detect viruses as they either travel the network before they can infect and spread through the network.

Antivirus may be used interchangeably to mean anti-malware.

## Malware

Malware refers to all malicious or spam applications that infect an endpoint against the wishes of the users or network administrators.

Malwares can include:
* Viruses - malicious software that infects the host and attempts to hide
* Worms - viruses that aggresively attempt to infect its host and then self-replicate and autonomously spread to new hosts
* Adware - installs itself on a host and then bombards the host with unwanted advertisements
* Spyware - silently observers the users actions and attempts to steal and exfiltrate sensitive data about the user
* Ransomware - encrypts the hosts filesystem and extorts the user for money in order to recover the decryption key and their files
* Rootkits - infects the root of the operating system, kernel, and/or boot system in order to gain elevated privilege and hide its existance

## Computer Virus

Computer virus is a program that replicates itself when executed and inserts its own, typically malcious code, into legitimate processes.

The act of replication and self-propogation of infection to new systems typically distinguishes viruses from the more general term 'malware'.

### Trojan

Trojan viruses infect an initial host by posing as another, legitimate application and tricks the user into running the application.

Trojan's can gain elevated privileges and circumvent the antivirus process by tricking the user into explicitly permitting it to run its actions.

## Virus Detection and Identification

### Signature-based

Signature based detection mechanisms rely on a pre-defined and downloaded databases of signatures that define how a virus is structured or behaves to detect and isolate viruses.

Signatures can involve certain actions invoked in code, the system calls themselves but also the order of actions, the files accessed, or the raw binary data that accompanies some viruses.

Signature-based detection cannot detect novel, unknown, or zero-day exploit viruses as they rely on the detection of specific, pre-downloaded definitions.

### Heuristic-based

Heuristic detection mechanisms rely on a set of algorithms to analyze program actions and features to look for viruses that have altered themselves to avoid known signature detection.

Heuristics can possibly detect polymorphic and even novel viruses but rely on complex and well configured algorithms that do not guarantee accuracy and possibly False Positive results.

Heuristic approaches do not depend entirely on a database of signatures, but rather the complex and often proprietary algorithm that it uses to find virus mutations.

## Actions

### Quarentine

Antivirus software will often quarantine suspected virus files, moving them to a sandboxed location where they do not have permissions to execute, isolating their payload and preventing infection and spread.

Once quarantined, the user or administrator is given the opportunity to review the action and determine if the detection was a false positive or not. With quarantining, the user can still elect to release and execute the file.

### Block or drop

Antivirus software can block or drop a connection, file transfer, or file execution if it detects a virus signature.

This response prevents any transmission or execution of the initial infection mechanism, but false positives completely prevent legitimate actions.

### Replace

Antivirus software may replace a file, either deleting or quarantining the file, with a message alerting the user to what has happened. 

This method is particularly useful for antivirus on mail servers and antivirus software operating on the network, as it will alert the end-user as to why their files or attachments were not transmitted.

This replacement is sometimes called Tombstoning.

### Sandboxing

Sandboxing moves a virus or malware into an isolated environment, cut off from legitimate system resources where it can be observed, and potentially even executed, without infecting the operable systems or networks.

Sandboxing isn't always an independent action but may be used in conjunction with other actions to isolate the virus without deleting it.

Often it is beneficial to preserve a suspected virus in an isolated environment so that it can be studied and analyzed to better understand the virus threat and to update signature databases.

## Challenges

Some viruses have morphing properties, known as polymorphism, such that they change their core code structure and sometimes behaviors to avoid detection.

For signature-based detection, virus definitions must be constantly updated in order to effectively detect threats.

False Positives can, and have, interrupt legitimate operations of applications and even operating systems, potentially leaving them unusable.

## Reference

[1] https://en.wikipedia.org/wiki/Computer_virus