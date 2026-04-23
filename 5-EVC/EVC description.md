# EUROPEAN VACCINATION CARD (EVC) - FUNCTIONAL DESCRIPTION

# Objectives

*This section is the overall rationale for the tool.*

The European Vaccination Card (EVC) is a portable, self-contained document, provided to citizens to carry their vaccination history without loss of information across different European national or regional health jurisdiction.

Its primary purpose is the continuity of care, allowing the health professionals to maintain the adequate level of protection of the person by having access to a reliable restitution of the vaccination history.

It has a dual format, with both a text representation readable by humans and a digital representation readable by applications. This digital representation allows to:

-   Upload the data to any electronic health records (EHR) application for sharing within a health facility or organization.
-   Present the codified information in the language of the reader, that can differ from the original language of the text representation.
-   Feed a Clinical Decision System (CDS) to know the next actions to be undertaken.
-   Bind to informative resources about the received vaccines (ePIL).
-   Assess the authenticity of the record through a digital signature.

The content of the EVC is minimized and similar to what already exists in legacy vaccination cards with:

-   Basic identity traits (family name, given name and date of birth), that will allow the receiving health professional that the presented EVC matches with the presenting person.
-   History of received vaccines, with for each vaccine a date, the identification of the administered product and a reference to the administering health facility.

# Involved stakeholders and their expectations

*These are all the actors within the implementing Member State using or contributing to the use of the tool once it has been implemented. Their expectations are requirements for any implementation of the tool.*

The participants are:

-   The citizen if he retrieves, carries, or shares the EVC. He his either the subject of the EVC or his legal representative (e.g. parents of a child)
-   The health professional if he delivers or imports/reading the EVC
-   The health authority from the issuing health jurisdiction
-   The health authority from the receiving health jurisdiction
-   The EHR suppliers if they have to deliver or interpret EVCs
-   The e-Health infrastructure operators
-   The accredited digital signature operators
-   The European Commission, as the guardian of the portability promise,
-   The WHO, acting as the reference for the trust chain across health jurisdiction through the Global Digital Health Certification Network (GDHCN)

## Citizens

For citizens, the EVC replaces the traditional, paper-based vaccination card, offering the benefits of being an authentic, replicable, explicit, automatically translatable to any language, and easily shareable with health professionals or health applications.

They expect a document at their hand, in a familiar format, easy to access and to transfer.

## Health professionals

The health professionals take the initiative of delivering or accepting EVCs. They will adopt the EVC only if they find a benefit in its use.

This benefit is visible when they import an EVC, since it saves them a work of entering the vaccination history into their own EHR application.

They have no immediate benefit in delivering an EVC, apart from occasionally satisfying a request from their patients or specific legal frames. It means that the effort for this delivery must be minimal, with a simple action from their own EHR application.

In countries where a Immunisation Information System (IIS) shared across health professionals has been deployed, the import or delivery of EVCs can be less useful, since the same data can be retrieved from or published to the IIS. Yet, the EVC will still be useful:

-   for patients that, by choice or because they are foreigners, are not recorded in the IIS,
-   for local patients travelling abroad.

The IIS itself would then be the tool used to import and deliver.

When they import an EVC, health professionals should be confident about the authenticity of the received information. They will want a clear distinction between the administrations reported under their responsibility, because they performed or recorded the action, and the ones coming from other parties (historical certified vaccination data).

## Issuing health authority

The issuing health authority must accredit the health professionals allowed to deliver an EVC, entitling the various health professions (medical doctors, nurses, pharmacists, midwives, etc) to perform or record vaccinations according to the local rules.

It must identify the different software applications allowed to deliver an EVC and organise an approval process to make sure that the delivered EVCs are readable by any other compliant application.

It must make sure that the proofs of authenticity (digital signature, binding to master records) are effective and accurate, and collaborate with the investigations on EVC records from any receiving health authority.

## Receiving health authority

The receiving health authority needs to organise the trust in the delivered information. It should use a common infrastructure, namely the WHO Global Digital Health Certification Network (GDHCN), with all issuing health authorities for the digital signature.

It must set an alert channel for suspicions of fraud and liaise with the health authority of the country where the master records are held for further analysis.

## EHR suppliers

The EHR suppliers, editors of the EHR applications supposed to import or deliver EVCs, need a technical toolbox to support these operations and ensure the compliance of their solutions. This toolbox could encompass:

-   An open-source implementation under a liberal license
-   Reference implementations and compliance test suites

Alternatively, they could rely upon preexisting interfaces with an IIS or a national repository of structured health documents.

## E-Health operators

The e-Health operator may be mandated by the health authority for:

-   Handling technically the authentication of accredited health professionals.
-   Setting up the infrastructure for the digital signature of the EVC. This may require collaboration with an external digital signature operator.

When relevant, an e-Health operator may have to integrate the import and delivery of the EVC into national resources such as an IIS or a repository of health documents. His expectations are then similar to the ones for an EHR supplier.

## Digital signature operators

