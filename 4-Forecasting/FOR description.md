# FORECASTING TOOL - FUNCTIONAL DESCRIPTION

# Description of the tool

*This section provides a functional overview of the intended tool and its usage. It outlines the goals and features without referring to any specific implementation.*

## Objectives

*This section is the overall rationale for the tool.*

The Forecasting Tool allows Member States (MS) to model, forecast, and simulate the spread and burden of infectious disease outbreaks, epidemics, and pandemics using continuously updated epidemiological, sociodemographic, healthcare, and intervention-related data. The tool supports the prediction of infection incidence, hospitalization burden, intensive care unit (ICU) admissions, mortality, healthcare system stress, demand for specialized treatments, and effects of pharmaceutical and non-pharmaceutical interventions (NPIs).

The Forecasting Tool is intended to support public health preparedness, evidence-based policymaking, healthcare resource allocation, outbreak response coordination, risk communication, long-term surveillance and preparedness activities. The tool enables simulation of multiple intervention scenarios, including vaccination strategies, NPIs, and combined mitigation approaches. It also facilitates the evaluation of variants of concern (VOCs), behavioural changes, seasonality, healthcare system constraints, and population mobility patterns. By integrating continuously updated surveillance data and recalibrating epidemiological models over time, the Forecasting Tool provides robust and adaptive decision support for public health authorities and healthcare systems.

## Involved stakeholders and their expectations

*This section outlines the various stakeholders within the implementing Member State who will use or contribute to the tool. Their expectations represent essential requirements for any implementation.*

For the successful implementation of the Forecasting Tool, various stakeholders play crucial roles, each with specific expectations and responsibilities. The key stakeholders are:

