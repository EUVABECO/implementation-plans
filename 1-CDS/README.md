# CLINICAL DECISION SUPPORT SYSTEM (CDS)

# Overview

The purpose of EUVABECO is to deliver to Member States implementation plans for several tools able to support existing or future vaccination practices.

These implementation plans are practical guides for a Member State to decide upon the launch of an implementation project, assign adequate resources, deploy the given tool and keep it operational after deployment.

# Structure

The CDS implementation plan consists of the following modules.

| Title                                          | Description                                                                                                                                                                                                                                                       |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Functional description](CDS%20description.md) | Functional analysis of the CDS tool with an overview, the stakeholders using or contributing to the use of the tool, their respective functional requirements, the non-functional requirements, and a collection of use cases illustrating the desired functions. |
| [Prerequisites](CDS%20prerequisites.md)        | Contextual conditions that must be met before the project is launched, and a few workarounds that could be used to anticipate upon their fulfilment.                                                                                                              |
| [Architecture](CDS%20architecture.md)          | This module details the architecture of the CDS tool as it as been envisioned and deployed within the EUVABECO project. Assumptions made with this architecture, although minimal, condition the CDS deployment plan                                              |
| [Data](CDS%20data.md)                          | This module details the external data that is needed for the operation of the CDS tool in terms of content, format and sources.                                                                                                                                   |
| [Security and Privacy](CDS%20privacy.md)       | This module details the risks for personal data security and privacy incurred within the CDS tool, and the mitigation measures used to make these risks acceptable.                                                                                               |
| [Deployment](CDS%20deployment.md)              | This module describes the resources, workflow and planning for the deployment of the CDS tool.                                                                                                                                                                    |
| [Verification](CDS%25verification.md)          | This module describes the verifications that should be applied before releasing to production a deployed CDS.                                                                                                                                                     |
| [Operations](CDS%20operations.md)              | This module proposes an organization and assigns tasks for keeping the CDS tool operational once it has been deployed.                                                                                                                                            |

# List of Abbreviations and Acronyms

This list is transversal to all modules in the CDS implementation plan.

| Abbreviation / Acronym |                                                | Meaning                                                                                                                                                                    |
|------------------------|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| API                    | Application Programming Interface              | Software interface between two computer systems.                                                                                                                           |
| CDC                    | Centre for Disease Control                     | US public health agency                                                                                                                                                    |
| CDS                    | Clinical Decision Support System               | A health information technology that provides person-specific information to help health and health care.                                                                  |
| CDSi                   | Clinical Decision Support for Immunisations    | Process defined by the US CDC to determine the US recommended immunisations needed for a patient.                                                                          |
| EHR                    | Electronic Health Record                       | Systematized collection of patient health information in a digital format                                                                                                  |
| EVC                    | European Vaccination Card                      | A portable, self-contained, dual format document provided to citizens to carry their vaccination history without loss of information across different health jurisdiction. |
| FHIR                   | Fast Healthcare Interoperability Resources     | Standard for exchanging electronic health care data.                                                                                                                       |
| GDPR                   | General Data Protection Regulation             | European Union regulation 2016/679 on personal information privacy.                                                                                                        |
| GNN                    | Global NITAG Network                           | Platform for sharing experiences and best practices among NITAGs                                                                                                           |
| HALO                   | Health, Age, Living conditions and Occupation  | Factors conditioning the immunisation recommendations for a patient.                                                                                                       |
| HPV                    | Human Papillomavirus                           | Vaccine preventable infection by a virus from the Papillomavirus family.                                                                                                   |
| IIS                    | Immunisation Information System                | Information system that collects vaccination data about all persons within a geographic area.                                                                              |
| MDR                    | Medical Device Regulation                      | European Union regulation 2017/745 of medical devices.                                                                                                                     |
| NITAG                  | National Immunization Technical Advisory Group | Expert body that provides evidence-based recommendations on immunization policy and practice.                                                                              |
| NUVA                   | Nomenclature Unifiée des Vaccins               | NUVA, developed by vaccinologists, is both a vocabulary and a comprehensive knowledge base                                                                                 |
| SMS                    | Short Message Service                          | Text messaging component of mobile phone services.                                                                                                                         |
