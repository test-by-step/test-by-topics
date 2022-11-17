# Blocking External Media

External media may be used to leak data or to load malware onto a system; blocking external media can help mitigate.

Computer systems which require additional security and hardening controls should consider blocking the use of external media such as USB drives in order to prevent the transfer of data to or from the system.

External Media Blocking is useful for:

* Device Hardening
* Dataloss Prevention

Group policies or endpoint protections (Endpoint DLP solutions, Host Based IDS (HIDS), Endpoint Detection and Response solutions (EDR)) can initiate automated responses to external media connecting to the device including:

- Automatically block data connection for the media link (typically USB)
- Generate alerts and notifications
- Block user accounts
- Block device

Cell phones connected to a computer system are particularly concerning, given that they contain substantial processing power and additional radios to initiate connections that may subvert the internal organizations protections.

## Dataloss Prevention

External Media such as USB drives, SD Cards and USB connectors for SATA drives are cheap, easy to use, and abundant making it trivial for any user to plug in a device and move files on to an external drive.

Systems that need to protect proprietary data may benefit from blocking external storage devices from the system.

## Device Hardening

External media can pose a danger to a system even if not a data storage device.

### Emulated input device

External media may emulate a keyboard or mouse device and send keyboard and mouse input instructions automatically without user interaction.

Typically, devices need keyboards or other input devices to be operated effectively, therefor blocking these devices is difficult and the best practice to avoid this is good user education and training.

### Malware

Some external media, and even modified malicious media devices may be capable of automatically loading malware on a system or exploiting the mounting process or auto-run process to automatically load malware onto the system.

Preventing external media connections or automatic mounting may help to prevent exploitation.

## References
