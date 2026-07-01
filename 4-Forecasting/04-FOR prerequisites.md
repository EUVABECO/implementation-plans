---
title: Forecasting prerequisites
---
# FORECASTING TOOL - PREREQUISITES

# Prerequisites

## Assessment of prerequisites

*Prerequisites represent the broader context or resources necessary for the successful implementation and operation of the Forecasting Tool. Although not specific to the tool itself, these prerequisites are essential for ensuring its proper functioning once deployed.*

### Operational

For the Forecasting Tool to function effectively, implementing Member States (MS) must establish clear operational governance structures involving public health authorities, epidemiological surveillance units, healthcare institutions, data governance bodies, and technical support teams. The implementation of the tool requires clearly defined roles and responsibilities for data collection, data validation, epidemiological analysis, model calibration, operational monitoring, cybersecurity, and reporting workflows. Continuous collaboration between healthcare providers, surveillance systems, public health authorities, and technical teams is necessary to ensure reliable and timely forecasting outputs.

A further key component if that the tool is not treated as a one-off technical build, but as a continuously managed public health capability. Model validation is therefore defined as an ongoing activity requiring explicit acceptance criteria, including predictive performance against historical data, robustness to uncertainty, and interpretability for non-technical users. During operation, technical verification, scientific validation, and operational readiness assessment is an ongoing process. Therefore, implementing MS should establish regular reporting mechanisms, operational standard operating procedures (SOPs), escalation protocols, communication workflows, and training programmes for end-users and administrators. They should also ensure the availability of all prerequisites throughout the whole period of use of the forecasting tool.

### Legal and ethical

The Forecasting Tool may process epidemiological and healthcare-related datasets that could include sensitive health information. Therefore, implementation requires compliance with the General Data Protection Regulation (GDPR), national health data regulations, ethical governance frameworks, and institutional data-sharing agreements. Implementing MS should establish clear data governance frameworks, ethical oversight mechanisms, audit trails, accountability procedures, and secure data access controls. Where possible, datasets should be anonymized or pseudonymized before integration into forecasting workflows. Data minimization principles should be applied to reduce unnecessary exposure of sensitive information. Transparent governance procedures should ensure that data ownership is clearly defined, access permissions are documented, forecasting outputs are responsibly communicated, and ethical implications of modelling assumptions are properly considered.

### Policy

Political and policy support are critical prerequisites for the successful adoption and sustainability of the Forecasting Tool. Implementation requires alignment with national public health preparedness strategies, outbreak response frameworks, digital health strategies, emergency preparedness policies, and European public health coordination initiatives. Stakeholder engagement activities should involve ministries of health, national public health institutes, regional authorities, healthcare providers, policymakers, and citizen representatives. Clear communication strategies are necessary to explain: the objectives of the forecasting tool, the limitations of epidemiological forecasts, uncertainty associated with predictive models, and the role of forecasting in evidence-based policymaking. Pilot demonstrations and validation exercises can help strengthen trust and support among policymakers and stakeholders.

### Technical

The successful deployment of the Forecasting Tool requires robust technical infrastructure capable of supporting epidemiological modelling, large-scale data integration, real-time forecasting, secure data exchange, and continuous monitoring. The required infrastructure includes modern multi-core servers, scalable cloud or hybrid computing environments, high-speed internet connectivity, secure Application Programming Interfaces (APIs), redundancy systems, and backup and disaster recovery mechanisms. The forecasting environment should support database hosting, automated data pipelines, epidemiological simulation engines, interactive dashboards, visualization systems, and interoperability with national health information systems. Technical infrastructures should also include cybersecurity protections, secure authentication systems, monitoring tools, automated alerts, and software maintenance procedures.

### Data availability

The effectiveness of epidemiological forecasting strongly depends on the availability of high-quality, timely, and geographically detailed data. Implementing MS should ideally provide incidence and surveillance data, hospitalization data, intensive care unit (ICU) admissions and bed capacity, mortality data, vaccination coverage, genomic surveillance data regarding variants of concern (VOCs), demographic data, healthcare capacity indicators, and non-pharmaceutical intervention (NPI) timelines. Data should be standardized, harmonized, regularly updated, geographically granular where possible, and stratified by age and sex/gender where available.

