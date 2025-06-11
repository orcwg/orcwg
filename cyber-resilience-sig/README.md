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

## Cyber Resilience Practices Project

In its [Deliverables Plan](./deliverables.md), the SIG has identified a [set of specifications](./deliverables.md#4-specifications) that are required to further its mission. The intention is for the Cyber Resilience Practices Project to host these specifications and develop them with guidance from the SIG.

* [Cyber Resilience Practices Project](https://projects.eclipse.org/projects/technology.crp)

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
| Deliverables Plan Task Force | Define a deliverables plan for the SIG for 2025 | Tobie Langel ([@tobie](https://github.com/tobie)) | [Deliverables Plan](./deliverables.md) | [Minutes](./minutes/deliverables-plan-task-force) | 2025-03-03 |
| FAQ Task Force | Collect, answer, and organize questions from the community on the CRA | [@orcwg/faq-task-force-leads](https://github.com/orgs/orcwg/teams/faq-task-force-leads) | [FAQ](https://github.com/orcwg/cra-hub/blob/main/faq.md) | [Minutes](./minutes/faq-task-force) | 2025-06-30 |
| Inventory Task Force | Collect and organize resources relevant to the implementation of the CRA | [@orcwg/inventory-task-force-leads](https://github.com/orgs/orcwg/teams/inventory-task-force-leads) | [Inventory](https://github.com/orcwg/cra-hub/blob/main/inventory.md) | [Minutes](./minutes/inventory-task-force) | 2025-06-30 |
| Vulnerability Handling Task Force | <li>Help coordinate input to [CEN/CENELEC PT 3](#cen-cenelec-wg-9)<li>Provide input to the SIG and Cyber Resilience Practices Project on [deliverables plan](./deliverables.md) and [proposed specs](./deliverables.md#4-specifications) | [@orcwg/vulnerability-handling-task-force-leads](https://github.com/orgs/orcwg/teams/vulnerability-handling-task-force-leads) | Possible white paper on vulnerability handling | [Minutes](./minutes/vulnerability-handling-task-force) | 2025-12-31 |
| Open Source Hardware Task Force | Provide input and comments to [key stakeholders](#key-stakeholder-coordination) on matters pertaining to open source hardware | [@orcwg/open-source-hardware-task-force](https://github.com/orgs/orcwg/teams/open-source-hardware-task-force) | Input and comments | [Minutes](./minutes/open-source-hardware-task-force) | 2027-12-31 |


## Key stakeholder coordination

In its [Deliverables Plan](./deliverables.md), the SIG has identified [key stakeholders](./deliverables.md#key-stakeholders) that it intends to collaborate closely with and provide input to. In order to coordinate this effort, the SIG relies on a [shared calendar][coord calendar] ([iCal format][coord ical]) and representatives from within its members. For their group or subgroups, liaisons leads (identified in the table below) are responsible for:

1. Keeping the [shared calendar][coord calendar] up to date.
2. Making sure important meetings are attended.
3. Collecting publicly shareable meeting notes.
4. Providing updates during SIG calls.
5. Sharing the consensus of the SIG.

Liaisons leads may delegate their responsabilities to other SIG members within their group or subgroup.

### Current liaisons

| Group | Subgroup | Representatives | Meeting notes |
|---|---|---|---|
| <a href="#cra-expert-group" name="cra-expert-group">CRA Expert Group</a> | _(work strands)_ | Dirk-Willem van Gulik, Mikaël Barbero, **Tobie Langel** _(lead)_ | [Notes](./coordination/cra-expert-group/) |
|  | Product categories | Timo Perala, **Tobie Langel** _(lead)_ |  |
|  | Open source | Timo Perala, **Tobie Langel** _(lead)_ |  |
|  | Risk assessment |  |  |
|  | Remote data processing |  |  |
|  | Market surveillance |  |  |
||
| <a href="#cen-cenelec-wg-9" name="cen-cenelec-wg-9">CEN/CENELEC WG 9</a> | _(project teams)_  | **Juan Rico** _(lead)_, Lars Francke, Marta Rybczynska, Mikaël Barbero, Roman Zhukov, Timo Perala, Tobie Langel | [Notes](./coordination/cen-cenelec-wg-9/) |
|  | PT 1 | Lars Francke, Mikaël Barbero, Timo Perala, Tobie Langel |  |
|  | PT 2 | Lars Francke, Mikaël Barbero, Timo Perala, Tobie Langel |  |
|  | PT 3 | Lars Francke, **Marta Rybczynska** _(lead)_, Mikaël Barbero, Roman Zhukov, Timo Perala, Tobie Langel |  |
||
| <a href="#etsi-cyber-eusr" name="etsi-cyber-eusr">ETSI CYBER-EUSR</a> | _(work items)_ | Daniel Thompson-Yvetot, Jordan Maris, Juan Rico, Roman Zhukov, **Simon Phipps** _(lead)_, Timo Perala | [Notes](./coordination/etsi-cyber-eusr/) |
|  | Browsers | **Daniel Thompson-Yvetot** _(lead)_ |  |
|  | Hypervisors | **Roman Zhukov** _(lead)_ |  |
|  | Operating Systems | **Roman Zhukov** _(lead)_ |  |

## Why a Cyber Resilience SIG?

ORC WG is chartered to address any regulation impacting open source communities and open source usage. It can establish Special Interest Groups (SIGs) for domain-specific work. 

The initial focus of ORC WG is to help open source communities and the broader tech industry better understand and prepare to meet the compliance requirements of the European Cyber Resilience Act (CRA). However, cyber resilience is a topic that is broader than Europe. And ORC WG aims to facilitate compliance _across jurisdictions_ (and not only in the EU). A SIG focused on cyber resilience in general--not just on the CRA--will help achieve this goal.

As new regulations impacting open source communities emerge, it is expected that additional SIGs modeled on this initial one will be formed.

[@dirkx]: https://github.com/dirkx
[@timop62]: https://github.com/timop62
[@mbarbero]: https://github.com/mbarbero
[@webmink]: https://github.com/webmink

[coord calendar]: https://calendar.google.com/calendar/embed?src=c_5c658735d0e74ce8caf97a1d06efd2ed01dbfc47ca6abbf6d13c90b48dd9e744%40group.calendar.google.com 
[coord ical]: https://calendar.google.com/calendar/ical/c_5c658735d0e74ce8caf97a1d06efd2ed01dbfc47ca6abbf6d13c90b48dd9e744%40group.calendar.google.com/public/basic.ics
