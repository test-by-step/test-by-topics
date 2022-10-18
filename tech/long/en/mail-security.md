# Mail Security

Mail security refers to providing protection to email services, storage, traffic, and activity.

Aspects of mail security that needs to be addressed include:
* Confidentiality in transit and in storage
* Authentication and Integrity via Digital Signatures
* Sender verification
* Spam protection
* Phishing and Social Engineering Protection
* Anti-virus and Anti-malware
* Data-loss protection

## Encryption and Signing

### S/MIME 

S/MIME is an IETF standard for encryption and signing used in e-mail that relies on public key infrastructure.

S/MIME Confidentiality and Integrity to email (but not Availability) as well as Non-repudiation. 

S/MIME uses a hybrid crypto system. Messages can be enveloped/encrypted using a randomly generated symmetric cryptographic key, which is then protected for each user using the recieving mailbox's public asymmetric key.

Integrity is provided via digital signatures, signed using the senders private key. The message contents are hashed, and then the hash value is encrypted using the senders private key. The recieve can then verify the message by decrypting using the senders public key and comparing a hash of the received message to the signed hash.

S/MIME is based on X.509 certificates. S/MIME requires that the participating parties are able to securely exchange or verify eachothers certificates. Since they are based on X.509 certificates, this generally means each certificate is signed by a trusted root authority and then the public key can be distributed from either a central distribution mechanism, or inline with the message.

### PGP

Pretty Good Privacy (PGP), or sometimes listed as OpenPGP, can protect email in much the same manner as S/MIME. PGP, however, depends on the concept of a web-of-trust model for trusted key distribution.

Instead of having a root authority and an authority chain that verifies all keys, PGP keys need to be verified either offline or via the key being signed by another trusted source vouching for its integrity.

## Anti-virus and anti-malware

A popular method of delivering malware and viruses to target systems is via email and email attachments. In most modern cases this requires the receiving user to download and execute an attachment from an email, however worms in the past have been able to self propogate.

Malware and viruses in email usually require some tandem social engineering from the email sender in which the sender must convince the receiver to download and execute the attachment. The sender will usually put in a lot of effort to make the attachment look like a legitimate business or personal document.

Binary executables are not unheard of, but macro-viruses, viruses embedded in the scripting languges of office documents such as Word or Excel documents, can pose and especially difficult problem as they can look like legitimate and urgent business.

The best answer for combating virus and malware in email is usually user training and education, instructing the users to never open attachments from unknown sources and to verify that expected users sent the message and/or attachment.

Viruses and malware can be mitigated using virus and malware scanning software on the mail exchange servers as well. Depending on the system used email encryption can interfere with virus scanning, and can sometimes be used by attackers to bypass virus scans.

## Spam Protection

Spam protections and phishing mitigations can go hand-in-hand as phishing often relies on many of the same tricks as spam to beat filters and trick users into opening the content.

### Spam Filters

Spam filters on the mail servers are an active mitigation technique that scans mail passing through the server for keywords, phrases, behaviors, suspicous origins (IPs and email addresses) and for suspicious attachments.

Spam filters can be highly configurable but are susceptible to false-positives, with the potential to mis-identify legitimate traffic as spam.

Spam filters can block, delete, quarantine, strip, or tag emails that appear to  the filter as spam.

Spam filters often can operate as phishing filters.

Spammers can attempt to use email encryption to bypass filters if the email cannot be decrypted before it gets to the spam filter.

### DKIM

DomainKeys Identified Mail (DKIM) can be used to prevent email spoofing and to protect against spam and potentially phishing by verifying the email is sent from the domain that it claims to be from.

With DKIM each message is affixed with a digital signature attached by the sending domain's mail exchange server that is signed by the domains DKIM private key. The receiving system can verify the message came from the claimed domain by looking up the domain's public key that is stored in and served from a special DNS record.

### SPF

Sender Policy Framework (SPF) can be used by the sending email exchange servers to verify that an IP is authorized to send mail on behalf of that domain by checking the list of authorized IP addresses in the domain's DNS records.

### DMARC

Domain-Based Message Authentication Reporting and Conformance (DMARC) is another email authentication specification. DMARC extends DKIM and SPF.

DMARC allows the domain owners to specify a policy in the DNS record on how the receiving mail system should verify the authenticity of the mail message via SPF and/or DKIM.

## Phishing Protection

The number one guard to phishing protection is user education and training.

Many of the strategies used in spam protection are also used in phishing protection, since both use similar strategies to bypass spam filters and to convince users to open the documents.

## DLP

Data-loss prevention filters can be installed on organizations mail servers to scan outgoing mail for potentially sensitive data, such as PII, proprietary business information, or other data controlled by law or regulation.

Like spam filters, DLP filters can be circumvented by encryption. It is possible to filter all attachments or encrypted messages to addresses outside the organization.

## References

[1] https://en.wikipedia.org/wiki/S/MIME
[2] https://en.wikipedia.org/wiki/DMARC
[3] https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail