# DATA LINKAGE PROCESS - PREREQUISITES

## Assessment of prerequisites

*Prerequisites represent the broader context or resources necessary for the successful implementation and operation of the data linkage process. Although not specific to the tool itself, these prerequisites are essential for ensuring its proper functioning once deployed.*

### Legal and ethical

**Legal authorisation**

Implementation of the data linkage process must have a valid legal basis complying with all applicable national and European legal frameworks[^1], which are checked by a legal department. The legal department must assess whether the implementer operates under a specific mandate or legal exemption allowing the deployment of the tool. If the linkage is not mandated under national or regional law as a public task, a GDPR-compliant consent mechanism must be established.

[^1]: GDPR Art. 6(1)(e) for public task, Art. 9(2)(h) for public health, or Art. 9(2)(j) for scientific research.

A Data Protection Officer (DPO) ensures, among other tasks, compliance with the EU data protection law (e.g. GDPR) and raises awareness on GDPR issues in an organisation. As data linkage can be a ‘*high-risk processing’*[^2], a notification or approval from the national Data Protection Authority (DPA) might be required depending on the type of data and purpose’ characteristics defined in GDPR and country-specific DPA rules (from national laws).

[^2]: ‘*High-risk processing*’ within the meaning of the GDPR refers to operations involving personal data which, by virtue of their nature, scope, context or purposes, are likely to result in a high risk to the rights and freedoms of natural persons should they become publicly available.

Additionally, signed agreements (e.g., data processing agreements) should be in place between all data providers, the trusted third party and the organisation using the linked data, clearly stating the roles and responsibilities of all involved parties.

**Specific legal framework**

Specific set of laws, regulations (GDPR, national, regional and/or local laws) and guidelines are in place to address circumstances as :

-   data sharing,
-   secondary use of data, and,
-   processing individual health-related data.

to ensure actions are compliant, ethical and secure. The legal framework should define data owners and users' specific roles. This transparency can help foster greater citizen trust in the initiative of linking individual data.

**Ethical approval by ethics committee**

Depending on the objectives, the tool’s implementation and country specificity, the approval and oversight from an ethics committee might be necessary. They guarantee ethical standards and principles to protect the rights, safety, and well-being of human subjects in research (and clinical trials). They evaluate the risk-benefit ratios and informed consent, and ensure that studies comply with fundamental moral and legal standards.

### Political

Practical implementation depends on access to data from multiple sources, which requires agreements and cooperative frameworks among the different health authorities and data owners. Collaboration is essential for technical and operational feasibility of the data linkage process.

### Technical

**IT infrastructure**

Complementary to characteristics described in [Linkage functional description](02-Linkage%20description.md) – *Constraints*, the IT infrastructure requires a number of measures to be put in place:

-   **Security:** The tool requires an IT infrastructure and network enabling the entry, collection, transfer, storage, and access of data in a secured manner (e.g., encryption, role-based access control and permission, audit logs, immutable logs, multi-factor authentification, etc.).
-   **Separation of environments:** Staging, linkage, validation storage and analysis environments need to be divided to ensure separation of rights and responsibilities. Each environment serves a distinct purpose (e.g. data cleaning, matching, long-term storage and analysis) while maintaining end-to-end security and compliance with relevant legal and ethical obligations, and guaranteeing data integrity.
-   **Reliability and availability:** the IT infrastructure must consistently perform linkage tasks without failure. The uptime (percentage of time it is operational), redundancy (backup systems ensuring continuity) and resiliency (capacity to recover in case of major failure) of the infrastructure should be assessed.
-   **Data quality control:**  clean, standardized and validated data is essential for accurate linkage and analysis.

All technical implementations need to be supervised by IT expert(s).

**Patient-level databases with unique identifier**

The data linkage process does not encompass the collection of data. As such, its implementation is dependent on the pre-existence of at least two databases at individual-level, using a common unique personal identifier (UPI) enabling direct matching. In the absence of such an identifier, probabilistic linkage can be performed, in which individual linkage is based on a combination of variables that appears across the different datasets, such as sex, postal code and date of birth.

**Trusted third party**

To protect patient interest and privacy, the UPI must be pseudonymised. A TTP with the knowledge and technology to organise the pseudonymisation is thus needed. In the case of probabilistic linking, the linking process relies on a probabilistic linking key.

## Filling the gaps

*Meeting the prerequisites is often a long-term endeavour that goes far beyond the scope of the implementation plans. This section suggests potential workarounds for launching the data linkage process even when some prerequisites are not fully met. Although these measures may not deliver the full benefits immediately, they can create the visibility and momentum needed to justify further efforts to meet the prerequisites.*

This section provides hints on how a data linkage process could be launched although the prerequisites above are not satisfied yet. It will impede reaching the full expected benefits but provide enough visibility and momentum to justify the effort of achieving the prerequisites.

### Legal and ethical

Legal and ethical authorisations, listed in *‘2.1 Assessment of the prerequisites’*, might be a long-term process but mandatory in the case of the usage of individual data. The implementers should obtain an approval related to data handling from the country’s official decision regulatory body. If the implementer considers conducting research beyond basic monitoring and screening, securing an approval from the Ethics Committee is most likely necessary.

### Political

Authorisation from the data owners is required for access, and collaboration is essential for technical and operational feasibility of the data linkage process. These authorisations define the objectives that can be addressed through access to linked data. If one of the entities does not authorise the sharing of its data, this does not prevent the data linkage from being implemented, but it does redefine the scope that can be reached by the linkage and the subsequent analysis. Depending on the content of the databases and their accessibility, different objectives can be achieved (*ref. Uses cases - 1.4.1 Vaccination surveillance*).

An overview of the different data owners in relation to the objective sought can be set up, in order to be able to find potential alternatives. Identifying the political entities in charge of health decisions, preparation, vaccination and any other subject related to the data used can be also essential to engage and support collaboration of the data owners. A decision-making committee can be set up to establish clear, shared objectives and processes, i.e. the questions that can be answered or the surveillance that can be undertaken by linking the data.

### Technical

**Unique Personal Identifier**

Ideally the UPI should be a national identification number (e.g. Social Security number, National Register Number, Civil Identification Number) to enable linkage of data coming from different data holders. If all data are collected by the same organisation, creating a unique patient identifier at the organisation level is acceptable.

Privacy-Preserving Record linkage is also an alternative if sufficient personally identifiable information is shared across databases. Although it decreases the quality of the linkage, this method allows the coupling of data without UPI and preserve privacy.

**Pseudonymisation**

If no TTP could be identified and all data are held by the same organisation, it is possible to set up the pseudonymisation process internally. The same pseudonymisation key should be used across the databases to enable the linkage.