Depending upon the organisation of the MS, the digital signature operators accredited for signing digital health records may be identical to the e-Health operator or can have a more general scope for all official signatures.

They have their own policy for the management and the use of their public key infrastructure (PKI).

They must participate in the WHO GDHCN, so that their public keys are identified and accepted by any other country.

## European Commission

Contrary to the other tools in EUVABECO, the EVC is relevant only if it is implemented consistently across all MS. After the end of the EUVABECO project, it will belong to the EC to organise the long-term management of the interoperability resources (structural and semantic) used for the EVC.

## WHO

The trust in EVCs should rely upon the GDHCN, a common repository of acceptable signatures curated by the WHO. The digital signatures operators must comply with the GDHCN rules.

By October 26h, 2025, among the 27 EU MS:

-   16 were already fully onboarded in GDHCN: Belgium, Cyprus, Czechia, Estonia, Finland, France, Ireland, Latvia, Lithuania, Malta, Netherlands, Slovakia, Slovenia, Spain, Poland and Portugal.
-   5 were onboarding: Croatia, Greece, Hungary, Luxembourg and Sweden.
-   6 were still to apply: Austria, Bulgaria, Denmark, Germany, Italy and Romania.

Worldwide, there were then 82 participants.

# Constraints

*Constraints are the non-functional requirements on the tool. They do not correspond to a function to be performed by the tool but not respecting them would impair the viability of the tool.*

## Personal data protection

The EVC by itself is a private document held by a natural person and does not fall under the scope of the GDPR.

Most of the means used to create or process it are EHR applications that are already entitled to use the same data, since they are used for the purpose of preventive or occupational medicine (GDPR Article 9.2.h).

Specific care has to be taken with the signature infrastructure, that must preserve the confidentiality of the data to be signed. Only statistical data on the use of the infrastructure should be retained.

## Accessibility

No information on the EVC should be hidden from the citizen. Each EVC can be printed with a readable content. Although the printed section of the EVC may be simplified (keeping only the date and vaccine product for each administration), dedicated online readers or mobile applications should allow to display every content.

## Non-discrimination

Paper-based vaccination cards have been around for more than one century. The EVC is only an augmented presentation of it. Yet, nobody should be deprived of any right or service because he does not hold an EVC. All use cases relying upon the EVC should also be possible based upon traditional vaccination cards, even if they demand more effort or the intermediation of a health professional.

# Use cases

*The use cases are illustrative scenarios representing how the actors identified above could use the tool to meet their expectations. They are as many use cases as needed to describe every desired function of the tool.*

The use cases below are built across the fictitious states of Alpharia, Betaria and Gammaria.

## UC01 – Delivering an EVC

### Actions

In Alpharia, Dr Costa receives her usual patient, Anna, a 27-year-old nurse. She is about to move from Alpharia to Betaria for several years and wants to carry her vaccination information.

Dr Costa access to Anna’s patient record in her EHR application. All Anna’s vaccinations are already documented there, she clicks on the “EVC” button and downloads the PDF document for the EVC. She asks Anna if she wants to receive it by secured file transfer or have a printout. Anna prefers a secured file transfer (out of the scope of this document, various public or private solutions exist with diverse restrictions according to MS regulations), so Dr Costa sends it to her. A local copy of the EVC is also kept into Dr Costa EHR application for future reference.

### Behind the scenes

A vaccination event in an EVC consists of a date of administration, an identifier for the administered vaccine, and the reference of a master record, that is a vaccination record held by any authorized EHR application in Europe attesting that the vaccination was performed or recorded by an accredited health professional using this system. There can be several master records for a same vaccination event, if several health professionals decided to endorse the information.

The EHR application assembles a vaccination history from the vaccination records it holds. For each vaccination event, it can use a memorized master record or declare itself as a new master record holder.

It then sends it for compacting and digital signature to a national pool of servers deployed by the eHealth operator.

A server in the pool packs the vaccination history for signature, then sends it to the digital signature operator.

The signed vaccination history forms the EVC. It is returned to the eHealth operator server, then to the originating EHR application.

The EHR application then builds the PDF document with the vaccination history printed in plain text and the signed digital information, both within the QR Code and in the metadata of the PDF document.

## UC02 – Translating an EVC

### Actions

The EVC held by Anna is written in Alpharian, while she wants to have it now in Betarian.

She connects to a public Betarian online EVC viewer and uploads there the EVC she has received from Dr Costa. She then views her vaccination history rebuilt from the digital representation in Betarian. She downloads the translated EVC as a PDF document.

### Behind the scenes

The EVC viewer application is a service proposed by the Betarian eHealth operator. It retrieves from the uploaded EVC the identifier of the key used for signing it and fetches from a local copy of the WHO GDHCN database the corresponding public key. It uses it to check that the signature is valid, and thus the EVC genuine. It then can present the corresponding textual view in Betarian.

The digital representation of the EVC is unchanged, whatever the language used for its textual representation. Thus the EVC downloaded from the viewer application has exactly the same digital representation as the original EVC from Dr Costa, without any need for a new signature process.

