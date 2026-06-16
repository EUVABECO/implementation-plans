# FORECASTING TOOL - DEPLOYMENT

# Project team

The project team should consist of multidisciplinary expertise covering epidemiology, modelling, public health, data science, infrastructure, and governance. The project team will typically consist of epidemiological modellers, public health epidemiologists, data scientists and statisticians, software developers, full-stack engineers, database administrators, cybersecurity specialists, technical infrastructure teams, healthcare informaticians, data providers from implementing Member States (MS), public health authorities, legal and data privacy advisors, quality assurance and testing teams, and project managers. Additional contributors may include genomic surveillance experts, healthcare operations specialists, communication experts, policymakers, and external academic collaborators.

A **core team** is required at minimum during the build phase, comprising:

1\. a technical lead;

2\. a scientific lead for epidemiological modelling;

3\. a data governance lead;

4\. a project manager;

5\. a data protection officer.

MS should also designate a quality assurance and testing function to support release checks, regression testing and documentation of operational readiness.

Additional roles, such as science communication specialists, extended testing teams or user support, may be added depending on national context and scale of deployment.

# Workflow

The deployment of the Forecasting Tool requires implementation of secure data infrastructures, integration of epidemiological models, deployment of forecasting services, establishment of operational governance, implementation of visualization and communication systems. The project team should then determine the instantiated architecture, establish secure data pipelines, implement forecasting models, deploy the forecasting infrastructure, implement dashboards and user interfaces, organize operational governance, validate and calibrate the forecasting workflows, deploy monitoring systems, and prepare operational support structures.

## Determine the instantiated architecture

The team should make decisions regarding server infrastructure, cloud or hybrid deployment, database technologies, Application Programming Interface (APIs), dashboard systems, computational environments, cybersecurity protections, backup infrastructures, and scalability requirements. The architecture should support epidemiological simulations, real-time data integration, visualization of forecasting outputs, user authentication, interoperability with national health systems, and operational resilience. The forecasting infrastructure may be deployed locally within national infrastructures, within institutional data centres, through secure cloud environments, or through hybrid infrastructures combining local and cloud resources. The deployment architecture should also define user access policies, operational responsibilities, disaster recovery plans, software update procedures, and audit and logging systems.

## Implement the trusted directory of references

Secure and standardized data pipelines should be established to support ingestion of epidemiological data, healthcare system indicators, genomic surveillance, vaccination data, demographic datasets, and intervention timelines. The implementation process should include definition of data standards, harmonization procedures, anonymization mechanisms, validation workflows, and automated synchronization processes. Data transfer mechanisms should rely on encrypted communication protocols, secure APIs, authenticated access procedures, audit trails, and automated validation checks. Where multiple implementing MS contribute data, interoperability and harmonization procedures should be jointly agreed upon.

## Organise the maintenance of epidemiological data and models

The updating of epidemiological datasets and forecasting models should become part of the routine operational workflows of implementing MS. The maintenance process should include periodic data updates, recalibration of models, validation against observed epidemiological trends, updating intervention scenarios, integration of new scientific evidence, and monitoring of forecasting performance. The organization of maintenance activities may adopt several approaches: manual review and validation by epidemiological teams, partially automated data integration workflows, fully automated synchronization pipelines, centralized modelling support structures, and distributed modelling collaborations between institutions. Responsible personnel should be identified, accredited, trained, and periodically evaluated. Version control systems should be implemented to track model modifications, parameter updates, software changes, calibration procedures, and forecasting outputs.

## Implement forecasting models

The epidemiological forecasting models should be implemented within robust computational environments capable of supporting deterministic models, stochastic simulations, compartmental models, scenario analyses, and uncertainty quantification. The implementation process should include model coding, calibration workflows, validation procedures, sensitivity analyses, reproducibility testing, and documentation of assumptions. The modelling environment may rely on open-source programming languages, containerized infrastructures, reproducible computational workflows, and automated execution pipelines. Where possible, models should support age stratification, sex/gender stratification, geographic stratification, healthcare capacity constraints, variant of concern (VOC) integration, and intervention simulations.

