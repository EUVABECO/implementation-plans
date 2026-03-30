# EUROPEAN VACCINATION CARD (EVC) - DATA

| *The purpose of EUVABECO is to deliver to Member States implementation plans for several tools able to support existing or future vaccination practices.*<br>*These implementation plans are practical guides for a Member State to decide upon the launch of an implementation project, assign adequate resources, deploy the given tool and keep it operational after deployment.*<br>*This module details the external data that is needed for the operation of the EVC tool in terms of content, format and sources.* |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

# Vaccine codes

The EVC payload is a list of administration events, each event consisting of the date of administration and the product that was administered.

This history may contain vaccines that were administered decades ago, or abroad. These vaccines could be identified as an explicit branded product or with a vaguer description, such as “Tdap” (some vaccine with the three valences tetanus, diphtheria low dose, acellular pertussis low dose), or even “Vaccine against poliomyelitis”.

Using the most precise available information is important. Routine vaccination schedules are written based upon actual products summaries of product characteristics, and trying to reinterpret them with generic descriptions may be misleading and create a responsibility blur between the NITAG and the digitization team.

Oppositely, catchup vaccination strategies require to understand the role of a foreign or past vaccine, that is not explicit only from its code or name. The codes used must be complemented with a minimal functional description of the vaccine, characterizing the effect on the human immunity system.

The existing electronic records of vaccinations rely upon heterogeneous code systems, such as national pharmaceutical codes (PZN, CIS, CNK, etc.), regional codes (CVX, EU identifier for centrally approved vaccines, etc.) or international generic codes (ATC, ICD-11, SNOMED-CT).

To gather all of these in a comprehensive and descriptive representation, EUVABECO endorses the NUVA unified nomenclature of vaccines, supported by the International Vaccine Codes Initiative[^1]. This pivot codification, used also in the EUVABECO European Vaccination Card, is built to integrate the alignments with any code system as well as a functional description of each vaccine concept.

[^1]: <https://ivci.org>

# Health structures identification

Depending upon the implementation in a given country, the master records can be centralized in a country-wide immunization information system or remain distributed within the vaccinating health structures.

In this last case, the structures holding master records must be identified and referenced into the national registry of repositories. This referencing could be based upon preexisting identifiers for the health structures.

# Accredited health care professionals

The access to the signing infrastructure for an EVC should only be granted to health professionals accredited for recording or performing vaccination and delivering the updated EVC.

This would generally rely upon preexisting directories of healthcare professionals, and possibly on existing authorization portals, such as the ones used for obtaining the reimbursement of vaccination acts.
