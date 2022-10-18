# Application Programming Interface (API) Gatweay / Extensible Markup Language (XML) Gateway

API and XML Gateways are endpoints on the internet that remote applications can access to request services, responses, or to publish updates.

The function of an API or XML gateway is to receive connection requests (typically HTTP) for individual back end services, verify the request is authorized to access that service, and then route the request to the service provider.

These gateways provide a single point of entry for service requests from various remote or subscribing applications that can be processed, logged, and filtered before being serviced. An API gateway is likely to sit logically in front of a load balancer which will distribute connections to a pool of identical service providers that can be dynamically provisioned or de-provisioned as demand changes.

API gateways can verify authorization though API keys (long, random strings unique to each application making the request) or tokens (such as Javascript Web Tokens, JWTs) in the connection headers to verify the connections authorization.

Authorization information should always be placed in HTTP headers and never in query strings, as the headers will be encrypted in HTTPS requests.

JWTs are most often registered as browser cookies and passed by the browser as header rather than set by the application to avoid storing tokens in the browsers local storage, where they would be susceptible to XSS attacks stealing the credentials. Browser cookies are still susceptible to CSRF attacks.

API/XML gateways can do protocol translation to and from web-friendly and non-web-friendly protocols.

## API Gateway

API gateways are often associated with microservices, REST endpoints, and functions as a service. Typically, API gateways are accessed through HTTP requests and can receive data via query string variables or as a JSON object in the body.

While the backend service may expect some data values in the API endpoints definition, the data passed to API gateways are unstructured objects.

## XML Gateway

XML gateways are functionally very similar, however they will expect XML formatted input and responses. API gateways will typically return the entire JSON object to the backend process, an XML gateway expects a formatted document structure.

## References

[1] https://security.stackexchange.com/questions/184067/whats-the-difference-between-an-api-gateway-and-xml-gateway
[2] https://www.nginx.com/learn/api-gateway/