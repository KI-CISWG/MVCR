# MVCR-v0.7
## Minimum Viable Consent Receipt - Core MVCR Receipt Profile

# Abstract

The Consent & Information Sharing Working Group (CISWG) is documenting a minimum set of requirements that will support informed consent on the part of the user. The goal is to identify the necessary information to make a transaction compliant with Fair Information Practice privacy instruments and standards (see References) regardless of legal jurisdiction. These common requirements constitute a Minimum Viable Consent Receipt (MVCR) specifying the minimum required policy links, consent fields, and data formats to meet the minimum legal, transparency, and trust obligations for information sharing.

The core Consent Receipt (CR) specification refers to the legal notices required for compliant consent to be valid when collecting personal information. This is currently managed by organizations separately with bespoke policies that are closed to systematic use. The Consent Receipt is being designed to address this problem.

# Status

The 0.7 version of this specification documents the *minimum* required and offers an alpha format for testing and implementation.  Some fields are under review for inclusion in later versions of the specification.

# Editors

Mark Lizar

Heather Flanagan


## Intellectual Property Rights

This document is being developed by Kantara Initiative's Consent and Information Sharing Working Group (see <https://kantarainitiative.org/groups/ciswg/>). Participation in this group is free and open, and all work contributed to the effort falls into the Reciprocal Royalty Free with Opt-Out to Reasonable And Non discriminatory (RAND) IPR policy <https://kantarainitiative.org/confluence/x/mQByAg>.

Kantara Initiative (KI) is a non-profit membership organization that connects businesses, consumers, governments, and citizens through innovations and programs that support more natively trust worthy on-line experiences. The mission of KI is to foster identity community harmonization, interoperability, innovation, and broad adoption through the development criteria for operational trust frameworks and deployment/usage best practices for privacy-respecting, secure access to trusted online services.

# TOC

- insert table of contents here

# Introduction

The Minimum Viable Consent Receipt (MVCR) is a simple specification that describes a few basic elements common to consent across several legal jurisdictions and across a variety of contexts.  The term 'Minimum' in the MVCR refers to the least amount of fields to make a consent receipt viable.  Viable, in this context, means to use the consent receipt independently of the issuer. The consent receipt should involve a minimal set of  notice requirements for the company or organization issuing the receipt.

The fields in this v0.7 specification are the Alpha MVCR fields that the CISWG will use to implement and test the consent receipt.

# Notational Conventions

CISWG - Consent & Information Sharing Work Group
CR - Consent Receipt
CRG - Consent Receipt Generator
DC - Data Controller
DS - Data Subject
MVCR - Minimum Viable Consent Receipt
PI - Personal Information


# Terminology (TBF v0.8)

[AQ: Is this list of terms necessary, or should this section be narrowed down to indicate that the privacy and consent terminology used are derived from ISO 29100?]

Purpose Specification - [definition needed]
Personal Information - all attributes that are collected about the individual and the consent session can be deemed personal.
Information Sharing - [definition needed]
Sensitive Personal Information Categories- refer to the legal categories defined in some jurisdictions like the EU and the US, which have additional notice and consent requirements.

Note: terminology reference for this project is ISO 29100
(NOTE: Collect terms - and term discussion items here for v0.8)

# Problem Statement(s)

The MVCR seeks to solve for a variety of problems that exist in the online marketplace today.

## Consent is a unique and closed construct per context
There is no common consent record format, making it difficult for a user to know what they have consented to when presented with different sites and interfaces.  Each organization has their own unique privacy policy, policy structures and policy formats, again making it difficult for a user to know what they are consenting to from one site or service to the next.  These things violate the Openness Privacy Principles found in FIPPs, APEC, Canadian and European Law.  

As a result, people have the burden to read, understand policies, log in to each service provider separately to select preferences and access personal data controls.  

## Cost, Regulation & Usability
Consent management is very costly to manage for all stakeholders,  difficult to regulate, and unusable for people at scale. The scale, however, continues to grow at a phenomenal rate with 90% of all data in the world has been created in the last two years.  

## Consent is Not Scalable

This is compounded by each organization posting their policies in different locations, while frequently changing not only the content but also the URI of the policies.

As described above, there is no common consent record format and consent is closed.  As the scale of information sharing relationships increases, the ability to managing consent and data control needs to scale accordingly.

# The Solution
The solution is an open consent model that provides people with a simple, standardized, easy-to-read consent receipt.  The act of providing a consent record will demonstrate the capacity for compliance and build trust with the management of personal data.

A common consent receipt format will enable people to communicate about consent after the point at which it is provided.

This transparency makes consent more usable because it provides the means for people and CRM systems to evolve greater personal data control in line with regulation and context.


# Scope
CISWG: Internal Spec revision: This next iteration of  the MVCR specification is the Alpha: Minimum core requirements for digital consent, to be viable independently.

Core use is to make a standard way to communicate about fine grained consent and contexts, using policy, between DS and DC.  

The Minimum Viable Consent Receipt (MVCR) specification as the core fields required for creating a legitimate digital consent that can be used to bind trust frameworks roles and requirements to a consent transaction.

The scope of the MVCR is limited to defining the basic and common consent fields for an explicit consent. With the transparent aim  to standardize the minimum fields to create a common base meta-format defined here and called a ‘consent receipt’ (CR).

# MVCR: Core Profile

## Design Principles (TBD v0.8)

