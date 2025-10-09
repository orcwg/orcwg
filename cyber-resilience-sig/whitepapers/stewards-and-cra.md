---
SIG: Cyber Resilience SIG
Task force:
Document type: White paper
Number: 3.5
Status: ✍️ Work in Progress
Input to: EU Guidance, Implementing Act, Harmonised standards
Relevant liaisons: EU Commission, CRA Expert Group, CEN/CENELEC, Market Surveillance
License: CC-BY 4.0
---

# Open Source Software Stewards and CRA Whitepaper

## Abstract

The Cyber Resilience Act (CRA) defines a new category of organizations, Open Source Stewards (Stewards hereafter). It also defines obligations for them that are different from those of other categories like manufacturers.

This whitepaper will aim at elaborating on the obligations, restrictions, and penalties that will be imposed to Stewards.

From the elaboration on the legal text, we will outline the missing pieces / documents / procedures that Stewards need to have to fulfil their obligations.

The goal is NOT to provide a definition or guidance about who is and who is not a steward for an Product with Digital Element qualifying as Open Source Software.

This document is NOT legal guidance, but the current understanding of the CRA by its contributors.

## Status of this document

This is a draft document and may be updated, replaced or obsoleted at any time. It is inappropriate to cite this document as other than a work in progress. Publication of this document as a draft does not imply endorsement by the Eclipse Foundation, Open Regulatory Working Group Members, or contributors.

## Obligations of Open Source Stewards

Open Source Stewards are defined in the CRA as a separate group of actors, different from Manufacturers. They have specific obligations related to Open Source projects they are Stewards for.

### Security Policy

Stewards shall put in place and document in a verifiable manner a cybersecurity policy. That policy has goal of:
- developing of secure products
- effective handling of vulnerabilities by developers of that product
- describe the process of voluntary reporting to CSIRT (see below)

The Steward may have the policy in paper or electronic form.

Market Surveillance Authorities may request such a Security Policy.

References: Article 24(1)

What is needed:
- A specification about how to demonstrate that the policy is put in place
- How to record it and store it such that an independent party can check that the policy exists (version-controlled documents, maintaining a change log, ...)
- It covers the required topics (scheduling regular reviews)
- It’s actually being followed (tying policy statements to evidence)
- The format of the Security Policy
- Specification on what it means for a policy to foster the development of secure PwDE: policy must list methodologies of risk assessment, secure by design, secure by default, and secure SDLC
an effective handling of vulnerabilities by the developers of that product: policy must contain description of CVD process


### Collaboration with Market Surveillance Authorities

When Market Surveillance Authorities request assistance from a Steward related to one of their projects,
the Steward shall cooperate with the goal of mitigating security risk posed by the Project they are a Steward for.

In particular, the Market Surveillance Authority may request a copy of the Security Policy.

Where a Market Surveillance Aurhority finds that a Steward does not comply with its obligations,
they require Steward to ensure that all appropriate corrective actions are taken.
As a result, Stewards must ensure that all appropriate corrective action is taken in respect of their obligations.

But: the steward cannot be subject to administrative fines for any infringement of the CRA.

References: Article 24(2), Article 64(10b)

### Mandatory reporting of exploited vulnerabilities and security incidents

Steward must notify simultaneously to the CSIRT and to ENISA, via the single reporting platform: 
- Any actively exploited vulnerability contained in the product
- Any severe incident having an impact on the security of the product that it becomes aware of

Stewards don’t have a delay for reporting actively exploited vulnerabilities or severe incidents.

Stewards also need to inform users (see below).

References: 16, 14(1), 14(3), 14(8), 24(3)

What is needed:

- How Stewards become aware of actively exploited vulnerabilities
- How Stewards become aware of severe incidents

### Informing users about exploited vulnerabilities and security incidents

In case a Steward knows about an exploted vulnerability or a security incident related to their product,
the Steward must inform the impacted users of the product,
of that vulnerability or incident and inform them of possible mitigations they (user) can deploy to mitigate
the impact. Such a security advisory should be distributed in structured, machine-readable format if possible.

References: 16, 14(1), 14(3), 14(8), 24(3)

What is needed: 
- The advisory format and content (CSAF, VEX etc)

### Voluntary vulnerability reporting

Stewards may voluntary report vulnerabilities and incidents to a CSIRT or ENISA.

References: Article 24(1)

### A policy to develop secure products

### A policy to effectively handle vulnerabilities

The policy to effectively handle vulnerabilities should be a part of the security policy and include processes of:
- documenting vulnerabilities
- addressing vulnerabilities
- remediating vulnerabilities
- promoting information sharing in the open source community
- enable reporting vulnerabilities to the project (or to the Stewards) by manufacturers including such a project in their product, according to obligations of the Manufacturer.

References: Article 24(1) and 13(6).

#### CSIRT designated as coordinator

Steward must know who is their CSIRT designated as coordinator. The CSIRT is the one from the Member State where (in order of priority):
- the Steward has their main establishment. Main establishment is where the decisions related to the cybersecurity of its products with digital elements are predominantly taken
- the Steward has the establishment with the highest number of employees in the Union

TODO: Check how this applies to Stewards who do not have a representation in the EU.

If the Steward has no main establishment in the Union, the appropriate CSIRT is the one from the Member State in which:
- the authorised representative acting on behalf of the Steward for the highest number of products of that Steward is established
- the highest number of users of products of that Steward are located

References: 24(3)

## Restrictions

Steward cannot affix the CE marking on the products they publish.

References: recital 19

### Glossary

ENISA - European Union Agency for Cybersecurity
CRA - Cyber Resilience Act
CSIRT - Computer Security Incident Response Team
CVD - Coordinated Vulnerability Disclosure
PwDE or PWD - Product with Digital Elements (as defined by the CRA)

### Contributors

TODO: List contributors of the document

### References

TODO: list useful references, previous work, talks etc including items from the Inventory and FAQ

## Acknowledgments

The following people have contributed to this document either directly or indirectly (e.g. by raising questions):

Mikaël Barbero
Æva Black
Arnout Engelen
Tobie Langel
Faidon Liambotis
Jordan Maris
Salve J. Nilsen
Juan Rico
Marta Rybczynska
Daniel Thompson-Yvetot
Martin von Willebrand

If you have contributed to this document and aren't properly acknowledged or if you want to edit or remove your name, please let us know by [opening an issue](https://github.com/orcwg/orcwg/issues/new) and we will fix this right away.
