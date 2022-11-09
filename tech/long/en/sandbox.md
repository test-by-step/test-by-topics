# Sandbox

A Sandbox is an isolated system with no, or extremely limited, connectivity to external inputs or networks.

Sandboxes provide a secure environment where system errors or malicous activity (such as viruses) cannot propogate to other parts of a system or network.

Sandboxes additionally can provide a clean environment where eternal influences cannot be injected to a development pipeline - this is typically referred to as a secure development environment.

Sandboxing can secure entire networks, devices, or individual applications.

## Virus Analysis and Research

Sandboxes are often used as an isolated environment where a newly discovered virus can be ran in order for researchers to observe its behavior and identify its signatures.

Sandboxes are essential for this process in order to contain the ill effects of the virus, and occaisionally to spoof the specific environment a virus will require to run.

## Secure Development Environment

A secure development environment is a type of sandbox where all the tools necessary to develop an application are provisioned in an isolated environment.

The benefit of this type of sandbox is that it can strictly control what development is flowing into an application which enhances the software assurance level.

Secure Develpment Environments are useful for ensuring stable and secure dependencies or third-party libraries by strictly controlling the introduction of dependencies into the environment. Critically, third party libraries and dependencies must be vetted and verified before they are injected into the environment, and are only as secure as their vendor can themselves assure.

## Virtual Machines

Virtual Machines can act as a logical sandbox, providing a guest system running inside of the host operating system.

Generally the guest should be unaware of the host for a VM sandbox.

Virtual Machines expected to be a sandbox must be properly hardened and configured, as many hypervisors have features that would otherwise permit bidirectional communication between host and guest.

Some virtual machines are susceptible to Virtual Machine Escape, in which a virus exploits the hypervisor to escalate its privilege and scope from the guest system to the host system.

## Applications

Many operating systems provide a mechanism in which to sandbox applications so that they do not have access to system resources that are not explicitly permitted.

Mobile Operating Systems such as Android and iOS typically implement full application sandboxing on every application.

## Browsers

Secure Browsers must isolate different pages and tabs from each other in order to ensure one malicious page cannot access another.

Browsers must also (with HTML5) sandbox iframes embedded within a page to prevent the iframe from accessing information from the parent page, such as authorization tokens, or from submitting actions on behalf of the parent page (which might have the user logged in).

## Quarantine

When a virus is quarantined it must be moved (typically logically) to a specially designated zone that prevents execution. This is a very limited sandbox.

## References

[1] https://en.wikipedia.org/wiki/Sandbox_(computer_security)