## Implement dashboards and user interfaces

Dashboards and user interfaces should allow stakeholders to visualize forecasting outputs, compare intervention scenarios, explore epidemiological trends, monitor healthcare capacity indicators, and export reports and figures. The interfaces should support web-based access, secure authentication, responsive visualization, accessibility standards, and multilingual support where applicable. Visualization tools may include epidemic curves, hospitalization projections, intensive care unit (ICU) occupancy forecasts, scenario comparison tools, and uncertainty visualizations. User interfaces should be designed for: public health authorities, healthcare planners, policymakers, epidemiologists, and operational response teams.

The implementation of the user interface is performed in two testing steps:

Alpha testing: Integration of validated models into the web-based tool and initial testing with controlled user groups.

Beta testing: Extended testing with broader user groups and refinement of the web-based tool based on user feedback.

## Implement operational monitoring systems

Continuous operational monitoring systems should be deployed to supervise server availability, data synchronization, forecasting performance, cybersecurity events, dashboard responsiveness, and API functionality. Automated alerts should notify technical teams when services fail, data updates are interrupted, abnormal forecasting behaviour occurs, cybersecurity threats are detected, and computational loads exceed thresholds. Monitoring systems should support incident management, performance optimization, operational continuity, and disaster recovery workflows.

During operation, verification activities must distinguish between:

1.  **technical validation**, ensuring fitness, adequacy of the models, system integrity and performance, fulfilling the objectives of its users;
2.  **technical** **verification,** ensuring model stability and coherence; therefore, the tool can be released to production.
3.  **operational readiness assessment**, ensuring fitness for decision support.

System governance must be based on a clear separation between institutional ownership, technical operation and scientific supervision, in order to avoid ambiguities in decision-making and to protect scientific processes from political interference.

A minimal release policy should be defined, clarifying which outputs are for internal use only, which may inform public communication, and which require prior scientific or institutional review before dissemination.

Communication should be treated as a **risk-management function**, defining clear principles for internal communication with decision-makers and for external communication. This includes explicit communication of uncertainties, assumptions and limitations inherent to predictive modelling, in order to prevent misinterpretation of results.

MS should also consider the long-term sustainability of the forecasting tool beyond the initial implementation or project funding period. This includes planning for stable institutional ownership, continuity of core expertise, maintenance of data pipelines and models, and periodic review of system relevance. Where appropriate, the tool may evolve from a crisis-driven capability into a permanent analytical asset supporting preparedness, resilience and response to future public health threats, including pathogens other than those initially targeted.

## Prepare operational support structures

Operational support structures should include user training programmes, technical support teams, operational Standard Operating Procedures (SOPs), governance committees, communication procedures, and maintenance workflows. Support mechanisms should ensure that users can interpret forecasting outputs, access technical assistance, report operational issues, request updates or modifications, and receive continuous training. Documentation should include user manuals, technical specifications, governance procedures, cybersecurity policies, data governance frameworks, and troubleshooting guides.

# Typical planning

The indicative roadmap presented below provides a tested, modular, and extensible technical foundation for national forecasting deployments. This roadmap provides an indicative sequencing of activities required to implement the forecasting tool in a MS. The roadmap is not a fixed timetable, but a planning instrument intended to help MS sequence implementation activities, identify prerequisites and structure progression from early deployment to long-term institutionalisation.

The roadmap is structured in **phases**, each concluding with a **decision or validation gate**. Progression to subsequent phases is conditional upon successful completion of the previous phase. Each decision or validation gate should be supported by one or more verifiable artefacts (e.g. validation reports, documented governance procedures, operational checklists), ensuring that progression between phases is based on objective criteria rather than informal assessment.

To make the implementation logic operational, it can be organised into six phases:

**Phase 0** — Strategic readiness and go/no-go decision;

**Phase 1** — Core setup and minimum viable implementation;

**Phase 2** — Operationalisation and stabilisation;

**Phase 3** — Consolidation and scaling;

**Phase 4** — Full operational use and communication;

**Phase 5** — Continuous improvement, sustainability and resilience.

## Phase 0 — Strategic Readiness and Go/No-Go Decision

