# CLINICAL DECISION SUPPORT SYSTEM (CDS) - PREREQUISITES

| *This module lists the contextual conditions that must be met before the project is launched, and a few workarounds that could be used to anticipate upon their fulfilment.* |
||

# Prerequisites

## Assessment of prerequisites

*Prerequisites represent the broader context or resources necessary for the successful implementation and operation of the CDS tool. Although not specific to the tool itself, these prerequisites are essential for ensuring its proper functioning once deployed.*

### Operational

To ensure trust in the recommendations delivered by the CDS, a credible and functioning National Immunization Technical Advisory Group (NITAG) is essential. NITAGs provide the scientifically grounded recommendations that are endorsed by health authorities. The NITAG Maturity Assessment Tool[^1].developed by the Global NITAG Network (GNN) in collaboration with the Centres for Disease Control and Prevention, the World Health Organization and the Task Force for Global Health, provides a solid framework for assessing the credibility of NITAGs. This tool evaluates NITAGs across seven indicators:

[^1]: [https://www.nitag-resource.org/external/nmat/\#/](https://www.nitag-resource.org/external/nmat/#/)

1.  Its formal existence, with written rules on its composition, a diversity of expertise and clear membership rules.
2.  Transparency and independence of members.
3.  Appropriate resources and secretariat support.
4.  Regular meetings with formal rules for operations and evaluation.
5.  Recommendations based on evidence and communicated in a structured way.
6.  An established process of collaboration with the Ministry of Health for enforcing and monitoring recommendations.
7.  Recognition of their role by the stakeholders and the general public.

Of these, at least indicators 2, 4, 5 and 7 should reach the Intermediate level (level 3 on a scale of 5).

### Legal and ethical

All CDS users (data processors) and suppliers (subcontractors) must comply with the personal data protection requirements outlined in the Constraints chapter 1.3.1.

Additionally, the CDS solution (software engine and ruleset) must be registered as a medical device under the MDR regulation.

### Political

In most countries, only a very limited set of vaccinations are mandatory, in which case they are also paid by the health insurance system. The CDS tool’s purpose is not to impose additional obligations, but to simplify complex decision-making processes. However, in settings where vaccine hesitancy is prevalent, even offering “recommended vaccinations” could be controversial.

If the health authority’s legitimacy is not well established, the CDS could become a target for political disputes.

### Technical

The CDS service must be accessible in all locations where vaccinations are performed, with constant updates to reflect the latest official recommendations. Whether centralized or distributed, the system requires a reliable Internet infrastructure to ensure seamless connectivity between any point in the Member State and the CDS data distribution centres.

## Filling the gaps

*Meeting the prerequisites is often a long-term endeavour that goes far beyond the scope of the implementation plans. This section suggests potential workarounds for launching the CDS project even when some prerequisites are not fully met. Although these measures may not deliver the full benefits immediately, they can create the visibility and momentum needed to justify further efforts to meet the prerequisites.*

This section provides hints on how a CDS project could be launched although the prerequisites above are not satisfied yet. It will impede reaching the full expected benefits but provide enough visibility and momentum to justify the effort of achieving the prerequisites.

### Operational

In the absence of a relevant and credible NITAG, an alternative trusted medical authority could be used. This could be a supranational organization, such as the WHO's Essential Program on Immunization (EPI), or a respected local health institution, possibly specialized in specific patient conditions (e.g., cancer or diabetes) or traveller vaccination programs.

### Legal and ethical

The GDPR provides a harmonized data protection framework across Member States. However, protective measures vary depending on the CDS implementation. The EUVABECO project offers a sample Privacy Impact Assessment that can be adapted by the implementer, assisted by the CDS provider, to the specific context of the CDS project.

A CDS that has not yet achieved MDR compliance (due to lack of clinical evidence, for example) could still be used in non-clinical contexts, such as training health students, conducting retrospective decision analyses, or guiding citizens - an option preferable to general web searches.

### Political

In contexts where vaccination itself is contested, endorsing the CDS through official channels might be counterproductive. A temporary solution could be to position the CDS as a private initiative, possibly delivered by non-governmental organizations (NGOs) and targeted at voluntary users, using publicly available vaccination recommendations.

### Technical

Depending upon its design, the CDS may not require high-end connectivity. This should be considered when selecting a solution for countries where such services are not generally available.
