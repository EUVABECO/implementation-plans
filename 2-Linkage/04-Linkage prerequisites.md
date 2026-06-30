# DATA LINKAGE PROCESS - PREREQUISITES

## Assessment of prerequisites

*Prerequisites represent the broader context or resources necessary for the successful implementation and operation of the data linkage process. Although not specific to the tool itself, these prerequisites are essential for ensuring its proper functioning once deployed.*

### Legal and ethical

**Legal authorisation**

Implementation of the data linkage process must have a valid legal basis complying with all applicable national and European legal frameworks[^1], which are checked by a legal department. The legal department must assess whether the implementer operates under a specific mandate or legal exemption allowing the deployment of the tool. If the linkage is not mandated under national or regional law as a public task, a GDPR-compliant consent mechanism must be established.

[^1]: GDPR Art. 6(1)(e) for public task, Art. 9(2)(h) for public health, or Art. 9(2)(j) for scientific research.

A Data Protection Officer (DPO) ensures, among other tasks, compliance with the EU data protection law (e.g. GDPR) and raises awareness on GDPR issues in an organisation. As data linkage can be a ‘*high-risk processing’*[^2], a notification or approval from the national Data Protection Authority (DPA) might be required depending on the type of data and the characteristics of the purpose defined in GDPR and country-specific DPA rules (from national laws).

[^2]: ‘*High-risk processing*’ within the meaning of the GDPR refers to operations involving personal data which, by virtue of their nature, scope, context or purposes, are likely to result in a high risk to the rights and freedoms of natural persons should they become publicly available.

Additionally, signed agreements (e.g., data processing agreements) should be in place between all data providers, the trusted third party and the organisation using the linked data, clearly stating the roles and responsibilities of all involved parties.

**Specific legal framework**

A specific set of laws, regulations (GDPR, national, regional and/or local laws), mandates and guidelines are in place to address circumstances as:

-   data sharing,
-   secondary use of data, and,
-   processing individual health-related data.

to ensure actions are compliant, ethical and secure. The legal framework should define data owners and users' specific roles. This transparency can help foster greater citizen trust in the initiative of linking individual data.

**Ethical approval by an ethics committee**

Depending on the objectives, the tool’s implementation and country specificity, the approval and oversight from an ethics committee might be necessary. They guarantee ethical standards and principles to protect the rights, safety, and well-being of human subjects in research (and clinical trials). They evaluate the risk-benefit ratios and informed consent, and ensure that studies comply with fundamental moral and legal standards.

### Political and governance

Implementation of the data linkage process can be influenced by several political considerations.

Policy priorities may determine the level of governmental support for investments in data infrastructure and systems, and the use of linked data for public health decision-making. Adequate funding and allocation of resources are also essential to develop, establish and maintain the technical systems and the human expertise and capacities required for data linkage.

A successful implementation and use of data linkage also depends on a data-driven culture among stakeholders. Stakeholders who value data-driven insights are more likely to prioritise and invest in the necessary infrastructure, training, and resources needed to implement and sustain a data linkage process. Such a culture promotes the integration of linked data into policy and decision-making processes.

Additionally, a commitment and contribution to the European Health Data Space (EHDS) ecosystem signs a recognition of a data-driven vision from the stakeholders, paving the way for a potential implementation of data linkage.

Relations between authorities can significantly influence implementation, particularly when health data are managed across different administrative levels (national, regional and local). Differences in priorities, legal mandates, or responsibilities may create barriers to cooperation and delay the implementation of data linkage. More broadly, practical implementation of data linkage depends on access to data from multiple sources, which requires formal agreements and cooperative governance frameworks among the different health authorities and data owners. Collaboration is essential for the technical and operational feasibility of the data linkage process.

Stakeholder interests may also shape implementation, as organisations can differ in their willingness to share data due to concerns related to autonomy, accountability, data ownership or perceived risks. In addition, public trust can also influence the implementation, as concerns regarding privacy, data security, and the use of personal information can affect the political acceptability of linkage initiatives.

### Technical

**IT infrastructure**

Complementary to characteristics described in [Linkage functional description](02-Linkage%20description.md) – *Constraints*, the IT infrastructure requires a number of measures to be put in place:

-   **Security:** The tool requires an IT infrastructure and network enabling the entry, collection, transfer, storage, and access of data in a secured manner (e.g., encryption, role-based access control and permission, audit logs, immutable logs, multi-factor authentication, etc.).
-   **Separation of environments:** Staging, linkage, validation storage and analysis environments need to be divided to ensure separation of rights and responsibilities. Each environment serves a distinct purpose (e.g. data cleaning, matching, long-term storage and analysis) while maintaining end-to-end security and compliance with relevant legal and ethical obligations, and guaranteeing data integrity.
-   **Reliability and availability:** the IT infrastructure must consistently perform linkage tasks without failure. The uptime (percentage of time it is operational), redundancy (backup systems ensuring continuity) and resiliency (capacity to recover in case of major failure) of the infrastructure should be assessed.
-   **Data quality control:**  clean, standardized and validated data is essential for accurate linkage and analysis.

All technical implementations need to be supervised by IT expert(s).

**Patient-level databases with unique identifier**

