CLINICAL DECISION SUPPORT SYSTEM (CDS) - DATA

| *This module details the external data that is needed for the operation of the CDS tool in terms of content, format and sources.* |
||

# Vaccine codes

To elaborate recommendations, the CDS needs the history of previously administered vaccines.

This history is made of a list of administration events, each event consisting of the date of administration and the product that was administered.

This history may contain vaccines that were administered decades ago, or abroad. These vaccines could be identified as an explicit branded product or with a vaguer description, such as “Tdap” (some vaccine with the three valences tetanus, diphtheria low dose, acellular pertussis low dose), or even “Vaccine against poliomyelitis”.

Using the most precise available information is important. Routine vaccination schedules are written based upon actual products summaries of product characteristics, and trying to reinterpret them with generic descriptions may be misleading and create a responsibility blur between the NITAG and the digitization team.

Oppositely, catchup vaccination strategies require to understand the role of a foreign or past vaccine, that is not explicit only from its code or name. The codes used must be complemented with a minimal functional description of the vaccine, characterizing the effect on the human immunity system.

The existing electronic records of vaccinations rely upon heterogeneous code systems, such as national pharmaceutical codes (PZN, CIS, CNK, etc.), regional codes (CVX, EU identifier for centrally approved vaccines, etc.) or international generic codes (ATC, ICD-11, SNOMED-CT).

To gather all of these in a comprehensive and descriptive representation, EUVABECO endorses the NUVA unified nomenclature of vaccines, supported by the International Vaccine Codes Initiative[^1]. This pivot codification, used also in the EUVABECO European Vaccination Card, is built to integrate the alignments with any code system as well as a functional description of each vaccine concept.

[^1]: <https://ivci.org>

# HALO factors

To elaborate the recommendations, the CDS needs the characterization of the regarded person. This characterization consists of Health, Ageing, Lifestyle and Occupation characteristics, known as HALO factors.

The HALO factors are identified by the NITAGs when elaborating the vaccination schedules for their health jurisdiction. They may be extremely diverse, ranging from basic notions such as age or sex to complex situations like living with an immunocompromised person.

When the CDS is invoked from a professional health application, it is desirable that the HALO factors are populated from the existing records. Yet, this is only partially achievable for many reasons:

-   The list of HALO factors is variable across time (new recommendations are issued on a monthly basis) and location (recommendations are country specific).
-   The equivalence between a HALO factor and an existing record must be assessed. This can be done through existing vocabularies of medical information. But these vocabularies themselves are diverse, either national (such as KMEHR in Belgium) or international (ICPC, ICD-11, SNOMED-CT)
-   Even if a matching concept is found in an existing record, it may be outdated. Diabetes is a persistent condition; pregnancy is not.

Yet, these difficulties should not exclude the use of such preexisting data, at least to populate a set of HALO characteristics submitted to human review before submitting. To support this, the EUVABECO project suggests that:

-   For any CDS implementation a list of its relevant HALO factors is published and maintained.
-   Whenever possible, these factors are provided with alignments with one or several health vocabularies.
-   The HALO factors for a CDS implementation can be fetched from higher level lists of HALO factors, published by health authorities at the regional, national or international level.

The overall structure of a HALO factors directory is described in TO BE DONE.

# Others

The rules for the CDS are elaborated from the documentation provided by the NITAG. This documentation could itself be structured as rules, or as content that can be converted to rules. This is for example the case of the CDSi project from the US NITAG, the ACIP.

The CDSi dataset is used to produce CDS rules, as well as test profiles for compliance of CDS implementations.

Not all NITAGs will reach this level of maturity in a near future. Yet, the EUVABECO project will contribute to the emergence of this approach with the publication of a common syntax for CDS rules described in this supporting document. The rulesets elaborated during the pilot projects are exposed HERE using this syntax.
