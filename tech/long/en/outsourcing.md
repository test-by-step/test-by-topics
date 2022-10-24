# Outsourcing and Contracting

Many organizations do not perform all business and necessary operations functions internally, but must contract out services to keep the operation running that may require some access to networks and services that would otherwise be internally available only to the main organization.

The security of the contracted / outsourced entity then has a direct affect on the organization.

This can come in any number of different forms. For example a large chain store may contract another service to provide heating, ventilation, and air-conditioning to its many retail locations. The HVAC systems are complex and controlled by a networked system controller that is provided and maintained by the contractor, but which must be connected over the organizations own network. If the HVAC network system is not properly isolated, a security flaw in that system, becomes a liability, which an attacker can use to access the payment processing system and steal payment card information.

Any outsourced or contracted services, whether an external system connected over the organizations physical network, or a contracted team that requires some access to internal business resources (file shares, servers, payment processors, etc) must be properly segmented. This means that they are given, by default, no permissions and access is only granted explicitly based on need.

Outsourced connections should be given access only the the bare minimum needed to conduct their contracted function.

If the contract requires some interconnection of the two business networks - an Interconnection Security Agreement (ISA) should be in place to describe the responsibilities of each party in securing the connection.

Regardless, the network and resource action should follow a 'Zero Trust' policy model, where each action is given the least privileges necessary and each action is strongly authenticated.

Vendors should additionally be strictly scrutinized for the repuation and competency, as well as their likelihood of persistance. If a contractor suddenly goes out of business, their connected products may become unmaintained, insecure and outdated.