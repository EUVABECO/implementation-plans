# EVC REGISTRIES AND REPOSITORIES MANAGEMENT

# Purpose

This document is a recommendation to implementers on the management of their registry of authorized issuers of European Vaccination Cards (EVCs).

# Principles

Systems delivering EVCs must keep detailed information about each vaccine administration in secured repositories. These constitute the master records that are referenced for each vaccine listed into an EVC.

Depending upon the organisation of a health jurisdiction, there can be a single national or regional repository, several ones, or even as many repositories as delivering health structures.

It belongs to the health authority to keep a registry of these repositories, that will be consulted when enquiries are received about a given master record.

A global directory of registries is managed by a central authority. It will initially be managed by the EUVABECO project.

Within the EVC, a master record is identified by a three letters code for a registry, then two numeric indexes, the first one identifying a repository in the registry, the second one a master record in the repository.

Since these references are held in EVCs that may be distributed anywhere, no record in a registry or repository should be deleted, unless clearly outdated.

# Directory of registries

The directory of registries is a unique global list of registries.

Each registry is identified by a code of up to 6 letters, attributed by the directory holder. Whenever possible, the registry code with be the ISO 3166 alpha 2 code for a country wide registry, or an ISO 3166-2 code for subdivisions of countries. For example:

-   FR, LT, PL respectively for France, Latvia, Poland.
-   BE-WAL, DE-SL, IT-25 respectively for Wallonia, Saarland, Lombardy

Registries that do not match with a country or region coded in ISO 3166 will receive an identifier that cannot be confused with an ISO one, typically with a \* as its third character.

The directory of registry is a public table consisting of:

-   The registry identifier
-   A descriptive label
-   A link to the public part of the registry, exposed and maintained by the health authority holding the registry.

# Registry

## Content and format

The registry is a table of repositories, consisting of a public part exposed through the link from the directory of registries and a private part for the use of the registering authority.

The public part contains:

-   A numeric index identifying a repository.
-   A label.
-   A status of the repository, that can be active or closed.
-   Dates of registration and of closing of the repository.

The private part complements it with:

-   Any additional information needed for the registry holder to identify the repository holder, such as a health structure identifier, a business register identifier, etc.
-   A contact person within the registry holder, with postal, phone and e-mail addresses. The person can be identified nominatively or as a role.

Any format convenient for the registering authority is acceptable.

## Registering new repositories

Repositories must be declared to a registering authority by the repository owner before any usage.

Systems delivering EVCs must obtain credentials (client certificates) to access to the signature servers. To make sure that all repositories are adequately registered, the request for these credentials should include the list of repositories where the system will store master records. The credentials should only be granted if all listed repositories exist.

## Updating repository information

The repository owner can update the status or the private details of his repository through simple declaration to the registering authority. A repository that has been closed cannot be reopened.

# Repositories

## Content and format

Any vaccination records held by an accredited health professional or institution can serve as a repository, as long as it is possible to retrieve from it a record identified by the date of administration of the vaccine and the numeric index stored in the EVC. Even paper records could be a suitable format.

Under normal circumstances, the value for this index is limited to 1.000.000. According to the activity of the repository, it can be reinitialized every day or less frequently. This daily threshold can be exceeded under exceptional circumstances (at the peak of COVID vaccination campaign, 5 million vaccinations were recorded in France for the week 13-19 of December 2021).

A vaccination record can correspond to a vaccine administered within the health facility, or to a vaccine only recorded there on the basis of previous proofs of vaccination, such as a paper vaccination card.

The record should contain at least:

-   the identity of the patient,
-   the date of administration,
-   the vaccine product used (as precisely identify as possible)
-   the identity of the recording health professional
-   whether this professional performed or only recorded the vaccination.

## Declaring a repository

The repository owner must declare its repository to his registering authority.

This declaration should include the information required for the registry entry, plus evidence on the measures taken by the owner to guarantee the century-long availability of the repository content. These measures should include at least:

-   Backup and retention strategies.
-   Policy to detect and to react obsolescence of formats and tools.
-   Policy to transfer the repository on dissolution of the organization.

## Closing a repository

The repository owner may close its repository through declaration to the registering authority. Closed repositories cannot receive further records but must be retained and kept available for reference enquiries.

## Transferring a repository

A repository can be transferred to another structure, typically when the holding structure ceases its vaccination activity. Apart from the technical operations of transfer, this must be declared to the registering authority by changing the contact information.

The receiving organization may wish to merge the transferred repository with its own one. Yet, even if the records are duplicated to the new repository, the original one must be retained and keep its identification until all its records are outdated.
