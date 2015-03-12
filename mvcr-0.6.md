# MVCR-Specification-Restructure
## Minimum Viable Consent Receipt Specification

The 0.6 version of the MVCR specification focuses on the requirements for the MVCR specification. Future versions of this specification will add additional material to allow for the technical implementation of an MVCR.  As a result this version of the specification has been reduced with material from previous edits being added in according the stage and agreed roadmap of the MVCR in the CISWG.

# Introduction & References
The MVCR comprises the core Consent Receipt (CR) specification and specifically refers to the notices required for consent to be valid when collecting personal information.  This is currently managed by each organisations separately, with bespoke policies that are closed to systematic use by an individual.  The MVCR addresses this problem.

The MVCR is written with terms and reference in context of:
* ISO/IEC 29100	Information technology – Security techniques – Privacy framework
* ISO/IEC 29115	Information technology – Security techniques – Entity Authentication Assurance


Supporting reference to ISTPA: Analysis of privacy principles:
* ISTPA, (2007) Analysis of Privacy Principals, pg. 64, [Online] http://www.istpa.org/ [Accessed Nov, 4 2010]
* Minister of Economy Office, Japan (2014) Guideline for the online notice and consent from  consumers, http://www.meti.go.jp/press/2014/10/20141017002/20141017002a.pdf. [[Includes examples of a consent receipt in guidelines proposed in the context of ISO 29100]

# Problem Described
Currently there is a static and binary notice and consent infrastructure that is regulated and neither usable nor suitable for its intended purposes.  An individual is expected to perform beyond what is reasonable in the current context. They are expected to find and read policies, understand all of the information sharing relationships in context, and manage each consent and personal information relationship with their associated identities with all of these organisations. In other words, each individual is expected to understand what information is being collected about them, how it will be used and for what purposes, with which types of entities their information will be shared. All of this is expected without having the ability to take a record and manage consent independently out of context.  Meanwhile in context people are expected to keep track of all active consent, when making new consent agreements.

Information sharing is dramatically increasing so the capacity for people to manage information sharing and identity based relationships needs also to increase.  A specification for a minimum core generically viable consent can address specific jurisdictional requirements and provided evidence of compliance with ISO 29100 or other privacy frameworks.

Individuals' capacity to manage their privacy is  increased if they are able to aggregate and manage consent & information sharing relationships with consent receipts.  Organisations can use these receipts to standardize the consent experience.  Consent receipts also provide a channel for  organisations to advertise trust.

The core receipt specification addresses general, or regulatory, consent requirements. More elaborate consent receipts can become a vehicle for trust networks, federations, trust marks, privacy icons, assurances, certifications and self asserted community and industry reputations.

# Background

Information sharing is a complex issue as organisations that require consent for the collection of personal information from individuals have specific legal obligations related to the context and the collection of those data.  These obligations require privacy policies and/or notices about how personal information may be collected, used, disclosed, retained and disposed of.  As each organisation posts their policies in different locations, and often change the content and URI of the policies, this is systematically unusable. Each organisation has their own best practices, policy structures and policy formats. This results in a closed (or 'siloed') type of transparency, that violates the  Openness (transparency and notice) privacy principles, is very costly to manage for all stakeholders and very difficult to regulate effectively.

# Executive Summary

The Consent & Information Sharing Working Group (CISWG) is distilling a small common set of consent requirements for information sharing that are salient across jurisdictions with Fair Information Practices based privacy instruments and standards.(ISO and ITPA footnote)  The aim is to use these for a common generic set of consent requirements and to specify the minimum required links, fields and data formats to meet the minimum obligations for information sharing.

# Objective

The Minimum Viable Consent Receipt (MVCR) specification will provide a generic standard that provides a verifiable metric. It is intended to be used with CISWG use cases.

# Scope

This v.06  MVCR specification further defines the requirements for a Minimum Viable Consent Receipt(MVCR). In this version the scope is limited to the context of when a user takes an action to consent to sharing information, noting that personal data will be collected in a consent transaction. This consent can occur before, during or immediately after their personal information is collected.

The receipt format is human and machine readable and may include icons. It will be accessible.

# Stakeholders

There are three general stakeholder audiences for the MVCR which are referenced through this material:

1. People:
People receive the consent receipt and may use this to track consent and exert control over information about themselves.

2. Organisations:
Organisations provide consent receipts when they obtain or assume consent and collect personal information.

3. Regulators - (privacy and data protection enforcement)
Regulators i.e. the FTC in the USA, the Canadian Federal and Provincial Privacy Commissioners, the EU Data Protection Regulators. Regulators may provide public processes for administration and enforcement of regulation in regards to notice and consent requirements

In summary, this MVCR receipt specification addresses the requirements of these three stakeholder groups with the aim to provide a business infrastructure organizations will implement, that people can use and that regulators can enforce.

