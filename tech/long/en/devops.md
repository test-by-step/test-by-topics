# DevOps

DevOps, or Development Operations, combines Software Development and Business or IT Operations practices and personnel with the goal of delivering high quality software that tightly aligns with business requirements at a rapid rate.

DevOps is a key aspect of Software Development and extremely closely related to the Software Development Lifecycle (SDLC)

DevOps is highly assocaited with:
* Agile Development Practices
* Continuous Integration / Continuous Delivery (CI/CD) practices

The key aspect of DevOps is the marrying of the software developers with business operations, ensuring that both aspects are continuously collaborating and evaluating eachothers requirements at every stage and cycle of development.

DevOps requires that all participants be working under a common criteria and understanding, as well as constantly communicating requirements that might change the pipeline.

The DevOps pipeline is not static but may be changed and adapted to meet the needs of the team and the software under development.

## Automation

Automation is a key requirement of effective DevOps.

Automated review and build processes reduce complexity and improve the speed and efficiency at which software can be developed and the rate at which changes can be made.

Automation can automatically initiate code review or present code for manual review.

Automation can automatically build changes accepted in a code repository after review.

Automations can help ensure standards compliance as well as timeliness.

Automation is criticial to the CI/CD model that is highly linked to DevOps, as it allows changes pushed to central repositories to be immediatelly built for testing or integration at a daily or even multiple-times per day rate, or any time a change is made.

## DevSecOps

DevSecOps adds security integration and considerations into the devlopment and operations teams.

The goal of DevSecOps (vs. DevOps) is to integrate security by design, with considerations for the secure development and operation of the software at every stage and cycle of the software development process, including before, during, and after core development.

## Defined DevOps Pipeline

Exact DevOps practices and procedures will vary from organization to organization but one key to properly executing a good DevOps environment is a well defined DevOps pipeline.

Within a team or organization the DevOps pipeline must be well-defined. This is key to achieving repeatable results, and continuous integration and delivery.

Generally, a DevOps pipeline involves all of the tools, processes, and automations required to build, test, and publish software.

A good DevOps pipeline is:
* Repeatable - generates the same output given identical input
* Continuous - changes are frequently merged or integrated into the code repository, resulting in frequent builds (automatic after changes are accepted)
* Always On - changes are immediately entered into the pipeline upon integration

Often pipeline tools are highly integrated into the tools used for programming, such as bundled as part of, or highly integrated into the IDE (Integrated Development Environment) or code editor application. Because of this, the text-editing features may often be included into the pipeline definition.

### Pipeline stages

* Plan - generate requirements and expectations
* Code - write the code to meet requirements
* Build - generate the executables that will perform the task
* Test - verify that the build behaves as expected
* Release - make the build available for consumption
* Deploy - push the build to production where real customers can interact with it
* Operate - the build is used by real customers
* Monitor - feedback and metrics are gathered to assess proper function of the build

The pipeline then wraps back to the planning stage where requirements and expecations are reassessed and the process begins again.

## References

[1] https://resources.github.com/devops/pipeline/

[2] https://en.wikipedia.org/wiki/DevOps#DevOps_automation