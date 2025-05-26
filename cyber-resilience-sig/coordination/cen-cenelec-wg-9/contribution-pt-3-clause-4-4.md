# Contribution to CEN/CENELEC WG 9 PT 3 Vulnerability Handling Standard Clause 4.4

## Request

Provide the content for the **informative** section on open source software stewards (Clause 4.4).

## Context

- This is the standard for vulnerability handling covering the requirements defined in [Annex I, Part II](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#anx_I) of the CRA.
- The standard only focuses on what's in this annex, not any other obligations.
- The standard is aimed at manufacturers, not stewards.
- The section we're asked to contribute too is _informative_ (not _normative_), which means it doesn't create any requirements for anybody; it's just there to provide context.

## Goals for the submission

Remind the reader that:

- There are such a thing as stewards.
- This standard doesn’t place requirements on stewards.
- Manufacturers might be considered as stewards for some of their open source projects.
- Manufacturers need to interface with stewards for reporting vulnerabilities.
- Stewards don’t have to fix vulnerabilities that are reported to them, nor do they have to accept fixes for it. In particular they won’t if those fixes don’t meet the project’s IP requirements.
- Not all open source projects have stewards and manufacturers might still need to interface with them.
- The existence of a steward isn’t a guarantee that the project meets manufacturer security requirements, manufacturers will need to exercise due diligence regardless. Free and open source security attestations might help facilitate due diligence in the future.

Rationale for these goals:

- Stewards are a new class of actors that manufacturers might not be familiar with, it’s useful to give them additional context.
- There’s a common misconception that all open source projects will have stewards, it is useful to remind manufacturers that this isn’t the case.
- As this standard will be behind a paywall, we want to avoid placing any requirements on open source in it.
- As this standard will apply to manufacturers that incorporate open-source, we want to provide sufficiently-clear guidance to support positive interactions between manufacturers and open-source projects.

## Contribution submitted on May 20, 2025

The CRA introduces a new class of market actors: Open-Source Software Stewards (Stewards). This standard does not place any requirements on Stewards. However, the CRA does impose a number of obligations on Stewards, particularly to facilitate vulnerability handling.

Manufacturers are expected to interface with Stewards when reporting vulnerabilities they have discovered in open-source products that the Steward supports. Manufacturers are encouraged to contribute fixes they might have developed for those vulnerabilities under a license compatible with the open-source product.

To facilitate the reporting of vulnerabilities, Stewards shall create, implement, make publicly available, and ensure adherence to a policy on vulnerability handling for the products for which they are Stewards.

Not all open-source projects that a manufacturer depends on should be expected to be supported by a Steward. The obligations of the manufacturers towards those projects remain the same regardless.

Stewards are not responsible for developing remedies for the vulnerabilities reported in the software for which they are Stewards. However, a Steward must report severe incidents of which they are aware that impact the tools and services they provide to support open-source software development. Additionally, a Steward has a limited reporting obligation if they are involved in developing the open-source software for which they are Stewards.

## Feedback received on May 21, 2025

Contribution was presented on May 21, 2025 during a PT 3 call.

- No major comments.
- ToDos:
  - We need to do away with all "shalls", this is informative text.
  - Also have to check that we don't duplicate CRA text.
  - Check with PT 3 Rapporteur that contribution covers what is necessary.

Some discussion in PT 3:

- Suggestion to doublecheck the text is in alignment with PT1's draft.
- Confirmation that the [Standardisation Request](https://github.com/orcwg/cra-hub/tree/main/resources#february-3-2025---standardisation-request) has no reference to stewards, therefore nothing to be considered from that point of view.
- Proposal to remove the text from the "General" clause (clause 4) and move it to Annex.
- Suggestion to consider if the the text is required in the standard at all.
- Conclusion: for time being the text remains as Clause 4.4, moving to Annex or deleting entirely is an easy quick job.

## Proposed updates to the Contribution

The CRA introduces a new class of market actors: Open-Source Software Stewards (Stewards). This standard does not place any requirements on Stewards. However, the CRA does impose a number of obligations on Stewards, particularly to facilitate vulnerability handling.

Manufacturers are expected to interface with Stewards when reporting vulnerabilities they have discovered in open-source projects that the Steward supports. Manufacturers are encouraged to contribute fixes they might have developed for those vulnerabilities under a license compatible with the open-source project.

To facilitate the reporting of vulnerabilities, Stewards shall create, implement, make publicly available, and ensure adherence to a policy on vulnerability handling for the projects for which they are Stewards.

Manufacturers may depend on open-source projects that lack support from a Steward. The obligations of the manufacturors towards those projects remains the same regardless, so long as the project has a vulnerability handling policy.

Stewards are not responsible for developing remedies for the vulnerabilities reported in the software for which they are Stewards. However, where a Steward provides tools or services to support open-source software development, they must report any severe incidents they become aware of which affects these tools or services. Additionally, a Steward has a limited reporting obligation if they are involved in developing the open-source software for which they are Stewards.

Finally, the CRA also enables the establishment of voluntary attestation programmes to allow Manufacturers of products containing open source software components to assess the projects' conformity with essential cybersecurity requirements. Stewards are encouraged to support the participation of open-source projects they support in such programmes.

## Acknowledgments

The following people have contributed to this document either directly or indirectly (e.g. by raising questions):

Aeva Black,
Arnout Engelen,
Juan Rico,
Lars Francke,
Marta Rybczynska,
Mikael Barbero,
Timo Perala,
and Tobie Langel.

If you have contributed to this document and aren't properly acknowledged or if you want to edit or remove your name, please let us know by [opening an issue](https://github.com/orcwg/orcwg/issues/new) and we will fix this right away.
