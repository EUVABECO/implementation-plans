# CDS - KNOWLEDGE MANAGEMENT POLICY

# Purpose
This document presents the policy applied by SYADEM to manage the rules elaborated for its vaccination clinical decision support systems and the knowledge bases serving in the elaboration of these rules. It is intended to be used as guidance for other implementations.

# Knowledge bases

The knowledge bases consist of:

-   The reference texts upon which the recommendation rules and messages are elaborated.
-   The nomenclature of prevention methods, and specifically for the vaccination CDS the NUVA ontology of administered vaccines.
-   The conditions and the rules used by the decision support systems.
-   The test cases and the expected results for each case.

All changes brought to a knowledge base are logged, and these logs are kept for 10 years.

## Reference texts

The reference texts are detected:

-   By SYADEM experts, through the regulatory and scientific monitoring described below.
-   By the local vaccinology experts of SYADEM clients.

They are systematically uploaded and retained on SYADEM system to make sure they will always be available for consultation by users or auditors.

They are qualified with their source organization, their nature (market authorization, product brief, methodological guide, scientific publication, etc.) and when relevant the corresponding vaccines and target diseases.

Texts are considered only if they come from a reliable source, such as health institutions, learned societies, peer-reviewed journals, etc. The list is established jointly for a given CDS instance by SYADEM and its client institution.

All SYADEM experts can add texts or update their qualification. A text can be qualified as obsolete but is never removed from the database.

## Prevention methods

In the case of a vaccination CDS, the prevention methods are vaccines, and the knowledge base consists in the NUVA – Nomenclature Unifiée des Vaccins curated by SYADEM.

The NUVA is a comprehensive ontology of administered vaccines designations, including their function described by valences, their target diseases and their representations in different national or international code systems.

New concepts are detected through authorization processes publications, notifications by vaccine producers, publication of clinical trials, alignment with further code systems, and occasionally notification from users for rare legacy vaccines or vaccines designations.

The NUVA is updated by SYADEM experts based upon these notifications and cross verification of the characteristics of the vaccine or valence.

## Conditions and rules

Elementary conditions are the premises for the rules of the decision support systems. In order to support their reuse, they are given a persistent identifier and are transverse to all decision support systems from SYADEM.

SYADEM experts create conditions on the basis of reference texts. A condition is characterized by a type (Boolean, integer, float, date or enumerated), labels in various languages, and possibly logical expressions binding it to formal medical knowledge representations. Since patient profiles can be store within the client systems, a condition can never be removed. However, it can be obsoleted, and then any request using it will raise an error condition.

Synthetic conditions are the results of logical equations on elementary conditions. They are specific to a given CDS and help experts to simplify the writing or rules. They are created by experts when needed and can be discarded if unused. The modification of a synthetic condition requires the revalidation of every rule that used it.

The rules are specific to a given CDS. They are structured by prevention objective (target disease for vaccination), then within nested folders. SYADEM experts can create, update or delete rules, and test them against the test cases before submission.

Any rule altered, explicitly or because of a change in a synthetic condition, must undergo the submission and validation process.

The rules are complemented with explanation or justification messages, without effect on the recommended action. The changes for these messages are logged, but do not impose to submit and validate again the related rules.

## Test cases

Test cases are patient profiles used to check the correct execution of rules, accompanied by expected results. They are created as needed by SYADEM experts.

Test cases can be freely created, modified or deleted, as long as the collection of test cases triggers all of the rules.

Each execution of a test case is logged, and the results are recorded during the publication process.

# Management of competence

## Vaccination experts

Experts are selected by SYADEM scientific director on the basis of their in-depth knowledge of vaccines, their efficiency, their administration and vaccination protocols.

Their missions include:

-   The regulatory and scientific monitoring within their health jurisdiction to keep the rules updated. Outside of France, they must be assisted by the local experts assigned by of SYADEM clients.
-   Writing the rules and the associated justification messages based upon the reference texts. Outside of France, the justification messages can be translated and adapted by the communication team from SYADEM clients.
-   Producing the test cases supporting the publication of rulesets.
-   Collecting the evidence on the scientific validity and the health efficiency of the delivered service.

## Regulatory and scientific monitoring

Experts detect the new knowledge items to model through several channels:

-   Publications from health authorities
-   Ad hoc communication with health authorities prior to publication
-   Ad hoc communication with vaccines manufacturers
-   Their own research activity
-   Notifications from users.

# Publication process

## Access to the knowledge bases

Only the experts from SYADEM are entitled to update the knowledge bases. They may receive proposals from external experts, but these are always subject to their review and endorsement.

## Submission and validation

All changes in knowledge bases must go through to a two steps publication process. The changes proposed by a submitting expert are put on hold until a second reviewing expert has validated them. The submission and validation operation are logged.

## Non regression

A reinforced validation process is applied for decision rules:

-   Rules are submitted for validation in consistent batches (typically all modified rules for a given prevention objective).
-   Upon submission, all test cases are processed twice, on the ruleset prior to the submission and on the ruleset after submission.
-   If some rules were not triggered, the submission is invalid. It belongs to the submitting expert to create the missing test cases.
-   Otherwise, a report is produced showing all the differences between the outcomes of the current and the proposed ruleset.
-   The submitting expert checks and confirms that each of these differences corresponds with the purpose of the submitted changes.
-   The reviewing expert also checks these differences prior to validation.

## Approval by an authority

SYADEM experts act on behalf of a client responsible for the delivered recommendations. Depending upon contractual dispositions, this client either intervenes directly as the reviewing expert or receives a copy of the report of differences for approval.

# Incidents management

## Detection

SYADEM has a support portal where incidents can be notified by its clients.

The notification is performed through an incident ticket, written in French or English, that will be used to track the incident along its processing.

## Qualification

A SYADEM administrator will first qualify the event as a technical or knowledge incidents. The processing of technical incidents is a general processus at SYADEM that is not described here. Tickets for events that are not considered as incidents can be closed at this stage.

A knowledge incident can cause codification mistakes in vaccination histories, an incorrect vaccination status assessment for the regarded persons, over or under-vaccinations. Its level is assessed by evaluating:

-   An impact, depending upon the risk of a wrong vaccination decision.
-   A frequency, since the situation could be systematic or very occasional.

The table below gives then the incident level among: neglectable, minor, or major.

|                       | **Risk of wrong decision** |             |          |
|-----------------------|----------------------------|-------------|----------|
| **Usage frequency**   | Unlikely                   | Possible    | Probable |
| \>= 10% of population | Minor                      | Major       | Major    |
| \>= 1% of population  | Neglectable                | Minor       | Major    |
| \< 1% of population   | Neglectable                | Neglectable | Minor    |

The evaluations and their justifications are recorded in the ticket, as well as the exposure duration (the elapsed time since the faulty resource was published).

## Treatment

The first treatment of the incident consists in restoring the resources to a safe state.

For a neglectable incident, the normal modification process is used. For a minor or major incident, the proposition and validation are performed by SYADEM experts within less than 2 working days, and the publication is done using an emergency process where validations are postponed.

## Communication

All tickets, current or past, are visible to all users having access to the portal.

For incidents that could impact several clients, such as those regarding the elementary conditions, a notification is sent by e-mail to all impacted clients when the incident is qualified, then for each of update of the ticket.

## Documentation

The incident ticket constitutes its documentation. Before it is closed, a root cause analysis cause is attached, including recommendations for technical or organizational enhancements to avoid its reproduction.

## Review

Once a year, all incident tickets are reviewed in a meeting between SYADEM and its Scientific and Ethical Committee, consisting of representants from all its clients.