The reference temporal unit is the day, and the minimum spatial resolution is at the national level, with sub-national resolution implemented where feasible. Data should be disaggregated by age, sex/gender, and, whenever possible, relevant clinical risk groups.

Where available, data should also be stratified by sex/gender and by vaccination status (including primary vaccination and booster doses), in order to support more granular modelling of epidemiological dynamics.

The implementation must include a **formal definition of all data used by the forecasting tool**. A **variable charter** must document for each variable the following information:

1.  definition, units, and scope;
2.  data source;
3.  update frequency (preferably daily);
4.  known limitations;
5.  responsible authority.

An example of a variable charter is provided below:

| **Variable Name**       | **Definition / Scope**                                                 | **Unit**      | **Stratification** | **Data Source**                 | **Update Frequency** | **Known Limitations**                                               | **Responsible Authority**        | **Missing Data Handling**               |
|-------------------------|------------------------------------------------------------------------|---------------|--------------------|---------------------------------|----------------------|---------------------------------------------------------------------|----------------------------------|-----------------------------------------|
| Daily confirmed cases   | Number of laboratory-confirmed COVID-19 cases reported in previous 24h | Cases/day     | Age, sex, region   | National Surveillance System    | Daily                | Reporting delays on weekends; under-detection of asymptomatic cases | Directorate-General of Health    | Backfill applied after 72h              |
| ICU occupancy           | Number of occupied ICU beds by COVID-19 patients                       | Patients      | Region             | Hospital Reporting Platform     | Daily                | Some hospitals report with 1-day lag                                | Ministry of Health               | Missing values interpolated if \<2 days |
| Vaccination coverage    | Percentage of population with completed primary vaccination scheme     | % population  | Age, sex           | National Vaccination Registry   | Daily                | Delays in private provider uploads                                  | National Vaccination Taskforce   | No interpolation                        |
| Rt estimate             | Effective reproduction number estimated from incidence data            | Dimensionless | National           | Computed from surveillance data | Daily                | Sensitive to testing fluctuations                                   | Epidemiological Modelling Unit   | Recomputed retrospectively              |
| Hospital length of stay | Mean duration of hospitalisation for COVID-19 patients                 | Days          | Age group          | Hospital discharge database     | Weekly               | Discharge coding inconsistencies                                    | National Health Analytics Office | Exclude incomplete episodes             |

Minimum data quality rules should be defined for each dataset, including expected completeness, acceptable reporting delays, handling of missing values, and procedures for retrospective corrections. Deviations from these rules should be documented and explicitly considered during model calibration and interpretation of results.

In practice, data availability may differ significantly from the ideal dataset definition. Such discrepancies should be explicitly documented, including missing variables, limited stratification or incomplete time series, and their impact on model outputs should be assessed.

All ingested datasets should be versioned and accompanied by provenance metadata (including data source, extraction time, and revision history) to ensure full reproducibility across model runs.

In addition to observational data, **epidemiological parameters** required by the models must be explicitly.

These include, among others,

1\. incubation and latency periods;

2\. duration of infectiousness;

3\. recovery times;

4\. length of stay in hospital and ICU;

5\. transition probabilities between clinical states;

6\. transmission parameters such as R₀ and Rₜ, or algorithms to compute those parameters from data;

7\. lethality of different compartments.

Epidemiological parameters can be estimated from data, obtained from scientific literature or expert consensus.

The initial definition of epidemiological parameters should be established prior to operational deployment, while their refinement and updating are part of the continuous implementation and operational phases.

The authority responsible for defining, updating, and validating parameters must be clearly identified as a pre-requisite of the implementation. Parameter updates should be versioned, documented, and traceable across model runs to ensure transparency and reproducibility.

A minimal change-control process should be established for epidemiological parameters, specifying who can propose changes, who is responsible for scientific review, and under which conditions updated parameters are released into operational use. All parameter changes should be logged and associated with specific model versions.

