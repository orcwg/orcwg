# Contribution to CEN/CENELEC WG 9 PT 3 Vulnerability Handling Standard

## Request

Provide the content for the **informative** section on open source software stewards (<strike>Clause 4.4</strike>Annex D).

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

## Discussion and feedback on May 28, 2025

The contribution was discussed again during the PT 3 call on May 28, 2025.

The result of the discussion:

- The current text rephrases CRA's sections on stewards, and it should not be doing that
- Instead, it should be describing (for manufacturers) how to interact with Open Source Stewards in the vulnerability reporting contect (like CVD - coordinated vulnerability disclosure)
- The section has been moved to Annex C and has been asked to aim at: helping manufacturers understand interactions with open source stewards, describe the role of open source as introduced in the CRA text, describe the relation with the standards and what is expected and reasonable.

## Proposition of the annex outline

As the expected main audience of the annex, the goal could be to explain main misconceptions, and also explain what could and could not be expected from open source projects.

Proposed outline:

- There will be open source with stewards and open source without stewards. Both types will likely use similar methods for vulnerbaility handling, but with some slight differences.

- Open source projects usually follow CVD practices, details of this varies from one project to another. They generally follow guidelines available under an open source licence. Security policies of each projects are publicly documented, if they have been agreed on.

- Open source projects are not suppliers, so they will usually not respond to request for filling CRA paperwork. It might be offered as a separate service by freelancers, service companies related with the project, or the project itself. Some project might decide to prepare templates, but this fact, and the scope of templates, is their choice.

- Relations between stewards and open source projects
 - Stewards usually cannot oblidge the project to perform a specific action (example: develop a fix)
 - Stewards can act as coordinators in the CVD process
 - Stewards prepare security policy for the projects they support

- Differences between projects with and without stewards
 - Projects with stewards will have security policies, while projects without stewards might not have them
 - Stewards might offer an unified way of contact for security issues for all projects they support, manufacturers needs to contact projects without stewards indirectly

- Expectations of open source project when being contacted by manufacturers about a potential vulnerability
 - Open source projects usually have SECURITY (.txt, .md...) file in their source repository with the preferred way to contact them for a security issue
 - Open source projects expect patches under a compatible (with that given project) open source licence
 - Open source projects will not sign NDAs (non disclosure agreements), but they do participate in CVD (coordinated vulnerability disclosure)
 - Open source projects may have expected response and time to fix, but it is not their obligation
 - Manufacturers who want to have a fix developed, might contact the project to suggest freelancers or support companies offering such services


## Acknowledgments

The following people have contributed to this document either directly or indirectly (e.g. by raising questions):

Arnout Engelen,
Juan Rico,
Lars Francke,
Marta Rybczynska,
Mikael Barbero,
Timo Perala,
and Tobie Langel.

If you have contributed to this document and aren't properly acknowledged or if you want to edit or remove your name, please let us know by [opening an issue](https://github.com/orcwg/orcwg/issues/new) and we will fix this right away.
