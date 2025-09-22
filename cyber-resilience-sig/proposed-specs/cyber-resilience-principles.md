---
SIG: Cyber Resilience SIG
Task force:
Document type: Specification
Number: 4.2
Status: 🗺️ Planned
Input to: ISO
Relevant liaisons: EU Commission, CRA Expert Group, CEN/CENELEC, Market Surveillance
License: CC-BY 4.0 or Apache 2.0
Final license: EFSL
---

# Specification on principles for cyber resilience for open source

## Description

This specification is intended address the requirements spelled out in [Annex I, Part I, point (1)][] but specifically targeted at the development of open source components and with a focus on the due diligence obligations of manufacturers. It will build on the white papers on [SBOMs][], [due diligence][], and [security attestations][] mentioned above.

This specification aims to address the following issue:

1. Provide a specification that is freely accessible and royalty-free so that open source projects can implement it.
2. Formalize recognized good practices that improve the security posture of open source projects.
3. Provide a machine-readable way (for example through dedicated SBOM fields) for open source projects to document and transparently share factual information about the cyber resilience practices that they implement in order to faciliate the due diligence of manufacturers.
4. Help resolve the challenge of assessing risk for components whose use-cases aren't known at the time of development, by providing transparency on the project's posture to manufactueres integrating them, allowing them to carry out their own risk assessment as part of their due diligence obligations.

Where appropriate, this specification will reference and build on existing material, notably collected in the [inventory][]. It may be broken down into separare documents or combined with the [Specification on generic security requirements for open source components][generic security requirements] detailed below to specify a "broad vertical."

Note: The challenge of assessing risk for components whose use-cases aren't known at the time of development might benefit from its own white paper.

[Annex I, Part I, point (1)]: https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#anx_I
[SBOMs]: ../whitepapers/sboms.md
[due diligence]: ../whitepapers/due-diligence.md
[security attestations]: ../whitepapers/security-attestations.md
[inventory]: https://github.com/orcwg/cra-hub/blob/main/inventory.md
[generic security requirements]: ./generic-security-requirements.md