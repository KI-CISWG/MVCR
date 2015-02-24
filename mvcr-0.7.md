# MVCR-Specification-restructure
## Minimum Viable Consent Receipt  Specification

The 0.7 version of this specification focuses on the user experience--
specifically, what they will see in a Minimum Viable Consent Receipt.  Future
versions of this specification will add material to allow for the technical
implementation of an MVCR.


# Introduction
Consent and the notice's required for consent when sharing personal information is currently managed with each organisations separately, by an individual. Often faced with a static and binary notice and consent infrastructure that is not usable.  An individual is expected to read the policies, understand all of the information sharing relationships, manage individually each consent and personal information relationship with their associated identities all of these organisations.

As information sharing is dramatically increasing, the capacity for people to manage information sharing relationships needs also to increased.  Addressed by creating a specification for the most minimum as well as generically viable Consent requirements. (With reference to ISTP consent requirements)

The capacity is then in increased as people are able to manage consent and information sharing relationships on aggregate and organisations can then use this to stream line the consent experience.  As well as advertise trust!   A consent receipt then becomes a vehicle for carrying trust marks, privacy icons, assurances, certifications, and self asserted community and industry reputations.

# Background

Information sharing is a complex issue as organizations that require consent have specific legal obligations related to the context and the collection of personal information to enable meaningful consent.  These obligations require privacy policies notices about how personal information may be collected, used, disclosed,and or retained.  As each organisation post their policies in different locations, and often change the URI and the policies, this is systematically unusable. Organisations have their own best practices, policy structures and policy formats this results in a closed (or silo) level of transparency, very costly to manage for the individual and difficult to regulate.

The Consent & Information Sharing WG is distilling a small common set of consent requirements for information sharing that are salient across jurisdictions with FIPPs based privacy instruments and standards.(footnote)  Aiming to use these for a common generic set of consent requirements. Specifying the minimum required links, fields and data formats to meet the minimum obligations for information sharing.

# Objective

The Minimum Viable Consent Receipt (MVCR) specification to provide a generic for standard that provides a verifiable metric.

Its intended to be used with CISWG Use cases.

# Scope
This v.06  MVCR specification further defines the requirements for a Minimum Viable Consent Receipt  (MVCR).
In this version the scope is very narrow to the context of when a user takes an action to consent.   During or immediately after their personal information is collected.

The receipt format is machine readable and iconically usable.


# Stakeholders

There are three general stakeholder groups:
1. People
- People receive the consent receipt and use this to track and make transparent consent and data control conditions.

2. Organisations - (profitability)
- Organisation provide consent receipts when they harvest consent and collect personal information. The more complex the information sharing requirements i.e. the frequency of policy changes, the sensitivity of data collected and its context, the number of third parties.

3. Regulators - (privacy and data protection enforcement)
- Regulators i.e. the FTC in the USA, the Canadian Federal and Provincial Privacy Commissioners, the EU Data Protection Regulators
- Regulators provide public process for administration and enforcement of regulation in regards to notice and consent requirements

In summary, MVCR receipt is comprised of these three stakeholder requirements with the aim to provide business infrastructure that people use and regulators can enforce.


## Intellectual Property Rights
This document is being developed by Kantara Initiative's Consent and
Information Sharing Working Group; see
<https://kantarainitiative.org/groups/ciswg/>. Participation is free
and open, and all work contributed to the effort falls into the Reciprocal
Royalty Free with Opt-Out to Reasonable And Non discriminatory (RAND) IPR
policy <https://kantarainitiative.org/confluence/x/mQByAg>.

Kantara Initiative is a non-profit membership organization that connects
businesses, consumers, governments, and citizens through innovations and
programs that support more natively trust worthy on-line experiences. The
mission of KI is to foster identity community harmonization, interoperability,
innovation, and broad adoption through the development criteria for
operational trust frameworks and deployment/usage best practices for privacy-
respecting, secure access to trusted online services.

## MVCR Requirements


1. The receipt MUST have a property to authenticate the origin.

2. The receipt MUST have an integrity protection property.

3. The audience SHOULD be restricted.

4. The receipt SHOULD be able to be transmitted over various transport protocols.

5. The payload MUST have a human readable section, and SHOULD have a machine readable section.

