# CLINICAL DECISION SUPPORT SYSTEM (CDS) - OPERATIONS

| *This module proposes an organization and assigns tasks for keeping the CDS tool operational once it has been deployed.* |
|--|

*Once the tool has been deployed, there is still a need for lasting resources to support its adoption and ensure its maintenance. This section details these further actions.*

## Governance

A continuous update process is needed to ensure the CDS remains aligned with evolving vaccination recommendations and newly available vaccines. Key governance actions include:

-   **NUVA Updates:** Updating the **NUVA** coding system is beyond the scope of this project. If an alternative terminology is used, the responsibility for its maintenance lies with the **MS Health authority**.

    **Rules and Conditions Updates**: Updates to the CDS rules and conditions requires a structured collaboration between the NITAG, the Health authority and the CDS provider medical team. The process involves:

-   **Preparation:** Collaborating during the recommendation development phase to prepare the rules and test cases. The digitization of the rules at this stage enhances their quality by identifying and addressing ambiguous scenarios.
-   **Validation:** Ensuring that the updated ruleset and justifications are validated before the new recommendations become officially applicable.
-   **Synchronization:** Coordinating the release of the updated ruleset with the official implementation of the new recommendations.

This collaboration is event-driven, initiated by the NITAG when new recommendations are being considered. Additionally, regular management meetings (typically every six months) monitor progress and execution.

In addition to medical governance, technical management is necessary to maintain the availability and performance of the CDS. Two scenarios can occur:

-   **Centralized CDS Service:** If the CDS is offered as a service by the MS health authority to multiple software editors, the MS will organize technical management to maintain the services availability and performance.
-   **Single Client Subscription:** If a single client software editor subscribes directly to the CDS, technical management becomes the responsibility of that editor.

These two cases can overlap when the MS e-Health national operator is the sole client software editor.

A quarterly technical management meeting involving the project’s technical team, client software editors, and the CDS provider will ensure proper system management. Operational meetings may be scheduled as needed to address short-term technical issues.

An incident management procedure should also be established to handle situations where the CDS becomes unavailable or outdated.

## Monitoring
Monitoring of the CDS service is crucial to ensure optimal performance and user satisfaction. Key technical monitoring indicators include:

-   **CDS Service Availability:** The target availability should be defined by project management, but could typically be 99.9% per calendar month, excluding planned maintenance periods.
-   **Response Time:** For interactive queries, the CDS should respond in less than 2 seconds per request. In batch processing mode (e.g., for entire populations), stricter performance targets may be necessary.
-   **Request Load:** Monitoring the average and peak flow of requests will help assess the system’s capacity and inform decisions about scaling the infrastructure.

A quality-of-service monitoring could also be implemented. However, delays in updating rules and conditions could stem from multiple stakeholders, including the CDS provider, MS immunization experts, the communication team, or the Health Authority.

## Communication

The communication strategy for the tool will vary depending on how it is introduced. If integrated into preexisting workflows - such as updating patient records in existing medical software - the communication effort may be minimal. However, if the tool is introduced as a new service for health professionals or the general population, a more substantial communication effort will be required. In this case, the tool can complement existing initiatives like targeted vaccination campaigns or World Immunization Week.

Regardless of the context, specific training should be offered to health professionals, based upon the material developed in Task D.2 of the Build phase. The method of delivery will depend on how the tool is exposed to users. For a standalone interface, online video courses may suffice. However, if the tool is integrated with existing medical software, training should be delivered by the software editor, in line with the usual practices for introducing new features.

In day-to-day operations, the justifications accompanying each recommendation are also a key communication tool. These justifications should be carefully tailored for each audience - whether health professionals or the general population.
