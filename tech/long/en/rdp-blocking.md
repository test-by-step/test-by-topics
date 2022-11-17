# Remote Desktop Protocl (RDP) Blocking

Remote Desktop Protocol (RDP) allows remote users to view and interact with a computer's desktop interface.

RDP can provide access to view the desktop, send keyboard and mouse input, and copy and paste between the remote and local interfaces.

RDP is also often used by support personnel to provide direct desktop support remotely.

RDP can be exploited by:

* a hacker to gain an internal foothold into the intranet
* an untrained or malicious user to steal or transfer data out of an organization

Blocking RDP by default is a good policy for all organizations unless there is a specific reason to enable RDP.

RDP can be blocked by group, user, or device policies, using endpoint protection mechanisms such as HIPS or EDR, or by filtering the service port 3389 in firewalls.