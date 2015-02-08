# MVCRT-Spec-proposed restructure
## Minimum Viable Consent Receipt  Specification

The 0.6 version of this specification focuses on the user experience--
specifically, what they will see in a Minimum Viable Consent Receipt.  Future
versions of this specification will add material to allow for the technical
implementation of an MVCR.

# Abstract
Organizations that collect personally identifiable information about 
individuals have legal obligations, regardless of jurisdiction or method of 
collectio.  These obligations are reflected in privacy policies, consent 
policies  notice to  individuals of the purpose for collecting personal 
information.(Ref needed ISTPA)  Informed consent requires notice, without 
sufficent notice of purpose informed consent is better referred to asset for 
obvious pupose. Legally, organisations obtain consent from individuals with 
respect to how their personal information may be collected, used, disclosed, 
retained, or destroyed by the data collector.

This specification defines the technical requirements for a Minimum Viable 
Consent Receipt  (MVCR).  For Organisations this format is intended to 
demonstate an open framework to streamline consent and compliance issues 
across jurisdictions.

Its minimum function is to provide individuals with a private and usable audit 
trail regarding any consent given or received in the course of collecting and 
consenting to the use of personally identifiable information.


# Introduction

Organizations that collect personally identifiable information 
about individuals typically have legal obligations, regardless of 
jurisdiction, to provide notice to the individuals from whom they are 
collecting personal information.  Those organizations must obtain 
knowledgeable consent from those individuals with respect to how 
their personal information may be collected, used, disclosed, retained, 
or destroyed by the data collector. This specification
defines the technical requirements for a Minimum Viable Consent Receipt 
(MVCR) token that will provide organizations and individuals with a verifiable
audit trail regarding any consent given or received in the course of
collecting and using personally identifiable information.

An MVCR, once created, is a record of the intent and permission to process 
personal information.  After an MVCR is received by an individual, it serves
as a record that can be used by that individual to further manage consent 
and acknowledge the allowed use of personal data by an [HF: organization? 
application?].  For example, receiving a consent receipt immediately during
or after a web, mobile or other internet-based service transaction provides 
an individual with an opportunity to confirm, and if needed, challenge 
collection and control of personal information. 

Similarly, the MVCR enables the data controller to send a clear 
signal of trust and compliance that states they will do with 
personal information.  The consent receipt provides clarity and, through 
the resulting process transparency, adds trust and protection for all 
parties against misunderstanding.

Above all else, the MVCR is specifically designed to provide the minimum 
viable and required legal notice to a data subject. This allows services that
use the MVCR to demonstrate compliance with common/basic data privacy and 
protection regulation found within and across jurisdictions. 

The details of the specification are designed to be both human- and machine-
readable.  Both characteristics are critical to allow for both automation and
human understanding.  A human-readable consent receipt makes personal data 
control much more usable by being systematically usable and administrable on 
aggregate.  The MVCR contains links to policy and contact information which is 
accessible with one click and enables more advanced and dynamic consent in 
context.   

A MVCR provides an advanced capacity for people to manage consent, in effect 
enabling a communication channel for consent and future policy communication 
between both parties.  

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

## Contents of a Consent Receipt
The term ‘Minimum Viable’ in this context, the most basic  and common 
requirements to record a consent found in regulation across jurisdictions.  
The MVCR will enable simple two-party personal data transactions to be 
recorded by both sides. The basic goal of this specification is to create a 
core MVCR format for the record of consent transactions. The format must be
a highly usable structure, with the minimum design goal to allow for the 
basic use of an MVCR on websites with users providing explicit consent to
the use of their data.

* The objective is to develop a core consent format for the record of a consent transaction.  

* As a result this work is this specification is for the development of the Minimum Viable Consent Receipt (MVCR).

* The aim of this format is to pull out the core requirements for a consent to be legitimate, and to put it into a highly usable structure. 

