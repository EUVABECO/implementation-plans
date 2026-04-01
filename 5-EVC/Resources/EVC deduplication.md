# EVC DEDUPLICATION POLICY

# Purpose

This document is a recommendation to implementers on the procedure to apply when importing a European vaccination card (EVC) in a system that already holds vaccination records for the same patient.

# Principles

A same vaccination event can be recorded in the Electronic Health Records (EHR) of the patient and in the EVC, but with some differences in its representation. A decision process must then be applied to determine whether two similar records correspond to a same event or to two different vaccine administrations.

This decision belongs to the health professional performing the import, but the software should assist him by providing hints about the interpretation of duplicates.

Imported events can be classified according to matching with preexisting ones, with three options:

-   Exact matches,
-   Likely matches,
-   Probably a new event.

The health professional importing the EVC will be presented proposals to accept or reject events that do not match exactly.

# Classification method

Each vaccination event is identified with a date and vaccine code.

## Aligning the representations

The EHR may record the date with a different calendar than the Gregorian one used for the EVC, but the conversion is univocal and there should not be any discrepancy caused by different interpretations of dates.

The EHR may record the administered vaccine with a different codification than the NUVA used for the EVC, or no codification at all (textual representation).

The NUVA embeds concept maps to align other codifications, designated as “external codes”, with NUVA concepts. If it is a national or international standard, the code present in the EHR should be aligned with a NUVA concept, but it is also possible that this alignment is missing, either because the EHR code system is unknown or the NUVA concept map incomplete.

The EHR supplier may also embed its own concept map with NUVA, although he is then encouraged to share it with the NUVA curators to make it a public resource.

The health facility using the EHR may also be proposed to create by itself the mapping between the codes and the NUVA, either explicitly or by recording it progressively when EVCs are imported. This option should be restricted to the case where the codification of vaccines is created locally within the health facility.

A system using local concept maps, provided by the EHR supplier or created locally, can import EVCs but should not be entitled to deliver EVCs from its own data.

If, because of the restrictions of its local encoding, a system may degrade the information from an EVC, he should not be entitled to deliver EVCs from its own data. As a workaround, since it should store the EVC for future reference, it can reuse the EVC data.

In some cases, the EHR may use several code systems for a same record, with different level of precision, such as a national pharmaceutical code and the ATC code. It is recommended that the alignment process here relies upon the most precise representation.

Ultimately, there are thus two situations, with either no correspondence between the EHR vaccine record and a NUVA code (textual representation or no alignment available), or a correspondence that can be determined from a local mapping, a mapping provided by the EHR supplier or a concept map from the NUVA resources.

## Determining the equivalences

Depending how the information was originally captured, a NUVA concept can correspond to the designation of a fully identified vaccine, or of a generic class of vaccines. NUVA includes a transitive relationship between concepts stating that a given code is a more precise representation of another code. For example, VAC0053 (PRIORIX) is a more precise representation of VAC0130 (MMR vaccine), itself more precise that any of the three VAC0114 (Measles vaccine), VAC0153 (Mumps vaccine) or VAC0113 (Rubeola vaccine).

When comparing a record from the EHR and a record in the EVC within the same date, several scenarios are thus possible:

-   The EHR record cannot be transcribed to a NUVA concept.
-   The EHR record can be transcribed to a NUVA code and:
    -   The EHR code is identical to the EVC code.
    -   The EHR code is a specialization of the EVC code
    -   The EHR code is a generalization of the EVC code
    -   Any other situation.

If the EHR has several vaccines recorded for a same date, the best possible option will be used for assessing the matching of a NUVA record.

Each vaccine for the EVC will be classified as:

-   An exact match if a record in the EHR exists with the same date and the same code.
-   A likely match if a record in the EHR exists with the same date and a code that is a specialization or a generalization of the EVC code.
-   A probable new event otherwise.

# Presentation

When importing of an EVC, a health professional will be asked to validate each proposed record, with the possibility for each record to update his EHR with the data from the EVC.

It is proposed to present side by side the vaccination history from the EHR and the vaccination history from the EVC, with the differences highlighted and proposed actions on each item.

It is up to the implementer to decide about:

-   The format of the presentation, tabular, sequential, or else, as long as all records from the EHR and the EVC are presented.
-   the order of presentation, chronological, per disease, per vaccine, or else.

Some EHRs hold several records for a same vaccine, one for each target disease. A single MMR vaccine would then create three records in the EHR, and a same EVC record would be in Likely match with all of the three EHR records.

The presentation recommendations are thus:

-   A vaccination event that matches exactly (same day and same vaccine) between the EHR and the CDS is presented without requiring any further action from the health professional.
-   A vaccination event from the EVC that has likely match with an existing record in the EHR can be accepted or rejected for import.
-   A vaccination event from the EHR that has no likely match with a record in the EVC can be accepted or rejected. This would allow to deprecate records that have been entered by mistake.
-   For each vaccination event in the EVC, all likely matches from the EHR are presented. Each of these matches can be accepted or rejected.
-   When a match between an event in the EVC and an event in the EHR is accepted, all other matches for this same two events are rejected.
-   If all matches for a vaccination event in the EVC are rejected, it will appear as an event with no matching candidate, that can be itself accepted or rejected.
-   If all matches for a vaccination event in the EHR are rejected, it will appear as an event with no matching candidate, that can be itself accepted or rejected.

The table below is a possible representation corresponding to these rules, with action buttons A for Accept and R for reject.

-   Row 1 is an exact match, with the action buttons greyed out.
-   Row 2 is a likely match, with an EVC vaccine more specific that the EHR record.
-   Rows 3 and 4 one corresponds to a case where a bivalent vaccine was encoded as two events in the EHR.
-   Row 5 is an event present only in the EHR
-   Row 6 is an event present only in the EVC

![](media/deduplication1.png)

# Resolution by the health professional

When a health professional accepts a matching that is not exact, he is asked to choose the administered vaccine among the two paired events. If an event has a more precise vaccine designation, it will be proposed as the default choice.

In the example above, if the health professional accepts the first option for the August 01 record, the layout will be updated as follows:
![](media/deduplication2.png)


He can then reject the redundant Polio vaccine record.

Once all resolutions have been done, the health professional can validate the final result and the EHR is updated accordingly.
![](media/deduplication3.png)

For a given vaccine administration, if the health professional has kept unchanged the data from the EVC, the master record reference registered in the EHR can be the one from the EVC. Otherwise, the modified record becomes the new master record for future EVCs that would be delivered from this EHR.
