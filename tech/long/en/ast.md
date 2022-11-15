# Application Security Testing

Application Security Testing is the rigorous security testing of an application integrated into the SDLC process and into the DevOps pipeline.

Application security testing is focused on security aspects and vulnerability detection, it is not a functionality test. It specifically searches for insecure patterns or known vulnerabilities; however, it may evaluate proper error and exception handling.

## Interactive Application Security Testing (IAST)

Interactive Application Security Testing (IAST) tests an application while it is running with some understanding of the underlying source code and expected behavior.

IAST is commonly associated with a **grey box** application test.

IAST combines both DAST and SAST techniques to assess the secure function of the application.

IAST allows for targeted testing of aspects of the application since the tester knows how the application is supposed to function and what is available or exposed.

### Advantages

Accurate - targeted testing and broad coverage increases accuracy

### Disadvantages

Requires in depth knowledge of the application 
Requires specific language support

## Dynamic Application Security Testing (DAST)

Dynamic Application Security Testing (DAST) tests an application while it is loaded, checking for security vulnerabilities and insecure practices or procedure calls.

DAST is commonly associated with **black box** application testing, as the tester or testing suite does not need to know anything about the underlying source code.

DAST will typically detect vulnerabilities by performing attacks against an application.

DAST should not be performed against production applications, but in a separate environment that replicates a production environment.

### Advantages

Independant of languages or pipeline technologies used.

### Disadvantages

Can't cover 100% of the source code

## Static Application Security Testing (SAST)

Static Application Security Testing (SAST) reviews the source code for vulnerabilities or insecure code patterns.

Commonly associated with **white box** testing.

SAST does not assess an application while it is running.

SAST tools are commonly integrated in to the development or DevOps pipeline.

SAST tools can be automatic, such as those that automatically scan repository commits or source code bundles, or may be manual such as a code review by a supervisor.

SAST may also analyze a binary for insecure procdures or signatures without executing the application.

SAST tools may have different scopes:
* function level 
* file/class level
* application level

### Advantages

Vulenerabilities are fixed earlier in the SDLC or pipeline

### Disadvantages

Many false positives
Lower accuracy

## References

[1] https://en.wikipedia.org/wiki/Static_application_security_testing

[2] https://en.wikipedia.org/wiki/Dynamic_application_security_testing

[3] https://www.techtarget.com/searchsoftwarequality/tip/SAST-vs-DAST-vs-IAST-Security-testing-tool-comparison