EUROPEAN VACCINATION CARD (EVC) - VERIFICATION

# Characteristics to be checked

## For the EHR system

Compliant implementations must be able to read EVCs provided from any other compliant system, and to write EVCs that can be read from other systems.

The ability to read can be checked against the EVC samples exposed from different implementations.

The ability to write can be checked:

-   Against the local EVC encoder and decoder for the PDF metadata, and possibly the QR Code content retrieved with an independent QR Code reader.
-   Or with the simplistic QR Code reader.

## For the signature server

The maximal throughput of the signature server should be measured with a load testing tool such as [Locust](https://locust.io/). It should be above 100 EVCs per second.

The signature server should be graded A or above using [Qualys SSL Server Test](https://www.ssllabs.com/ssltest/).

The digital signature operator should run an information security management system certified against ISO 27001, encompassing the service of signature of the EVCs.

# Verification resources
+ [Implementation of an EVC scanner](https://github.com/EUVABECO/evc_scan)
+ [EVC scanner exposed](https://evc.euvabeco.eu/)
+ [Standalone encoder and decoder](https://github.com/EUVABECO/EVC-generator)
+ [EVC samples ](Resources/EVC%20samples)

