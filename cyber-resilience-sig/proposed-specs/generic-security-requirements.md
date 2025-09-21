---
SIG: Cyber Resilience SIG
Task force:
Document type: Specification
Number: 4.3
Status: 🗺️ Planned
Input to: ISO
Relevant liaisons: EU Commission, CRA Expert Group, CEN/CENELEC, Market Surveillance
License: CC-BY 4.0 or Apache 2.0
Final license: EFSL
---

# Specification on generic security requirements for open source components

This specification is intended to addresses the requirements spelled out in [Annex I, Part I, point (2)][] but specifically targeted at open source components and with a focus on the due diligence obligations of manufacturers. It will build on the white papers on [SBOMs][], [due diligence][], and [security attestations][] mentioned above and work closely with the [Specification on principles for cyber resilience for open source development][cyber resilience principles] mentioned above.

This specification will provide a machine-readable way (for example through dedicated SBOM fields) for open source projects to document and transparently share factual information about which cyber security requirements defined in [Annex I, Part I, point (2)][] are relevant to the project, whether they are addressed by the project, or whether they need to be handled by the integrator.

Where appropriate, this specification will reference and build on existing material, notably collected in the [inventory][]. It may be broken down into separare documents or combined with the [Specification on principles for cyber resilience for open source][cyber resilience principles] detailed above to specify a "broad vertical."

## Acknowledgments

The following people have contributed to this document either directly or indirectly (e.g. by raising questions):

Tobie Langel.

If you have contributed to this document and aren't properly acknowledged or if you want to edit or remove your name, please let us know by [opening an issue](https://github.com/orcwg/orcwg/issues/new) and we will fix this right away.

[Annex I, Part I, point (2)]: https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#anx_I
[SBOMs]: ../whitepapers/sboms.md
[due diligence]: ../whitepapers/due-diligence.md
[security attestations]: ../whitepapers/security-attestations.md
[inventory]: https://github.com/orcwg/cra-hub/blob/main/inventory.md
[cyber resilience principles]: ./cyber-resilience-principles.md