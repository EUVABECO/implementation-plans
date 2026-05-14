# EUROPEAN VACCINATION CARD (EVC) - SECURITY AND PRIVACY

# Purpose

This document provides the necessary information for a data protection officer to assess the adequacy of an EVC implementation with the requirements of the European Global Data Privacy Regulation (GDPR), or any equivalent regulation for the protection of personal data.

It relies upon the EVC architecture hypothesis that are documented in Module 8 – EVC tool architecture. For an implementation that would deviate from these hypotheses a specific study would be needed.

# Identification of the processing

The EVC by itself is a private document held by a natural person that does not fall under the scope of the GDPR. Yet this document considers:

-   The processing required to deliver an EVC
-   The new uses that could be induced by the existence of the EVC

## Processing to deliver an EVC

The delivery by a health professional to his patient of a document from its electronic health record (EHR) is a preexisting processing routinely used.

The specificity of the EVC lies into the transaction used to sign the EVC digital content. Several implementations are possible, such as:

-   Local – The signature is performed locally within the delivering EHR system. Each delivering system keeps its own secrets for signature.
-   Centralized – The data to be signed is submitted to a central server holding the secrets for signature.
-   Distributed – The signature process is split between the delivering EHR system and a central signer. Only a hash of the signed information is sent to the signing server.

To preserve the security of signature secrets and the simplicity for EHR systems suppliers, the implementation plan assumes a centralized model. This implies that the signature process is a specific processing of personal data distinct from the requesting EHR system. It is this processing that will be discussed here.

## Potential induced processing

The EVC in its content is identical to legacy paper vaccination cards. Its sole purpose is to facilitate continuity of care by allowing citizens to transmit reliably and efficiently their vaccination history to a caring health professional.

Yet, its digital signature may also suggest its use as a vaccination proof for administrative purposes, typically for occupations where given vaccinations are mandatory.

Such a use for the EVC should have a specific legal basis. Moreover, in such a case the required proof should not be the EVC by itself, with the full history of administered vaccinations, but a minimized vaccination certificate, delivered by a decision support system on the basis of the EVC content, limited to a binary statement of compliance with a predefined set of rules.

The definition of how such a vaccination certificate could be derived from the vaccination card was not in the scope of the EUVABECO project. Yet chapter 4 details considerations on the personal data protection for such a use.

# Processing to deliver an EVC

## Characterization

### Purpose

The purpose of the process is to generate a document based upon the existing data in the delivering electronic health records. This document consists of a signed history of administered vaccines.

### Responsibilities

The EVC is delivered by an accredited health professional. Either the delivering health professional or the health structure employing him is the data controller.

The delivery of an EVC implies (in this implementation) the submission of its digital content to a signature server. The operator for the signature server is a data processor acting on behalf on the data controller. Typically, he will also be a part or a subcontractor of the national public health authority.

### Regarded persons

The only regarded person is the EVC subject.

### Nature of data

The processed personal data consists of:

-   Basic demographic data: date of birth, family name and given name
-   History (date and substance) of administered vaccines

### Lifecycle of data

The data is:

-   Collected within the delivering health professional EHR.
-   Submitted through a call to the signature service
-   Returned under the format of a compacted and signed block of data.
-   Used by the delivering EHR to build a PDF document including the same data in human readable format and as a digital content.
-   Kept lastingly by the regarded person, either as a printout or as the PDF document itself.
-   Never retained on the signature server beyond the few seconds needed to elaborate the answer.

## Liceity of processing

### Transparency of purpose

The processing is dedicated to the sole purpose of delivering the EVC.

There is no further processing for any purpose.

### Legal basis

The legal basis is the explicit consent of the patient, as per articles 6.1a and 9.2a of the GDPR.

### Minimization of data

Beyond the vaccination history, that is the core purpose of the EVC, the contained data consists only of minimal identity traits used for regulatory identity verification by health professionals against an acceptable identity document.

### Accuracy of data

The data mirrors exactly what is in the EHR of the delivering health professional. If needed, it can be corrected under the responsibility of the health professional, as long as the data in the EVC and the referenced master records remain consistent.

