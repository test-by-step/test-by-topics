# API Management

API Management is the tools, administration, management, and policies used to create, remove, update, monitor, and control Application Programming Interfaces.

API Management is closely associated with API Gateways and microservices.

API Management allows for centralization of the management and monitoring functions of APIs and endpoints.

API Management: 
* helps ensure availability of application services and microservices.
* *helps ensure secure access to application services and microservices.
* helps consolidate logs and alerts for APIs and microservices.

API Management should ensure proper access control for all endpoints, and that APIs and API endpoints disallow access by default, unless specifically intended for public use. API Management should authorize and verify access on each API request for non-public endpoints for every access request.

API endpoints may be restricted to authorized access only.
* API Application Keys are a private key assigned specifically for a single applications use to access an endpoint or group of endpoints
* Tokens may be used to authorize access to API endpoints for logged in users or systems

API Management should also support monitoring of APIs and gateways, as well as logging.

## Components

### API Gateway

Many APIs are accessible through a gateway which is responsible for routing requests to endpoints and may also verify authentication and/or access to the endpoint.

APIs typically consist of many *endpoints* which are accessible over the internet, usually as a URL, and which are used to route service requests to the appropriate service or function.

### Portal

API management should have an interface from which to view and monitor all API statistics, and to possibly make configuration changes.

The developer or API portal functions as a centralized interface from which to view the entire API ecosystem and to manage alerts, logs, and errors.

### Reporting and analytics

API management should consume and centralize reporting information for all APIs and endpoints in to single digestable solution.

API Management should be able to monitor and trigger alerts for all APIs.

## References

[1] https://www.ibm.com/cloud/learn/api-management

[2] https://en.wikipedia.org/wiki/API_management

[3] https://www.redhat.com/en/topics/api/what-is-api-management