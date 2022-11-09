# Middleware

Middleware is a software application that acts as a connector and translator between distributed network/system applications and appliances. 

Middleware can help to connect appliances that may otherwise not be able to communicate directly due to distance, differing protocols, or differing physical mediums.

Middleware operates transparently, passing mesages to Applications after they have been fully translated.

Middleware is typically considered below the Application Layer (Layer 7) but above the Transport Layer (Layer 4). 

Middleware handles the message processing, transactions, and translating necessary to receive and then transmit the message to all subscribed appliances in a format that they are individually able to digest.

Middleware is important for software development and the SDLC as it provides an abstraction that makes it easier to develop inter-application communications by not needing to explicitly provide an extended suite of protocol support to external communications.

Middleware can be occaisionally referred to as a Message Broker, particularly when being used explicitly as a means to link and distribute messaging among cloud and microservice systems. Message Brokers often operate under a Pub/Sub (Publish Subscribe) arrangement.

## Enterprise Service Bus

Enterprise Service Bus (ESB) is highly related to Middleware.

Enterprise Services Buses act as a common medium for network and system applications to share information, regardless of operating protocol or standard of the end appliance.

The ESB is responsible for receiving, translating, and delivering messages and data between applications connected to the bus.

## Web Middleware

Middleware is used on the Internet and in web applications to communicate between user endpoints (typically browsers) and the application back end.

Web Middleware will typically be associated with concepts, protocols, and standards for messaging and communicating of data between user and application:

* SOAP
* JSON
* REST

## References

[1] https://www.ibm.com/cloud/learn/middleware

[2] https://azure.microsoft.com/en-us/resources/cloud-computing-dictionary/what-is-middleware/

[3] https://en.wikipedia.org/wiki/Middleware