## UC03 – Importing an EVC for a new patient

### Actions

Once arrived in Betaria, Anna visits her new doctor, Dr Muller, at the hospital where she will work. She presents a printout of her EVC.

Dr Muller creates her a patient record in his EHR application. He scans the EVC with a 2D barcode reader. The name, given name and date of birth of Anna are presented, so that he can confirm they correspond with his patient. He validates the import, and all vaccination records are entered in Anna’s record.

### Behind the scenes

The digital content of the EVC is captured with the QR Code. The EHR application checks the validity of the EVC with the same mechanism as the EVC viewer. It then unpacks the digital content, displays the identity traits (name, given name and date of birth), and after confirmation from Dr Muller includes all the vaccination records into the current patient record.

Each vaccination record is accompanied by its link to the corresponding master record. Another option would have been to endorse the vaccination records locally and consider that the newly created records are also master records, but this would engage more the responsibility of Dr Muller.

If Dr Muller did not have an EVC enabled EHR application, he could also use the public EVC viewer to check that the document is genuine and its text representation aligned with the digital representation, then keep it as a paper record.

## UC04 – Updating an EVC

### Actions

Anna will work into a paediatric service, and she has to be revaccinated against pertussis. Dr Muller administers to Anna her booster dose against pertussis, records it into his EHR application, and delivers to her an updated EVC including the newly administered pertussis vaccine.

### Behind the scenes

The pertussis vaccine performed locally by Dr Muller is immediately recorded as a master record.

The elaboration process for the EVC is then equivalent to the one used in Alpharia by Dr Costa, but the signature is performed by the Betarian infrastructures.

## UC05 – Reconciling two EVCs

### Actions

When unpacking her boxes, Anna found a partial EVC that she was given at a travel vaccination centre three years ago when she got the yellow fever vaccination. She had never reported this vaccination to Dr Costa in Alpharia, and this it is missing in her last EVC.

On her next day at the hospital, she sees Dr Muller and shows him the old EVC. He scans it and is presented with a comparison screen showing the differences:

-   Vaccines prior to the yellow fever administration are both in the old EVC and the EHR.
-   The yellow fever is vaccine is in the old EVC but missing in the EHR.
-   Vaccines administered after the yellow fever one are in the EHR, but not the old EVC.

Dr Muller revalidates all new records from the EHR except the yellow fever one, plus the yellow fever from the EVC. He then delivers to Anna a new EVC.

### Behind the scenes

The EHR application includes a comparison function that compares its preexisting records with the ones from a submitted EVC. This function includes a tolerance when two vaccination events are recorded at the same date, for a same vaccine but with different levels of precision is the vaccine product encoding, such as “FLUARIX” and “Flu vaccine”. The identification of a same vaccine at different levels of precision is possible based upon a structured description of vaccines (the NUVA terminology used in the EUVABECO project).

## UC06 – Obtaining a vaccination certificate

### Actions

Anna has to provide to the administrative services of the hospital a proof that she has received every mandatory vaccine foreseen for a nurse in a paediatric service, according to the Betarian law. Since the administration does not have to know of the details of her vaccination, they only require a vaccination certificate rather than a full vaccination card.

Anna connects to a vaccination certificates platform provided by the Betarian eHealth operator and selects the purpose of the certificate. She then uploads her EVC and receives in return a vaccination certificate. This is again a PDF document enriched with a signed digital content, but stating only that at the date of today she was compliant with the enforced rules for her role.

She can then address this certificate to the hospital administration without any need to disclose all or part of her vaccination history.

### Behind the scenes

The vaccination certificates platform runs a Clinical Decision Support System (CDS) to determine whether Anna received all the vaccine series required for her occupation. It then generates a certificate using the same technology as the EVC, but with a content limited to the identity traits from the EVC, the purpose of the certificate and a binary decision on compliance.

The vaccination certificates platform is actually able to deliver certificates for different purposes, using a set of rules specific for each purpose. For example, there could be another model of certificate for accepting children in kindergartens.

## UC07 – Checking upon a fraud suspicion

### Actions

In her service, Anna receives a child that presents symptoms of meningococcus, although his EVC indicates that he was vaccinated, according to a record held in Gammaria.

While treating the patient, she submits to the Betarian health authority a request for verification, containing the identification of the master record in Gammaria and the date of birth of the child (this is the only attached personal information, not allowing for reidentification).

The Betarian health authority forwards the request to the Gammarian health authority, that determines which health structure holds the master record, and forwards again the request to this health structure.

Ultimately, it comes out that the vaccination had been recorded in the health structure because it was performed there, but that they had at the same period a conservation problem that was duly registered.

Gammaria reports to Betaria that the record was genuine, although the vaccine was defective. Anna adds the information to the vaccine record into her own EHR application and makes it a new master record to facilitate tracking if it was questioned again.

### Behind the scenes

This forensic process is exceptional and non-automated. Adequate communication channels have to be set up within each MS and between the MS to transmit and track the requests.