**Objective:** Ensure that minimal strategic, legal and institutional conditions exist to justify launching an implementation project.

**Key activities**

1\. Identification of the competent public authority acting as institutional owner.

2\. Initial political endorsement in principle.

3\. High-level legal and ethical assessment (GDPR, ethical committee recommendations, national health data law).

4\. Preliminary assessment of data availability and quality.

5\. Decision on deployment model (e.g., on-premises, cloud).

6\. Identification of funding and resource envelope.

**Key outputs**

1\. Statement of institutional ownership.

2\. Preliminary risk assessment (legal, political, technical).

3\. High-level implementation intent.

**Decision gate**

**Go / No-Go decision** for initiating the build phase. High-level decision-markers intervene at this stage.

## Phase 1 — Core Setup (Minimum Viable Implementation)

**Objective:** Deliver a first operational version of the forecasting tool enabling restricted internal use.

**Key activities**

1\. Definition of the mandatory datasets and production of a variable charter.

2\. Setup of basic infrastructure (servers, security, access control).

3\. Implementation of a baseline epidemiological model.

4\. Manual or semi-automated data ingestion.

5\. Initial parameter definition based on literature and available data.

6\. First calibration using historical data.

7\. Internal technical and scientific sanity checks.

**Key outputs**

1\. Operational baseline model.

2\. Documented data definitions and parameters.

3\. First internal forecasts and scenario runs.

**Decision gate**

**Validation of minimum operational capability**.

## Phase 2 — Operationalisation and Stabilisation

**Objective:** Transform the baseline system into a stable operational tool for decision support.

**Key activities**

1\. Automation of data pipelines.

2\. Formalisation of data governance and access rules.

3\. Introduction of versioning and audit trails for data and parameters.

4\. Definition of model validation criteria and monitoring indicators.

5\. Implementation of uncertainty quantification and sensitivity analysis.

6\. Deployment of a basic user interface.

7\. Initial user training (internal decision-makers and analysts).

8\. Definition of internal communication protocols.

**Key outputs**

1\. Stable and repeatable forecasting runs.

2\. Documented governance and validation procedures.

3\. Trained core user group.

**Decision gate**

**Operational readiness approval**.

## Phase 3 — Consolidation and Scaling

**Objective:** Increase robustness, analytical depth and policy relevance of the tool.

**Key activities**

1\. Integration of additional data sources (e.g. sub-national data, healthcare capacity).

2\. Refinement of models and parameter estimation.

3\. Implementation of uncertainty quantification and sensitivity analysis.

4\. Expansion of scenario capabilities (NPIs, vaccination strategies).

5\. Improvement of dashboards and reporting.

6\. Definition of external communication principles.

**Key outputs**

1\. Enhanced forecasting accuracy and interpretability.

2\. Broader scenario analysis capacity.

3\. Improved decision-support interfaces.

**Decision gate**

**Scientific and operational consolidation review**.

## Phase 4 — Full Operational Use and Communication

**Objective:** Embed the forecasting tool into routine decision-making processes.

**Key activities**

1\. Formal integration into public health decision workflows.

2\. Definition of publication and communication rules.

3\. Establishment of feedback loops with policymakers.

4\. Regular monitoring of model performance.

5\. Documentation of lessons learned.

**Key outputs**

1\. Tool used routinely for policy support.

2\. Transparent communication of results and uncertainties.

3\. Documented performance metrics.

**Decision gate**

**Formal acceptance as an operational public health tool**.

## Phase 5 — Continuous Improvement, Sustainability, and Resilience

**Objective:** Ensure long-term relevance, credibility, sustainability, and resilience.

**Key activities**

1\. Periodic reassessment of models and assumptions.

2\. External scientific review where appropriate.

3\. Adaptation to new pathogens or use cases.

4\. Capacity building and knowledge transfer.

5\. Long-term funding and maintenance planning.

**Key outputs**

1\. Sustained forecasting capacity.

2\. Institutionalised governance and expertise.

3\. Evolution pathway for future crises.

**Key Principles Underpinning the Roadmap**

1\. Progressive implementation over bulk deployment.

