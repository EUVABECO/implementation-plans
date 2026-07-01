---
title: CDS operations
---

# CLINICAL DECISION SUPPORT SYSTEM (CDS) - OPERATIONS

# Governance

A continuous update process is needed to ensure the CDS remains aligned with evolving vaccination recommendations and newly available vaccines. Key governance actions include:

-   **NUVA Updates:** Updating the **NUVA** coding system is beyond the scope of this project. If an alternative terminology is used, the responsibility for its maintenance lies with the **MS Health authority**.
-   **Rules and Conditions Updates**: The knowledge update loop initiated during the deployment project must remain active. Its cycles are triggered by the NITAG when new recommendations are being considered, and the releases should be synchronised with the entry into force of these new recommendations. Additionally, regular management meetings (typically every six months) monitor progress and execution.

In addition to knowledge governance, technical management is necessary to maintain the availability and performance of the CDS. Two scenarios can occur:

-   **Centralized CDS Service:** If the CDS is offered as a service by the MS health authority to multiple software editors, the MS will organize technical management to maintain the services availability and performance.
-   **Single Client Subscription:** If a single client software editor subscribes directly to the CDS, technical management becomes the responsibility of that editor.

These two cases can overlap when the MS e-Health national operator is the sole client software editor.

A quarterly technical management meeting involving the project’s technical team, client software editors, and the CDS provider will ensure proper system management. Operational meetings may be scheduled as needed to address short-term technical issues.

An incident management procedure should also be established to handle situations where the CDS becomes unavailable or outdated.

# Monitoring

Monitoring of the CDS service is crucial to ensure optimal performance and user satisfaction. Key technical monitoring indicators include:

-   **CDS Service Availability:** The target availability should be defined by project management, but could typically be 99.9% per calendar month, excluding planned maintenance periods.
-   **Response Time:** For interactive queries, the CDS should respond in less than 2 seconds per request. In batch processing mode (e.g., for entire populations), stricter performance targets may be necessary.
-   **Request Load:** Monitoring the average and peak flow of requests will help assess the system’s capacity and inform decisions about scaling the infrastructure.

A quality-of-service monitoring could also be implemented. However, delays in updating rules and conditions could stem from multiple stakeholders, including the CDS provider, MS immunization experts, the communication team, or the Health Authority.

# Use in crisis situations

The CDS is most helpful in routine vaccination, helping professionals to handle the subtleties of vaccination schemes for all specific patient conditions and assisting citizens in understanding their vaccination needs.

Yet, its features also make it very valuable in the case of emergency situations, such as the COVID-19 crisis, since:

-   The recommendations can be adapted within a couple of days, keeping them aligned with the new knowledge about the emerging disease.
-   They are instantly broadcasted to all vaccinators, giving them a clear course of action without requiring massive communication campaigns.
-   They can also be exposed to the general population, with adequate justifications that will support confidence.

These benefits are however only achievable if the confidence of professionals and citizens in the CDS has been established upfront with a stabilised and reliable routine use.
