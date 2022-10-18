# Web Application Firewalls

Often abbreviated as WAF, web application firewalls are placed infront of web applications in order to inspect packets and protocols as they connect to the back end of a web based application.

The most common structure of questions regarding web application firewalls involve looking for exploit events related to technologies used in the web, e.g. SQL Injection, potential Cross Site Scripting (XSS), and Denial of Service (DoS).

WAFs can also protect outbound traffic, usually guarding against data loss as a data loss prevention tool.

WAFs will also have typical functions of simple firewalls, able to reject or allow traffic based on rules.

Web Application Firewalls differ from traditional firewalls as they protect a specific backend service set, rather than a network or network segment. Additionally WAFs will generally focus on HTTP/HTTPS protocol; network firewalls will almost always be incapable of scannining packet contents of HTTPS (encrypted) traffic.

WAFs can operate by:
* Blocking or dropping a connection
* Removing malicous input values
* Reconstruct or rebuild a request in a standard format (combats request mis-formatitng exploits)

## Pitfalls

### API Gateway

API gateways are closely related conceptually. API Gateway will usually be distinguished from WAFs by reference to specific endpoints (REST endpoints, e.g.) or access control to specific or various services. API gateways will not be referenced inpsecting most protocols or inputs, but may inspect headers (usually for API keys or authentication credentials).

API gateways are also more likely to related to individual services, microservices, or functions. Web Application Firewalls in contrast will protect an entire interactive application.

## Related Ideas

* Reverse Proxy: A web application firewall is functionally a reverse proxy, though the concepts are unlikely to be directly conflated.

## Reference

[1] https://www.crowdstrike.com/cybersecurity-101/web-application-firewall/