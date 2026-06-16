# DATA LINKAGE PROCESS  - DATA

# Data
Data to be used will depend on the objectives defined for the data linkage process, the datasets available and allowed to be shared, as well as their structures.

As a reminder: for deterministic linkage, each datasets to be used should include a common unique personal identifier, shared among all datasets to be used, enabling the data linkage. In the absence of such an identifier, other techniques can be applicable (ref. Module 4 - *Pre-requisites*)

In the scope of the EUVABECO project, vaccination data is the main information requested as the basis of data linkage. This information can range from something as simple as whether or not a person has been vaccinated against a particular disease, to more detailed details such as the date of administration, the vaccine used and its code, whether a booster dose has been administered, and the interval between doses.

Examples of data sources, (possible) content and reachable outputs, when linked to vaccination data are reported in the table below (Module 02 – *Functional description* (*Use cases*)):

| DATA SOURCE                                            | (POSSIBLE) CONTENT                                                                                                                                                                    | (POSSIBLE) OUTPUT                                                                                                                                                                          |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Laboratory test results database                       | Data on tested patients<br>Information on test prescriptions, test results (including rapid tests), symptoms, variant, suspected false negatives and false positives                  | Identification of breakthrough cases<br>Estimation of **vaccine effectiveness against symptomatic infection**                                                                              |
| Hospitals clinical database                            | Data on hospitalised patients (e.g. comorbidities, symptoms, complications, length of stay, treatments, outcome of hospitalisation, entry and discharge of intensive care unit, etc.) | Identification and characterisation of hospitalised breakthrough cases<br>Estimation of **vaccine effectiveness against hospitalisation**                                                  |
| Healthcare professional database                       | Data allowing identification of healthcare workers (HCWs)                                                                                                                             | Determination of **vaccination coverage among healthcare workers**                                                                                                                         |
| National statistics databases                          | Socio-economic information (family composition, nationality/origin, employment status, income, etc.)<br>                                                                              | Differences in **vaccine uptake by:** <br>**Underlying conditions**<br>**Socio-economic status**<br>**Socio-demographic groups**<br>Confounders for **vaccine effectiveness** calculations |
| Insurance databases <br>(Care reimbursement databases) | Data on reimbursed care and medicines of citizens insured in the country (e.g. pseudo-pathologies as comorbidities, nursing home<br>resident status, medications, etc.)               |                                                                                                                                                                                            |

Achievable outputs will highly depends on the structures and contents of the vaccination database and linked data sources.

# Synthetic data

## Purpose

Synthetic data are used to support the technical development, testing, and validation of the data linkage process while ensuring compliance with data protection regulations. Synthetic data enable all project stakeholders to collaborate throughout the early phases of implementation, without the risk of security issues (e.g. data leaks).

## Generation methodology

The generation of synthetic datasets should follow a structured methodology, according to which it may be necessary to ensure statistical validity and confidentiality.

-   **Synthesis model selection**: The appropriate generation methods (e.g. model-based, rule-based, hybrid or fully artificial) should be selected based on data complexity and which element of the data linkage process is supposed to be tested.
-   **Validation of synthetic fidelity**: Based on the model selected, generated datasets are evaluated against the original data distributions by using appropriate statistical metrics to confirm that key analytical properties are preserved.
-   **Privacy evaluation**: Disclosure risk assessments must be applied, including identity disclosure or attribute disclosure to verify that synthetic records cannot be linked back to real individuals.

All generation scripts and parameters are required to be version-controlled and documented to ensure full reproducibility of the synthetic datasets across project phases.

## Scope and implementation

Synthetic datasets can be introduced as a key component in the early phases of the project. Synthetic data can be designed to:

-   Mimic the structure, variables, and statistical distributions of real-world datasets used in the context of the linkage process (e.g. mortality, vaccination, hospitalisation data, etc).
-   Simulate the complete data linkage process, including matching procedures based on pseudonymised identifiers, replicating the actual flow between data providers, the TTP, and analysts.
-   Allow testing of:
-   Linkage algorithms and matching rules, to assess their accuracy and robustness prior to use with real data.
-   Data quality checks and validation procedures, including completeness, plausibility, and compliance controls.
-   Train data analysts and test analytical scripts developed in R or SAS prior to their application on sensitive data.
-   Reproduce realistic use cases, thereby supporting iterative development and reducing the risk of errors when transitioning to real data.

It should be explicitly documented that synthetic data do not contain any real personal data and are entirely artificially generated, and are produced in compliance with GDPR, as they do not allow identification of real individuals.

**Link with architecture**

Synthetic data can be used upstream of real data integration and form an integral part of the technical environment described in *Module 8 - Architecture*, to validate the system’s design, scalability, robustness and compliance, without risking real data exposure. They can be mobilised during :

-   **System testing** : To verify that the secure data server, data transfer protocols, performance, pseudonymisation and accuracy procedures are correctly configured. To validate the technical infrastructure, including data environments, pipelines, and access control mechanisms.
-   **Workflow validation**: To test the full end-to-end data flow, from data providers through the TTP to the operational environment.

Synthetic data can support the structured transition across the three implementation phases :

-   **Development**: Building and configuring the technical infrastructure using simulated data.
-   **Validation**: Confirming that all components of the process function as intended and are secure before moving to production.
-   **Production**: Onboarding real data only once all systems and processes have been validated.

**Link with verification**

Synthetic datasets can support the verification activities described in Module 12, by simulating scenarios with known linkage outcomes, allowing direct comparison between expected and observed results before production release.

Specifically, they allow testing across the five data quality dimensions defined in Module 12: completeness, conformance, consistency, plausibility and representativeness.

This benchmarking approach provides an objective basis for assessing linkage tool performance prior to deployment, within both the technical and operational environments described in Module 12.
