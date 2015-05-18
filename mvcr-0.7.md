# MVCR-Specification-Restructure
## Minimum Viable Consent Receipt - Core Consent Receipt Profile Specification

[This paragraph to be removed prior to final publication] The 0.7 version of the MVCR specification focuses on the requirements for the MVCR specification. Future versions of this specification will add additional sections to facilitate the technical implementation of an MVCR. To keep this document focuses on the requirements alone, this version of the specification has removed material from earlier releases that will be added back in as needed and indicated by the roadmap of the MVCR in the Kantara Initiative's CISWG.

# Executive Summary

The Consent & Information Sharing Working Group (CISWG) is distilling a common set of consent requirements for information sharing that are salient across jurisdictions and compliant with Fair Information Practice privacy instruments and standards (see References). These common requirements constitute the minimum viable consent receipt, specifying the minimum required policy links, consent fields and data formats to meet the minimum legal, transparency and trust obligations for information sharing.

The core Consent Receipt (CR) specification refers to the legal notices required for compliant consent to be valid when collecting personal information. This is currently managed by organizations separately with bespoke policies that are closed to systematic use by an individual. The CR addresses this problem.

## Intellectual Property Rights
This document is being developed by Kantara Initiative's Consent and Information Sharing Working Group; see <https://kantarainitiative.org/groups/ciswg/>. Participation is free and open, and all work contributed to the effort falls into the Reciprocal Royalty Free with Opt-Out to Reasonable And Non discriminatory (RAND) IPR policy <https://kantarainitiative.org/confluence/x/mQByAg>.

Kantara Initiative is a non-profit membership organization that connects businesses, consumers, governments, and citizens through innovations and programs that support more natively trust worthy on-line experiences. The mission of KI is to foster identity community harmonization, interoperability, innovation, and broad adoption through the development criteria for operational trust frameworks and deployment/usage best practices for privacy-respecting, secure access to trusted online services.

# Problem Statement
There is no common consent record format.

Information sharing is a complex issue for organizations that require consent for the collection of personal information. Legal obligations require privacy policies that reflect how personal information may be collected, used, disclosed, retained and disposed of or deleted.

Each organization has their own best practices, policy structures and policy formats. This results in a lack of transparency that violates the best practice of open privacy principles [citation needed], is very costly to manage for all stakeholders, and very difficult to regulate effectively. The issues are compounded by each organization posting their policies in different locations, while frequently changing not only the content but also the URI of the policies.

The result is the current static and binary notice and consent infrastructure that, while regulated, is neither usable nor suitable for its intended purposes. An individual is asked to perform beyond what is reasonable in the current context.  Each individual is expected to understand what information is being collected about them, how it will be used and for what purposes, with which types of entities their information will be shared and to understand and manage the consequences long past the first point of consent. All of this is without a record or the ability to manage consent independently out of context. Meanwhile, in context, people are expected to read all policies, keep track of all active consents, so as to be informed when making new consent agreements.

# The Solution
Increase the capacity for people to manage and understand consent.

Information sharing is dramatically increasing, as a result, the capacity for people to manage information sharing also needs to increase. A specification for a  core viable consent (or authorisation) will address specific jurisdictional requirements and provide a useful framework for developing compliance with ISO 29100 and other trust standards and frameworks.

The ability for individuals to manage privacy is improved if they are able to aggregate and manage consent after it is provisioned.  A digital consent record, which in this specification is called a consent receipt, enables people to manage information sharing relationships. Organizations can use these receipts to reduce friction and streamline the consent experience.

The core receipt specification addresses general, or regulatory, consent requirements. Consent receipts additionally become more useful as a channel for trust services, trust networks, identity federations, trust marks, privacy icons, standards, assurances, certifications and self asserted community and industry reputations.

# Scope
The Minimum Viable Consent Receipt (MVCR) specification will provide the generic consent record profile for  consent requirements and is intended to be used as a legal and open notice with Kantara CISWG use cases.

This v0.7 of the MVCR further defines the requirements for a Minimum Viable Consent Receipt (MVCR). In this version, the scope is limited to covering when a user takes an explicit action to consent to sharing information, noting that personal data will be collected in a consent transaction. This consent can occur before, during or immediately after their personal information is collected.

The receipt format is required to be both human and machine readable.

# Stakeholders

There are three general stakeholder audiences for the MVCR which are referenced through this specification:

1. People:
People receive the consent receipt and may use this to independently track consent and manage terms of sharing personal information.

2. Organizations:
Organizations provide consent receipts when they obtain or assume consent to collect personal information.