-   citizens/patients;
-   healthcare professionals (HCPs);
-   public health authorities;
-   government agencies;
-   academic and research institutions;
-   international organizations ((e.g., WHO, ECDC, UNICEF, OECD, Gavi, CEPI, World Bank, and other supranational public health and humanitarian organizations);
-   non-governmental organizations (NGOs);
-   community and patient advocacy groups;
-   data providers;
-   digital health infrastructure operators;
-   technology and software development companies;
-   funding bodies;
-   private sector partners;
-   media and communication experts.

### Citizens/patients

Citizens and patients expect transparent and accessible information regarding public health risks, outbreak evolution, and intervention strategies. They expect accurate forecasts, equitable public health planning, proper protection of personal health data, and clear communication regarding how forecasting outputs influence public health decisions.

### Healthcare professionals

HCPs, including physicians, nurses, pharmacists, hospital administrators, and emergency response teams, expect reliable forecasting outputs supporting healthcare resource planning and operational preparedness. HCPs also expect interoperable systems capable of integrating with existing electronic health infrastructures and healthcare workflows.

### Public health authorities

Public health authorities expect the Forecasting Tool to support outbreak preparedness, surveillance, intervention planning, vaccination campaign evaluation, healthcare system resilience assessment, early warning systems, and evidence-based decision-making. Public health authorities also expect forecasting outputs to be timely, interpretable, geographically granular, and continuously updated.

### Government agencies

Government agencies expect forecasting systems capable of informing national preparedness planning, emergency response coordination, healthcare resource allocation, strategic policy development, and public communication strategies. They also expect the tool to support scenario analysis under uncertainty.

### Academic and research institutions

Academic and research institutions contribute epidemiological expertise, mathematical modelling, statistical analysis, data science methodologies, and model validation approaches. They expect access to robust data infrastructures and opportunities for continuous methodological improvement and collaborative research.

### International organizations

International organizations expect forecasting systems to align with international public health standards and support cross-border coordination during epidemics and pandemics.

### Non-governmental organizations

NGOs expect the Forecasting Tool to support equitable public health interventions and provide actionable insights for vulnerable populations and underserved communities.

### Community and patient advocacy groups

Community organizations and advocacy groups expect the tool to support inclusive and equitable public health planning, transparency in decision-making, and effective communication regarding public health risks and interventions.

### Data providers

Data providers, including surveillance agencies, hospitals, laboratories, genomic surveillance systems, and statistical offices, expect secure and standardized data integration procedures, clear governance frameworks, and robust data protection measures.

### Digital health infrastructure operators

Operators maintaining digital health infrastructures expect interoperability with national healthcare systems, reliable Application Programming Interfaces (APIs), cybersecurity compliance, scalability, and operational continuity.

### Technology and software development companies

Technology providers and software developers expect standardized technical architectures, interoperable infrastructures, scalable deployment environments, and clearly defined security and operational requirements.

### Funding bodies

Funding bodies expect sustainable, scalable, and cost-effective forecasting infrastructures capable of delivering measurable public health impact and long-term operational viability.

### Private sector partners

Private sector partners contribute to the development, deployment, and maintenance of the Forecasting Tool by providing technological infrastructures, cloud computing resources, data analytics solutions, artificial intelligence and modelling expertise, interoperability support, and cybersecurity services. Private sector stakeholders may also support healthcare logistics optimization, vaccine and pharmaceutical supply-chain forecasting, operational scalability, and innovation activities through technical partnerships, collaborative research, or co-funding mechanisms.

### Media and communication experts

Media and communication experts support the dissemination and communication of forecasting outputs, epidemiological trends, preparedness recommendations, and public health alerts generated by the Forecasting Tool. They contribute to transparent risk communication, public engagement, and education regarding the interpretation of forecasts, uncertainty, intervention scenarios, and public health implications, thereby helping strengthen public trust, situational awareness, and informed decision-making during outbreaks, epidemics, and pandemics.

## Constraints

*Constraints are the non-functional requirements that, while not directly related to the tool's specific functions, are critical to its overall viability.*

For the successful implementation of the Forecasting Tool, several constraints must be addressed.

### Data availability and quality

The effectiveness of epidemiological forecasting depends heavily on the availability of timely data, geographically granular data, standardized surveillance systems, reliable hospitalization and mortality records, genomic surveillance data, vaccination coverage data and information on demographic covariables. Incomplete or inconsistent data may reduce forecasting precision and reliability.

### Legal and ethical constraints

The Forecasting Tool may process sensitive health-related information requiring compliance with the European Union General Data Protection Regulation (GDPR), national data protection regulations, ethical governance frameworks, and secure data-sharing agreements. Where possible, anonymization and data minimization principles should be applied.

### Computational and technical constraints

Forecasting applications require high computational capacity, scalable server infrastructures, secure APIs, high-speed connectivity, continuous monitoring systems, and redundancy and disaster recovery plans. Long-term operational sustainability also requires maintenance resources and technical expertise.

### Model uncertainty and epidemiological variability

Forecasts are inherently uncertain and sensitive to changes in transmission dynamics, behavioural adaptations, emergence of VOCs, intervention compliance, seasonality, and healthcare system changes. Continuous recalibration and validation are therefore necessary.

### Political and governance constraints

Public health forecasting may influence politically sensitive decisions. Successful implementation therefore requires stakeholder engagement, policy alignment, transparency, communication strategies, and trust-building mechanisms.

### Sustainability constraints

Long-term sustainability requires financial support, operational maintenance, workforce training, environmentally sustainable infrastructures, scalable architectures, and continuous model adaptation.

## Use cases

*The following use cases illustrate how different stakeholders can use the Forecasting Tool to meet their expectations. Each scenario demonstrates a specific function of the Forecasting Tool.*

### UC01 - Forecasting outbreak trajectories

A national public health authority monitors a rapidly increasing number of respiratory infections associated with a newly emerging VOC. The authority uses the Forecasting Tool to simulate future incidence rates, hospitalizations, ICU admissions, and mortality under multiple intervention scenarios. The simulation outputs help decision-makers anticipate healthcare pressures and determine whether additional public health interventions are required.

### UC02 - Evaluating vaccination strategies

MS can evaluate different vaccination strategies during an ongoing epidemic. Using the Forecasting Tool, policymakers compare booster campaign timing, age-prioritization strategies, vaccine coverage scenarios, combined pharmaceutical and non-pharmaceutical interventions. The resulting simulations support optimization of vaccine allocation and public health planning.

### UC03 – Monitoring healthcare system capacity

Regional healthcare authorities use the Forecasting Tool to estimate future healthcare demand, including hospital bed occupancy, ICU capacity, ventilator demand, and healthcare staffing requirements. The forecasts support proactive healthcare resource allocation and emergency preparedness planning.

### UC04 – Assessing the impact of variants of concern

A genomic surveillance network detects increasing circulation of a new VOC associated with increased transmissibility. Epidemiological modellers integrate genomic surveillance data into the Forecasting Tool to evaluate potential impacts on outbreak growth, hospitalization burden, vaccine effectiveness, and healthcare system resilience.

### UC05 – Supporting routine preparedness activities

Outside emergency periods, the Forecasting Tool is continuously updated using surveillance and demographic data to support preparedness exercises, seasonal outbreak monitoring, healthcare planning, resource optimization, and public health surveillance activities.

### UC06 – Supporting public communication

Public health authorities use forecasting visualizations and scenario analyses generated by the tool to communicate outbreak risks, intervention rationales, expected healthcare impacts, and preparedness measures. Transparent communication supports public trust and informed decision-making.
