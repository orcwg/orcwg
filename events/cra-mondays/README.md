# CRA Mondays

## Upcoming

CRA Mondays will take a break for the holiday season and return with new sessions in January. 

🗓️ When: **January 19, 5pm CEST** - right after the SIG Call ([in your time zone](https://www.timeanddate.com/worldclock/fixedtime.html?iso=2025-06-23T15:00:00.000Z&msg=CRA%20Mondays))\
📍 Where: [Zoom](https://eclipse.zoom.us/j/82349283943)\
➕ [Add to calendar](https://calendar.google.com/calendar/event?action=TEMPLATE&tmeid=NGo1YWhzZ3YydG1rb2dmZzVrcGcxZnEzdGpfMjAyNjAxMTlUMTYwMDAwWiBjXzdkYjhlM2YxM2M0ZmFjOTg0MTAzOTE4YTk3YzcwNGJiMWQ2MTlkYTBmZGI2NmQzM2YxNzQ3ODQ5YjYwMjBhZWFAZw&tmsrc=c_7db8e3f13c4fac984103918a97c704bb1d619da0fdb66d33f1747849b6020aea%40group.calendar.google.com)

---

## Previous episodes

<a name="episode-12"></a>
### 🗓️ November 24, 2025: When Disclosure Fails: Europe’s Struggle with CVD

Coordinated Vulnerability Disclosure (CVD) is written into NIS2 and the Cyber Resilience Act as a cornerstone of Europe’s cybersecurity policy. In practice, though, the system is failing. When I reported a vulnerability in a major Belgian bank through the official channels, I was met with bureaucracy, legal threats, and a total lack of technical engagement; both from both the bank and Belgium’s national cybersecurity authority. What should have been a routine disclosure turned into a long standoff that perfectly illustrates how Europe’s CVD framework is broken. ([slides](2025-11-24_CVD.pdf) | [video](https://youtu.be/G37gXO0KG6I))

<details>
<summary>More info</summary>

In this talk, I’ll show how these problems aren’t just Belgian, but systemic. Across the EU, policymakers treat CVD as a means to impose requirements on reporters instead of a commitment by organisations to receive and fix vulnerabilities. They confuse disclosure with bug bounties, enforce pointless formalities, and discourage the very people trying to help. I’ll explain what went wrong, why it matters for NIS2 and the CRA, and how we can fix CVD before it collapses under its own red tape. 

**Speaker: Piet De Vaere, Product Cybersecurity Consultant**

Piet is an electrical engineer, computer scientist, and consultant specializing in product cybersecurity compliance. His focus areas include the EU Cyber Resilience Act (CRA), the EU Radio Equipment Directive (RED DA), and the UK Product Security and Telecommunications Infrastructure (PSTI) Act. He regularly applies standards such as EN 303 645 and IEC 62443 to support compliance projects.

</details>

<a name="episode-11"></a>
### 🗓️ November 10, 2025: OSS provenance and code signing: how SignPath Foundation guarantees software integrity for its member projects

Some OSS projects are maintained by a foundation like Eclipse, Apache, or Mozilla with often rigorous governance over the release process. However, this approach doesn’t scale, so most OSS projects ship unverified and often unsigned releases. This breaks the trust model of Linus’s Law, which is based on source code. Also, OSS releases are often unsigned, leading to a major security degradation and often usability issues. Unverified signing can lead to issues like the 2024 XZ Utils incident. ([video](https://youtu.be/_fGOgByN08c))

<details>
<summary>More info</summary>

 SignPath Foundation provides free and secure code signing for 250 OSS projects. To achieve this, we had to go beyond key security: how can we guarantee that releases are safe to use?

Key points:

- Introduction of SignPath foundation
- OSS project vetting and approval process
- Automatic provenance verification of releases
- Code signing challenges
- CA certificate provisioning
- Goals and limits of security and process vouching

**Speaker: Stefan Wenig, Founder of SignPath GmbH, director of SignPath Foundation**

</details>

<a name="episode-10"></a>
### 🗓️ October 27, 2025: From closed rooms to open dialogue: how to participate in CRA vertical standards

The development of vertical standards under the Cyber Resilience Act (CRA) is a critical step toward implementation, yet these processes are often opaque and difficult for stakeholders that are not members of the standardization bodies to engage with. This presentation introduces a new open platform designed to make participation accessible to the wider community. It enables developers, manufacturers, and open source contributors to review, comment, and share feedback, creating a bridge between technical expertise and regulatory work. ([video](https://youtu.be/lCGBoNm0G08))

<details>
<summary>More info</summary>

This session will cover: 

- CRA vertical standards development under ETSI
- Open participation in a traditional closed process
- Tooling for participating
 
**Speaker: Jordan Maris**

Jordan is the OSI's EU Policy Analyst. He spent the last three years as an assistant to a Member of the European Parliament, campaigning for Open Source Software in negotiations on laws such as the AI Act, Cyber Resilience Act and Product Liability Directive among others. Jordan is a long-time user of Open Source software and a strong advocate for the Public Money–Public Code principle. 

</details>


<a name="episode-9"></a>
### 🗓️ October 13, 2025: Demystifying "simplified CC for CRA"

Let's unpack the sCC4CRA methodology, specially designed to facilitate early compliance for default products, based on EUCC, fully self-assessed and simplified for CRA. ([slides](2025-10-13_DemystifyingsCC4CRA.pdf) | [video](https://youtu.be/2JfterY07j8) | [project link](https://github.com/sCC4CRA))

<details>
<summary>More info</summary>

This session will cover: 

- What is sCC4CRA and why it matters
- EUCC vs sCC4CRA: key differences
- sCC4CRA alignment with standardisation work
- how to use sCC4CRA
- Future and next steps
 
**Speaker: Roger Riera**

Roger Riera is a member of the European Commission’s Cyber Resilience Act (CRA) Expert Group as a Type A member, contributing to the effective implementation of the CRA regulation. Technical Manager at Applus+ Laboratories, specialising in hardware security, with 10 years of experience in the field

</details>

<a name="episode-8"></a>
### 🗓️ September 15, 2025: Why Do You Trust Software? Operationalizing CRA with the Eclipse Trustable Software Framework

Modern products—from cars and planes to medical devices and consumer gadgets—depend on millions of lines of software hidden deep inside. The EU Cyber Resilience Act (CRA) now requires manufacturers and suppliers to prove that this software is secure, maintained, and resilient over the long term. But while the CRA defines *what* must be achieved, the industry is still asking *how*.

The Eclipse Trustable Software Framework (TSF) may provide part of the answer. Built around six trustable tenets and exploring a FICO-style Trustable Score, TSF suggests a path for making software trust more measurable and auditable. In this session, we’ll discuss how TSF could complement CRA obligations, where it may help engineers, executives, and regulators, and why open collaboration is essential to shaping the future of trustable software. ([video](https://youtu.be/Jnk_I2mI5xQ?si=FHcHSxE_ykxC3rFC))

<details>
<summary>More info</summary>
 
**Speaker: John Ellis**

John Ellis is the President and Head of Product for Codethink, a world-class provider of
critical, high-performance software projects for international-scale companies in a range
of industries including Automotive, Finance, Medical, and IoT. Headquartered in
Manchester, UK, Codethink has pioneered software industry thinking around concepts of
trustable software, with a view to improving the quality of software engineering for
societal good. Example customers include Arm, Bloomberg, BMW, Bosch, JLR, John
Deere, Mercedes-Benz, Panasonic, Volkswagen, and Tesla.

As a former executive at Motorola, Global Technologist at Ford Motor Company, and a
consulting and startup veteran, John led or participated in teams that built many of the
innovations we see today in connected vehicles on the ground and in the air.

John is the best-selling author of _The Zero Dollar Car_, a former adjunct professor at
University of Notre Dame, as well as a former translator in the 1992 Summer Olympics.

John can be found online @ [www.johntellis.com](https://www.johntellis.com/).

**Key Points:**

- Exploring CRA in Practice: Learn how the Eclipse Trustable Software Framework (TSF) could help translate CRA’s broad legal requirements into practical engineering steps.

- Trust Made Measurable: Consider how a FICO-style “Trustable Score” might offer a way to make software assurance auditable and comparable across organizations.

- An Open Conversation: Join engineers, executives, regulators, and lawyers in the Eclipse community to discuss how TSF may evolve as part of CRA’s future.
 
</details>

<a name="episode-7"></a>
### 🗓️ September 1, 2025: Unlocking Software Supply Chain Security: Updates from Ecma TC54 and OWASP

At the heart of the EU Cyber Resilience Act (CRA) and other emerging EU regulations lies a critical focus on supply chain security and Software Bill of Materials (SBOM). Ecma TC54, in collaboration with OWASP, is advancing this agenda through its work on “Software and system transparency.” ([slides - part 1](2025-09-01-TC54_CRA_Monday.pdf) [slides - part 2](2025-09-01-Framework_Ecma_CRA.pdf) | [video](https://youtu.be/NglPCEu4pok))

<details> 
<summary>More info</summary>
In this session, you will gain insights into key initiatives shaping the future of software transparency—from OWASP CycloneDX to new efforts around software identifiers (PURL), Common Lifecycle Enumeration (CLE), and the Transparency Exchange API (TEA) for automating the delivery of transparency artefacts across the supply chain.
 
The session will also provide an overview of Ecma International’s role as a global standards organisation. A Q&A segment will give you the chance to engage directly with experts on these critical CRA-related standards.

**Speakers**
- Olle E Johansson 
- Steve Springett
- Philippe Ombredanne
</details>

<a name="episode-6"></a>
### 🗓️ June 23, 2025: Pedro Demolder on The CRA: Why even your fridge might need a lawyer

Most of the impact of the Cyber Resilience Act (CRA) on the open source ecosystem will be indirect – but not insignificant. As manufacturers face new due diligence obligations when integrating open source components into their products and services, it’s essential to understand how open source is legally categorized under the CRA and what that means in practice.
In this session, we’ll explore what this categorization implies for open source contributors and maintainers, how we can prepare for the changes ahead, and how the open source community might even benefit from constructive dialogue around compliance. You’ll gain insight into how manufacturers and their legal teams approach CRA compliance – and how that mindset could affect your project.
Who better to guide us through this than a lawyer specializing in IT compliance? That’s why we’re excited to welcome Pedro Demolder, attorney at Timelex, who will share how he advises clients navigating the CRA and what it means for the future of open source. ([slides](2025-06-20-Pedro-Demolder.pdf) | [video](https://youtu.be/SP1xjDDLt9U))

<details>
<summary>More info</summary>

**Key-points**
- The CRA as a category of legislation
- The importance of the CRA for businesses
- The role of components, including open source, under the CRA
- Due diligence obligations for manufacturers
- Conformity assessments and security attestations
 
**Bio:** Pedro Demolder is an IP/IT and data protection lawyer at Timelex. He assists both SMEs and multinationals with GDPR and Data Act compliance, performing audits and helping implement legal requirements into daily operations, systems, and processes. He regularly advises on complex matters at the intersection of technology law and other domains, such as online platforms, product manufacturing, and HR. Pedro is well-versed in drafting information notices for a wide range of target audiences and negotiating data processing, data exchange, and data sharing agreements.
Pedro also advises clients on all aspects of cybersecurity, including the legal, technical, operational, and organisational dimensions of information security. He supports the setup of compliance frameworks, breach notification procedures, and contingency planning. In addition, he provides trainings on data protection and cybersecurity obligations, ensuring that legal requirements are understood and embedded in practice.

</details>

<a name="episode-5"></a>
### 🗓️ June 9, 2025: Arnaud Le Hors on Supply-chain Levels for Software Artifacts (SLSA)

SLSA is a security framework, a specification, for describing and incrementally improving supply chain security, established by industry consensus within OpenSSF. It is organized into a series of levels that describe increasing security guarantees, to prevent tampering, improve integrity, and secure packages and infrastructure. It’s how you get from "safe enough" to being as resilient as possible, at any link in the software supply chain. This presentation will introduce attendees to SLSA, its current status, and what’s in the works. ([slides](2025-06-09-ArnaudLeHors.pdf) | [video](https://youtu.be/5t9EGPTll64))

<details>
<summary>More info</summary>
 
**Bio:** Arnaud Le Hors is Senior Technical Staff Member of Open Technologies at IBM, working on a range of technologies with a primary focus on Open Source supply chain security and AI. He has been working on standards and open source for over 30 years. Arnaud was editor of several key web specifications including HTML and DOM and was a pioneer of open source with the release of libXpm in 1990. Arnaud is the main representative for IBM at W3C and INCITS, Co-Chair of the LF AI & Data Generative AI Commons, a member of the OpenSSF Technical Advisory Committee.

</details>


<a name="episode-4"></a>
### 🗓️ May 26, 2025: Fukami on learning how to stop worrying and love the NLF
The New Legislative Framework (NLF) is a package of EU measures that reinforces the application and enforcement of internal market legislation in the EU. It also establishes a common legal framework for products in the form of a toolbox of measures for use in future legislation on which the CRA builds. In this presentation, Fukami will dive into the NLF and how it relates to the CRA and other European product legislation. The aim is to get a better understanding of the key parts, including market oversight, the role of standards, CE marking and the Blue Guide and document how to place products on the European market.
([slides](2025-05-26-Fukami.pdf) | [video](https://youtu.be/7CbHwsKVD80))

<details>
<summary>More info</summary>
 
Bio: [Fukami](https://www.linkedin.com/in/fukami/) lives in Brussels and works for the OpenSSF as EU Policy Advisor. He is member of ETSI, the CRA EG on behalf of OpenSSF and in JTC13/WG9.

</details>


<a name="episode-3"></a>
### 🗓️ May 12, 2025: Maxim Baele on OWASP SAMM
The [OWASP Software Assurance Maturity Model (SAMM)](https://owasp.org/www-project-samm/) is an open framework designed to help organizations implement a Secure Development LifeCycle (SDLC). 
Understanding how manufacturers implement the processes required to build products that are secure by design, is essential to understand how they will consider their due diligence requirements when ingesting open source components. 
Maxim Baele is one of the SAMM core team members that maintain the model, using it on a daily basis to help organizations across the globe build secure products.
([slides](2025-05-12-maxim-baele.pdf) & video - coming soon)

<details>
<summary>More info</summary>

[Maxim Baele](https://www.linkedin.com/in/maximbaele/) is an experienced cybersecurity consultant specializing in product and application security​, with a background in Linux system engineering, security architecture, and automation​.
He spends his days coaching organizations in building secure products and implementing cybersecurity strategies​, while spending many of his evenings contributing to OWASP as a liaison, as a board member for OWASP BE and a core team member of the OWASP SAMM project.
 
</details>

<a name="episode-2"></a>
### 🗓️ April 28, 2025: Olle E. Johansson on managing CVEs in an unstable world
The cybersecurity community has been up in arms over the last few days as MITRE announced that its US government funding for running the Common Vulnerabilities and Exposures (CVE) program wasn't being renewed. While the funding was extended since, this was a wakeup call for the community. Olle E. Johansson shared an [opinionated white paper](https://docs.google.com/document/d/1u6yPlCla7SO6YuHakjvmcGtcEmHdp-NANaqpTDTA7Q0/edit?usp=sharing) on this topic. He'll be presenting this paper during the call and we'll use it as a basis for discussion.
([slides](2025-04-28-olle-e-johnansson.pdf) | [video](https://youtu.be/zSsGLJTgWvU?si=11oIsKc8ac43pH5M))

<details>
<summary>More info</summary>

This talk will cover a proposal for a globally coordinated platform for vulnerability reporting that ensures transparency, strengthens manufacturer accountability, and enables trusted third-party data enrichment. As cybersecurity regulations for connected products advance worldwide, the current model—primarily funded by a single state and dependent on unaffiliated third parties for critical data—faces limitations in scalability and neutrality. A new approach is needed: one that gives manufacturers control over submitted data, integrates independent data providers, and is governed and funded by a diverse coalition of global stakeholders. The session will explore how such a system can enhance trust, regulatory alignment, and security for both users and industry.

**Olle E.Johanson** is an experienced and appreciated speaker, teacher as well as an Open Source developer and consultant. He is currently project lead for OWASP Project Koala- developing the Transparency Exchange API (TEA), member of the CycloneDX industry working group, the OWASP SBOM Forum, co-founder of SBOMEurope.eu and a leader for the DNS TAPIR Open Source project. While not trying to save the world with SBOMs, he is helping clients with the journey towards CRA compliance as a consultant in his company Edvina AB.
  
#### References 
 - *A call for action: The path towards a global platform for vulnerability reporting*. [This document](https://docs.google.com/document/d/1u6yPlCla7SO6YuHakjvmcGtcEmHdp-NANaqpTDTA7Q0/edit?usp=sharing) is the base for the discussion
 
</details>

<a name="episode-1"></a>
### 🗓️ April 14, 2025: Sébastien Heurtematte on facilitating CRA compliance for SMEs with OCCTET

Sébastien Heurtematte will be joining us to tell us more about OCCTET, an EU-funded initiative aimed at improving the cybersecurity and CRA compliance of SMEs. He'll also share with us the initial report on a survey OCCTET has been running with SMEs and open source stewards to learn more about their concerns when it comes to CRA compliance.
([slides](./2025-04-14-sebastien-heurtematte.pdf) | [video](https://www.youtube.com/watch?v=1CWy55AhEnc))

<details>
<summary>More info</summary>

**Sébastien Heurtematte**, member of the Eclipse Foundation, is the coordinator of the OCCTET project, leading a consortium of 7 partners across Europe working to make Cyber Resilience Act (CRA) compliance simpler and more accessible for SMEs. With a strong technical background in open source, release engineering, and supply chain, he brings years of experience simplifying complex processes and addressing security challenges. Passionate about collaboration and accessibility, he focuses on making CRA compliance practical and approachable for both open source projects and SMEs.

#### References
- [OCCTET Website](https://occtet.eu/)
- [European Cybersecurity Competence Centre and Network](https://cybersecurity-centre.europa.eu/index_en)
 
</details>
