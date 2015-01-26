# MVCRT-Spec-proposed restructure
## Minimum Viable Consent Receipt  Specification
<<<<<<< HEAD
Draft version 0.6

Status: T

Draft version 0.6 specification for MVCR

This is the first draft version of the Minimum Viable Consent Reciept  (MVCR), collaboratively developed, using Git Hub Version Tracking

# Scope

* The objective is to develop a core consent format for recording of a consent transaction.  

* As a result this specification is purposely crafted for the development of the Minimum Viable Consent Receipt (MVCR).  

* The aim of the MVCR is to be usable as an independent copy of a consent transaction record. The format is to clearly illustrate the core regulated consent notice requirements.

* This MVCR version of the consent receipt is for explicit consent.

* The term ‘Minimum Viable’ in this context refers to the minimum capture of consent transaction elements to provide a default level of legal compliance.  For any other purpose it needs to be extended.  Via use case and then extension. review process.

* The MVCR is the compliant by default version. Any additional functionality for consent receipt, other than the default version and web demonstrator use case, will need an extension. Description of compliant by default is below. (note: should this be added here? )

* The MVCR contains links to policy and contact information which is required to be accessible with one click to enables a range of responsive to context options .


=======
Based on draft version 0.6

# Abstract
Organizations that collect personally identifiable information
about individuals have legal obligations, regardless of
jurisdiction or method of collectio.  These obligations are reflected in privacy policies, consent policies  notice to  individuals of the purpose for
collecting personal information.(Ref needed ISTPA)  Informed consent requires notice, without sufficent notice of purpose informed consent is better referred to asset for obvious pupose. Legally, organisations obtain
 consent from individuals with respect to how their personal information may be collected, used, disclosed, retained, or destroyed by the data collector.

This specification defines the technical requirements for a Minimum Viable Consent Receipt  (MVCR).  For Organisations this format is intended to demonstate an open framework to streamline consent and compliance issues across jurisdictions.

Its minimum function is to provide individuals with a private and usable audit trail regarding any consent given or received in the course of collecting and consenting to the use of personally identifiable information.

# Introduction

An MVCR, is a compliance by default design. Once created, it is a record of the intent and permission to process personal information.  After an MVCR serves as a record that can be used by the individual to manage consent.

The MVCR provides the individual with an opportunity to manage consent and if needed, withdraw consent, challenge collection and manage consent over the use of personal information.

Similarly, the MVCR enables the data controller to send a clear signal of trust and compliance with scalable consent transparency.  The consent receipt provides process transparency, enabling trust and protection for all parties in  consent transaction against misunderstanding.

This MVCR specification proposes a minimum visual (i.e., human readable) format that can be aggregated, audited, used for experiential purpose or for reporting on data protection and privacy compliance.


## Required Fields

A Minimum Viable Consent Receipt (MVCR) is comprised of several pre-defined
data fields that are used to capture legally required consent elements of a
consent transaction.

(Note: The determination of legally required is from the Consent Legal Framework - a core extension - which references all of the consent legal requirements by jurisdiction. Reference link needed)

All consent receipts require that a DC do the following:

* Identify themselves clearly.

* Provide a static link to their privacy policy.

* Identify the intended purpose(s) for any personal information that is
collected.

* Indicate whether or not PII will be shared with third parties.

* Indicate whether or not SPII is being collected

* Provide an optional contextual requirements checklist with a Y/blank/N Flag. with the minimum statement: I agree that this info is true and that I will follow the laws of my jurisdiction.

Note: An additional log of consent related information will also be captured.
- Time & Date, do not track flags, related policies, identifier used to consent with and any other links to policies included in the consent, TOS/Cookies etc.  

## Extensions

Extensions in the MVCR are primarily discussed in the context of compliance and the use of a receipt as a consent management token.  

The MVCR format is designed to be highly extensible.  As a result this specifications requires a format for creating extensions. Any use beyond the default settings will require an extension.

There are 3 categories of core extensions that will extend both the usability and compliance of the MVCR format.

Core extensions:
* Consent  Legal Framework (providing Multi-Jurisdiction Checklist Requirements and consent exemptions)
* 3rd Party PII Sharing Extension
* Sensitive Data Sharing Extension
* Context Checklist (ML - discussion: should this be in MVCR or a core extension? I think for MVCR to be self asserted then it needs to be in MVCR by default)

