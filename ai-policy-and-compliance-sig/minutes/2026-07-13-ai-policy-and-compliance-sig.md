---
SIG: AI Policy and Compliance SIG
Document type: Minutes
Status: 📝 Draft
Date: 2026-07-13
---

## Agenda
| Min | Agenda Topics | Moderator |
| --: | ----- | --- |
|   0 | Comments on today's agenda; approval of previous minutes| Ciarán |
|   5 | Launch of PanEval, soon | Ciarán |
|  10 | Proposal for Co-Lead of ORC AI SIG | Ciarán |
|  15 | AI Act EC consultation on high-risk AI (ORC submission) | Ciarán |
|  20 | | |
|  25 | | |
|  30 | | | 
|  35 | AI Act standards (not officially an ORC project) | Ciarán |
|  40 | | |  
|  45 | SIG scope: should we produce advice for projects, e.g. "AI Act conformity statement" for projects with no obligations (discussed on Slack) | Ciarán |
|  50 | AOB | |
|  55 | | |

## Participants

- Alistair Woodman (Erlang Ecosystem Foundation)
- Ciarán O'Riordan (Eclipse Foundation)
- Dave Russo (Red Hat)
- Isabel Drost-Fromm (Apache Software Foundation)
- Juan Rico (Eclipse Foundation)
- Karen Bennet
- Matt Albrecht (Zilliant)
- Mathias Schindler (GitHub)
- Pavel Hruza (Red Hat)
- Pierre Pronchery (FreeBSD Foundation)
- Salve J. Nilsen (CPANSec)
- Sebastian Raible (APELL)


## Minutes (Draft)

- The meeting agenda was circulated the same day as the meeting, with apologies, so it was proposed (and accepted), that approval of the kick-off minutes, and the vote on the Co-Lead would be left for the following meeting
- The PanEval launch is very close, but not yet official.  It will be presented in the near future.
- EC Draft guidelines on high-risk AI: There was discussion of paragraph 12 and whether FOSS might always be qualified as high-risk:
    - "If the instructions for use, contractual arrangements, terms of service, usage policy, promotional and sales materials, or the technical documentation present the AI system as broadly applicable across a generality of contexts and functions, and do not consistently limit its application or exclude high-risk uses, the system’s intended purpose will be deemed to also encompass high-risk use cases and therefore qualify as high-risk."
        - Some felt this is not a problem, because we can "consistently" state that a package is not for high-risk use, even if we don't put the limits in our licences (contractual arrangements).
        - Others felt that FOSS could not unambiguously fulfil the "consistently" obligation because our licences allow all uses and a later sentence in paragraph 12 adds that "merely asserting (...) is insufficient"
        - There was general agreement that more clarity in paragraph 12 would be good, to ensure that the material options available in FOSS (such as READMEs) are considered sufficient, and so that there is a way to express a limitation without contradicting FOSS definitions
    - Ciarán agreed to integrate this feedback into a text to be proposed to the group
- AI Act standards:
    - There was discussion on how to share pieces of text that we are discussing, Ciarán highlighted the reasons to be conservative but agreed to try to find a way to get clarity on what is possible
    - There was discussion of 11.5.4 of the draft AI Act standards "Cybersecurity specifications for AI Systems"; Ciarán is looking into this but the timeline doesn't allow for an ORC collaboration
- AI Act conformity statements, e.g. projects including a statement if they believe they do not have AI Act obligations
    - It was agreed that this topic is within scope and of interest to this group
    - Some expressed concerns that having such a statement in a project could create the impression that other projects are in scope
    - Or that doing this for the AI Act could raise questions of how many other laws should a project make declarations about
    - Some agreed that we should look for alternatives for how to create clarity