* This version of the specification is being written for simple basic use on websites as the context.    

* This version of the consent receipt is for explicit consent in this context.

* The term ‘Minimum Viable’ in this context, the most basic  and common 

Note that:

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

An additional log of consent related information will also be captured.
- Time & Date, do not track flags, related policies, identifier used to consent with and any other links to policies included in the consent, TOS/Cookies etc.  


## MVCR Fields
The fields consists of:

 * Contact information of Data Controller

 * Identity provided by the individual.

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

 * Extensions

## MVCR - Compliant by Default

The objective of the MVCR specification is to make a MVCR which by default 
settings is compliant by default.  

 Defined specifically with the defualt settings in the MVCR which are 
represented by the Yes/No  flag settings -  (No) 3rd party sharing, (No) 
collection of sensitive personal data, and an optional,checklist for self 
asserting that the consent harvested is, fair, reasonable and conforms to the 
law where it is issued.

Compliant by default represents the express (or highly automated) version of 
consent, and is used to match the current 'click ware' consent system that is 
common today. It is this version that  is based on compliance requirements.  
Compliance requirements are based ultimately on a number of sources, legal 
regulation,  3rd party contracts, previous legal judgment, case and statute 
law and best practices.  These all become relevant beyond the minimum viable 
CR default self assertions.

That being said, the consent receipt is also being designd to be a consent 
token.  So that it can be used with third parties to manage consent 
independently of the service provider.  

(Discussion Note: Compliance by default approach is designed for an audience 
that wants an open commercial channel for 3rd party consent and trust services.)

Nevertheless, just the provision of a consent receipt is signal of partial 
compliance and ability to assist in consent management if needed.

[Ref - UK DP scale  of compliance reference and proposed consent receipt scale of compliance ]

* Every extension will provide additional checklist requirements and variables.

{Discussion: does this require CIS-Wg to propose a common methd for registering variables to the consent receipt specification}.

Note: In each jurisdiction their are exceptions to consent which are not 
covered in the MVCR.  The rationale is that the MVCR defaults provide a very 
low risk of being non-compliant, and in the case that there is an exemption to 
compliance, the organisation is still able to evolve their practice to be 
compliant.

Approach: The MVCR requires some implementation and testing for a 
jurisdictional exemption alanlysis to be 100% sure of this assertion. A good 
use case for this would be Do Not Track Requirement.

### Consent Notice Fields and Descriptions

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


# Appendix B: Flags Defined

### 3rd  Party sharing (TBD)

### Sensitive Personal Data (TBD)

### Operational Context (OC): Consent Context Scope & Requirements

As a part of creating a receipt for a Data Subject (DS) there are often legal 
requirements based on the operational content. OC requires that a checklist 
accompany the receipt. This functions as a flag: YES or NO.

If YES, there is a self-assertion that the receipt and company side 
consent management practices follow the legal requirements for fair and 
reasonable consent harvesting.

Consent Context Flag in the MVCR is optional.

Non-Checked provides a default status of partially compliant and signals 
ability  to respond if required. (Note see compliance scale)

We have started to collected a default subset of option (Variables) to be 
legally fair and reasonable.

[HF: The mention of a checklist that functions as a single-value flag doesn't
make sense.  Should this be something other than a checklist? For example,
perhaps a set of variables that have separate fields for context and action.  
Example: OC_context=UK;notice_provided=yes/no] I think this needs to be a checklist clicked and agreed upon by the provisioning org.

[ML: HMMM,, good food for thought.  I think we are thinking very similar things, except a default checklist is conceptually placed on the back of the receipt and used to help educate. But maybe variables is the a tasks for this spec or an extension.]  [Need to discuss: Does the MVCR require  a variable set? if so where an when?]

Operational Context - Defined by either jurisdictionally specific requirements 
or use case specific requirements. The OC also is a space/scope for company 
side assertions (e.g. customer service, quality, etc.).


