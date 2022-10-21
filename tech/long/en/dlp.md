# Data Loss Prevention

Data Loss Prevention is/are mitigation tools concerned with preventing the exfiltration of sensitive, proprietary, or regulated data from an organizational network.

DLP might also involve preventing unauthorized use of sensitive data between internal organizations or by unauthorized users.

Data can exist in three states:
1. Data in motion - data that is traveling across networks or connections between systems and/or devices
1. Data in use - data that is loaded in memory and actively being processed by users and/or applications
1. Data at rest - data that is stored or saved onto a drive

DLP may be associated with regulatory restrictions that mandate where and how DLP has to be implemented such as: HIPAA, GDPR, and PCI-DSS.

DLP solutions need to have effective data identification, being able to identify sensitive data such as PII, PHI, credit card numbers, or proprietary business data using algorithms and signatures.

DLP can be associated with True Positive, True Negative, False Positive, and False Negative rates. These are the rates at which the DLP software appropriately (TP, TN) or inappropriatelly (FP, FN) triggers data loss prevention measures.

## Network DLP

Network DLP detects data in motion as it travels the organizations network and can attempt to prevent its exfiltration or notify administrators to the data's transit.

Network DLP protection is very often placed at network perimiters and is most concerned with data going out of the network, rather than that coming in.

## Endpoint DLP

Endpoint DLP relies on an agent installed on host devices that actively monitors user, system, and network activity for signs of potential data leakage. 

Endpoint DLP can assess data in use, data in motion, and data at rest.

Endpoint agents watch memory, system processes, and file system access to protect data in use.

Endpoint agents can also parse files saved to the filesystem looking for sensitive data such as PII, PHI, credit card numbers, etc. that should be otherwise stored in an encrypted or protected space.

Endpoint DLP agents can be associated with HIDS and sometimes NAC agents, as the they have some overlapping scope of operation.

## Cloud DLP

A cloud DLP solution monitors cloud network activity using Software Defined Networking (SDN) to mirror traffic to an interface that can assess the aggregated traffic for signs of leakage.

Cloud DLP functions much like Network DLP, but is hosted by the cloud provider and managed remotely.

## Challenges

### Encryption

Encrypted connections or encrypted data can stymie DLP software's ability to assess data and prevent data leakage.

### Steganography

Steganography is the practice of hiding information or data by disguising it in another object without significantly altering the appearance of the other object. An example would be encoding data into JPEG images by altering one bit in every pixel - the resulting image would not look significantly to the human eye and may go unnoticed.

Steganography attempts to get around DLP by hiding the attempted exfiltration of data in innocuous files.

Steganography is NOT encryption.

## DLP Actions

DLP's active responses are extremely similar to mail security and antivirus responses.

### Quarentine

DLP can cache or stash an action for later approval based on human intervention. If DLP is triggered on some action, it may require administrator intervention, or in some cases it may just require the user to confirm they want to perform the requested action to prevent accidental data leakage.

### Block or delete

DLP applications may block a connection or transaction, strip files from transmissions, and even delete files from filesystems if it detects sensitive data.

### Strip/sanitize

DLP may strip, tokenize, or replace sensitive data in files and connections.

Replacing files or information while leaving a replacement message, such as a textfile, is sometimes called Tombstoning.

## References

[1] https://en.wikipedia.org/wiki/Data_loss_prevention_software
[2] https://www.crowdstrike.com/cybersecurity-101/data-loss-prevention-dlp/