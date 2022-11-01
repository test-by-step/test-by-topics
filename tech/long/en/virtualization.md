# Virtualization

Virtualization creates virtual instances (as apposed to phsical) versions of some system or component that behaves like and appears to all connecting systems as if it were the physical device or system, that it is virtualizing, known as Virtual Machines or VMs.

Virtualized instances are separated from the underlying hardware, access to hardware resources instead being arbitrated through a hypervisor that manages Virtual Machine access to the system resources.

Virtualization relies on a hypervisor that manages scheduling of the guest OSes and host OSes resource utilization, apportioning memory, CPU usage, data storage access, etc.

Virtualization typically virtualizes:

* Operating Systems
* Appliances such as firewalls and IDs
* Network devices such as routers and switches
* Servers
* Desktops

Virtualization allows efficient and cheap provisioning and deployment of new systems on top of existing hardware.

Virtualization can enable scalability by allowing for new instances or redundant instances to be efficiently constructed and deployed.

Virtualization can improve security by isolating systems and appliances that are otherwise running on the same hardware.

## Hypervisor

### Type 1 Hypervisor

A type 1 hypervisor is a hypervisor that runs directly on top of the system hardware and hosts the guest operating systems directly, without a primary host operating system.

Sometimes called a bare metal hypervisor.

Type 1 hypervisors can be more efficient since there is no full operating system needed to host the VMs.

### Type 2 Hypervisor

A type 2 hypervisor is a hypervisor that runs in the host operating system as an application, allowing the user or system to start virtual machines from within the desktop or working environment.

## Full Virtualization

Full virtualization virtualizes underlying hardware components as well.

Full virtualization is closely related to emulation, in which features of hardware, such as CPUs with different isntruction sets, are replicated or translated in software.

## Virtualization vs Containerization

virtualization creates an instance of an entire system or operating system that runs on top of and/or is managed by a hypervisor that translates instructions to the host processor.

Virtualization instances come with their own kernel that is translated to the CPU and/or host kernel by the hypervisor.

VMs typically have more overhead than containers, but more versatility as they are not dependent on the host kernel.

Containerization creates an isolated, packaged application environment that contains all of the supporting dependencies, libraries, objects, and tools the application needs to run.

Containers run on top of existing operating systems and are managed by container run times.

Containers make use of the host kernel. 

## References

[1] https://en.wikipedia.org/wiki/Virtualization