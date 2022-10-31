# Autoscaling

Autoscaling is a process that automatically provisions or assigns more resources to a system when the system reaches a certain service load in order to ensure sufficent resources are available as demand increases.

Autoscaling can also deprovision or reduce assigned resources as service demand decreases.

Autoscaling is an automated or automations process.

Autoscaling is closely associated with cloud services that handle the process of creating additional resource instances automatically or based on pre-defined load triggers.

Autoscaling can scale vertically or horizontally.

Vertical scaling adds additional resources to existing instances, such as allocating additional RAM or network bandwidth to an operating VM.

Horizontal scaling adds additional instances to the servicing pool, such as adding an additional web server to a load-balanced server pool.

Autoscaling typically requires triggers that are based on load metrics (number of active sessions, amount of RAM consumed, ammount of CPU consumed, for example) that can be expressed as a number, e.g. 10Mbps, but most often as a percentage, e.g. 80% CPU load.

Autoscaling for cloud services is often related to on-demand or pay-as-you-go services in which the client organization only pays for the resources they use, saving money during slow periods but remaining stable and active during high traffic periods.

## Maximum and Minimum Sizes

Autoscaling often requires maximum and minimum sizes or expectations: 

The minimum size is the minimum amount of resources that will ever be provisioned for the system. Autoscaling will not reduce resources below this point.

This may ensure the system does not reduce resources to 0, or so low that it becomes unresponsive to any requests.

The maximum size is the most amount of resources ever to be provisioned for the system. Autoscaling will not add resources above this point.

This ensures the amount of resources consumed will not cost more than the client organization can afford.

## Scheduled Scaling

Autoscaling can also involve **scheduled scaling** in which scaling happens on a pre-defined schedule, usually based on a historical understanding of system demand during certain times or periods, in order to anticipate rapid changes in demand.

## References

[1] https://en.wikipedia.org/wiki/Autoscaling

[2] https://learn.microsoft.com/en-us/azure/architecture/best-practices/auto-scaling