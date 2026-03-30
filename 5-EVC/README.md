# EUROPEAN VACCINATION CARD (EVC)  

# Overview

The purpose of EUVABECO is to deliver to Member States implementation plans for several tools able to support existing or future vaccination practices.

These implementation plans are practical guides for a Member State to decide upon the launch of an implementation project, assign adequate resources, deploy the given tool and keep it operational after deployment.

# Structure

The EVC implementation plan consists of the following modules. 

| Title  | Description      |
|-------|-------------------|
| [Functional description](EVC%20description.md) | Functional analysis of the EVC tool with an overview, the stakeholders using or contributing to the use of the tool, their respective functional requirements, the non-functional requirements, and a collection of use cases illustrating the desired functions.    | 
| [Prerequisites](EVC%20prerequisites.md)         | Contextual conditions that must be met before the project is launched, and a few workarounds that could be used to anticipate upon their fulfilment.  |
| [Architecture](EVC%20architecture.md)   | This module details the architecture of the EVC tool as it as been envisioned and deployed within the EUVABECO project. Assumptions made with this architecture, although minimal, condition the EVC deployment plan|
| [Data](EVC%20data.md)   | This module details the external data that is needed for the operation of the EVC tool in terms of content, format and sources. |
| [Security and Privacy](EVC%20privacy.md)  | This module details the risks for personal data security and privacy incurred within the EVC tool, and the mitigation measures used to make these risks acceptable. |
| [Deployment](EVC%20deployment.md) | This module describes the resources, workflow and planning for the deployment of the EVC tool. |
| [Verification](EVC%verification.md) | This module describes the verifications that should be applied before releasing to production a deployed EVC. |
| [Operations](EVC%20operations.md) | This module proposes an organization and assigns tasks for keeping the EVC tool operational once it has been deployed.|

# List of Abbreviations and Acronyms

This list is transversal to all modules in the EVC implementation plan.

| Abbreviation / Acronym |                                             | Meaning                                                                                                                                                                                |
|------------------------|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CBOR                   | Compact Binary Object Representation        | A concise binary data serialization format based on JSON.                                                                                                                              |
| CDS                    | Clinical Decision Support System            | A health information technology that provides person-specific information to help health and health care.                                                                              |
| COSE                   | CBOR Object Signing and Encryption          | A security standard for the CBOR format.                                                                                                                                               |
| EHR                    | Electronic Health Record                    | Systematized collection of patient health information in a digital format                                                                                                              |
| ePIL                   | Electronic Patient Information Leaflet      | Regulatory patient information leaflet, presented as an online digital resource                                                                                                        |
| EVC                    | European Vaccination Card                   | A portable, self-contained, dual format document provided to citizens to carry their vaccination history without loss of information across different health jurisdiction.             |
| GDHCN                  | Global Digital Health Certification Network | An open, interoperable public infrastructure to facilitate the verification and secure exchange of verifiable digital health certificates.                                             |
| GDPR                   | Global Data Protection Regulation           | European Union regulation of personal information privacy.                                                                                                                             |
| IIS                    | Immunisation Information System             | Information system that collects vaccination data about all persons within a geographic area.                                                                                          |
| ISO 27001              | ISO/IEC 27001:2022                          | International standard for information security management.                                                                                                                            |
| JSON                   | JavaScript Object Notation                  | Open standard file format that uses human readable text to transmit data objects consisting of attribute-value pairs and arrays.                                                       |
| MR                     | Master Record                               | A vaccination record held by any authorized EHR application in Europe attesting that the vaccination was performed or recorded by an accredited health professional using this system. |
| MS                     | Member State                                | Any European country of the European Union                                                                                                                                             |
| NUVA                   | Nomenclature Unifiée des Vaccins            | A public ontology of vaccines designations, aligned with many vaccine code systems.                                                                                                    |
| PDF                    | Portable Document Format                    | A standard file format to present documents in a manner independent of application software, hardware and operating systems.                                                           |
| PKI                    | Public Key Infrastructure                   | Set of roles, policies, hardware, software and procedures needed to create, manage, distribute, use, store and revoke digital certificates and manage public-key encryption.           |
| RFC                    | Request for Comments                        | A publication in a series from the principal technical development and standard-settings bodies for the Internet.                                                                      |
| QR Code                | Quick Response Code                         | A type of two-dimensional matrix bar code, used to store information as a machine-readable optical image.                                                                              |
| WHO                    | World Health Organisation                   | Agency of the United Nations responsible for international public health.                                                                                                              |
| X509                   | ITU X.509 standard                          | Standard defining the format of public key certificates, binding an identity (a hostname, or an organisation, or an individual) to a public key using a digital signature.             |
