---
SIG: Cyber Resilience SIG
Document type: Minutes
Status: ⚠️ Draft
Date: 2026-05-11
---

##  Agenda


| Min | Agenda Topics | Moderator |
| --: | ----- | --- |
|   0 | Welcome & approve [previous minutes](https://github.com/orcwg/orcwg/pull/297) | Juan |
|   5 | Intro to attestations | Æva |
|  10 | | |
|  15 | Intro to due diligence | Timo |
|  20 | 
|  25 | Open conversation to discuss the main friction points| Juan |
|  30 | | | 
|  35 | | |
|  40 | | |  
|  45 | Definition of the main action points per group | Æva, Timo and Juan |
|  50 | | |
|  55 | AOB | |

## Participants

-  Alistair Woodman (Erlang Ecosystem Foundation (EEF))  
-  Mathias Schindler, GitHub  
- Juan Rico (Eclipse Foundation)  
- Timo Perälä (Nokia)  
- Olle E. Johansson (OWASP / Edvina AB)  
- Marta Garcia (Eclipse Foundation)  
- Dave Russo (Red Hat)  
- Æva Black (Null Point Studio)  
- Adrian O’Sullivan ( Huawei )  
- Pierre Pronchery (FreeBSD Foundation)  
- Dirk-Willem van Gulik (Apache Software Foundat (ASF))  
- Anne Dickison (FreeBSD Foundation)  
- Tobie Langel (UnlockOpen)

## Notes

### Welcome & approve previous minutes

- Minutes approved will be merged after the call

### Intro to attestations

* Voluntary attestations under CRA Article 25 exist solely to lower manufacturer due diligence burden when using open source in commercial products.  
* Current gap: no European-citable standard defines the "low bar" for reasonable due care in handling open source commercially.  
* Courts typically look at industry/international standards to define "sensible professional" conduct, but these don't exist for secure open source development.  
* Small open source libraries cannot know product-specific use cases and cannot perform risk assessments; only larger "product-like" projects close to manufacturers can reasonably do this.  
* A mapping exists from the BSI lightweight self-attestation to specific Annex 1, 2, and 7 requirements, but it doesn't cover use case or risk assessment parts**.**

### Intro to due diligence

* Update on country-level adaption \- Finland removed the proposed fines for Open Source stewards\! (Timo) \- [details here](https://www.parliament.fi/asiat-ja-aanestykset/valtiopaivaasiat/asiakirjat/edktunnus/EDK-2026-AK-23895)   
* Due diligence work started late January 2026; currently in [Google Doc](https://docs.google.com/document/d/1_IpLqgWogDNGzN4J51L1pXQv0GsCYR4xPdn-BwXVBrk/edit?tab=t.em8fjxfncrmt) being migrated to GitHub for better tracking.  
* CRA states manufacturers must do due diligence but doesn't define what it is for software context.  
* CEN-CENELEC Working Group 9 **r**emoved their draft text on manufacturer due diligence for third-party components from specifications.  
* Plan to reach out to Finnish market surveillance authority to understand their expectations.

### Open conversation to discuss the main friction points

* The original scope was preventing denial of service attacks on maintainers from the manufacturer due diligence requests.  
* Manufacturers face thousands of dependencies in SBOMs and cannot do full due diligence on all; need categorization (direct dependencies, important ones, transitive).  
* Attestations may simplify due diligence for level 1-2 dependencies.  
* Only maintainers can provide assurances about their own project's security posture (security policy, promises).  
* Due diligence is context-dependent on the business application; manufacturers know their use case, not open source projects.  
* Practical due diligence quickly focuses on checking Annex 1 controls for each specific module and how it's used in the product  
* Suggested integrating due diligence into manufacturer risk assessment process for each product/software component, and based on that define the attestation level required to comply.  
* Open source often fails the first CE compliance step: prescribed product description and intended use. Open source can help with general risk assessment and provide QA/testing outputs, but anything beyond that requires knowing product description and intended use.

### Definition of the main action points per group

- [ ] Juan, Timo and Æva to define a list of actions to work on until the next SIG call in 2 weeks.  
- [ ] Define the agenda for the Task Forces and SIG call aligned with the actions defined  
- [ ] Communicate topics and plans through the mailing list.

### AOB

- No time for them

### Materials shared during the call

- Mapping on obligations \- [https://github.com/orcwg/cra-attestations/blob/main/proposals/gen-two-tier-approach.md\#template](https://github.com/orcwg/cra-attestations/blob/main/proposals/gen-two-tier-approach.md#template)   
- CISA provides guidance for manufacturers, [https://cisa.gov/sag](https://cisa.gov/sag)  
- The US Energy industry is discussing update procurement contract langauge that includes the "Secure by Design" question (bullet 20):  [https://naesb.org/pdf4/weq\_bps\_css052126w1.docx](https://naesb.org/pdf4/weq_bps_css052126w1.docx)
