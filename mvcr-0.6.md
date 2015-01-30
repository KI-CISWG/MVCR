# MVCR-Spec-proposed restructure
## Minimum Viable Consent Receipt Specification
Based on draft version 0.6

# Abstract

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
personal information.  After an MVCR is received [HF: by whom/what?], it serves
as a record that can be used by the individual to further manage consent 
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

## Scope
The term ‘Minimum Viable’ in this context, the most basic  and common 
requirements to record a consent found in regulation across jurisdictions.  
The MVCR will enable simple two-party personal data transactions to be 
recorded by both sides. The basic goal of this specification is to create a 
core MVCR format for the record of consent transactions. The format must be
a highly usable structure, with the minimum design goal to allow for the 
basic use of an MVCR on websites with users providing explicit consent to
the use of their data.

This receipt specification proposes both a minimum visual (i.e., human 
readable) format and an equivalent machine readable record that can be 
aggregated, audited, or used for reporting on data protection and privacy 
compliance. 

Extensions and developments of the consent receipt infrastructure, although 
out of scope for a MVCR, will allow auditing, third party (including 
regulator) validation, and confirmation of consent notices for compliance.

While a full description of possible extensions and developments of the 
consent receipt infrastructure are out of scope for the MVCR specification,
possible examples will be listed in order to make clear how the MVCR can 
and will be extended to allow auditing, third party (including regulator) 
validation, and confirmation of consent notices for compliance.

The objective of the consent receipt is to capture the minimum viable 
consent transaction specific information. This includes:

 * Contact information of Data Controller and digital identity provided by 
the consenter.

 * Links to policies explaining use of personal and sensitive personal data

 * A collection of the purpose(s) (like a collection of items being purchased)

 * YES or NO Flags (compliant by default design)

   * 3rd party data sharing

   * Collecting Sensitive Personal Information

   * Context Requirements Checklist

## Terminology
 
