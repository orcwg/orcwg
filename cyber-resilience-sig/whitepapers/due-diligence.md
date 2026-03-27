---
SIG: Cyber Resilience SIG
Task force:
Document type: White paper
Number: 3.2
Status: 🗺️ Planned
Input to: EU Guidance, Implementing Act, Harmonised standards
Relevant liaisons: EU Commission, CRA Expert Group, CEN/CENELEC, Market Surveillance
License: CC-BY 4.0
---

# White paper on due diligence obligation of manufacturers

## Abstract

The due diligence obligation of manufacturers outlined in [Article 13(5)][] of the CRA is the cornerstone of the relationship between manufacturers and the open source ecosystem.

This white paper will attempt to clarify this obligation along with the related requirement that integrated open source components must not compromise the cybersecurity of the products they are integrated into. It will list the constraints manufacturers might face when integrating open source components—in particular components which aren't supported by open source software stewards, and propose solutions to enable manufacturers to continue leveraging open source components securely and at scale despite those constraints.

Secondly, this paper will outline steps that open source projects could take to help facilitate this due diligence obligation—notably by providing increased transparency about their security posture, recommend existing standards or specification that projects could adopt, and propose new ones where appropriate.

Finally, this paper will examine the tension between the practical necessity for manufacturers to shift security left (i.e. with the open source projects) and their inability to compel those projects to take on this responsability—given that compliance obligations rightfully rest with the manufacturers—and will underline the need for incentives-aligning mechanisms to resolve this tension.

This white paper will be shared with the [EU Commission][] and the [CRA Expert Group][] and will provide important context for the [Specification on generic security requirements for open source components][].

Note: This white paper might be combined with the paper on [security attestations][].

## Status of this document

This is a draft document and may be updated, replaced or obsoleted at any time. It is inappropriate to cite this document as other than a work in progress. Publication of this document as a draft does not imply endorsement by the Eclipse Foundation, Open Regulatory Working Group Members, or contributors.

## Contents

1. What is due diligence
2. To what do we apply due diligence

    2.1 Which products

    2.2 Which components of the product
3. What and how to record due diligence, evidence

    3.1 Levels of due diligence

    3.2 What has to be checked

4. What happens when due diligence fails

5. How open source projects and stewards can help manufacturers to achieve due diligence
    * Voluntary attestation
    * Provide security history
    * Maintain security process description and evidence it is followed
6. Additional aspects/references
    
    >e.g. What will MSA investigate, what will they check, what should we be prepared for to show them?

## What is Due Diligence

**Due diligence** is the obligation of manufacturers to

1.  carry out **concrete verification actions** on third-party components (including
    free and open-source software) before integrating them into their
    **products with digital elements**,
2.  **act on the findings** of those verifications, and to
3.  **continuously monitor** integrated components throughout the product lifecycle,

to ensure those components do not compromise the product's cybersecurity.

The **scope and intensity** of the verification actions is determined
by **two prior risk assessments**, both of which serve as preconditions
for due diligence:

-   **Component-level risk assessment**: an evaluation of the inherent
    cybersecurity risk of the component itself, independent of context
    (e.g., a cryptographic library carries inherently higher risk than
    a basic UI component)

-   **Product-level risk assessment**: an evaluation of the
    manufacturer's own product and the intended use context of the
    component within it

Together, these two assessments determine how extensive the
verification actions need to be in order to judge the risk
that the component compromises the product's cybersecurity.

Due diligence is only **complete** when the manufacturer has not just
verified but also **acted on the findings**, which may include:

-   **Accepting** the component as-is (if verification confirms it is
    adequate and/or residual risk is accepted)
-   **Applying mitigations** (e.g., adding a security wrapper, restricting
    the component's access)
-   **Rejecting** the component entirely (if cybersecurity risks cannot be
    adequately addressed)

Due diligence is a **continuous process**, not a one-time event:

-   **Initial due diligence**: carried out before integration, as
    described above
-   **Ongoing due diligence**: continuously monitoring integrated
    components for, e.g.:
    -   Newly discovered vulnerabilities
    -   Changed risk profiles
    -   Changes in the component's maintenance status (e.g., a component
        becoming abandoned)

**Note:** Due diligence spans the **entire product lifecycle** and
complements but is distinct from  the **ongoing vulnerability
handling** obligations that apply separately under Annex I, Part II
of the CRA.


## Acknowledgments

The following people have contributed to this document either directly or indirectly (e.g. by raising questions):

Tobie Langel, Gergely Csatari, Timo Perälä. 

If you have contributed to this document and aren't properly acknowledged or if you want to edit or remove your name, please let us know by [opening an issue](https://github.com/orcwg/orcwg/issues/new) and we will fix this right away.

[Article 13(5)]: https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#art_13
[EU Commission]: ../README.md#key-stakeholders
[CRA Expert Group]: ../README.md#cra-expert-group
[Specification on generic security requirements for open source components]: ../proposed-specs/generic-security-requirements.md
[security attestations]: ./security-attestations.md