### Retention of data

The EVC data is kept only into the document held by the patient.

## Risks management

### Evaluation of risk level

#### Illegitimate access to data

If the data in the EVC was divulgated, the history of administered vaccines may indirectly reveal some health characteristics of the data subject. For example, reinforced vaccination schemes are applied for immune-compromised persons. In such cases, the impact could be severe.

Yet, this data is present in the EHR independently of the EVC delivery. The EVC specific risks regard:

-   The signature process, during the delivery of the EVC
-   Further divulgation of the EVC document, either when transmitted by the HCP to the patient or later when under the control of the patient.

Regarding the signature process, this could be caused by:

-   spying the online transactions
-   usurpation of the service
-   instrumentation of the signing software

Among the mitigation measures listed below, the relevant ones are the encryption of data in transfer, the authentication of the signature server, the traceability of changes, and personnel management rules.

If these mitigation measures are applied consistently, the likelihood if the risk is extremely low.

Regarding the divulgation of the EVC after its delivery, with such scenarios as compromission of an e-mail sent by the HCP or of an EVC stored into a public cloud, the level of risk is the same with an EVC as with any personal document. Modern content analysis tools do not need a structured content for retrieving the information.

#### Unwanted modification of data

The alteration of data may result in inadequate further vaccinations, or possibly a delayed reaction if a patient was infected with a disease when pretendedly vaccinated, with a limited impact. Still, this is much more probable without an EVC.

The digital signature of the EVC precludes any modification of data.

The alteration of data could result into the recommendation of a contraindicated vaccine, or the absence of recommendation for an indicated vaccine, possibly resulting in a delayed vaccination.

The impact of the administration of a contraindicated vaccine can be severe, but vaccines are administered by health professionals that are trained and responsible for checking all adverse conditions before performing a medical act. So globally the impact of unwanted modification of data can be considered as limited.

Since the data is not retained by the CDS, the alteration would have to be done on the fly, either by intervening on data in transfer or with a man-in-the middle attack. The measures of encryption of data in transfer and authentication of the CDS server make this risk extremely unlikely.

#### Data disappearance

This is not relevant for this processing, that does not retain any personal data.

#### Summary

| Impact       |                 |          |          |        |            |
|--------------|-----------------|----------|----------|--------|------------|
| Catastrophic |                 |          |          |        |            |
| Severe       | Confidentiality |          |          |        |            |
| Limited      | Integrity       |          |          |        |            |
| Negligible   |                 |          |          |        |            |
|              | Very unlikely   | Unlikely | Possible | Likely | Likelihood |

### Mitigation measures

Considering the above-mentioned risks, the following mitigation measures are to be considered and demonstrated to the data protection officer.

#### Encryption of data in transfer

Transactions between the EHR and the signature server must be encrypted according to the state of the art, both in terms of protocol (TLS 1.2 or above) and cipher suites. This level of encryption should be verified periodically with reference tools.

#### Absence of retention of data

The signature server described in the architecture document is an independent stateless system. It should not retain any of the submitted data.

#### Authentication of the signature server

The signature server must be authenticated with a server certificate delivered by a trusted provider.

#### Website security

The signature server offers a single endpoint, limiting the attack surface to a minimum. Depending upon its use case, further restriction on access can be applied (IP filtering, security tokens, client certificates).

#### Access control

The signature server must be accessible only from allowed EHR systems by accredited health professionals. The check for accreditation belongs to the client EHR system, typically according to the profession of the using health professional. Depending upon the architecture, the allowance for the EHR system can be implemented by different technological means, from closed local networks to distribution of client certificates, as described in the EVC deployment module.

#### Certification of IT management

The signature infrastructure must be operated under a consistent information security management system, certified at least against ISO 27001:2013, or more specific certifications if applicable.

#### Distributed computation of signature

If needed, it is possible to split the signature process between the client EHR system, performing all the data compression process until the computation of the hash value for the content to be signed, and the signature performed only on the hashed value. Yet this induces a much more complex and costly work for the EHR suppliers, for a security benefit that is quite limited.
