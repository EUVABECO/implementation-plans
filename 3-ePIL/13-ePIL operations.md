# ELECTRONIC PATIENT INFORMATION LEAFLET (ePIL) - OPERATIONS

# Governance

## Governance of contents

The governance of contents covers both:

-   The list of vaccines to be referenced
-   The updates of the ePIL for a given vaccine

The list of vaccines is curated by the National Competent Authority. It should be updated when new vaccines are introduced. However, vaccines that are no longer used in the health jurisdiction should be kept in the list, since their ePIL could still be accessed from historical records.

New content of the ePIL for an existing vaccine is released by the vaccine manufacturer. When indirections are used, it belongs to the last referencing authority in the chain to update its references list. Such an update will then be implicitly propagated to all consuming other health authorities.

If the choice has been made to delegate the last references file to a vaccine manufacturer, this update could be done without intervention of a health authority. This is a political choice that goes beyond the scope of this study.

## Governance of infrastructure

The infrastructure, consisting of both the general-purpose Web server holding the references list and the redirection server, should be managed by a professional hosting provider, performing maintenance and technical upgrades on behalf of the health authority.

# Monitoring

The availability of both the general-purpose server holding the references file and the redirection server towards the actual documents should be monitored continuously with online probes.

Depending upon the implementation by each client application, the redirection server could be used for all ePIL accesses, or only for the ones that belong to centrally approved products or other health jurisdictions.

In the first case, the number of accesses to the redirection server will give a measure of the use of the ePIL. In the second one, it should be cumulated with the number of accesses to the national repository of ePILs.