## Intellectual Property Rights
This document is being developed by Kantara Initiative's Consent and Information Sharing Working Group; see <https://kantarainitiative.org/groups/ciswg/>. Participation is free and open, and all work contributed to the effort falls into the Reciprocal Royalty Free with Opt-Out to Reasonable And Non discriminatory (RAND) IPR policy <https://kantarainitiative.org/confluence/x/mQByAg>.

Kantara Initiative is a non-profit membership organization that connects businesses, consumers, governments, and citizens through innovations and programs that support more natively trust worthy on-line experiences. The mission of KI is to foster identity community harmonization, interoperability, innovation, and broad adoption through the development criteria for operational trust frameworks and deployment/usage best practices for privacy-respecting, secure access to trusted online services.

## Generic Requirements (TBF v.06)
The word “SHOULD” indicates a recommendation and does not impose an obligation. The word "CAN" means that this is a common option.

1. The receipt MUST have a property to authenticate the origin.
2. The receipt MUST have an integrity protection property.
3. The audience SHOULD be restricted and transparent.
4. The receipt SHOULD be able to be transmitted over various transport protocols.
5. The payload MUST have a human readable section, and SHOULD have a machine readable section.
6. The payload MUST include the following properties:
  a) Issuer
  b) Date
  c) Time
  d) direct contact information to data controller
  e) Contain a static Link to privacy policy
  f) Purpose (s)
  g) YES or NO Flags
    * 3rd party data sharing
    * Sensitive Personal Data Collection
    * Context
7. The payload SHOULD include the following properties:
  a) A description of the types of personally identifiable information to which the consent applies.
8. The payload SHOULD include the following information:
  a) the personal identifier used in the consent receipt
  b) some or all of the personally identifiable information to which the consent applies

### Consent Notice Fields and Descriptions (TBF v.07)

| Term | Definition | Example |
| ---- | ---- | ---- |
| Consent Receipt  (CR) | A record of a single consent transaction provided to (or obtained by) the data subject as a receipt.  | This record is a summary of legal requirements of  the notice and a capture of consent related data provided at the point of consent. |
| Data Controller (DC) | The organisation or individual that is accountable for the operation of the web site. | This is contact information for the management of consent. |
| Data Subject (DS) | The natural person that is registering on the web site. | This is typically when a person registers to get access to a web site service. |
| Identity Provider (IdP) | A third party that uses identity and/or authentication information about the data subject for access management. | |
| Minimum | A Receipt will contain the purposes to which is consented to | The links to all policies that inform the consent and the contact information of the data controller. |
| Operational Context of Consent | The list of legal (best practice) requirements for notice for consent in the jurisdiction and context in which the consent is given. | This includes jurisdiction requirements as well as the contextual elements to the method of consent capture |
| Personally Identifiable Information (PII) | Any information that (a) can be used to identify the Data Subject to whom such information relates, or (b) is or might be directly or indirectly linked to a Data Subject. | |
| Sensitive Personally Identifiable Information (SPII) | this a flag in the consent receipt that is used for what is legally defined as sensitive and protected data, this varies from jurisdiction to jurisdiction. For this type of data explicit consent is required and a consent receipt extension is needed for this functionality. | include health, financial, children’s data,  sexual data, political/religious data, surveillance data,  (note I think this should include participate in identifying SPII |  |


# Appendix A: Flags Defined (TBF v.07)

### 3rd  Party sharing

### Sensitive Personal Data

### Operational Context (OC): Consent Context Scope & Requirements

As a part of creating a receipt for a Data Subject (DS) there are often legal
requirements based on the operational content(OC). OC requires that a checklist
accompany the receipt. This functions as a flag: YES or NO.

i.e.
If YES, there is a self-assertion that the receipt and company side
consent management practices follow the legal requirements for fair and
reasonable consent harvesting.

Operational Context - Defined by either jurisdictionally specific requirements or use case specific requirements. The OC also is a space/scope for company-side assertions (e.g. customer service, quality, etc.

informing PII principals about the consequences, if any, of withholding their consent in whole or in part; and

informing on the ways to withdraw consent

- whether replies to the questions are obligatory or voluntary, as well as the possible consequences of failure to reply,
- the existence of the right of access to and the right to rectify the data  concerning him
�
NOTE: Burying the privacy related notice obscurely in the other matters and having user accept it is a common privacy attack.

## Audit Notes
 is Consent is action based
 is it an independent permission (i.e. only one policy  with same scopes of purpose)

 ## Meaningful Policy Changes Requiring a New Consent Receipt
 - Change in overview of the service
 - change the PII Controller
 - change PII items being collected
 - change the purpose of use to something outside the scope
 - change 3rd party- unless DS consented to scope of 3rd parties and this is within scope
 - consent required if extend retention period or extend disposal date
 - change matters related to disclosure, suspension of use, correction, deletion, suspension of provision or revoking of consent
 - change the contact information for inquiry