6. The payload MUST include the following properties:

 a) Issuer

 b) Date

 c) [TBD]

7. The payload SHOULD include the following properties:

 a) [TBD]

Receipts need to make consent in informations sharing systematically usable and automate the discovery and hence usability of consent.

Be usable as a consent token to enable transparent digital audit trails of consent for   information sharing relationships.

## MVCR Fields
The fields consists of:

 * Contact information of Data Controller

 * Identity provided by the individual

 * Link to privacy policy
 (note: static link format required - raised by John W) (Comment: Note: For
the consent receipt to be audit-able and verifiable the consent policy should
be accessible by any entity with the URI for the policy. Subsequent changes to
the policy should not invalidate the URI for the policy in effect with the CR
was issued.)

 (Discussion Point : Rationale: If invalidated (URI Is broken), is the consent
still compliant?  If the policies (materially) change is a process needed to
update broken links and the consent before receipt can be used as a token?)

 * The purpose(s) listed: itemised on receipt

 * YES or NO Flags

   * 3rd party data sharing

   * Sensitive Personal Data Collection

   * Context Scope and Requirements


## MVCR - Default Settings

Default settings in the MVCR which are
represented by the Yes/No  flag settings -  (No) 3rd party sharing, (No)
collection of sensitive personal data, and an optional,checklist for self
asserting that the consent harvested is, fair, reasonable and conforms to the
law where it is issued.

Compliant by default represents the express (or highly automated) version of
consent, and is used to match the current 'click ware' consent system that is
common today. It is this version that is based on compliance requirements.
Compliance requirements are based ultimately on a number of sources, legal
regulation,  3rd party contracts, previous legal judgment, case and statute
law and best practices.  These all become relevant beyond the minimum viable
CR default self assertions.

The consent receipt and default settings are based on ISTPA work with reference: (http://xml.coverpages.org/ISTPA-AnalysisOfPrivacyPrinciplesV2.pdf)

Note: In each jurisdiction their are exceptions to consent which are not
covered in the MVCR but should be referenced in reference the MVCR default settings.

### Consent Notice Fields and Descriptions

| Term | Definition | Example |
| ---- | ---- | ---- |
| Consent Receipt  (CR) | A record of a single consent transaction provided to (or obtained by) the data subject as a receipt.  | This record is a summary of legal requirements of  the notice and a capture of consent related data provided at the point of consent. |
| Data Controller (DC) | The organization or individual that is accountable for the operation of the web site. | This is contact information for the management of consent. |
| Data Subject (DS) | The natural person that is registering on the web site. | This is typically when a person registers to get access to a web site service. |
| Identity Provider (IdP) | A third party that uses identity and/or authentication information about the data subject for access management. | |
| Minimum | A Receipt will contain the purposes to which is consented to | The links to all policies that inform the consent and the contact information of the data controller. |
| Operational Context of Consent | The list of legal (best practice) requirements for notice for consent in the jurisdiction and context in which the consent is given. | This includes jurisdiction requirements as well as the contextual elements to the method of consent capture |
| Personally Identifiable Information (PII) | Any information that (a) can be used to identify the Data Subject to whom such information relates, or (b) is or might be directly or indirectly linked to a Data Subject. | |
| Sensitive Personally Identifiable Information (SPII) | this a flag in the consent receipt that is used for what is legally defined as sensitive and protected data, this varies from jurisdiction to jurisdiction. For this type of data explicit consent is required and a consent receipt extension is needed for this functionality. | include health, financial, children’s data,  sexual data, political/religious data, surveillance data,  (note I think this should include participate in identifying SPII |  |


# Appendix A: Flags Defined

### 3rd  Party sharing (TBD)

### Sensitive Personal Data (TBD)

### Operational Context (OC): Consent Context Scope & Requirements

As a part of creating a receipt for a Data Subject (DS) there are often legal
requirements based on the operational content(OC). OC requires that a checklist
accompany the receipt. This functions as a flag: YES or NO.

i.e.
If YES, there is a self-assertion that the receipt and company side
consent management practices follow the legal requirements for fair and
reasonable consent harvesting.

Operational Context - Defined by either jurisdictionally specific requirements
or use case specific requirements. The OC also is a space/scope for company
side assertions (e.g. customer service, quality, etc.).
