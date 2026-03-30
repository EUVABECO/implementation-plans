# CLINICAL DECISION SUPPORT SYSTEM (CDS) - SECURITY AND PRIVACY

\| *This module details the risks for personal data security and privacy incurred within the CDS tool, and the mitigation measures used to make these risks acceptable.* \| \|\|

# Purpose

This document provides the necessary information for a data protection officer to assess the adequacy of a vaccination CDS implementation with the requirements of the European Global Data Privacy Regulation (GDPR), or any equivalent regulation for the protection of personal data.

It relies upon the CDS architecture hypothesis that are documented in Module 8 – CDS tool architecture. For an implementation that would deviate from these hypotheses a specific study would be needed.

# Characterization of the processing

## Purpose of processing

The vaccination clinical decision support system (CDS) is an online service providing personalized immunization recommendations based upon the individual characteristics of a subject and the history of previously administered vaccines.

It can be proposed:

-   as a standalone service to the general population, using data collected through online forms.
-   as a complementary service to health professionals, using data from their Electronic Health Records (EHR) application.

## Responsibilities

When the CDS is used from a system operated by a health professional, such as an Immunization Information System (IIS) or an Electronic Health Records system (EHR), the data controller is the health professional himself or the health structure employing him.

When the CDS is used from a public portal, the data controller is the public health organization proposing the service to the public.

In any case, the CDS supplier is a data processor acting on behalf of the data controller.

## Regarded persons

The CDS only processes personal data regarding the subject of the vaccination recommendations. The identity of the users is handled by the client system of the CDS, not the CDS itself.

## Nature of data

The processed data consists of:

-   Basic demographic data: date of birth, sex, country or region of residence.
-   Lifestyle data, such as presence of young children, intended or ongoing pregnancy, regular usage of drug, risky sexual behaviour.
-   Occupational data
-   Health data, such as chronical diseases, overweight, organ transplants, immunosuppressive therapies.
-   Serological test results
-   History (date and substance) of administered vaccines
-   Generally, any data required per the statutory, regulatory or scientific reasoning premises for a specific immunization recommendation.

The processed data do not include any directly identifying information.

## Lifecycle of data

The data is:

-   Collected by the client system querying the CDS.
-   Submitted through a call to the CDS service
-   Returned together with the vaccination recommendations
-   Never retained on the CDS beyond the few seconds needed to elaborate the recommendations.

It may have a lasting existence in the client system, such as the EHR application of a health professional, but this is part of another processing for the purpose of healthcare.

# Liceity of processing

## Transparency of purpose

The CDS is dedicated to the sole purpose of delivering vaccination recommendations. This is clearly stated in every documentation made available to the implementers and users of the client systems.

There is no further processing for any purpose.

## Legal basis

For the standalone service, the legal basis is the explicit consent of the user, as per articles 6.1a and 9.2a of the GDPR.

For the complement to an EHR application, the basis is the purpose of preventive medicine (article 9.2h).

Other uses, such as assessing the vaccination status of a population, could rely upon the public interest in the field of public health (article 9.2i)

## Minimization of data

The dataset is determined by the legal or regulatory rules determining the elaboration of immunization recommendations.

## Accuracy of data

The data is provided by the user and is not kept after the recommendation transaction. It may regard a non-existent person, and no update is needed.

## Retention of data

The CDS is a stateless system that does not retain any personal data beyond the few seconds needed for the elaboration of the recommendations.

# Risks management

## Evaluation of risk level

### Illegitimate access to data

The divulgation of data with the reidentification of the data subject would have a severe impact on the data subject. Some elements in the characterization of the regarded person may lead to discrimination at work, in access to a service (e.g. health insurance) and reputation impact.

This could be caused by:

-   spying the online transactions
-   usurpation of the service
-   instrumentation of the CDS software

Among the mitigation measures listed below, the relevant ones are the absence of directly identifying data, the encryption of data in transfer, the authentication of the CDS server, the traceability of changes, and personnel management rules. The reinforced obfuscation of dates could also be used when compatible with the intended use.

If these mitigation measures are applied consistently, the likelihood if the risk is extremely low.

### Unwanted modification of data