2\. Clear separation between scientific/technical and political responsibilities.

3\. Transparency, traceability and reproducibility of results.

4\. Adaptability to heterogeneous Member State contexts.

The following table summarizes the different phases of the Indicative Roadmap for the Implementation of the Forecasting Tool.

| **Dimension \\ Phase**         | **Phase 0**<br>**Strategic Readiness**                              | **Phase 1**<br>**Core Setup**                                                                  | **Phase 2**<br>**Operationalisation & Stabilisation**                                    | **Phase 3**<br>**Consolidation & Scaling**                      | **Phase 4**<br>**Full Operational Use**                            | **Phase 5**<br>**Continuous Improvement**        |
|--------------------------------|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------|
| **Data & Variables**           | Data availability<br>assessment                                     | Variable charter & min.<br>dataset defined<br>+ Semi-automated data ingestion                  | Versioning & provenance<br>metadata                                                      | Sub-national &<br>healthcare capacity data                      | Operational data<br>monitoring                                     | Periodic data                                    |
| **Infrastructure**             | Deployment model decision<br>(cloud / on-prem)                      | Servers, security,<br>access control                                                           | Audit trails &<br>backup policies                                                        | Enhanced<br>infrastructure                                      | ----                                                               | Long-term<br>maintenance planning                |
| **Epidemiological Model**      | ----                                                                | Baseline model calibrated<br>on national data                                                  | Validation criteria &<br>monitoring indicators                                           | Model & parameter<br>estimation refined                         | Regular model<br>performance monitoring                            | Periodic model &<br>assumptions reassessment     |
| **Epidemiological Parameters** | ----                                                                | Initial parameters defined<br>(literature + data)                                              | Change-control process<br>established                                                    | Parameter updates<br>versioned & traceable                      | ----                                                               | Parameter governance<br>sustained                |
| **Validation & Verification**  | ----                                                                | Internal technical &<br>scientific sanity checks<br>+ Initial validation on<br>historical data | Formalised validation criteria<br>+ Uncertainty quantification<br>& sensitivity analysis | Back-testing &<br>stress tests                                  | Operational readiness<br>assessment                                | External<br>scientific review                    |
| **Governance & Team**          | Institutional owner identified<br>+ Legal/ethical assessment (GDPR) | Core team in place<br>(tech, science, data, PM, DPO)                                           | Data governance &<br>access rules formalised                                             | Strategic vs. operational<br>roles separated                    | Formal integration into<br>public health workflows                 | Institutionalised governance<br>& expertise      |
| **Interface & Communication**  | ----                                                                | ----                                                                                           | Basic user interface<br>+ Internal user training                                         | Dashboard improvement<br>+ External comms<br>principles defined | Release & publication<br>policy defined<br>Public-facing dashboard | Capacity building &<br>knowledge transfer        |
| **Sustainability**             | Funding<br>identification                                           | ----                                                                                           | ----                                                                                     | ----                                                            | Lessons learned<br>documented                                      | Long-term funding +<br>evolution pathway defined |

Legend:

| **● Mandatory**                    | Element required for any credible implementation. Absence prevents reliable, reproducible outputs.             |
|------------------------------------|----------------------------------------------------------------------------------------------------------------|
| **○ Optional / Context-dependent** | Element whose form or depth may legitimately vary by national legal, institutional or technical circumstances. |
| **— Not applicable**               | This dimension is not relevant or not referenced in the document for this phase.                               |

# Build resources

The deployment phase may rely on open-source epidemiological modelling frameworks, statistical computing environments, containerization technologies, cloud infrastructures, visualization libraries, dashboard frameworks, cybersecurity toolkits, and interoperability standards. Build resources may include reference architectures, example forecasting workflows, API specifications, data harmonization guidelines, calibration procedures, training materials, deployment templates, and technical documentation. Reference implementations developed within the EUVABECO project and related forecasting initiatives may support epidemiological simulation infrastructures, web-based dashboards, forecasting APIs, secure data delivery pipelines, and public health visualization tools. These resources facilitate scalable and interoperable deployment of forecasting infrastructures across multiple MS.
