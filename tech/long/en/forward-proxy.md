# Forward/transparent Proxy

A forward or transparent proxy is a proxy that resides on the local network and acts as an intermediary primarily for outbound traffic.

The forward proxy is typically implemented in order to protect the organization from compromises due to actions by inside parties and authorized or unauthorized users within the organizations network.

A forward proxy can implement:
* Data loss prevention (DLP)
* Anti-virus and anti-malware scans
* Break-and-inspect traffic
* Web-filtering
* Spam filtering

A forward proxy is also useful as protection from external threats as it is functionally similar to a NAT Gateway in which the internal IP address and port numbers are obscured by the proxies translation, also making the internal devices unroutable directly from the Internet unless explictly configured. One benefit is that this shrinks the attack surface.

In some cases the forward proxy might also cache frequently requested content to make it more quickly accessible to the client devices. 

## Break-and-inspect

In some corporate networks, devices deployed internally can be provisioned with a custom root certificate chain created and maintained by the company. With this certificate set as trusted in the company devices, the forward proxy can intercept HTTPS and some other encrypted requests and replace the web domains certificate with their own.

Through this process, the company is able to break open the encrypted payload and do a deep inspection on the connection before returning the results to the user. Since the companies certificate is set to trusted, the browsers will still accept the response.

Without break and inpsect, connections to TLS secured services would not be able to be observed, posing a challenge for data-loss prevention, anti-virus and anti-malware scanning, and for detecting insider threat behavior. Without break-and-inspect, the best option would be web filtering based on domain and/or IP.

## Pitfalls

A forward proxy sits in front of client devices (on the local organizational network); a reverse proxy sits in front of the server (on the remote service network).

## Key Ideas

* Sits in front of client devices on local organization network
* Can break and inspect SSL traffic
* Protects largely against threats from internal actions
* Protects from external network by concealing internal IPs and port numbers