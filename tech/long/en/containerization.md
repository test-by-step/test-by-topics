# Containerization

Containerization is the isolation and abstraction of applications and services into self-contained executing environments.

Containerization may be referred to as OS-level virtualization.

Containerization allows for deployment of applications that will run consistently across any operating system that supports the container run time.

Containers are packaged with all the required binaries, dependencies, libraries, and supporting tools, all of the specific version required by the application, included within the container package.

Containers create isolated user-space instances for each application container.

Containers are useful for deploying multiple applications on a single operating system where dependencies between applications would otherwise conflict if run natively on the operating system.

Containers enable scalability, as they can be easily provisioned and de-provisioned to respond to changes in demand.

With containers, application faults are isolated to the container run time; application faults are less likely to cause a kernel panic or system fault that interrupts other applications on the same hardware.

Because containers are isolated, they improve security of the system by preventing security flaws in an application from being able to access other applications on the system.

## Containerization vs Virtualization

Containerization is similar to virtualization.

Containerization creates an isolated, packaged application environment that contains all of the supporting dependencies, libraries, objects, and tools the application needs to run.

Containers run on top of existing operating systems and are managed by container run times.

Containers make use of the host kernel. 

Sharing the host kernel is more efficient, as multiple kernels do not need to be scheduled for.

A separate guest kernel is not useable with containerization, limiting the containers capabilities to the capabilities of the hosts kernel.

Containers use less overhead than VMs.

virtualization creates an instance of an entire system or operating system that runs on top of and/or is managed by a hypervisor that translates instructions to the host processor.

Virtualization instances come with their own kernel that is translated to the CPU and/or host kernel by the hypervisor.

## References

[1] https://en.wikipedia.org/wiki/Containerization

[2] https://www.ibm.com/cloud/learn/containerization