The alteration of data could result into the recommendation of a contraindicated vaccine, or the absence of recommendation for an indicated vaccine, possibly resulting in a delayed vaccination.

The impact of the administration of a contraindicated vaccine can be severe, but vaccines are administered by health professionals that are trained and responsible for checking all adverse conditions before performing a medical act. So globally the impact of unwanted modification of data can be considered as limited.

Since the data is not retained by the CDS, the alteration would have to be done on the fly, either by intervening on data in transfer or with a man-in-the middle attack. The measures of encryption of data in transfer and authentication of the CDS server make this risk extremely unlikely.

### Data disappearance

This is not relevant for this processing, that does not retain any personal data.

### Summary

| Impact       |                 |          |          |        |            |
|--------------|-----------------|----------|----------|--------|------------|
| Catastrophic |                 |          |          |        |            |
| Severe       | Confidentiality |          |          |        |            |
| Limited      | Integrity       |          |          |        |            |
| Negligible   |                 |          |          |        |            |
|              | Very unlikely   | Unlikely | Possible | Likely | Likelihood |

## Mitigation measures

Considering the above-mentioned risks, the following mitigation measures are to be considered and demonstrated to the data protection officer.

### Absence of directly identifying data

The CDS does not need to receive any directly identifying data, such as a patient name or identification number. Reidentification of a patient would require a prior knowledge of a substantial part of the submitted data, typically the birth date and the dates of previous vaccine administrations.

According to the context of use and the possibilities of access to correlative data, this measure could be strengthened more with the optional reinforced obfuscation of dates. This is mostly relevant if the CDS is dedicated to a small population (e.g. for corporate use).

### Encryption of data in transfer

Transactions between the client systems and the CDS server must be encrypted according to the state of the art, both in terms of protocol (TLS 1.2 or above) and cipher suites. This level of encryption should be verified periodically with reference tools.

### Absence of retention of data

The CDS described in the architecture document is an independent stateless system. It should not retain any of the submitted data beyond the actual delivery of the recommendations. If there is an identified need for demonstrating the authenticity of a CDS transaction, only a hashed signature of the data could still be retained.

### Authentication of the CDS server

The CDS server must be authenticated with a server certificate delivered by a trusted provider.

### Website security

The CDS by itself is limited to very few webservices with strongly typed inputs, limiting the attack surface to a minimum. Depending upon its use case, further restriction on access can be applied (IP filtering, security tokens, client certificates).

The environment used by the vaccination experts for producing and publishing the rules is potentially more vulnerable, but the very limited number of users (typically less than 10) allows for strong authentication measures. The CDS provider should organise regular penetration tests.

### Traceability of changes

All changes brought to the CDS, be it the rule processing engine or the rules by themselves, must be controlled, traced and allocated.

### Accountability of health professionals

The terms of service of the CDS must clearly state that, beyond the recommendation, it belongs to the administering health professional to check for the veracity of the submitted data and the appropriateness of the actual vaccine, particularly taking into consideration all contraindications.

### Awareness of CDS supplier personnel

The CDS supplier must have policies for quality and data protection. Its personnel, both in the technical and medical teams, must be trained, evaluated, and if needed disciplined for applying these policies.

### Certification of IT management

The IT infrastructure must be operated under a consistent information security management system, certified at least against ISO 27001:2013, or more specific certifications if applicable.

### Reinforced obfuscation

If needed, it is possible to the client system of the CDS to apply an obfuscation strategy on the dates mentioned in the requests to the CDS. A typical strategy would be:

-   For children under 18 months, round the birthdate to the first day of the next week, and each vaccine administration to a date giving the next exact number of weeks since birth.
-   From 18 months to 12 years, use the same method but rounding to months.
-   Above 12 years, use the same method but rounding to years.

As an example, for a child under 18 months, born on Tuesday, April 1st and having received a vaccine on Monday, August 4th:

-   The birth date is rounded to Monday, April 7th
-   The interval from birth to administration, 125 days, is rounded up to 7x18 = 126 days
-   The administration date is thus rounded to Monday, August 11th

This method should be used only when needed and excluded when the CDS provides information about the reimbursement conditions of administered vaccines, since these conditions are generally dependent upon exact age at the date of administration.
