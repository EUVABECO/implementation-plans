# DATA LINKAGE PROCESS - VERIFICATION

Within the data processor, a distinction is made between the technical (or validation) environment, and the operational (or analysis) environment.

The **technical environment** is the location on the server where the data arrives from internal and/or external data providers. Database managers are responsible for management of the different datasets, and for ensuring that the linkages are performed correctly. Furthermore, data validation can be performed here, i.e. verification that no errors occurred during the data transfer and/or linkage. Although nominative data are not included in the technical environment, the granularity of the data could be quite detailed (e.g. date of birth), therefore not completely ruling out the possibility of re-identification.

The **operational environment** is the server location to which data analysts have access. This is also the environment on which statistical analysis and reports are based. The granularity of the operational environment should be rather coarse, ensuring that there is no possibility of re-identification of individuals in the database. Furthermore, there should be a strict separation in roles and functions between staff having access to the technical and staff having access to the operational environment.

# Verification of user interfaces

The data linkage tool does not contain a user interface.

# Verification of rules

The number and diversity of relevant databases define the data linkage range of applications. The quality of the data will determine the performance of the linkage tool. The quality can be split up in various criteria, including:

-   **Completeness**: ensuring that all relevant data are completely filled in; e.g., “*is the date of vaccine administration recorded for all vaccinated persons?*”.
-   **Conformance**: refers to the extent in which the data values adhere to specified standards and formats (i.e. data values comply with permitted values or ranges; e.g., sex only has the values “*Male*”, “*Female*” or “*Unknown*”; age is a natural number and is in a specified range).
-   **Consistency**: this is the uniformity, coherence, and lack of contradiction in data across multiple datasets. It ensures that the same information (e.g., a persons’ age) is represented identically across all databases.
-   **Plausibility**: checks whether data values are believable, i.e. there is a plausible sequence of events and relationships between values; e.g., vaccine administration dates falling before the first vaccine administered in country.
-   **Representativeness**: the extent to which the study population is representative for the target population (e.g., *do they reflect the population breakdown of the country in terms of sex, age, geographical location?*).
