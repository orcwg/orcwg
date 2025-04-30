# Cyber Resilience SIG

Cyber Resilience Special Interest Group (SIG) of ORC WG.

## Meetings

* [Meeting info](../MEETINGS.md)
* [Minutes](./minutes/)

## Leads
* Dirk-Willem van Gulik ([@dirkx][]), The Apache Software Foundation
* Simon Phipps ([@webmink][]), Software Heritage Foundation - Inria Foundation
* Timo Perala ([@timop62][]), Nokia

## Scope

The Scope of the Cyber Resilience SIG is a strict subset of the scope of ORC WG. Whereas the working group is chartered to address any kind of emerging regulation impacting open source, the Cyber Resilience SIG is solely focused on cyber resilience regulation. Expect all of the CRA-related work to happen in this SIG.

<a name="deliverable-plan"></a>
## Deliverables Plan

In 2025, the SIG will focus on deliverables necessary to help the open source community (and notably _open source software stewards_) meet the regulatory obligations outlined in the CRA and help downstream users (_manufacturers_) be able to continue to leverage open source in their products and services while meeting their own regulatory requirements.

* [Deliverables Plan](./deliverables.md)

```mermaid
gantt
    title Deliverables Timeline
    dateFormat  D MMMM YYYY
    axisFormat %b %Y
    tickInterval 1month

    section CRA FAQ
    Collect community FAQs: 1 December 2024, 31 December 2025
    Draft v1.0: 1 January 2025, 1 June 2025
    Publish CRA FAQ v1.0: milestone, 1 June 2025, 1d
    Draft v2.0: 1 June 2025, 1 November 2025
    Publish CRA FAQ v2.0: milestone, 1 November 2025, 1d

    section Inventory
    Collect community input: done, 1 December 2024, 30 April 2025
    Organize inventory: 1 February 2025, 30 May 2025
    Publish Inventory: milestone, 30 May 2025, 1d
    
    section Input to draft act on product categories
    Collect community input: done, 13 March 2025, 18 April 2025
    Submit input: done, milestone, 18 April 2025, 1d

    section on SBOMs

    section on Due diligence

    section on Attestations

    section Vulnerability management spec
    Create proposal: done, 1 November 2024, 1 March 2025
    Contribution proposal to WG: done, milestone, 1 March 2025, 1d
    Draft v1.0 RC: 1 March 2025, 1 June 2025
    Publish v1.0 RC: milestone, 1 June 2025, 1d
```

## Cyber Resilience Practices Project

* [Proposal for the Cyber Resilience Practices Project](https://projects.eclipse.org/projects/technology.crp)

### Project leads
* Dirk-Willem van Gulik ([@dirkx][]), The Apache Software Foundation
* Mikael Barbero ([@mbarbero][]), Eclipse Foundation
* Simon Phipps ([@webmink][]), Software Heritage Foundation - Inria Foundation
* Timo Perala ([@timop62][]), Nokia

## Task Forces

The Cyber Resilience SIG can form task forces that focus on a particular topic for a fixed period of time.

A task force must have one or more leads, an area of focus, a set of deliverables, and an end date by which it must present its deliverables and recommendations to the SIG and/or request an extension.

A task force's proceedings are public.

Task forces do not have any decision-making authority. Their role is advisory. Their deliverables do not represent the consensus of the SIG nor of the WG unless the SIG or WG formally adopts them.

### Current task forces

| Name | Focus Area | Lead(s) | Deliverables | Minutes | End date | 
|---|---|---|---|---|---|
| Deliverables Plan Task Force | Define a deliverables plan for the SIG for 2025 | Tobie Langel ([@tobie](https://github.com/tobie)) | Deliverables Plan | [Minutes](./minutes/deliverables-plan-task-force) | 2025-03-03 |
| FAQ Task Force | Collect, answer, and organize questions from the community on the CRA | [@orcwg/faq-task-force-leads](https://github.com/orgs/orcwg/teams/faq-task-force-leads) | [FAQ](https://github.com/orcwg/cra-hub/blob/main/faq.md) | [Minutes](./minutes/faq-task-force) | 2025-06-30 |
| Inventory Task Force | Collect and organize resources relevant to the implementation of the CRA | [@orcwg/inventory-task-force-leads](https://github.com/orgs/orcwg/teams/inventory-task-force-leads) | [Inventory](https://github.com/orcwg/cra-hub/blob/main/inventory.md) | [Minutes](./minutes/inventory-task-force) | 2025-06-30 |

## Why a Cyber Resilience SIG?

ORC WG is chartered to address any regulation impacting open source communities and open source usage. It can establish Special Interest Groups (SIGs) for domain-specific work. 

The initial focus of ORC WG is to help open source communities and the broader tech industry better understand and prepare to meet the compliance requirements of the European Cyber Resilience Act (CRA). However, cyber resilience is a topic that is broader than Europe. And ORC WG aims to facilitate compliance _across jurisdictions_ (and not only in the EU). A SIG focused on cyber resilience in general--not just on the CRA--will help achieve this goal.

As new regulations impacting open source communities emerge, it is expected that additional SIGs modeled on this initial one will be formed.

[@dirkx]: https://github.com/dirkx
[@timop62]: https://github.com/timop62
[@mbarbero]: https://github.com/mbarbero
[@webmink]: https://github.com/webmink

[EFSL]: https://www.eclipse.org/legal/efsl/
[TFs]: #current-task-forces
[Cyber Resilience Practices Project]: #cyber-resilience-practices-project

[Article 13(5)]: https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#art_13
[Article 24(1)]: https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#art_24
[Article 25]: https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#art_25
[Annex I, Part I, point (1)]: https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#anx_I
[Annex I, Part I, point (2)]: https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#anx_I

[FAQ]: #cra-faq
[inventory]: #inventory 
[SBOMs]: #white-paper-on-sboms
[input product categories]: #input-to-the-draft-eu-commission-implementing-regulation-on-the-technical-description-of-important-and-critical-product

[due diligence]: #white-paper-on-due-diligence-obligation-of-manufacturers
[security attestations]: #white-paper-on-security-attestations
[vulnerability management]: #vulnerability-management-specification
[cyber resilience principles]: #specification-on-principles-for-cyber-resilience-for-open-source 
[generic security requirements]:#specification-on-generic-security-requirements-for-open-source-components
[security policy]: #security-policy-for-open-source-software-stewards

[EU Commission]: #key-stakeholders
[CRA Expert Group]: #key-stakeholders
[CEN/CENELEC]: #key-stakeholders
[ETSI]: #key-stakeholders
[ESOs]: #key-stakeholders
[ENISA]: #key-stakeholders
[Market Surveillance]: #key-stakeholders