The data linkage process does not encompass the collection of data. As such, its implementation is dependent on the pre-existence of at least two databases at individual-level, using a common unique personal identifier (UPI) enabling direct matching.

**Trusted third party**

To protect patient interest and privacy, the UPI must be pseudonymised. A TTP with the knowledge and technology to organise the pseudonymisation is thus needed.

**Computer literacy and knowledge on privacy rules among healthcare workers**

For the data linkage process to be used effectively, healthcare workers (HCW) should have a basic level of computer literacy to interact with their recording/reporting system (primary data collection system). A lack of computer literacy can lead to user errors, data entry mistakes, and improper use of the system, which can compromise the integrity and accuracy of the linked data. The system may not be usable, regardless of its technical capabilities. HCW with adequate computer skills can use the system more efficiently and are more prone to accept and use the system.

As they are working with personal and sensitive (medical) data, it is also essential that HCW have some knowledge on privacy regulations, such as the GDPR. This can be accommodated by following (online) trainings related to this topic, organised by a data protection authority.

## Filling the gaps

*Meeting the prerequisites is often a long-term endeavour that goes far beyond the scope of the implementation plans. This section suggests potential workarounds for launching the data linkage process even when some prerequisites are not fully met. Although these measures may not deliver the full benefits immediately, they can create the visibility and momentum needed to justify further efforts to meet the prerequisites.*

This section provides hints on how a data linkage process could be launched although the prerequisites above are not satisfied yet. It will impede reaching the full expected benefits but provide enough visibility and momentum to justify the effort of achieving the prerequisites.

### Legal and ethical

Legal and ethical authorisations, listed in Module 02 *- Functional description (Assessment of the prerequisites)*, might be a long-term process but mandatory when individual-level data are used. The implementers should obtain an approval related to data handling from the country’s competent regulatory authority. If the implementer considers conducting research beyond basic monitoring and screening, securing an approval from the Ethics Committee is most likely necessary.

### Political

Authorisation from the data owners is required for access, and collaboration is essential for technical and operational feasibility of the data linkage process. These authorisations define the objectives that can be addressed through access to linked data. If one of the entities does not authorise the sharing of its data, this does not prevent the data linkage from being implemented, but it does redefine the scope that can be reached by the linkage and the subsequent analysis[^3]. Depending on the content of the databases and their accessibility, different objectives can be achieved (Module 02 - *Functional description* (*Uses cases - 1.4.1 Vaccination surveillance*)).

[^3]: The implementation of the EHDS regulation may influence this aspect. However, given the current status of its rollout and the projected timeline for full application by 2029, this factor has not been incorporated into the drafting of this implementation plan.

An overview of the different data owners in relation to the objective sought can be set up, in order to be able to find potential alternatives. Identifying the political entities in charge of health decisions, preparation, vaccination and any other subject related to the data used can also be essential to engage and support collaboration of the data owners. A decision-making committee can be set up to establish clear, shared objectives and processes, i.e. the questions that can be answered or the surveillance that can be undertaken by linking the data.

### Technical

**Absence of Unique Personal Identifier**

Ideally the UPI should be a national identification number (e.g. Social Security number, National Register Number, Civil Identification Number) to enable linkage of data coming from different data holders.

If such an identifier is not available, several linkage options[^4] are possible, including:

[^4]: Details of the data linkage methods are set out in the following document: [*Shlomo, N. (2019). Overview of Data Linkage Methods for Policy Design and Evaluation*.](https://doi.org/10.1007/978-3-030-59706-1_3) (pp 47 -75)

-   If all data are collected by the same organisation, creating a unique patient identifier at the organisational level is acceptable.
-   Probabilistic linkage is a record linkage method that estimates the likelihood that records from different datasets refer to the same individual by comparing identifiers (such as name, date of birth, sex, address, postal code or other personal identifiers, which may be prone to error) and calculating match probabilities. It allows errors, missing data, or variations in the matching variables.
-   Privacy-Preserving Record linkage (PPRL) enables records to be linked across datasets, without directly exposing sensitive personal identifiers. It uses cryptographic and privacy-enhancing techniques to encode or hash matching variables before comparison. Only encoded/hashed versions of data are shared with the TTP or data analysts. This reduces the disclosure of sensitive information, while enabling linkage when sharing of identifiers is restricted or not permitted.

The key difference between the two last methods is how the identifying information is handled during the matching. PPRL may reduce linkage accuracy compared with linkage performed on raw or quasi-identifiable data because some information is ‘*lost’* during encoding and errors or variations in identifiers can be more difficult to detect. However, the extent of any reduction depends on the specific PPRL method and data quality.

Unlike UPI-based linkage, probabilistic and PPR linkages inherently involve a degree of uncertainty as matches are inferred from similarities between multiple identifiers rather than being established by a single unique identifier, which can lead to both false positives and missed matches. The quality of the linkage therefore depends on the completeness, accuracy and discriminatory power of the available personal identifiers (as well as the linkage methodology used). Consequently, additional validation and quality assessment procedures are often necessary to manage this uncertainty.

**Absence of TTP**

If no TTP could be identified and all data are held by the same organisation, it is possible to set up the

pseudonymisation process internally. The same pseudonymisation key should be used across the databases to enable the linkage.
