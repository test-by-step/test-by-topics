# Continuous Integration / Continuous Delivery (CI/CD)

Continuous Integration is the frequent (i.e. daily or multiple times per day) merger of small, independent feature code changes back into the main code base.

Continous Delivery is the frequent (i.e. daily or multiple times per day) re-building and deployment of code changes accepted into the main repository.

CI/CD is a core part of Agile software development practices.

CI/CD is frequently associated with the Software Development Lifecycle (SDLC).

CI/CD is typically directly associated with a DevOps pipeline.

## Continous Intgration

Continous Integration involves:
* frequent mergers into the main branch.
* automated building
* automated testing

## Continous Delivery

Continous Delivery involves
* Packaging built code
* Moving built products to staging environments or testing environments

Continous delivery requires a manual step to accept the built products for production.

## Continous Deployment

Continous deployment takes continous delivery on step further, and automatically deploys the built products to a production environment.

## CI/CD Pipelines

CI/CD pipelines are the procedures, tools, and protocols in place that automate the process of merging, reviewing, accepting, testing, building, and deploying changes to the code base.

Where the CI/CD pipeline starts will vary from organization to organization but typically will look similar to:
* Code is commited to a development repository (that may or may not run pre-tests on the code)
* A pull request (a request for inclusion of development changes in another repository) is made to incorporate development changes into the main code base
* Tools in the CI/CD pipeline will perform static tests of the code for acceptability and correctness
* If the static tests pass the pipeline attempts to build the code
* If the code builds successfully it is again tested with unit tests and/or integration tests
* If all tests pass at this point, the code is merged into the repository
* The build is automatically released to the testing or staging environment
* With continous deployment, the build may subsequently be automatically released to production

This process has three key pipeline parts:
* Pull Request Pipeline - which handles validation prior to merger into the next repository
* Continuous Integration pipelines which run after Pull Requests complete to perform integration tests prior to release into the repository
* Continous Delivery Pipelines which run after Continous integration piplines which prepare the built applications or components and perform acceptance tests and release to the appropriate environment

CI/CD pipelines are critical to the Software Development Lifecycle and DevOps.

## References

[1] https://en.wikipedia.org/wiki/CI/CD

[2] https://www.architect.io/blog/2022-10-24/cicd-pipeline-guide/

[3] https://www.redhat.com/en/topics/devops/what-cicd-pipeline