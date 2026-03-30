EUROPEAN VACCINATION CARD (EVC) - VERIFICATION

| *The purpose of EUVABECO is to deliver to Member States implementation plans for several tools able to support existing or future vaccination practices.*<br>*These implementation plans are practical guides for a Member State to decide upon the launch of an implementation project, assign adequate resources, deploy the given tool and keep it operational after deployment.*<br>*This module describes the verifications that should be applied before releasing to production a deployed EVC.* |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

Compliant implementations must be able to read EVCs provided from any other compliant system, and to write EVCs that can be read from other systems.

Compliance is verified through a verification process consisting of:

-   Reading in an imposed sequence a set of reference EVCs for several test patients
-   Adding to these patients an imposed set of vaccines
-   Creating the corresponding EVCs and testing them against the expected results

The test suite, with the set of reference EVCs, the list of vaccines to add and a checking tool to compare the produced EVCs with the expected results, is provided as a resource by the EUVABECO project.

The maximal throughput of the signature server should be measured with a load testing tool such as Locust[^1]. It should be above 100 EVCs per second.

[^1]: <https://locust.io/>

The signature server should be graded A or above using Qualys SSL Server Test[^2].

[^2]: <https://www.ssllabs.com/ssltest/>

The digital signature operator should run an information security management system certified against ISO 27001, encompassing the service of signature of the EVCs.
