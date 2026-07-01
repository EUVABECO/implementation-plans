---
title: Forecasting data
---
# FORECASTING TOOL - DATA

# Epidemiological surveillance data

The effectiveness of epidemiological forecasting strongly depends on the availability of high-quality, timely, and geographically detailed surveillance data. The Forecasting Tool requires epidemiological datasets describing infection incidence, confirmed cases, test positivity, hospitalization burden, intensive care unit (ICU) admissions, mortality, and outbreak dynamics over time. Where available, next-generation data sources, such as wastewater surveillance data, digital epidemiology signals, participatory surveillance platforms, wearable device data, and other novel data streams, may complement traditional surveillance systems and enhance forecasting capabilities. These datasets should ideally be continuously updated, standardized, geographically granular, temporally resolved, and stratified by age and sex/gender where available. The primary sources of epidemiological surveillance data may include national public health institutes, surveillance systems, ministries of health, hospital reporting systems, regional public health authorities, and international surveillance repositories. The quality and completeness of surveillance data directly influence forecasting precision and model reliability.

# Healthcare system and resource data

The Forecasting Tool requires healthcare system indicators to estimate healthcare burden and operational resilience. Relevant healthcare data include hospital bed occupancy, ICU capacity, ventilator availability, healthcare workforce indicators, emergency department activity, pharmaceutical supply chain indicators, and healthcare utilization metrics. These data allow forecasting of healthcare system saturation, resource shortages, operational pressures, and treatment demand. Healthcare data should ideally be updated in near real-time during outbreaks and harmonized across reporting institutions.

# Vaccination data

Vaccination-related data are essential for modelling intervention effects and population immunity dynamics. Relevant vaccination datasets include vaccine coverage, vaccine uptake by age group, booster campaigns, vaccine schedules, vaccine effectiveness estimates, and temporal deployment information. Vaccination data should preferably be geographically stratified, temporally resolved, linked to demographic structures, and continuously updated. These datasets may originate from immunization information systems, national vaccination registries, public health authorities, and healthcare providers.

# Genomic surveillance data, including Variants of Concern

The Forecasting Tool integrates genomic surveillance information regarding circulating variants of concern (VOCs), prevalence of variants over time, regional distribution of variants, transmissibility changes, immune escape characteristics, and severity indicators. Genomic surveillance data help forecasting systems adapt to evolving outbreak conditions and support recalibration of epidemiological parameters. Potential data sources include genomic surveillance laboratories, sequencing consortia, national surveillance programmes, and international repositories. The availability and timeliness of genomic surveillance data significantly affect the ability to anticipate epidemiological transitions.

# Non-Pharmaceutical Intervention Data

The Forecasting Tool requires information regarding implemented public health interventions and policy measures. Relevant NPI datasets may include school closures, lockdown measures, mask mandates, travel restrictions, social distancing policies, testing strategies, quarantine regulations, and public gathering restrictions. Intervention timelines are necessary to evaluate intervention effectiveness, behavioural changes, transmission dynamics, and scenario simulations. These data may be collected from government reports, public health authorities, policy tracking systems, and international databases.

# Sociodemographic and Population Data

Demographic datasets are required to support population stratification, age-specific modelling, healthcare demand estimation, regional forecasting, and vulnerability assessments. Relevant demographic variables include population size, age distribution, sex/gender distribution, regional population density, mobility patterns, and household composition. Demographic data may originate from national statistical offices, census databases, population registries, and mobility datasets.

# Behavioural and Mobility Data

Where available, behavioural and mobility data may improve forecasting accuracy by capturing population movement, behavioural adaptation, healthcare-seeking behaviours, adherence to interventions, and social mixing patterns. Potential data sources include mobility reports, transportation datasets, survey data, and aggregated digital mobility indicators. The use of behavioural and mobility data should comply with all applicable privacy and ethical regulations.

# Data format and inter-operability

The Forecasting Tool requires standardized and interoperable data formats to support automated ingestion, harmonization, reproducibility, scalability, interoperability between Member States (MS). Preferred characteristics include machine-readable formats, standardized coding systems, structured metadata, documented schemas, Application Programming Interface (API)-based access where possible. Data harmonization procedures should address inconsistent variable naming, missing values, temporal inconsistencies, geographic mismatches, and heterogeneous reporting practices. Where possible, interoperability with national health information systems, surveillance infrastructures, healthcare databases, and vaccination registries should be supported.

# Data quality and validation

The quality of forecasting outputs strongly depends on data reliability. Data validation procedures should assess completeness, consistency, timeliness, plausibility, reporting delays, outlier detection, duplication, and harmonization quality. Automated validation checks should identify corrupted records, inconsistent entries, missing variables, abnormal trends, and synchronization failures. Data quality monitoring should be continuous and integrated into operational workflows.

# Data governance, security, and monitoring

The Forecasting Tool may process sensitive epidemiological and healthcare-related data requiring robust governance and security frameworks. Data governance should define data ownership, access permissions, data-sharing agreements, retention policies, accountability mechanisms, and audit procedures. Security measures should include encryption, secure APIs, authentication systems, access control, cybersecurity monitoring, backup procedures, and disaster recovery plans. Where personal or sensitive data are processed, compliance with General Data Protection Regulation (GDPR), national data protection regulations, and ethical governance standards must be ensured.

# Limitations and Data gaps

The availability of high-quality epidemiological data may vary substantially between implementing MS. Potential limitations include incomplete reporting, delayed updates, lack of geographic granularity, inconsistent definitions, absence of age stratification, missing healthcare indicators, and limited genomic surveillance coverage.

Where data gaps exist, forecasting systems may rely on aggregated datasets, proxy indicators, literature-derived assumptions, publicly available international data, and statistical imputation methods. However, reduced data quality or granularity may limit forecasting precision, interpretability, operational usefulness, and robustness of intervention analyses.

Another viable option could be represented by synthetic data, which may be used to support the development, testing, calibration, and validation of forecasting models and associated analytical pipelines. Synthetic datasets can facilitate algorithm development, system verification, interoperability testing, training activities, and scenario-based simulations while minimizing privacy and data protection concerns. However, synthetic data should not be considered a substitute for real-world data during operational deployment, as they may not fully capture the complexity, heterogeneity, biases, and uncertainties present in real populations and healthcare systems. Forecasting models developed or tested using synthetic data should therefore undergo subsequent validation using representative real-world datasets whenever possible. Clear documentation of synthetic data generation methods, underlying assumptions, and limitations should be maintained to ensure transparency, reproducibility, and appropriate interpretation of forecasting results.
