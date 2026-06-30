# DATA LINKAGE PROCESS  - DATA

# Data
Data to be used will depend on the objectives defined for the data linkage process, the datasets available and allowed to be shared, as well as their structures.

As a reminder: for deterministic linkage, each dataset to be used should include a common unique personal identifier, shared among all datasets to be used, enabling the data linkage. In the absence of such an identifier, other techniques may be applicable (Module 04 - *Prerequisites*)

In the scope of the EUVABECO project, vaccination data is the main information requested as the basis of data linkage. This information can range from something as simple as whether or not a person has been vaccinated against a particular disease, to more detailed information such as the date of administration, the vaccine used and its code, whether a booster dose has been administered, and the interval between doses.

Examples of data sources, (possible) content and reachable outputs, when linked to vaccination data are reported in the table below (Module 02 - *Functional description* (*Use cases*)):

| DATA SOURCE                                            | (POSSIBLE) CONTENT                                                                                                                                                                    | (POSSIBLE) OUTPUT                                                                                                                                                                          |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Laboratory test results database                       | Data on tested patients<br>Information on test prescriptions, test results (including rapid tests), symptoms, variant, suspected false negatives and false positives                  | Identification of breakthrough cases<br>Estimation of **vaccine effectiveness against symptomatic infection**                                                                              |
| Hospitals clinical database                            | Data on hospitalised patients (e.g. comorbidities, symptoms, complications, length of stay, treatments, outcome of hospitalisation, entry and discharge of intensive care unit, etc.) | Identification and characterisation of hospitalised breakthrough cases<br>Estimation of **vaccine effectiveness against hospitalisation**                                                  |
| Healthcare professional database                       | Data allowing identification of healthcare workers (HCWs)                                                                                                                             | Determination of **vaccination coverage among healthcare workers**                                                                                                                         |
| National statistics databases                          | Socio-economic information (family composition, nationality/origin, employment status, income, etc.)                                                                                  | Differences in **vaccine uptake by:** <br>**Underlying conditions**<br>**Socio-economic status**<br>**Socio-demographic groups**<br>Confounders for **vaccine effectiveness** calculations |
| Insurance databases <br>(Care reimbursement databases) | Data on reimbursed care and medicines of citizens insured in the country (e.g. pseudo-pathologies as comorbidities, nursing home<br>resident status, medications, etc.)               |                                                                                                                                                                                            |

*The data sources identified and used in the implementation of a data linkage process are specific to each implementation protocol and registries organisation and management. These sources may be local, regional or national eHealth database.*

Achievable outputs will highly depend on the structures and contents of the vaccination database and linked data sources.

# Synthetic data

Synthetic data may be considered to support the technical development, testing, and validation of the data linkage process, facilitating collaboration among project stakeholders during early implementation phases while limiting exposure to real personal data.
