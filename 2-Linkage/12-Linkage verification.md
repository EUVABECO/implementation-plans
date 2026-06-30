# DATA LINKAGE PROCESS - VERIFICATION

Within the data processor, a distinction is made between the technical (or validation) environment, and the operational (or analysis) environment.

The **technical environment** is the location on the server where the data arrive from internal and/or external data providers. Database managers are responsible for management of the different datasets, and for ensuring that the linkages are performed correctly. Furthermore, data validation can be performed here, i.e. verification that no errors occurred during the data transfer and/or linkage.

The **operational environment** is the server location to which data analysts have access. It is also the environment in which statistical analysis and reports are based. The granularity of the operational environment should be verified as rather coarse, reducing the chance of re-identification of individuals in the database. Furthermore, the strict separation in roles and functions between staff having access to the technical and staff having access to the operational environment should be assessed.

Given that the implementation of a data linkage process may differ substantially according to the context, the parties involved, the technical infrastructure, and intended objective, due consideration should be given to the elements outlined in Module 10 - *Security and Privacy*, with a particular attention to the section *Risk Management*.

# Verification of legal obligation

As reiterated in several modules, the data linkage process must be performed according to strict data protection rules, which fails under the responsibility of the data controller or its associated DPO (Module 10 - *Security and Privacy*).

Verification of compliance with legal obligations may be carried out on the basis of evidence of compliance, depending on the context of the processing:

-   If the processing is based on consent: evidence of free, specific, informed and unambiguous consent (e.g. signed form, digital record).
-   If the processing is based on a legal obligation or a contract: a specific reference to the relevant legislation or contract.
-   If the processing is based on a legitimate interest: documentation demonstrating that the legitimate interest overrides the rights of individuals and that appropriate safeguards are in place (e.g. information letter).

# Verification of data quality criteria

The number and diversity of relevant databases define the data linkage range of applications. The quality of the data will determine the performance of the linkage tool. The quality can be broken down into various criteria that will, at a minimum, include:

-   **Completeness**: ensuring that all relevant data are completely filled in; e.g., “*is the date of vaccine administration recorded for all vaccinated persons?*”.
-   **Conformance**: refers to the extent to which the data values adhere to specified standards and formats (i.e. data values comply with permitted values or ranges; e.g., sex only has the values “*Male*”, “*Female*” or “*Unknown*”; age is a natural number and is in a specified range).
-   **Consistency**: this is the uniformity, coherence, and lack of contradiction in data across multiple datasets. It ensures that the same information (e.g., a person’s age) is represented identically across all databases.
-   **Plausibility**: checks whether data values are believable, i.e. there is a plausible sequence of events and relationships between values; e.g., vaccine administration dates falling before the first vaccine administered in the country.
-   **Representativeness**: the extent to which the study population is representative for the target population (e.g., *do they reflect the population breakdown of the country in terms of sex, age, geographical location?*).

The values for each of the indicators that can be considered as acceptable depends on the context and the purpose of the data linkage, and as such no golden standards can be given. Data is considered high quality if it is completely "*fit for its intended use*" in analysis, reporting and decision-making.

Data quality criteria can be assessed during the different stages of the data linkage process (e.g. after the release of linked data in production, or after initial usage of the data).