Function Related Extensions:
* Consent Receipt Metrics & Auditing
* third party validation (including regulator)

 3rd Party Trust & Consent Extensions: (note: needs assessment criteria)
* Privacy Icons
* Trust Networks & Identity Federation
* Terms Of Service Extension
* Cookie Extension
* PIMS & User Submitted `terms`
* PII Log address


DC’s that share personally identifiable information and/or collect sensitive
personal information can go beyond an MVCR and develop a custom extension,
register their consent receipt format with a  3rd Party Trust Service. Trusted Service providers include (but not limited to) privacy icons, trust seals and certificates, trust enhancing protocols, reputation service providers, trusted networks, federated networks, standards and the like.  All of which offer assurance and can be used on audit frameworks.  Audited and enforced frameworks/services represent third party trust services that enable compliance with more stringent and complex obligations.  Covering complex and dynamic compliance requirements for sensitive information and/or 3rd party disclosure.

(Discussion Note:) Do we need to create a separate document and process? How to create an extension.

## MVCR Fields
The fields consists of:

 * Contact information of Data Controller

 * Identity provided by the individual.

 * Link to privacy policy
 (note: static link format required - raised by John W) (Comment: Note: For the consent receipt to be audit-able and verifiable the consent policy should be accessible by any entity with the URI for the policy. Subsequent changes to the policy should not invalidate the URI for the policy in effect with the CR was issued.)
 (Discussion Point : Rationale: If invalidated (URI Is broken), is the consent still compliant?  If the policies (materially) change is a process needed to update broken links and the consent before receipt can be used as a token?)

 * The purpose(s) listed: itemised on receipt

 * YES or NO Flags

   * 3rd party data sharing

   * Sensitive Personal Data Collection

   * Context Scope and Requirements

 * Extensions

## Flags Defined

### 3rd  Party sharing (TBD)

### Sensitive Personal Data (TBD)

### Operational Context (OC): Consent Context Scope & Requirements

As a part of creating a receipt for a Data Subject (DS), Depending on context their are often legal requirements.  OC requires that a
checklist accompany the receipt. This functions as a flag: YES or NO.

If YES, then there is a self-assertion that the receipt and company side consent management practices  follow the legal requirements for fair and resonable consent harvesting.

Consent Context Flag in the MVCR is optional.

Non-Checked provides a default status of partially compliant and signals ability  to respond if required. (Note see compliance scale)

We have started to collected a default subset of option (Variables) to be legally Fair and reasonable.

[HF: The mention of a checklist that functions as a single-value flag doesn't
make sense.  Should this be something other than a checklist? For example,
perhaps a set of variables that have separate fields for context and action.  
Example: OC_context=UK;notice_provided=yes/no] I think this needs to be a checklist clicked and agreed upon by the provisioning org.

[ML: HMMM,, good food for thought.  I think we are thinking very similar things, except a default checklist is conceptually placed on the back of the receipt and used to help educate. But maybe variables is the a tasks for this spec or an extension.]  [Need to discuss: Does the MVCR require  a variable set? if so where an when?]

Operational Context - Defined by either jurisdictionally specific requirements or use case specific requirements. The OC also is a space/scope for  company side assertions. e.g. customer service, quality etc ]

### Fair & Reasonable Consent Conditions
Elements for Operational Consent, I think these should go into the Consent Legal Framework Requirements. 

| Context: Location Specific | Description | UK | EU | USA | Canada |
| ---- | ---- | ---- | ---- | ---- | ---- |
| Website Consent Form | Provides notice at point of consent for the consequences of not provisioning consent | X | X |  |  |
| Website consent form | Indicates what is required, and optional information, to provide for consent | X | X |  |  |
| Mobile application |  |  |  |  |  |
| Entering Physical Space | Sign posted upon entry to physical space |  |  |  |  |  |

(Note: Not sure this section is titled properly - Doese this need definitions of Fair and Reasonable across jurisidctions? )

## MVCR - Compliant by Default

The objective of the MVCR specification is to make a MVCR which by default settings is compliant by default.  
 Defined specifically with the defualt settings in the MVCR which are represented by the Yes/No  flag settings -  (No) 3rd party sharing, (No) collection of sensitive personal data, and an optional,checklist for self asserting that the consent harvested is, fair, reasonable and conforms to the law where it is issued.