3. Regulators (privacy and data protection enforcement):
Regulators include, but are not limited to, the FTC in the USA, the Canadian Federal and Provincial Privacy Commissioners, and the EU Data Protection Regulators. Regulators provide public processes for administration and enforcement of regulation in regards to notice and consent requirements

In summary, this MVCR receipt specification addresses the requirements of these three stakeholder groups with the aim to provide a self-regulatory market trust tool that organizations will implement, people can use, and regulators can enforce.


## Generic Requirements
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
  f) Purpose(s)
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

### Consent Notice Fields and Descriptions (TBF v.07)
The fields consists of:

- In MVCR v0.7 WB while this document is in draft - https://docs.google.com/spreadsheets/d/1YcBz7tgnD8AOMYQ-NywfDSODyg2ArRu2FlYrkM3Ifuc/edit?usp=sharing


### Consent Notice Fields and Descriptions (TBF v.07)

- In MVCR v0.7 WB while this document is in draft - https://docs.google.com/spreadsheets/d/1YcBz7tgnD8AOMYQ-NywfDSODyg2ArRu2FlYrkM3Ifuc/edit?usp=sharing


# References and Further Reading
The MVCR is written with terms and reference in context of:
* ISO/IEC 29100	Information technology – Security techniques – Privacy framework
* ISO/IEC 29115	Information technology – Security techniques – Entity Authentication Assurance

Supporting reference to ISTPA: Analysis of privacy principles:
* ISTPA, (2007) Analysis of Privacy Principals, pg. 64, [Online] http://www.istpa.org/ [Accessed Nov, 4 2010]
* Minister of Economy Office, Japan (2014) Guideline for the online notice and consent from consumers, http://www.meti.go.jp/press/2014/10/20141017002/20141017002a.pdf.  [Includes examples of a consent receipt in guidelines proposed in the context of ISO 29100]

Note: as an international framework the MVCR aims to include all the requirements for Sensitive Personal Information, this because, people change jurisdictions, and people provide fake jurisdiction. In this regard the consent record framework aims to harmonise these requirements so they are consistent across jurisdictions.  This is a guiding principle for the appendix and in particular Sensitive Personal Information classifications. (Note: this will need to be more specific for v0.8)

# Appendix A: Data Controller Contact Types (TDF v0.8)

Address, phone number and email, twitter, live online support,
- This should include proportional contact capabilities that are proportionate to the contexts

# Appendix B: Track Identifiers and Attributes for People

UID, IP Address, Email Address, Browser Finger Print,

# Appendix C: Purpose Specification (TBD V0.8)

Purpose specification approach is to create a list here that will act as a catalogue of purpose short notices. In the processes described we will require an option for use cases and data controllers  to be able to add additional purposes.

The purpose here may need to add Operational Context for type of devices (See NTIA Best Practices for Short Notices for Mobile etc. )

# Appendix D: 3rd Party Sharing

# Appendix E: Sensitive Personal Information

# Appendix  F:  Operational Contexts

As a part of creating a receipt for a Person, Data Subject (DS) there are often legal requirements based on the operational content(OC).

 The Operational Contexts obligations are listed when the Use Case for implementation is created, these are found in legal requirements, best practices, and are a bucket for context specific identifiers which enable operation policy.

This functions as a flag: YES or NO in the MVCR

Each use case or implementation requires an OC check list.

i.e. If YES, the Yes is defined by a self-assertion that the receipt and company side consent management practices follow the legal requirements for fair and reasonable consent harvesting.

Operational Context - Defined by either jurisdictionally specific requirements and or use case specific requirements.

## Examples of Operation Contexts

#Informing PI principals about the consequences, if any, of withholding their consent in whole or in part; and
informing on the ways to withdraw consent

# whether replies to the questions are obligatory or voluntary, as well as the possible consequences of failure to reply,
# the existence of the right of access to and the right to rectify the data  concerning him

## Audit Notes
NOTE: Burying the privacy related notice obscurely in the other matters and having user accept it is a common privacy attack.

Consent is action based is it an independent permission (i.e. only one policy  with same scopes of purpose)

 ## Meaningful Policy Changes Requiring a New Consent Receipt
 - Change in overview of the service
 - change the PII Controller
 - change PII items being collected
 - change the purpose of use to something outside the scope
 - change 3rd party- unless DS consented to scope of 3rd parties and this is within scope
 - consent required if extend retention period or extend disposal date
 - change matters related to disclosure, suspension of use, correction, deletion, suspension of provision or revoking of consent
 - change the contact information for inquiry