## Functional Objective (TBD v0.8)

## 5 Sections
The MVCR is broken down into 5 sections for usability and to aid in understanding the core function. The 5 sections are:
1. Header
2. Contact & Policy
3. Purpose Specification
4. Personal Information
5. Information Sharing

### Header
The administrative data for a consent receipt

### Contact & Policy
Contact provides a channel for preference  communication and the privacy policy the basis.  Contact  includes the name, address and direct contact information.  The quality and service level of the contact information can vary dramatically.

### Purpose Specification
The purpose should be explicit, specified and legitimate.  Specifying the service name and the action for using personal information is required.  This can be used post consent for Preference management, privileges/roles assignment and access authorization policy.

### Personal Information
Split into two types: 
A) PI (the data captured at the point of consent, as well as the categories of PI that the Data Controller (consent button installer) defines when creating the consent receipt button (e.g., IP Address, DNT Header))

B) Sensitive PI (a category of PI, with check boxes that are ticked by the creator of the consent receipt button.

These categories have legal notice and consent requirements in some jurisdictions that is beyond the scope of the MVCR format, but are required in various jurisdictions and context.  

In the MVCR, if a Sensitive data category is selected then additional notice and purpose requirements exists.

For example:  A very common Sensitive category list would be:
 Health  [X]
 Child PI  [ ]
 Financial [ ]
 Sexual Life [ ]
 Add +

In this example if the data capture was doctor or health related in the US, then health should be checked above and a HIPPA compliant purpose list and PI category list can then be added or linked to this receipt.

### Information Sharing.
In the MVCR this is a Y/N flag, and if yes then the 3rd parties, the data categories and the purpose can be listed here.

(Note: TBD In v0.8 binding roles and policy)

 ## Fields in Review v0.8:
 * Review consent transaction data
 * Review consent context
 * Review - Link to short privacy notice
 * Review consent payload
 * Review Resource Server Identifier
 * Review OAuth Scopes
 * Review and what is —> Audience URI

## Field Description Table: Field, Logic, JWT Claim

table can be found at : https://kantarainitiative.org/confluence/display/infosharing/MVCR%3A+Core+Consent+Receipt+Profile+v0.7
                        |

### Consent Receipt Generator (CRG) Example

A prototype for a consent receipt generator can be found at

http://api.consentreceipt.org/

This example site consists of two pages
1. for the Consent Receipt Generator Input Example and Receipt Rendering, this is used to develop implementations and see how the consent receipt (GitHub repository) code works.

The github repository for this code is
--> https://github.com/bspk/cr_web

2. for API Documentation and examples, these can be found at
http://api.consentreceipt.org/doc/

### Consent Receipt Generator API
This server provides a consent receipt generation API. The API consists of a single endpoint:

http://www.consentreceipt.org/mvcr/api

This endpoint accepts HTTP POST requests with input in the form of JSON (application/json) documents and output in the form of a signed JSON Web Token (application/jwt).


## How It Works

The API takes in a JSON document describing the consent transaction for which the receipt is to be generated. This object includes artifacts such as the presiding jurisdiction for the consent action, an identifier for the party consenting. The output of the API is a signed JSON Web Token (JWT) whose payload consists of all of the input data as well as several additional fields. This JWT is digitally signed by the server.

## Digital Signature Information
The output JWT is signed using the RS256 algorithm defined in JSON Web Signatures. The server's public key is published in JSON Web Key format at:

http://www.consentreceipt.org/api

## Example

Example

An example input to the API is the following JSON object:

The latest documentation for example input can be found at
http://www.consentreceipt.org/api
(Note: At the moment 1-Aug-2015 It is out of sync with this v0.7 of the specification, when it is in sync it should be pated here)

# References and Further Reading
[AQ: The References section will need to be restructured to link to specific citation points in the text. Should that be done for 0.7 or at a later version of the draft?]

The MVCR is written with reference to terminology found in:
* ISO/IEC 29100	Information technology – Security techniques – Privacy framework
* ISO/IEC 29115	Information technology – Security techniques – Entity Authentication Assurance

Supporting reference to ISTPA: Analysis of privacy principles:
* ISTPA, (2007) Analysis of Privacy Principals, pg. 64, [Online] http://www.istpa.org/ [Accessed Nov, 4 2010]
* Minister of Economy Office, Japan (2014) Guideline for the online notice and consent from consumers, http://www.meti.go.jp/press/2014/10/20141017002/20141017002a.pdf.  [Includes examples of a consent receipt in guidelines proposed in the context of ISO 29100]

# Appendix A: Generic Requirements

[AQ: Given the usage pattern very similar to the RFC 2119 requirements language, do you want to reference that document instead of redefining the terms? Do you want to use requirements language outside the Appendix, in the body of the specification?]

"MUST" indicates a required component, the word “SHOULD” indicates a recommendation and does not impose an obligation. The word "CAN" means that this is a common option.

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
    * Operational Context
7. The payload SHOULD include the following properties:
  a) A description of the types of personally identifiable information to which the consent applies.
8. The payload SHOULD include the following information:
  a) the personal identifier used in the consent receipt
  b) some or all of the personally identifiable information to which the consent applies
8. The receipt MUST be systematically usable and automatically discoverable
9. Receipts MUST contain the minimum information to enable request for more information, if required
10. Receipts MUST contain the minimum information to enable requests for more information, if required

