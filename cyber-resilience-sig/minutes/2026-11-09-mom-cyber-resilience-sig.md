---
SIG: Cyber Resilience SIG
Document type: Minutes
Status: 📝 Draft
Date: 2026-11-09
---

## Agenda

| Min | Agenda Topics | Moderator |
| ----- | ----- | ----- |
| 0 | Welcome & approve [previous minutes](https://github.com/orcwg/orcwg/pull/376) | Juan |
| 5 |  Code & Compliance and ORC @FOSDEM  Topics and potential activities| Juan |
| 10 |  | |
| 15 |  | |
| 20 |  | |
| 25 |  Status of due diligence, attestations, stewards and maintainers and FAQ | |
| 30 |  | |
| 35 |  | |
| 40 |  | |
| 45 |  ENISA Technical Advisory on security.txt, CVD and Security Advisories - [Link](https://github.com/orcwg/orcwg/issues/375) - **(Deadline Nov 15th)**| Juan| 
| 50 |  Marketing update | |
| 55 | AOB |  |

## Participants

- Marta García (Eclipse Foundation)  
- Timo Perälä (Nokia)    
- Salve J. Nilsen (CPANSec)  
- August Bournique (Law Office of August Bournique)    
- Tobias Frech (iJUG)  
- Juan Rico (Eclipse Foundation)  
- Alistair Woodman (Erlang Ecosystem Foundation (EEF))  
- Dave Russo (Red Hat)  
- Matt Albrecht (Zilliant)  
- Tobie Langel (UnlockOpen)  
- Alice Sowerby (FreeBSD Foundation)  
- Jakub Zelenka (PHP Foundation)  
- Georg Kunz (Ericsson)

## Notes

### Welcome & approve previous minutes

- Minutes from the previous meeting were approved.

### Code & Compliance and ORC @FOSDEM Topics and potential activities

**Upcoming Events:** Code and Compliance is happening Thursday. ORC is partnering with FOSSapolooza (together with AboutCode, OpenChain, OWASP). FOSDEM devrooms were announced featuring relevant sessions like "Beyond the CRA" (OpenSSF) and the EU Policy Dev Room.

**Code & Compliance Workshop Format:** Based on steering committee feedback, the Code & Compliance session will allocate half its time to talks (working group activities) and half to practical, workshop-style discussions (one long or two short sessions).  
**Workshop Preparation:** A brief preparatory document will be shared in advance so attendees can come ready to discuss specific, tangible scenarios rather than purely theoretical concepts.

**Topic Brainstorming & Feedback:**

* **Practical Implementation:** Suggestions were made to focus on what due diligence looks like practically from a manufacturer's side, and how open-source stewards benefit from providing it. It was emphasised that this should be framed around the daily ecosystem needs of open-source developers, many of whom are employed by companies acting as manufacturers.  
* **Sustainability Concerns:** Participants highlighted a severe sustainability problem. Volunteer maintainers of heavily relied-upon projects are overwhelmed by CVEs and unpaid work. It was noted that certain ecosystems face unique challenges due to deep dependency trees, rapid library turnover, and a lack of alternative programming languages in specific environments.  
* **Use Case Selection:**  The group agreed it is safer to stick to pure software supply chain examples (e.g., 1Password) that are firmly under the CRA's purview.

### Status of due diligence, attestations, stewards and maintainers and FAQ

Minutes from last meetings:

- DD \- [https\://github.com/orcwg/orcwg/pull/378/changes](https://github.com/orcwg/orcwg/pull/378/changes)  
- Attestations \- [https\://github.com/orcwg/cra-attestations/pull/43/changes](https://github.com/orcwg/cra-attestations/pull/43/changes) 

#### FAQ Update:

* Substantial work has been completed on the CRA FAQs GitHub hub. Most issues related to maintainers and stewards are closed, organised into actionable categories, and directly linked to new guidance.  
* Halfway done with the manufacturers' section. References to external texts (like the AI Act) are being prepared.  
* **Call to Action:** The SIG is requested to review the current FAQs, utilise the "edit on GitHub" function for any unclear text, and discuss an approval process to anchor this as a "V1" for an announcement at upcoming events.

#### Due Diligence Update:

* The last meeting featured intense discussion on the scope of Remote Data Processing Services (RDPS) and its relation to due diligence.  
* The task force is adjusting the white paper's tone of voice to ensure it reads as guidance/best practices rather than a normative standard. The goal is to agree on PRs and finalise a Version 1 document soon.

#### Attestations & Stewardship Update:

* **Current Status:** Evaluating tools and deciding whether to proceed with an industry survey or start specifying attestations. Also discussing downstream/upstream AI Act obligations and aligning with the ENISA playbook for secure-by-design (the lightweight attestations PR).  
* **The Manufacturer Gap:** It was pointed out that current compliance tools focus solely on code state, ignoring project health and integration processes. It was emphasised that CE marking covers the entire product lifecycle; if security attestations only focus on "Day 1" (T0) and ignore long-term maintenance, they will fail to deliver on CRA goals.  
* **Lack of Standard:** Manufacturers have an obligation to monitor upstreams for EOL/CVEs, but there is no clear harmonised standard (like PREN 40000-3) for compliance officers or Market Surveillance Authorities to point to. Without a standard, manufacturers are unlikely to comply properly. It was noted that this gap is already being filled by commercial vendors forking OSS without funding upstream maintainers.  
* **Distributed Stewardship Model:** A proposal was shared outlining a distributed ecosystem steward model, a community-owned cooperative to assist manufacturers with due diligence by making membership a viability/security signal.

### ENISA Technical Advisory on security.txt, CVD and Security Advisories \- (Deadline Nov 15th)

* This was shared on the mailing list a few weeks ago, but no contributions have been received from the group yet.  
* Due to the tight deadline (tomorrow), if no group consensus or contributions are formulated before Tuesday 10th EOD, members will be encouraged to submit their individual views directly rather than submitting collectively as a working group.

### Marketing update

Currently open CfP:

- FOSDEM  
  - Code\&Compliance \- [https\://codeandcompliance.orcwg.org/code-compliance-fosdem-edition-2027/](https://codeandcompliance.orcwg.org/code-compliance-fosdem-edition-2027/)   
  - FOSSApalooza \- [https\://fossapalooza.eu/\#cfp](https://fossapalooza.eu/#cfp)   
  - FOSDEM Devrooms  
- OCX \- [https\://ocxconf.org/call-for-proposals/](https://ocxconf.org/call-for-proposals/) 

### AOB

- No time for AOBs
