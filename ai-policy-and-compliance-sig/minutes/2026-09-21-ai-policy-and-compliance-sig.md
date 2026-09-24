---
SIG: AI Policy and Compliance SIG
Document type: Minutes
Status: 📝 Draft
Date: 2026-09-21
---

## Agenda
## Agenda
| Min | Agenda Topics | Moderator |
| --: | ----- | --- |
|   0 | Approve previous minutes | Ciarán |
|   5 | Review of the [Scope document](https://docs.google.com/document/d/1hTyRaniaZ9eNTZr1hUz5tHMux-_7MxDRF1uI_shTfgU/edit) | Ciarán |
|  10 | | |
|  15 | | |
|  20 | Review of the new [FAQ document](https://docs.google.com/document/d/1V-3Yw0Es2jqu8QlbDH-3gjUjv1MBZwm6zhNcs-CXTIg/edit) | Ciarán |
|  25 | | |
|  30 | | | 
|  35 | | |
|  40 | | |  
|  45 | AOB | |
|  50 | | |
|  55 | Meeting ends at __:55 | Ciarán |


## Participants 
* Adrian O'Sullivan (Huawei)
* AEva Black (Null Point Studio)
* August Bournique
* Ciarán O'Riordan (Eclipse Foundation)
* Dave Russo (Red Hat)
* Javier Valiño (Eclipse Foundation)
* Juan Rico (Eclipse Foundation)
* Isabel Drost-Fromm (Apache Software Foundation)
* Karen Bennet
* Marcel Kurzmann (Bosch)
* Mathias Schindler (GitHub)
* Rachel Foucard (TYPO3)
* Shanda Giacomoni (Eclipse Foundation)
* Timo Perala (Nokia)
* Tobie Langel (Unlock Open)
* William Janssen 

## Notes

**Reminder to attend Code & Compliance**

A brief reminder was shared regarding the upcoming [Code & Compliance](https://codeandcompliance.orcwg.org/) event scheduled for October 27 in Brussels. The event will feature a hybrid program covering topics related to the Cyber Resilience Act (CRA), the AI Act, and intersecting compliance issues. All SIG members are strongly encouraged to attend in person to participate in these overarching regulatory discussions.

**Review of the Scope document**

The group reviewed the draft [Scope document](https://docs.google.com/document/d/1hTyRaniaZ9eNTZr1hUz5tHMux-_7MxDRF1uI_shTfgU/edit), which formally establishes the SIG’s focus on analyzing AI Act compliance specifically from the perspective of the FOSS ecosystem. After a brief discussion, the document was approved without objection, with the agreement to make one editorial change: removing the specific governance section to clarify that the SIG inherently operates under the overarching governance rules of the Eclipse ORC working group.

**Review of the new FAQ document**

Participants discussed the proposed format and tooling for a new FAQ document designed to track and resolve regulatory questions. A debate took place regarding the merits of using a Google Doc (which lowers the barrier to entry for policy and legal experts) versus GitHub (which provides better tracking and centralizes ORC workflow). Ultimately, it was agreed that SIG leadership will discuss offline how best to engage non technical stakeholders and return with a consolidated proposal for the official FAQ gathering system.

**AOB: The new ENISA consultation**

The group reviewed a recent [ENISA draft technical advisory](https://www.enisa.europa.eu/sites/default/files/2026-09/ENISA%20Technical%20Advisory-AI-assisted-software-development-draft.pdf?utm_source=chatgpt.com) regarding secure-by-design software development, noting that the draft critically omits guidance on securing AI agents, managing the supply chain of AI developer tools, and adapting to the realities of AI-augmented code generation. Participants emphasized that the industry's shift toward high velocity, AI-assisted development requires automated security paradigms akin to DevOps, rather than relying on manual code reviews. Consequently, the SIG agreed to open a collaborative issue to draft and submit a formal, unified response to the consultation ahead of the October 15 deadline.

**AOB: AI-Assisted Compliance Tool**

A brief discussion took place regarding a newly shared AI-powered automated EU AI Act compliance tool that attempts to measure model bias by evaluating output deltas based on modified input criteria (e.g., changing names or demographics on a CV). As most members had not yet reviewed the project in depth, it was agreed to defer a detailed analysis of the tool's utility to a future meeting.

## Action points

* [Ciarán] Update the approved Scope document to remove the redundant governance section and publish the final version.
* [Eclipse Foundation] Discuss offline to determine the best platform (e.g., GitHub vs. Google Docs) and outreach strategy for engaging non-technical legal/policy stakeholders in the FAQ creation process.
* [ALL] Provide contribution to an issue to collaboratively draft and submit a formal SIG response to the ENISA secure-by-design consultation before the October 15 deadline.
