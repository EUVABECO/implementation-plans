---
title: Linkage deployment
---
# DATA LINKAGE PROCESS - DEPLOYMENT

# Project team

Setting up and then exploiting the data linkage requires experts from a large range of specific and technical fields.

Experts from each field need to collaborate in an iterative process:

-   **Health/epidemiology experts** (*data analysts* - Module 02) identify the needs to be met by the linkage, inventory the data required to do so, and compare it to the existing resources. They play a role before (work on study design, preparing an analysis plan) and after (interpreting the results, and translating it in real-world recommendations) the data linkage.
-   **Data scientists** (*data analysts* - Module 02) extract, prepare and analyse the data.
-   **Legal experts and DPO** (*legal authorities* - Module 02) ensure compliance with the legal framework and establish guidelines in terms of data protection. They are a solid understanding of GDPR and national/local rules, a general and comprehensive awareness about the EHDS can also help.
-   **IT experts** offer guidance on the technologies and resources that meet the information needs of the linkage, the protection regulations, and the security of the data

All parties remain in collaboration during the process to assess and respond to new use cases.

# Workflow

-   Define the objectives expected by the data linkage, identify the relevant datasets and ensure their interoperability (data format compatibility, use of standardised data formats and semantic interoperability).
-   Once interoperability is assessed, define a detailed protocol and description for a secure and pseudonymised data transfer and data flow, which safeguards the data during transmission and maintains privacy.
-   Draw up an agreement on the defined objectives of the data linkage and the way to meet those. In practice, it could mean reaching a compromise between the legal and technical constraints, and the ideal needs in terms of health surveillance.
-   Request a security clearance by the Data Protection Officer, and if necessary from an Ethics committee.
-   Set up the technical infrastructure which will bring data together and the system to monitor usage of linked data.
-   Depending on the complexity and number of data sources, datasets are gradually added to the data flow, allowing for a phased integration process.
-   As datasets are incorporated, indicators of data quality (e.g. plausibility, completeness, conformance, timeliness and representativeness[^1]) and the robustness of the automated processes (e.g. % of successful transfer, % of records transmitted, comparison of aggregated values between the original database and data in the operational environment) are monitored.
-   Once the data flow is established, continuous maintenance is performed to ensure smooth operation, data are made available for use.
-   Data scientists and epidemiologists collaborate to analyse the data and derive surveillance indicators, recommendations, and scientific knowledge from it.
-   Effective communication of the data is maintained to ensure that relevant stakeholders are informed and engaged.
-   Training and capacity building activities are provided to relevant stakeholders to ensure appropriate use of the system.

[^1]: *The quality dimensions cited are not specifics to linked data quality measures. These are some examples of data quality criteria, this list is not exhaustive.*

# Typical planning

As outlined in Module 04 – *Prerequisites*, the implementation of a data linkage process requires a valid legal basis that complies with all applicable national and European legal frameworks. This legal basis must authorise the sharing of data, the secondary use of data, and the processing of individual health-related data by the relevant actors.

Prior to any planning or discussion of the implementation timeline, compliance with these requirements must be verified and confirmed. The parties involved, together with their respective roles and responsibilities, must also be clearly identified as part of the preparatory phase.

| **Task**                                                              | **Timeline** |   |   |   |   |   |
|-----------------------------------------------------------------------|--------------|---|---|---|---|---|
|  **Conceptual phase**                                                 |              |   |   |   |   |   |
| A.1 Define objectives                                                 | X            |   |   |   |   |   |
| A.2 Identify relevant data sources                                    | X            |   |   |   |   |   |
| A.3 Define use case(s)                                                | X            |   |   |   |   |   |
| A.4 Define detailed project description                               | X            |   |   |   |   |   |
|  **Legal phase**                                                      |              |   |   |   |   |   |
| B.1 Coordination with external data providers and Trusted Third Party |              | X | X |   |   |   |
| B.2 Data Protection Impact Assessment\*1                              |              | X | X |   |   |   |
| B.3 Contracts                                                         |              | X | X |   |   |   |
| B.4 Application for security clearance and ethical approval           |              | X | X |   |   |   |
|  **Technical procedure**                                              |              |   |   |   |   |   |
| C.1 Define data linkage protocol and data flow                        |              | X | X |   |   |   |
| C.2 Develop secure space for data linkage                             |              | X | X |   |   |   |
|  **Approval phase**                                                   |              |   |   |   |   |   |
| D.1 Security clearance\*2                                             |              | X |   |   |   |   |
| D.2 Ethical committee approval                                        |              | X |   |   |   |   |
|  **Data transfer and linkage**                                        |              |   |   |   |   |   |
| E.1 External data transfer                                            |              |   | X | X | X | X |
| E.2 Linkage through Trusted Third Party                               |              |   | X | X | X | X |
| E.3 Disclosure Risk Assessment                                        |              |   | X | X | X | X |
|  **Analysis environment**                                             |              |   |   |   |   |   |
| F.1 Data available to researchers\*3                                  |              |   |   | X | X | X |

**\*1) Data Protection Impact Assessment (DPIA)** *is a systematic assessment of the risks to individuals’ rights and freedoms, carried out prior to any processing of personal data that is likely to result in a high risk (e.g. sensitive data, mass surveillance, automated decision-making). It enables risks to be identified, measures to mitigate them to be proposed, and compliance with the GDPR (Art. 35) to be demonstrated. (Further information are available in Module 10 - Security and privacy).*

**\*2) Security clearance** *refers to the formal authorisation allowing access to classified or restricted information, following a background check. It is the process of* *regulating the secure processing and exchange of personal data within public administrations, healthcare, and social security. Specific organisations are in place to oversee data sharing to protect citizen privacy. The exact mandate differs by country, but clearance from such a committee could be required in order to proceed with data linkage.*

**\*3) Disclosure Risk Assessment (DRA)** *is the process of evaluating the potential risk of re-identifying individuals within a dataset, particularly when dealing with small populations and/or high granularity. This risk arises when data is aggregated or presented in a way that small groups (or "small cells") contain very few individuals, making it easier to deduce their identities. DRA is crucial to protect individual privacy, especially if the dataset contains sensitive information such as health or demographic data. Conducting a DRA before making data available in an analysis environment ensures that individual privacy is preserved, sensitive data is protected, and legal obligations are met, all while maintaining the data’s usefulness for operational purposes.*

# Build resources

Below is a list of example tools and software that could be considered for different aspects of data linkage:

-   Protocol/software for data transfer
-   Data ready for analysis can be placed in a sftp server after which can access via the WinSCP app.
-   Protocol/software for operational environment access
-   [*Citrix Gateway*](https://docs.citrix.com/en-us/citrix-gateway.html)
-   Protocol/software for data analysis/management
-   [*SAS Enterprise Guide*](https://www.sas.com/en_us/software/enterprise-guide.html)
-   [*R*](https://www.r-project.org/) and [*RStudio*](https://posit.co/products/open-source/rstudio/)
-   Software for data reporting
-   [*Shiny app*](https://shiny.posit.co/)
-   [*Power BI*](https://www.microsoft.com/en-us/power-platform/products/power-bi)
-   [*Looker Studio*](https://docs.cloud.google.com/data-studio/connect-to-looker)
-   Tool to generate and manage synthetic data (Module 09 - *Data*)
-   [*Synthetic Data Vault (sdv)*](https://datacebo.com/sdv-dev/)
-   [*Synthea*](https://github.com/synthetichealth/synthea)