| Term | Definition | Example |
| ---- | ---- | ---- |
| Consent Receipt (CR) | A record of a single consent transaction provided to the data subject at the point of consent.  | This record is a summary of legal requirements of  the notice provided at the point of consent about the collection, use and disclosure of information by a data controller, and has given consent for that collection, use and disclosure. |
| Data Controller (DC) | The organization or individual that is accountable for the operation of the web site. | This is contact information for the management of consent. |
| Data Subject (DS) | The natural person that is registering on the web site. | This is typically when a person registers to get access to a web site service. |
| Identity Provider (IdP) | A third party that provides identity and/or authentication information about the data subject. | |
| Minimum | A Receipt will contain the purposes to which is consented to | The links to all policies that inform the consent and the contact information of the data controller. |
| Operational Context of Consent | The list of legal (best practice) requirements for notice for consent in the jurisdiction and context in which the consent is given. | This includes jurisidction requirements as well as the contextual elements to the method of consent capture |
| Personally Identifiable Information (PII) | Any information that (a) can be used to identify the Data Subject to whom such information relates, or (b) is or might be directly or indirectly linked to a Data Subject. | | 
| Sensitive Personally Identifiable Information (SPII) | this a flag in the consent receipt that is used for what is legally defined as sensitive and protected data, this varies from jurisdiction to jurisdiction. For this type of data explicit consent is required and a consent receipt extension is needed for this functionality. | include health, financial, children’s data,  sexual data, political/religious data, surveillance data,  (note I think this should include participate in identifying SPII | 
| Trusted Services | A provider of Trust Product, like a Privacy icons,a certification for standard assurance, a reputation services, a trusted networks, trusted protocols, etc |  |
| Viable | Meets or exceeds regulatory minimum for notice in the jurisdiction where it is issued |  |
 | Open Notice Framework | An Open Notice is a standard consent format for policy notice summaries as required by law.  The use of an Open Notice is further facilitated by a framework which enables the independent use of the Open Notice.   |  |
 
 
## Minimum Viable Consent Requirements

A Minimum Viable Consent Receipt (MVCR) is comprised of several pre-defined 
data fields that are used to capture legally required consent elements of a 
consent transaction. Recording the links [HF: what kind of links?] to a consent 
policy, purpose specification, name, address and contact information of the 
Data Controller (DC).

Note: For the consent receipt to be auditable and verifiable the consent 
policy should be accessible by any entity with the URI for the policy. 
Subsequent changes to the policy should not invalidate the URI for the 
policy in effect with the CR was issued. 

An MVCR enables organizations to transparently demonstrate self-asserted 
compliance with legislation and their own policies while also providing a 
record of the consent to the website/service user that is usable by the 
individual post consent.  

DCs that provide a MVCR will be able to demonstrate their intent to follow 
the best practices embodied in data protection and privacy regulation across 
many jurisdictions. This document provides some more detailed insight into
potential compliance points with EU, US, Canadian, and UK jurisdictions.

All consent receipts require that a DC do the following: 

* Provide a static link to their privacy policy.

* Identify themselves clearly.

* Identify the intended purpose(s) for any personal information that is 
collected.

* Indicate whether or not PII will be shared with third parties. 

* Indicate whether or not SPII is being gathered so that this [HF: what is 
"this"?] can be used by trust networks for service discovery.

DC’s that share personally identifiable information and/or collect sensitive 
personal information can go beyond an MVCR and develop a custom extension, 
use an existing standard, or register their consent receipt format with 
Trusted Service providers. Trusted Service providers can offer assurances and 
audit frameworks that enable compliance with more stringent and complex 
obligations for sensitive information and/or 3rd party disclosure. 

### Consent Notice Data
[HF: This section needs someone with experience in designing JSON-based 
specifications to adjust this details of the MVCR fields to a more 
programmatically viable list of fields and allowable values (e.g., 
multivalued strings, etc.)]

| Field | Description | Example (XDI) |
| ---- | ---- | ---- |
| Data Subject | Name or pseudonym of the Data Subject | Data Subject: Alice [=]!:uuid:1111 |
| Sensitive Personal Data Flag (Y/N) | Flag to categorise the information collected as sensitive or not.  Each jurisdiction has classifications of sensitive personal information (privacy): The generally include health, financial, child protection (>14), youth protection(>19 or >22), educational, religious, or political categorisations.  May trigger additional legal notice and consent requirements | [#receipt]!:uuid:1234<#sensitive>&/&/true |
| Data Controller | Name of the entity issuing the consent receipt. This is the entity accountable by law for the information collected. | Data Controller: Amazon [+]!:uuid:9999 | 
| Purpose | The purpose(s) for which the information is being collected. | [#receipt]!:uuid:1234[<#purpose>]<@0>&/&/"We need to process your payment."  [#receipt]!:uuid:1234[<#purpose>]<@1>&/&/"We  need your data to prevent fraud."  [#receipt]!:uuid:1234[<#purpose>]<@2>&/&/"We will advertise to you."
| Privacy Policy | The issuing entity's privacy policy (either inline copy, or reference to URI) | [#receipt]!:uuid:1234<#privacy><#policy>&/&/"copy of privacy policy here" or [#receipt]!:uuid:1234<#privacy><#policy><$uri>&/&/"https://..." |
| Location of Consent | The location of the consent provision. from which the consent receipt originates.(i.e. The web page with the consent button.) | [#receipt]!:uuid:1234<#location><$uri>&/&/"....." |
| Third Party Sharing| Flag whether data is shared with third parties. (Y/N)  May trigger special notice or consent requirements | [#receipt]!:uuid:1234<#third><parties>&/&/true |
| Site Specific Fields | Additional field or fields as necessary to fulfill the notice and other requirements that the Data Controller may need | --  |

 
### Extension Types (added as site specific fields)
[HF: This section needs someone with experience in designing JSON-based 
specifications to adjust this details of the MVCR fields to a more 
programmatically viable list of fields and allowable values (e.g., 
multivalued strings, etc.)]
[HF: There is a lot of detail here for something that is stated as out-of-scope.]

| Core Extension | Extend the MVCR | 
| ---- | ---- |
| Operation Context | Core extension Note: For the MVCR draft there is only the online website format context, additional context can be added by extension |
| 3rd Party Extension | Extension that Lists Third Parties | 
| PII List Extensions | Summarizes or lists the PII Collected and used by the DC | 
| Trusted Services | Trust Framework Extensions | 
| Usability | Extensions that increase usability and adoption of the consent receipt | 
 
### Jurisdictional Extensions

In each jurisdiction, there are sensitive types of personal information found 
in privacy and data protection law.  Each sensitive type has prescribed 
contextual requirements that needs to be included in a notice.  Jurisdictional
extensions can be added to the MVCR to meet complex notice requirements and 
the requirements of multiple regulatory jurisdictions.

Jurisdictional extensions may be used by data controllers to localise the use 
of consent notices for greater usability, to specific operational contexts, and 
for more granular applications of enforcement.

### Operational Context (OC)

As a part of creating a receipt for a Data Subject (DS), the OC requires that a 
checklist accompany the receipt. This functions as a flag: YES or NO. If 
YES, then there is a self-assertion that the notice will be provided in a 
fair manner with all of the required considerations as prescribed in law in 
that jurisdiction.  This is then reflected on the consent receipt.

[HF: The mention of a checklist that functions as a single-value flag doesn't
make sense.  Should this be something other than a checklist? For example, 
perhaps a set of variables that have separate fields for context and action.  
Example: OC_context=UK;notice_provided=yes/no]

  Instructions: This is a self-asserted option. The Operational Context is a 
  YES or NO flag that the receipt provisioner turns on or off.  Operational 
  Context is dependent on the location of consent, the use of personal data, 
  the origin of the data, and type of data provided. Operational requirements
  can vary significantly as the context of the MVCR changes with different
  jurisdictions.

### Fair & Reasonable Consent Conditions
Here is a beginning to a list of elements for Operational Consent
 
| Context: Location Specific | Description | UK | EU | USA | Canada |
| ---- | ---- | ---- | ---- | ---- | ---- |
| Website Consent Form | Provides notice at point of consent for the consequences of not provisioning consent | X | X |  |  | 
| Website consent form | Indicates what is required, and optional information, to provide for consent | X | X |  |  | 
| Mobile application |  |  |  |  |  | 
| Entering Physical Space | Sign posted upon entry to physical space |  |  |  |  |  | 
 
### Trusted Services

Third-party trusted services can also be used to extend the compliance or 
trust inherent to corporate process and these can be added in the form of 
linked icons in a MVCR. (Note should this refer to a trusted services index)

# Appendix A = Site Registration Use Case

## Description

This draft of the specification is based on the following scenario: 

[HF: It is not clear what this use case is describing.  Is it describing the
creation of an MVCR, the creation and use of an MVCR, or just the use of 
an MVCR?]

* Alice registers with a website, bob.com, to donate to listen to bob.com’s 
podcast using either a third-party identity provider or a local account at
bob.com.  

* Upon registration, bob.com displays all the appropriate privacy policies in 
a prominent location on the website.

There are two scenarios for this use case:

  * prior notice was given for consent and needs a receipt 

  * current notice is given and requires a receipt

* The bob.com website cites the notice and consent requirements of the 
regulatory regime in which the web site operates. For the the purposes of 
this this specification, it is assumed that either prior consent receipt has 
been provided, that this is the first time a consent receipt is provided, or 
that this is a request for a consent receipt to be provided or confirmed.

* Consent receipt for bob.com website is code that is created via from and is 
put behind the consent receipt button. 

  * This is previously made by filling out a form.

* A consent receipt is provided at point of consent with a modified consent 
button.

  * To be added:

    * walk through of the creation and provision of a consent receipt that 
conforms to the data specification below.

   * The creation of web site will either provide, or offer to provide, the 
user with a copy of the consent receipt to complete the registration process. 

   * The use case ends when the user accepts the consent receipt, or declines 
the offer.
 
[HF: What is this table describing?]

| Description Detail | Notes |
| ---- | ---- |
| Related Requirements | The provision of a consent receipt enables data providers to demonstrate their compliance with regulatory requirements for notice and consent. |
| Preconditions | Before a consent receipt can be issued the following conditions must be true: *  The user has provided the necessary information about themselves to complete registration ** This should include sufficient notice to meet regulatory requirements for the jurisdiction in which the site operates * The organization has a privacy policy and/or terms of use and/or equivalent documentation to complete the mandatory fields in the consent receipt. * The consent receipt that will be issued is authorized by an appropriate authority in the organization (i.e. this consent receipt is a business record of a transaction). |
| Successful End Conditions | • A consent receipt that contains the fields described below has been generated and offered to the data subject. • A copy of the consent receipt is stored by the Data Controller. • A record of the creation of the consent receipt has been created and logged. • The data subject has received a copy of the consent receipt or has indicated that they do not want a copy of the consent receipt. o The data subject’s decision about accepting or not accepting the consent receipt will be logged. |
| Failed End Conditions | The data subject completes site registration with receiving being offered a consent receipt. | 
| Primary Actors | Data Subject, Data Controller|
| Secondary Actors | Identity Provider; Open Notice Registry: A third party that provides validated information about the Data Controller’s compliance. | 
| Trigger | Data Subject provision of site registration information. | 
| Main Flow| 1. Data Controller display or provides notice to the data subject 2. Data subject provides registration information, including personally identifiable information where required. 3. Data Controller validates input 4. Data Controller generates and displays consent receipt 5. Data subject decision receives a copy of the consent receipt 6. Data Controller stores a copy of the consent receipt 7. Data Controller logs transaction | 
| Extension | 2a: Data subject identity information is provided by a third party 5a: Data subject elects not to receive a copy of the consent receipt 6a: Data Controller does not store a copy of the consent receipt | 
 

     

# Appendix: Sample Consent Receipts
[missing diagram]

## Example 1. Basic Physical Receipt

A sample consent receipt modelled after a cash register receipt, produced as a pdf file for the data subject to download or print.

## Example 2. Personal Data Store
The following example is based on a technical walkthrough with the Respect Network. Respect Network (RN) Technical Demo:

* Store a Consent Receipt in your RN personal cloud using XDI: http://amazon-respect-consent.herokuapp.com/
* List Consent Receipts in your RN personal cloud: http://open-notice.github.io/respect-network-receipts/

Amazon Respect Use Case: With the Respect Network and Open Notice
(Note: Amazon Respect is a Fictitious organisation used here only as an example) 
 
(http://open-notice.github.io/consent-receipt/amazon-mock/signup.html)

Implementation of consent receipt which is signed & created by a DC and stored in a personal cloud. 

To make consent receipt use scalable, CRs needs to be signed and put in a personal data store as part of the Respect Network. 

This specification and demo is created to demonstrate a MVCR being implemented without the need for an Open Notice Registry with the Respect Network (Trusted Network) Trust Framework  which natively has the ability to provision receipts to the highest level of compliance.

This walk-through demo is intended to demonstrate how a consent receipt can be stored in a personal cloud from this spec document and demonstrate 'Fast Track' usability. 

1. DS goes to amazonrespect.com website
2. Website presents form and asks for consent:
1. either to sign up initially, or
2. for additional consent and profile management when already logged in
3. DS agrees (clicks on “i agree” button)
4. DC website initiates creating a receipt for the consent just given.
5. DC checks for reciept data collection and notice extensions and finishes creating the receipt.
6. The receipt is signed by DC.
7. DC website sends an XDI message to DC’s RN cloud to store the signed receipt.
8. DC shows popup window with options (what to do with the receipt).

The signed receipt is embedded in the popup window.

1. email to DS using email address in amazon profile
2. store in users personal cloud
3. capture in browser
4. download receipt as pdf
5. opt out of a receipt.  
9. DS clicks on “store receipt in my RN cloud”. (default option)
10. Popup window asks DS: what is your cloud name?
11. DS types cloud name =alice
12. Popup window runs XDI discovery to find DS’ RN cloud
13. Popup window sends an XDI message to DS’ RN cloud to store the signed receipt
The Re-usability of a MVCR can then be made scalable for re-use in aggregate. This is beyond the point of consent for the data subject, with a process in whch the receipt is digitally signed by both parties.
This process also identifies the jurisdiction of the Data Controller and of the Data Subject. This example includes signing of the receipt by the DC. (Note: The digital signing of the  DS (data subject) is currently out of scope of the first draft1.)
MVCR Mock Up for Amazon Respect Use Case


## Appendix: Consent Receipt Code Generator

In order to enable organizations to provide static consent receipts to their data subjects, a code generator will be provided to enable organizations to enter the basic information for their own MVCR to receive code that they can embed on their own web site.

Main Flow

 1. Organization provides content for minimum viable consent receipt
 2. System validates input
 3. System generates code for embedding
 4. Organization downloads code
 5. Organization installs code on their web site

Please see the conceptual wireframe on the next page.

## Appendix C

This is the start to the brief for the demonstrator that this specification will be used to create. 
Sample code generator page


## Change log

| Version | Status | Writer | Editor | Notes | 
| ------- | ------ | ------ | ------ | ----- |
| v.01 | Done | Mark Lizar | Mary Hodder | Summary of Intent |
| v.02 | Done | Mark Lizar, Mary Hodder | John Wunderlich | Stakeholder Analysis| 
| v.03 | Done | John Wunderlich, Mark Lizar | Mary Hodder | Summary of Compliance Contents |
| v.04 | Done | Mark Lizar, Markus Sabadello | John Wunderlich, Mary Hodder | Spec Outline & Demo (Mark), Technical Walkthrough (Markus)|
| v.05 | Done | John Wunderlich | Mary Hodder, Mark Lizar | Word updating. |
| v.06 | In process | John Wunderlich | Mary Hodder | Clean up; Added Basic Use Case Describe; MVCR Generator |
