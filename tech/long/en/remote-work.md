# Remote Work

Remote work is employees or offices performing their business functions from a geographcally dispersed or remote location, physically outside of the primary network infrastructure of the organization.

Remote work is consideration for Deperimiterization.

Remote work can be entire offices, but often refers to employees working while traveling or from home.

Remote work is realized in many diverse ways:

### VPN

A VPN can be used to secure the connection of entire office (site-to-site) or from a single device (client-to-site) back to the organizations intranet.

VPN can be combined with Network Access Control or Mobile Device Management to ensure the endpoint is sufficiently secured and maintains all the appropriate security policies and protocols before allowing a connection into the network.

### Enterprise SaaS Collaboration Products

Collaboration products such as Microsoft Office365, Microsoft Teams, Slack, Lotus Software, and other SaaS driven business office products can allow collaboration over a web interface.

Web-based SaaS products may be convenient for remote work where it is not feasible to enforce security policy through NAC or MDM as the entire session is relatively sandboxed within the web-browser session.

Security is handled by the browser and the controls implemented by the SaaS provider.

### Virtual Desktop Infrastructure (VDI)

Virtual Desktop Infrastructre allows companies to host desktop operating systems in a cloud environment and make the desktop session available through a web based interface.

Much like enterprise SaaS products, VDI can provide convenience for remote workers without the need to enforce strict security policies on the users device.

Furthermore, VDI can have additional security benefits over other cloud services, particularly for concerns such as Data Loss Prevention (DLP). All files, actions, and traffic when using VDI occurs inside the organizational network, meaning they are still subject to strict logging, intrusion detection and DLP controls. Copy-and-paste can also be disabled between the VDI interface/session and the host desktop itself, further aiding in preventing DLP.

## Key Ideas

A consideration for deperimiterization.

Remote working connections should always be strongly authenticated.

Remote connections should be strongly or sufficiently encrypted.

Consider Zero trust model.

VPNs can be used to secure authenticated users, devices, and offices with strong and verified security polcies access to the organizations intranet.

SaaS business products such as Office365, Microsoft Teams, Slack, etc. can be used as a collaborative tool accessible from a web browser; the web browser and the SaaS provider handle the security of the connection/session.

VDI can be used to provide a virtual desktop session from the cloud accessible from a web browser. The desktop session is logically inside of the organizational network, subject to all the internal security policies and mitigations.

VDI can disable copy-and-paste to help with DLP.