Compliant by default represents the express (or highly automated) version of consent, and is used to match the current 'click ware' consent system that is common today. It is this version that  is based on compliance requirements.  Compliance requirements are based ultimately on a number of sources, legal regulation,  3rd party contracts, previous legal judgment, case and statute law and best practices.  These all become relevant beyond the minimum viable CR default self assertions.

That being said, the consent receipt is also being designd to be a consent token.  So that it can be used with third parties to manage consent independently of the service provider.  

(Discussion Note: Compliance by default approach is designed for an audience that wants an open  commercial channel for 3rd party consent and trust services.)

Nevertheless,  Just the provision of a consent receipt is signal of partial compliance and ability to assist in consent management if needed.

[Ref - UK DP scale  of compliance reference and proposed consent receipt scale of compliance ]

* Every extension will provide additional checklist requirements and variables.

{Discussion: does this require CIS-Wg to propose a common methd for registering variables to the consent receipt specification}.

Note: In each jurisdiction their are exceptions to consent which are not covered in the MVCR.  The rationale is that the MVCR defaults provide a very low risk of being non compliant, and in the case that there is an exemption to compliance, the organisation is still able to evolve their practice to be compliant.

Approach: The MVCR requires some implementation and testing for a jurisdictional exemption alanlysis to be 100% sure of this assertion. A good use case for this would be Do Not Track Requirement.

### Field Formats

 (ML Discuss -: Do we need a table of the fields, with accepted formats?)

### Consent Notice Data Structure
[HF: This section needs someone with experience in designing JSON-based
specifications to adjust this details of the MVCR fields to a more
programmatically viable list of fields and allowable values (e.g.,
multivalued strings, etc.)]

[ML: Agree we need a data structure for MVCR, the XDI structure should be removed to Respect Network Use Case]

(note: removed XDI and added it to the Use Case v.01 - XDI use case) 

## Terminology

| Term | Definition | Example |
| ---- | ---- | ---- |
| Consent Receipt  (CR) | A record of a single consent transaction provided to (or obtained by) the data subject as a receipt at the point of consent.  | This record is a summary of legal requirements of  the notice and a capture of consent related data provided at the point of consent. |
| Data Controller (DC) | The organization or individual that is accountable for the operation of the web site. | This is contact information for the management of consent. |
| Data Subject (DS) | The natural person that is registering on the web site. | This is typically when a person registers to get access to a web site service. |
| Identity Provider (IdP) | A third party that provides identity and/or authentication information about the data subject. | |
| Minimum | A Receipt will contain the purposes to which is consented to | The links to all policies that inform the consent and the contact information of the data controller. |
| Operational Context of Consent | The list of legal (best practice) requirements for notice for consent in the jurisdiction and context in which the consent is given. | This includes jurisidction requirements as well as the contextual elements to the method of consent capture |
| Personally Identifiable Information (PII) | Any information that (a) can be used to identify the Data Subject to whom such information relates, or (b) is or might be directly or indirectly linked to a Data Subject. | |
| Sensitive Personally Identifiable Information (SPII) | this a flag in the consent receipt that is used for what is legally defined as sensitive and protected data, this varies from jurisdiction to jurisdiction. For this type of data explicit consent is required and a consent receipt extension is needed for this functionality. | include health, financial, children’s data,  sexual data, political/religious data, surveillance data,  (note I think this should include participate in identifying SPII |
  | Trusted Services | A provider of Trust Product, like a Privacy icons,a certification for standard assurance, a reputation services, a trusted networks, trusted protocols, etc |  |
  | Viable | Meets or exceeds regulatory minimum for notice in the jurisdiction where it is issued |  |
  | Open Notice Framework | An Open Notice is a standard consent format for policy notice summaries as required by law.  The use of an Open Notice is further facilitated by a framework which enables the independent use of the Open Notice.

# Appendix A: Usability Metrics
(place holder for a sub document)
- information verified
- level of transparency
- reputation
- Audited/Rated trust service
- type of org  From charity specific to commercial  internet service provider.
- audited by a 3rd party,
- is it enforced? how well? ,
- Reputation: how long in biz? etc ,
- context/scope, mesuring of transparency, usability of format, etc )
- 3rd parties assessment against all of the above.

UMA Context Categories and Metrics (ref UMA consent paper)
Existing Consent Categories
ToS opt-in
Cookie opt- in/out
OAuth
“Share”
Consent directive

Metrics
* Choice
* Relevance
* Granularity
* Scalability
* Automation
* Reciprocity
