# FORECASTING TOOL - SECURITY AND PRIVACY

# Purpose

This document provides the necessary information for a Data Protection Officer (DPO) or equivalent governance authority to assess the adequacy of a Forecasting Tool implementation with the European General Data Protection Regulation (GDPR), national health data regulations, cybersecurity frameworks, and ethical governance standards. It relies upon the forecasting architecture hypotheses documented in Module 8 – Forecasting Tool Architecture. For implementations significantly deviating from these architectural assumptions, additional security and privacy assessments may be required.

# Characterization of the processing

## Purpose of processing

The Forecasting Tool is an epidemiological and public health forecasting infrastructure designed to: analyse epidemiological trends, forecast outbreak dynamics, estimate healthcare system pressures, simulate intervention scenarios, support vaccination strategy planning, and support public health preparedness and response. The system may operate as a centralized forecasting platform, as a distributed interoperable infrastructure, as a national or regional epidemiological modelling environment, or as a federated forecasting ecosystem. The processing of data is limited to purposes directly related to epidemiological surveillance, outbreak forecasting, public health decision-support, healthcare preparedness, and vaccination planning. No unrelated secondary processing should occur outside explicitly authorized governance frameworks.

## Responsibilities

The data controller may vary depending on the implementation context. Potential data controllers include Ministries of Health, National Public Health Institutes, Regional Public Health Authorities, Healthcare Systems, and Authorized Surveillance Organizations. The Forecasting Tool supplier or infrastructure operator generally acts as a data processor, a technical operator, or an authorized infrastructure provider acting on behalf of the data controller. Responsibilities should be explicitly defined through governance agreements, data-sharing agreements, operational contracts, and access control policies.

## Regarded persons

The Forecasting Tool may process data regarding citizens, patients, healthcare workers, vaccinated individuals, and vulnerable population groups. However, whenever possible, forecasting systems should prioritize aggregated datasets, anonymized data, pseudonymized data, and population-level indicators. The identity of operational users should be managed through authenticated access systems, institutional identity providers, and role-based access control systems.

## Nature of data

The processed data may include epidemiological surveillance data, hospitalization indicators, intensive care unit (ICU) occupancy, mortality data, vaccination coverage, sociodemographic information, mobility indicators, genomic surveillance data, intervention timelines, and healthcare system indicators. Potentially sensitive data may include health status, chronic conditions, immunological information, geographic localization, and sociodemographic vulnerability indicators. The forecasting infrastructure should minimize processing of directly identifying information, unnecessary personal information, and excessive granularity. Where possible, only aggregated, anonymized, pseudonymized, and/or statistically necessary data, should be processed.

## Lifecycle of data

The data lifecycle generally includes collection from surveillance systems, secure ingestion, harmonization, validation, integration into forecasting models, generation of forecasting outputs, visualization and dissemination. Depending on the architecture, data may remain within source institutions, be synchronized through Application Programming Interfaces (APIs), be temporarily cached, or be processed in secure computational environments. Data retention policies should define storage duration, archival procedures, deletion procedures, backup policies, and audit retention periods.

# Liceity of processing

## Transparency of purpose

The Forecasting Tool should clearly communicate the purpose of epidemiological forecasting, the categories of processed data, governance responsibilities, operational limitations, and privacy safeguards. Transparency documentation may include privacy notices, governance frameworks, technical documentation, operational policies, and public communication materials.

## Legal basis

Potential legal bases under GDPR may include explicit consent where applicable (Articles 6.1a and 9.2a), public interest in the field of public health (Article 9.2i), preventive medicine and healthcare management (Article 9.2h), scientific research purposes (Article 9.2j), and legal obligations of public authorities. The applicable legal basis depends on implementation context, data granularity, governance structures, and national legislation.

## Minimization of data

The Forecasting Tool should process only the data necessary for epidemiological forecasting, healthcare preparedness, intervention simulation, and public health analysis. Data minimization should apply to variables, temporal resolution, geographic resolution, demographic granularity, and retention duration. Highly granular or identifiable datasets should only be processed where operationally justified.

## Accuracy of data

Forecasting accuracy depends on quality of surveillance systems, harmonization procedures, timely updates, and validation workflows. Validation mechanisms should assess completeness, plausibility, consistency, synchronization quality, reporting delays, and outliers. Forecasting systems should also document uncertainty, assumptions, model limitations, and calibration procedures.