As a supporting resource, MS may develop a standardised parameter governance template specifying parameter definition, source, update rules and validation procedures.

| **Parameter**              | **Meaning**                                       | **Initial Value Initial Value** | **Source Source**        | **Update RuleUUpdate Rule** | **Validation Method**                   | **Owner**              |
|----------------------------|---------------------------------------------------|---------------------------------|--------------------------|-----------------------------|-----------------------------------------|------------------------|
| Incubation period          | Time between infection and symptom onset          | 5.2 days                        | Peer-reviewed literature | Quarterly review            | Comparison with national cohort studies | Scientific Coordinator |
| Infectious period          | Duration during which transmission may occur      | 7 days                          | Literature + calibration | Updated if variant changes  | Sensitivity analysis                    | Epidemiological Team   |
| ICU transition probability | Probability of hospitalised patient requiring ICU | 12%                             | National hospital data   | Monthly recalibration       | Retrospective fit                       | Modelling Unit         |
| R₀ baseline                | Basic reproduction number                         | 2.8                             | Historical estimation    | Updated by wave             | Back-testing                            | Scientific Coordinator |

### Human resources

The implementation and long-term sustainability of the Forecasting Tool require multidisciplinary human resource capacity, including epidemiologists, mathematical modellers, statisticians, data scientists, software engineers, cybersecurity specialists, public health analysts, healthcare informaticians, and technical support personnel. Comprehensive training programmes should be developed for system administrators, end-users, public health personnel, healthcare professionals, and policymakers. Continuous technical support and maintenance teams are also necessary to ensure operational continuity.

As **minimum organisational conditions** for implementation, we recommend a core team including, at a minimum, a technical lead, a scientific lead for epidemiological modelling, a data governance lead, a project manager, and a data protection officer, supported by quality assurance and testing function. More broadly, the framework emphasises the need to separate strategic responsibilities, typically held by public authorities, from operational responsibilities, which may involve research institutions or specialised technical providers. This separation is necessary both for effective governance and for protecting scientific processes from undue political interference.

## Filling the gaps

*Meeting the prerequisites is often a long-term endeavour that goes far beyond the scope of the implementation plans. This section suggests potential workarounds for launching the forecasting project even when some prerequisites are not fully met. Although these measures may not deliver the full benefits immediately, they can create the visibility and momentum needed to justify further efforts to meet the prerequisites.*

### Operational

If implementing MS lack sufficient local operational capacity, regional collaborations and centralized technical support structures may temporarily support model deployment, server hosting, technical maintenance, and user training, operational monitoring. Shared infrastructures between multiple MS may also support pilot deployments where feasible.

### Legal and ethical

If full integration of sensitive health data is not immediately feasible due to legal or ethical constraints, the Forecasting Tool may initially rely on publicly available epidemiological datasets, aggregated surveillance data, anonymized datasets, and/or literature-derived epidemiological parameters. Forecasting activities can therefore begin using less granular data while governance frameworks and legal agreements are progressively established.

### Policy

Where political support is limited, pilot projects and demonstration studies may help illustrate the value of forecasting systems for outbreak preparedness, healthcare resource planning, and public health decision-making. Stakeholder engagement workshops, webinars, and evidence dissemination activities may progressively strengthen institutional support.

### Technical

If local technical infrastructures are insufficient, cloud-based or externally hosted infrastructures may temporarily support deployment, provided that cybersecurity requirements are met, legal constraints are respected, and data governance agreements are established. Open-source software infrastructures may also reduce implementation costs and facilitate scalability.

### Data availability

If fine-grained epidemiological data are unavailable, forecasting activities may still proceed using aggregated national datasets, proxy indicators, publicly available surveillance data, literature-derived assumptions, and/or international datasets. However, reduced data granularity may limit forecasting precision and increase uncertainty.

### Human resources

Where specialized modelling expertise is limited, implementing MS may initially rely on centralized modelling teams, academic collaborations, external technical support, training partnerships, and international collaboration networks. Progressive local capacity building should nevertheless remain a long-term objective.
