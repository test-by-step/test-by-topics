# Third Party Libraries

Third party libraries are standardized or pre-built dependencies for software applications that greatly improve the speed and effiency of software development by providing common core features that do not need ot be re-created for each new application.

Third Party Libraries are often referred to as dependencies (in most common contexts).

Applications will often 'depend' on a library and will also require a specific version or versions of the library.

Third Party Libraries can be: Open Source, meaning their source code is publicly available for review, modification, and redistribution; Closed Source, meaning that their source code is not available for review; and/or Proprietary, meaning that the organization developing the library retains all rights to the library that cannot be modified or redistributed without their permission or license - this almost always means closed source.

## Securing, Validating, Vetting Third Party Libraries

Third Party Libraries must be vetted before inclusion in software or in the business environment.

Vetting should include, where possible:
* Vendor / supplier evaluation
* Source Code analysis
* Fuzzing / testing
* Performance
* Validation of signatures
* Documentation

### Vendor 

The quality and reliability of a vendor should be evaluated as part of third party library validation.

An untrustworthy vendor may produce untrustworthy libraries, but even generally trusted vendors are not immune to risk.

Vendors are also subject to the laws of the nation or state in which they are incorporated or where they operate out of, which should be taken in to account.

A vendor should be evaluated for reliability and longevity; for example, there should be reasonable assurance that the vendor will not go out of business soon after integrating their library, thereby leaving it unsupported.

### Source Code

Source code analysis and testing is generally only available for open-source products. It is possible that source code for proprietary software may be made available by the vendor, but before purchasing the license should be checked to verify whether such assessments of the source is permitted by the terms of the license agreement.

Source code can be analyzed using Static Application Security Testing (SAST) techniques such as automated code assessments that scan for common insecure practices and patterns or even manual code review by opening the files and reading them.

Some libraries support reproducible builds, which allow for the source to be compiled after review to verify that the official released binaries exactly match the binaries built from verified source code.

In the case of It is may be possible to reverse engineer the binary files of proprietary and closed source libraries to inspect it for liabilities. Again in this case, the license agreement should be taken in to account before performing any terms breaking assessment.

### Fuzzing / testing

The library should be rigorously tested using well defined unit tests as well as autoamted fuzzing tests in order to validate that the library: accepts the proper or necessary inputs, produces the expected outputs, and operates without errors or at least handles errors and exceptions appropriately.

### Performance

Libraries should be tested to ensure that they meet minimum performance requirements necessary to execute the applications function.

Generally, the use of libraries can improve the performance of an application by providing a well developed and specialized feature; however, a poorly constructed library can become a bottleneck in an application and/or an over abundance of libraries will add increased latency to processing.

While often speed or efficiency of processing is the most common metric considered, memory performance is also important. Too many, or too bulky dependencies may require excessive RAM.

Many cloud envirnments will bill based on amount of RAM required multiplied by the time spent processing at that RAM capacity, so lower memory usage is directly proportional to lower cost.

Moreover, excessive RAM consumption will reduce the ability for a service to scale or create new service instances on a single peice of hardware.

### Validation of Signatures

Especially where source code is not available for reveiw, it is important to validate the code signing signatures of library releases. Vendors should sign their packages with a well guarded private key, then make the public key available for clients and customers to validate the integrity of the libraries they downlod, to verify they are the proper package from the fully vetted and trusted source.

### Documentation

Robust and complete documentation is also important in vetting a third party library. It is important to understand how to use the library and how to troubleshoot issues.

Good documentation can be invaluable to a library, especially if the source code is not available to review for expected behaviors.

Documentation might include anything from expected inputs and outputs to API or procedure calls, to expected behaviors of library such as exceptions or errors that it might generate.

## References