## Retention of data

Retention periods should remain proportionate to forecasting needs, operational monitoring, legal obligations, audit requirements, and scientific reproducibility. Where possible, temporary processing, stateless architectures, federated learning approaches, or aggregated storage should be preferred. Sensitive datasets should not be retained longer than operationally necessary.

# Risks management

## Evaluation of risk level

### Illegitimate access to data

Unauthorized access to epidemiological or healthcare data could result in privacy violations, reidentification risks, discrimination, reputational harm, and misuse of sensitive health information. Potential causes include cyberattacks, unauthorized access, infrastructure vulnerabilities, insecure APIs, insider threats, and data leakage. The impact may range from moderate, to severe, depending on data granularity and sensitivity.

### Unwanted modification of data

Manipulation of epidemiological datasets or forecasting parameters could result in inaccurate forecasts, incorrect public health decisions, inappropriate allocation of healthcare resources, operational disruptions, and erosion of public trust. Potential attack vectors include tampering with surveillance data, unauthorized model modifications, manipulation of APIs, and software vulnerabilities. The impact could become severe during epidemic emergencies.

### Data disappearance

Loss of epidemiological datasets or forecasting infrastructure availability could interrupt forecasting operations, delay outbreak detection, impair healthcare preparedness, and disrupt public health decision-making. Potential causes include infrastructure failure, ransomware, synchronization errors, accidental deletion, and cloud outages.

### Misinterpretation of forecasting outputs

Forecasting systems may also create risks linked to overconfidence in projections, misunderstanding of uncertainty, inappropriate policy decisions, and misuse of scenario analyses. Transparent communication of uncertainty is therefore essential.

## Mitigation measures

Considering the above-mentioned risks, the following mitigation measures are to be considered and demonstrated to the DPO.

### Anonymization and pseudonymization

Whenever possible anonymized, aggregated, or pseudonymized data should be preferred over identifiable datasets. Direct identifiers should generally not be processed unless operationally necessary. Reidentification risks should be periodically assessed.

### Encryption of data in transfer

All data exchanges should use encrypted communication protocols, secure APIs, and encrypted synchronization channels. Encryption standards should follow state-of-the-art cybersecurity practices, national cybersecurity recommendations, and institutional governance policies.

### Encryption of data at rest

Stored datasets should be protected through encrypted databases, encrypted backups, secure key management systems, and restricted storage environments. Cloud infrastructures should comply with recognized security certifications, healthcare data governance requirements, and national cybersecurity regulations.

### Authentication and access control

The forecasting infrastructure should implement strong authentication, role-based access control, least-privilege principles, multi-factor authentication (MFA), and audit logging. Administrative access should be highly restricted. User permissions should be periodically reviewed.

### API and infrastructure security

The forecasting APIs and infrastructures should support authentication tokens, secure API gateways, rate limiting, intrusion detection, penetration testing, and vulnerability management. Where applicable, IP filtering, client certificates, or network segmentation may be implemented.

### Traceability and auditability

All critical actions should be logged, traceable, attributable, and auditable. This includes model modifications, parameter changes, software updates, access events, and data synchronization activities. Audit trails should support accountability, incident investigation, and regulatory compliance.

### Backup and disaster recovery

Operational continuity requires redundant infrastructures, backup systems, disaster recovery plans, failover mechanisms, and incident response procedures. Recovery procedures should be periodically tested.

### Cybersecurity monitoring

Continuous cybersecurity monitoring should supervise unauthorized access attempts, abnormal behaviour, malware, infrastructure vulnerabilities, API misuse, and denial-of-service attacks. Security monitoring should integrate automated alerts, incident escalation, and forensic analysis procedures.

### Personnel awareness and governance

Personnel involved in the forecasting infrastructure should receive cybersecurity training, GDPR training, operational governance training, and incident response training. Governance structures should define responsibilities, escalation procedures, accountability mechanisms, and operational policies.

### Certification and compliance

The forecasting infrastructure should ideally operate under ISO 27001-certified environments, recognized cybersecurity frameworks, or institutional governance systems. Additional certifications may be considered depending on national requirements, healthcare regulations, and operational criticality.
