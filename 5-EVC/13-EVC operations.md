---
title: EVC operations
---
# EUROPEAN VACCINATION CARD (EVC) - OPERATIONS

# Governance
## Maintenance of the registry

Within each health jurisdiction, new repositories can be deployed, existing repositories can be merged or contact persons for repositories may change. It is the responsibility of the local health authority curating the registry to attribute an identifier to each new repository and manage the contact list for existing ones. A [registry management guide](Resources/Registry%20management.md) has been released by the EUVABECO project.

## Maintenance of the software applications

Each contributing software application should be maintained by its provider:

| Application               | Maintained by              |
|---------------------------|----------------------------|
| EHR software              | EHR supplier               |
| EVC viewer for citizens   | eHealth operator           |
| Signature server          | Digital signature operator |
| Public Key Infrastructure | Digital signature operator |

## New EHR software

Every new EHR software should go through the same process of onboarding as the ones in the initial project, including the verification of compliance (C3).

## New client systems

New client systems should be notified to the digital signature operator by the health authority, or by the eHealth operator on behalf of the health authority.

It then belongs to the digital signature operator to attribute client certificates to those new systems, and to renew the client certificates of the existing systems when they would expire.

Certificates are attributed only to systems that run an EHR software that passed the compliance verification (C3).

## Response to investigations

Requests for investigation from other health authorities about master records will be processed first by the health authority holding a registry, then forwarded to the contact person for the referenced repository.

Requests for investigation from local health professionals should be processed by their direct health authority, possibly with the assistance of the eHealth operator for the means of collecting and tracking the requests.

# Monitoring

In order to anticipate for upscaling of the resources, the monitoring should include:

-   The daily number of EVCs submitted for signature,
-   The number of master records held by each repository

# Use in crisis situations

Unlike the EU Digital Covid Certificate, the EVC is not intended to be used as a [certificate of sterilizing immunity](https://www.adultimmunizationboard.org/wp-content/uploads/2026/05/26ANT702_Tassinari.pdf). If such a certificate was necessary again, it should not be a vaccination history, but a minimized statement of compliance at a given time for a given set of rules. This certificate could be delivered by a Clinical Decision Support system, based upon the EVC as a trusted source of information, but also other sources for test results or past infections, as described in use case [UC06](02-EVC%20description.md\#uc06--obtaining-a-vaccination-certificate) of the EVC description.

# Communication

The EVC is an equivalent of the existing paper vaccination cards and should be proposed in every context where the paper card was already used. This can be achieved through the same channels that distributed blank paper cards to health professionals.

Also, the primary use of the EVC being international mobility, it could be proposed in the context of travels, such as when a person requires a European Health Insurance Card.

It can also be promoted first towards specific populations moving frequently within the country or across Europe, such as militaries, truck drivers, seasonal workers, ship crews, etc.

The EVC will also be pulled by value added services using the vaccination history, and typically the Clinical Decision Support Systems (CDS) dedicated to vaccination, either proposed to the general population or to health professionals.
