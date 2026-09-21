---
SIG: AI Policy and Compliance SIG
Document type: Minutes
Status: 🗓️ Proposed agenda
Date: 2026-09-07
---

## Agenda
| Min | Agenda Topics | Moderator |
| --: | ----- | --- |
|   0 | Approve previous minutes | Ciarán |
|   5 | Plan: scpoe discussion in google doc, for adoption 21 Sep| Ciarán |
|  10 | | |
|  15 | | |
|  20 | CRA & AI Act interaction: is CRA for models even possible? Part 2: getting structured | Ciarán |
|  25 | | |
|  30 | | | 
|  35 | AI Act logging standard (PREN18229-1) | Ciarán |
|  40 | ETSI working group on policy, and "AIPP" collaboration with South Korea & Japan| |  
|  45 | AOB | |
|  50 | | |
|  55 | Meeting ends at __:55 | Ciarán |

Note: It's a public holiday in parts of the world, so the 7 September meeting will not be for decisions (other than approval of minutes).

## Participants 

* Juan Rico (Eclipse Foundation)
* Ciarán O'Riordan (Eclipse Foundation)
* Javier Valiño (Eclipse Foundation)
* Rachel Foucard (TYPO3)
* Sankalp Gilda 
* Mathias Schindler (GitHub)
* Tobias Frech (iJUG)
* Isabel Drost-Fromm (Apache Software Foundation)
* Roman Zhukov (Red Hat)
* AEva Black (Null Point Studio)
* Gregor Bransky (inöG)

## Minutes

**Minutes approved: for 24th of August 2026 meeting**

**Plan: scope discussion in google doc, for adoption**

The group reviewed the [draft scope document](https://docs.google.com/document/d/17EjOCd4LjLunnDPB4MSDB51yfs53ceeECuqcm4g64cY/edit?tab=t.0#heading=h.c30vi6jobft8) designed to establish the SIG’s focus and guide future deliverables. To define clear boundaries, members proposed that the Cyber Resilience (CR) SIG handle CRA compliance for software components, while the AI SIG handle CRA compliance specifically for AI models. It was emphasized that cross-referencing information between the two groups will be essential to provide seamless, unified guidance for end-users attempting to achieve compliance.

**CRA & AI Act interaction: is CRA for models even possible? Part 2: getting structured**

The group debated how to map compliance across both acts, noting the necessity of aligning with CEN/CENELEC Working Groups 5 and 9 to avoid duplicating standardization efforts. Discussions highlighted the need to compare the AI Act's use-based requirements with the CRA's foreseeable use requirements, alongside an unresolved debate over whether shipping raw model files (e.g., .gguf) or configuration files triggers CRA obligations. Ultimately, members agreed that systematically reviewing CRA Annex 1 point-by-point offers the most structured approach for evaluating its applicability to open-source AI models.

**AI Act logging standard (prEN 18229-1)**

A a detailed review of the draft logging standard (prEN 18229-1) should be done. The primary objective of this review will be to identify any careless wording or proprietary-centric assumptions (such as presuming single-company development pipelines or the ability to remotely recall published code and models) that conflict with the realities of FOSS development.

**ETSI working group on policy, and "AIPP" collaboration with South Korea & Japan**

An update was shared regarding ETSI’s new AI Partnership Project (AIPP) following a recent introductory call and ahead of an upcoming hybrid meeting in Brussels. While the concrete technical standardisation goals of the AIPP remain undefined, the initiative is viewed as a strategic move to build alliances with global digital partners like Japan, South Korea, Canada, and Singapore to maintain relevance in EU standard-setting, with the group reportedly open to US participation as well.

**AOB: Overlap of NIS2, AI Act, CRA, and other regulations**

Members examined the complex challenge of mapping compliance overlaps across NIS2, the AI Act, the CRA, and sector-specific rules (such as DORA and MDR) without overwhelming development and security teams. Proposal to share sanitized versions of simplified internal compliance templates designed to streamline administrative tasks and shield technical teams from regulatory burdens.

## Action Points

* [ALL] Finalise the [draft scope document](https://docs.google.com/document/d/17EjOCd4LjLunnDPB4MSDB51yfs53ceeECuqcm4g64cY/edit?tab=t.0#heading=h.c30vi6jobft8) based on mailing list feedback over the next two weeks.
* [ECLIPSE FOUNDATION] Explore inviting a representative from CEN/CENELEC (WG5/WG9) to speak at a future meeting.
* [ALL] Analyse the use case applicability overlaps between the AI Act and the CRA to see if one is a clean superset of the other.
