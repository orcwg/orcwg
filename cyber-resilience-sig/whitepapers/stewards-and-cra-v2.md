---
SIG: Cyber Resilience SIG
Task force:
Document type: White paper
Number: 3.5v2
Status: ✍️ Work in Progress
Input to: EU Guidance, Implementing Act, Harmonised standards
Relevant liaisons: EU Commission, CRA Expert Group, CEN/CENELEC, Market Surveillance
License: CC-BY 4.0
---

# The Open Source Steward Playbook

## From Policy to Practice Under the Cyber Resilience Act

## Version 2.0 — Draft — May 2026

---

> **Disclaimer**: This document does not constitute legal advice. It reflects the current understanding of the CRA held by its
> contributors. It may be updated, replaced, or obsoleted at any time. Publication does not imply endorsement by the Eclipse
> Foundation, the ORC Working Group, or any of its members. An authoritative interpretation of the CRA may only be given by the
> Court of Justice of the European Union.

---

## Executive Summary

This whitepaper addresses the legal category of Open Source Software Stewards ("Stewards") introduced by the European Union's
Cyber Resilience Act (CRA), Regulation (EU) 2024/2847. It serves as an analysis and elaboration of the specific obligations,
restrictions, and penalties imposed on Stewards, who are defined as legal persons (e.g., foundations, companies) distinct from the
Open Source Projects they support and separate from commercial Manufacturers. This role imposes a lighter regulatory burden on
open source actors who do not monetise their software, though many projects currently lack a Steward.

While introduced in the CRA, the concept of stewardship reflects a broader regulatory need across EU digital legislation,
including cybersecurity, AI governance, and certification frameworks, where no equivalent ecosystem-level actor is formally
recognised.

Version 2.0 incorporates clarifications from the European Commission's March 2026 draft guidance on the application of the CRA
(Ares(2026)2319816), including the graduated reporting framework, dual-role determinations, the not-for-profit exemption, and
upstream reporting obligations. The goal of this document is not to provide comprehensive guidance on who qualifies as a Steward
rather than a Manufacturer. The Commission's draft guidance (Section 3\) and the
[ORC WG CRA FAQ](https://cra.orcwg.org/faq/stewards/) address that question in detail.

The core of a Steward's responsibility centres on implementing a verifiable Cybersecurity Policy in cooperation with their
Projects. This policy must aim to: foster the development of secure products; ensure the effective handling of vulnerabilities,
including documentation, addressing, and remediation; promote information sharing within the open source community; and describe
the Project's vulnerability reporting and handling processes, including voluntary reporting to a national CSIRT.

Additionally, Stewards have obligations related to mandatory reporting and regulatory cooperation:

- **Mandatory Reporting (graduated by type of support)**: The Commission's guidance confirms that reporting obligations scale with
  the nature of the Steward's involvement. Stewards providing only non-technical support (governance, branding, finances) are not
  required to report vulnerabilities or incidents, but should share relevant information with maintainers. Stewards providing IT
  infrastructure (repositories, signing keys, CI/CD) must report severe incidents affecting that infrastructure. Stewards involved
  in engineering (employing developers, managing releases, handling vulnerability reports) must additionally report actively
  exploited vulnerabilities. All mandatory reporting is done via the single reporting platform.
- **User Notification**: When an exploited vulnerability or severe incident occurs, Stewards must inform affected users and
  provide necessary mitigation or corrective measures, preferably in a machine-readable format. The Commission's guidance
  clarifies that notification should be risk-based and proportionate.
- **Upstream Reporting**: Stewards may receive vulnerability reports and security fixes from manufacturers who integrate their
  Projects' FOSS under Article 13(6). The cybersecurity policy should include processes for receiving and triaging such upstream
  contributions.
- **Market Surveillance Cooperation**: Stewards are required to cooperate with Market Surveillance Authorities (MSAs) to mitigate
  security risks and provide the required security documentation.

Crucially, the CRA explicitly excludes Stewards from the administrative fines and penalties that apply to Manufacturers for
non-compliance, reflecting the reduced risks and lighter burden intended for this non-monetising role. This document is not legal
guidance but a reflection of the contributors' current understanding of the CRA requirements, outlining practical steps and
resources needed by Stewards and their Projects to fulfil these new legal obligations.

## What's New in Version 2.0

Version 2.0 incorporates clarifications from the **European Commission's draft guidance** on the application of the CRA
(Ares(2026)2319816, published 3 March 2026 for public consultation). Key additions and changes:

- **Steward definition context expanded**: sustained support taxonomy, per-project determination, dual roles, not-for-profit
  exemption ([Definition and Context](#open-source-stewards-definition-and-context))
- **Graduated reporting framework**: three-tier model linking reporting duties to support type: non-technical, IT infrastructure,
  or engineering
  ([Reporting Obligations Scaled by Type of Support](#reporting-obligations-scaled-by-type-of-support))
- **"Becoming aware" threshold**: aligned with NIS 2 and GDPR precedent
  ([Becoming Aware](#becoming-aware-when-do-deadlines-start))
- **Upstream reporting and sharing security fixes**: Article 13(6) obligations and their interaction with the steward role
  ([Upstream Reporting](#upstream-reporting-and-sharing-security-fixes))
- **Contributors and downstream uses**: contributor protection and manufacturer due diligence
  ([Contributors and Downstream Uses](#contributors-and-downstream-uses))
- **Illustrative scenarios expanded**: eight concrete cases covering all three reporting tiers
  ([Illustrative Scenarios](#illustrative-scenarios))
- **Open questions updated**: split into resolved vs. remaining
  ([Open Questions](#open-questions-and-areas-requiring-further-guidance))

## Open Source Stewards: Definition and Context

### Who Is a Steward?

Open Source Software Stewards are defined in the CRA as a **distinct category of legal persons, separate from Manufacturers**.
Article 3(14) defines a steward as:

> a legal person, other than a manufacturer, who has the purpose or objective of systematically providing support on a sustained
> basis for the development of products with digital elements qualifying as free and open-source software that are intended for
> commercial activities, and that ensures the viability of those products.

A Steward must be a **legal person** (i.e. a registered legal entity such as a for-profit or non-profit company, a foundation,
etc.) and should be distinguished from the Open Source Project itself. Natural persons cannot be stewards. The role distinguishes
open source actors who do not monetise the software they produce from Manufacturers who place it on the market in the course of a
commercial activity. It imposes a **lighter regulatory burden** on Stewards and reduces the risks they face in the event of
non-compliance.

Most open source projects today, especially small ones, do not have a steward. The obligations described in this document do not
apply to them. A legal person that merely hosts source code or provides a collaboration platform but does not systematically
support specific FOSS projects or ensure their viability is also not necessarily a steward in respect of those projects.

The CRA introduces this role in light of:

> the importance for cybersecurity of many products with digital elements qualifying as free and open-source software that are
> published, but not made available on the market within the meaning of the \[CRA\]. (Recital 19\)

### Steward vs. Manufacturer: The Boundary

This whitepaper does not provide a comprehensive definition of who qualifies as a Steward rather than a Manufacturer. That
determination depends on whether the FOSS in question is "placed on the market", i.e., supplied in the course of a commercial
activity. The Commission's draft guidance (Section 3.2) provides detailed interpretive context, including:

- **Charging a price** for FOSS makes the supplier a manufacturer.
- **Monetising other services** through the software (e.g., providing a platform for purchasing goods or services, or requiring
  personal data processing beyond security/compatibility purposes) constitutes a commercial activity.
- **Support services** bundled with access to the product and conditioned on remuneration constitute a commercial activity.
  Optional support offered separately from a freely available product does not.
- **Donations** alone do not make FOSS commercial, unless access to the software or its essential functionalities is conditioned
  on making a donation.
- **Financing** of FOSS development by third parties does not determine the commercial nature of the activity.
- **Community vs. paid versions**: Where a manufacturer offers both a paid version and a free "community" version of the same
  FOSS, the paid version is placed on the market (manufacturer obligations), while the free version is not (steward obligations
  for the legal person publishing it, if applicable).

The Commission's guidance also provides a **stylised flowchart** (Figure 1 of the draft guidance) to help determine CRA coverage
of FOSS.

### Dual Roles: Steward for One Project, Manufacturer for Another

The Commission's draft guidance (paragraphs 69–71) confirms that a legal person may simultaneously hold different roles for
different FOSS projects:

- A legal person may be a **steward** for one specific FOSS (where it systematically provides support on a sustained basis and
  ensures the software's viability, but does not place it on the market) and a **manufacturer** for another specific FOSS (where
  it places it on the market in the course of a commercial activity).
- Being a manufacturer for one specific FOSS does not prevent the legal person from being a steward for other FOSS.
- This includes providing "community" versions of the same FOSS alongside monetised versions: the entity is the manufacturer of
  the monetised version and may be the steward of the community version.

For each specific FOSS that it publishes, the legal person must ascertain whether that FOSS is considered to be placed on the
market. If so, the entity is the software's manufacturer. If not, and if the conditions of Article 3(14) are met, the entity may
be the steward.

### Per-Project Determination

The steward determination is **per-project, not per-entity**. The Commission's guidance (paragraph 71\) clarifies:

> For each specific FOSS that it publishes, the legal person will need to ascertain whether that FOSS is considered to be placed
> on the market within the meaning of the CRA.

A legal person may also **not be subject to any obligations** under the CRA for a specific FOSS, in cases where: (i) that FOSS is
not placed on the market; and (ii) the legal entity does not meet the definition of steward in relation to that specific FOSS
(e.g., because it does not provide systematic support or does not ensure its viability).

### Sustained Support and Ensuring Viability

The Commission's draft guidance (paragraphs 72–79) elaborates on what constitutes "sustained support" for the purposes of Article
3(14). Recital 19 indicates that this includes, but is not limited to:

- Hosting and managing software development collaboration platforms
- Hosting source code or software
- Governing or managing products qualifying as FOSS
- Steering the development of such products

The type of sustained support varies significantly across entities. Some provide only **non-technical support** (branding,
governance rules, community events, collecting donations). Others provide **IT infrastructure** (hosting repositories, providing
version control, generating signing keys). Others go further by providing **engineering resources** (employing developers,
coordinating development, reviewing or merging code, managing releases, handling vulnerability reports and security patches).

While all stewards must comply with Article 24(1) and (2), the extent to which Article 14(1), (3), and (8) obligations apply
**varies depending on the type of support provided** (see
[Reporting Obligations Scaled by Type of Support](#reporting-obligations-scaled-by-type-of-support)
for details).

### Not-for-Profit Entities

The Commission's draft guidance (paragraph 63 and Section 3.2.6) clarifies that where a legal person publishing a FOSS is a
**not-for-profit organisation** set up in such a way that ensures that all earnings after costs are used to achieve not-for-profit
objectives, the FOSS it publishes is **not considered to be placed on the market**. This is true even if the FOSS is directly
monetised (e.g., via search engine partnerships), provided the not-for-profit structure ensures earnings after costs serve
not-for-profit purposes.

Where such a not-for-profit entity meets the definition of steward, it is subject to the corresponding obligations under Article
24\.

**Example** (from Commission guidance, Example 18): A legal person publishes a free and open-source browser that is directly
monetised via search engine partnerships, but all its earnings after costs are used for not-for-profit objectives. The browser is
not deemed to be placed on the market. The entity may be the steward.

### Relationship Between Steward and Project

Establishing a formal relationship between a Project and its Steward is something the two parties may need to define themselves. A
Steward organisation may already be performing a supporting role due to ownership of intellectual property, historical reasons, an
explicit agreement entered into by the project leadership, or because the project was originally founded as such.

The concept of "responsibility" for FOSS is linked to who **publishes and exercises primary control** over development, releases,
and distribution decisions (often referred to as "maintainers"). Persons who contribute source code but do not control releases,
roadmaps, or governance decisions are considered "contributors"; in such cases, the FOSS is not under their responsibility, even
though they contributed code to it. The mere existence of technical permissions, such as commit access, is not sufficient to
establish responsibility.

### Becoming and Ceasing to Be a Steward

The CRA does not define a formal mechanism by which a legal person becomes, or ceases to be, a steward for a given FOSS project.
There is no registration, notification, or opt-in procedure. Whether an entity qualifies as a steward is a factual determination
based on whether it meets the criteria of Article 3(14) in relation to a specific FOSS project at a given point in time.

This raises practical questions. If a foundation decides to wind down its support for a project (e.g., due to funding changes or
strategic realignment), at what point do its steward obligations cease? What transitional steps, if any, are expected (for
instance, with respect to ongoing vulnerability handling or cooperation with MSAs)? Conversely, when a legal person begins
providing sustained support for a FOSS project, how should it signal that it accepts the corresponding obligations?

**Open question**: The CRA and the Commission's draft guidance do not address steward lifecycle transitions. Practical guidance on
entry into and exit from the steward role, including any transitional obligations, would benefit both stewards and the projects
they support.

## Cybersecurity Policy Obligations (Article 24(1))

Stewards shall, with the cooperation of their Projects, develop, document, and implement a cybersecurity policy that these
Projects adopt. Article 24(1) states:

> Open-source software stewards shall put in place and document in a verifiable manner a cybersecurity policy to foster the
> development of a secure product with digital elements as well as an effective handling of vulnerabilities by the developers of
> that product. That policy shall also foster the voluntary reporting of vulnerabilities as laid down in Article 15 by the
> developers of that product and take into account the specific nature of the open-source software steward and the legal and
> organisational arrangements to which it is subject. That policy shall, in particular, include aspects related to documenting,
> addressing and remediating vulnerabilities and promote the sharing of information concerning discovered vulnerabilities within
> the open-source community.

### Required Elements

The cybersecurity policy must:

1. **Foster the development of secure products with digital elements**, encourage secure-by-design and secure-by-default
   principles in the project's development practices.
1. **Foster the effective handling of vulnerabilities** by the developers of the product, including documentation, addressing, and
   remediation of vulnerabilities, as well as sharing of information on discovered vulnerabilities within the open source
   community.
1. **Foster the voluntary reporting of vulnerabilities** as laid down in Article 15 by the developers of the product, including
   policies for voluntary reporting to, and coordination with, a national CSIRT.
1. **Take into account the specific nature** of the open source software steward and the legal and organisational arrangements to
   which it is subject.

The Steward may maintain the policy in paper or electronic form, but it must be **"verifiable"**. As the relationships between
Stewards and their Projects vary, the Policy should take into account their shared modes of operation. Market Surveillance
Authorities may request access to this Security Policy.

**Note on "fostering"**: The legal text's "fostering" language means enabling and supporting, rather than enforcing, and may apply
to the FOSS project's own development, to the integration of the FOSS project into Products by Manufacturers, or to both. This
question is tracked in a dedicated [ORC WG FAQ entry](https://cra.orcwg.org/faq/stewards/).

### Fostering Secure Development

The clause requiring the policy to "foster the development of a secure product with digital elements" lacks further detailed
clarification in the CRA text itself. However, a reasonable interpretation includes:

- Promoting methodologies for risk assessment during development
- Encouraging secure-by-design and secure-by-default principles
- Recommending a secure software development lifecycle (SDLC)
- Providing guidance on dependency management and supply chain security

This section may require updates as the concept is further clarified through delegated acts, harmonised standards, or additional
Commission guidance.

### Effective Vulnerability Handling

Effective vulnerability handling should form part of the overall security policy and include processes for:

**(a) Documenting vulnerabilities**, understood as documenting fixed or mitigated vulnerabilities once public, using techniques
such as CVE/EUVD entries or security advisories in textual and/or machine-readable formats, made available in a location easy for
users to find (e.g., via a link in `SECURITY.md`).

**(b) Addressing vulnerabilities**, establishing processes for receiving, triaging, and prioritising vulnerability reports,
including from internal and external sources.

**(c) Remediating vulnerabilities**, developing and distributing fixes, patches, or workarounds in a timely manner.

### Promoting Information Sharing

The policy must promote the sharing of information concerning discovered vulnerabilities within the open source community. This
includes:

- Publishing security advisories in human-readable and, where feasible, machine-readable formats
- Contributing to public vulnerability databases (CVE, EUVD)
- Sharing vulnerability information with downstream users and integrators
- Coordinating with other projects that share common dependencies

### Steward–Project Policy Relationship Examples

In open source projects, Security Policies are typically public, fulfilling the publication requirement. They are usually
published on the Project site and/or included in the source code repository. The relationship between the Steward's policy and
each Project's implementation may take various forms:

**Scenario 1 — Steward-provided template**: The supporting organisation provides a template, and Projects publish their own
policies based on that template. The number of changes to the template may be significant, depending on the Project's specific
practices.

**Scenario 2 — Project-originated policy, adapted by Steward**: The Project has a long-established public policy, which is adapted
by the Steward to serve as its policy in CRA terms.

**Scenario 3 — Pre-existing compliant policy**: The Project already has an established policy that meets CRA requirements and
therefore continues to use it. However, this policy may differ substantially from the Steward's default policy.

In all cases, both the Steward and the Project must verify that the Policy includes all required elements and that it is
effectively followed. If the Project does not follow the policy, the Steward needs to define an action plan. For example,
accepting a generic Policy from a Foundation acting as Steward may be a prerequisite for creating a Project or for that Project to
be admitted to the foundation.

The Project and the Steward also need to agree on how changes to the Policy are introduced, to align legal requirements with
current practices (e.g., bug tracking tools, communication methods).

### Suggested Resources

To assist stewards in implementing these obligations, the following deliverables are recommended or under development:

- A **specification and/or template for the Policy**, illustrating what it means for a policy to foster the development of secure
  products with digital elements — including methodologies for risk assessment, secure-by-design and secure-by-default principles,
  a secure SDLC, effective vulnerability handling, and a description of the coordinated vulnerability disclosure (CVD) process.
- **SECURITY.md templates** including identification of the relevant CSIRT and MSA.
- **Machine-readable security advisory formats** for use in vulnerability documentation.
- The ORC WG **Vulnerability Management Specification** (see `orcwg/vulnerability-management-spec`).

## CE Marking and Documentation

Stewards **cannot affix the CE marking** to the products they publish. As stated in Recital 19:

> Given that the light-touch and tailor-made regulatory regime does not subject those acting as open-source software stewards to
> the same obligations as those acting as manufacturers under this Regulation, they should not be permitted to affix the CE
> marking to the products with digital elements whose development they support.

Stewards do not provide the full set of CRA documentation (technical documentation, EU declaration of conformity) for their
Projects. However, Stewards may operate an **attestation programme** that provides documentation for use by Manufacturers who
integrate the steward's FOSS into their products. Such attestation programmes may support Manufacturers in fulfilling their due
diligence obligations under Article 13(5)., and may be further specified in a Delegated Act as outlined in Article 25\.

## Voluntary Security Attestations as an Operational Model for Stewardship

### Rationale and Objective

The Cyber Resilience Act introduces the role of the open source software steward as a distinct actor supporting the security and
long-term viability of free and open source software. Article 24 requires stewards to put in place and document a verifiable
cybersecurity policy, to foster secure development, effective vulnerability handling, voluntary reporting, and information sharing
within the open source community.

However, the CRA does not itself define an operational mechanism by which the outcomes of stewardship activities are made reusable
by downstream manufacturers, integrators, market surveillance authorities, or certification bodies.

This creates a structural gap:

- Stewards may perform security-relevant functions.
- Manufacturers must exercise due diligence when integrating third-party components, including FOSS components.
- Market actors need evidence that is reusable, understandable, and proportionate.
- Open source projects should not be burdened with duplicative questionnaires, incompatible assurance requests, or de facto
  private compliance regimes.

Voluntary Security Attestations can help bridge this gap. They translate stewardship practices into structured assurance artefacts
that manufacturers and other downstream actors can reuse, while preserving the open and collaborative nature of the underlying
software.

Article 25 of the CRA provides the most direct legal basis for this concept. It empowers the Commission to establish voluntary
security attestation programmes for FOSS, in order to facilitate manufacturers’ due diligence obligations under Article 13(5).
Until such programmes are formally established through delegated acts, community-developed attestation models should be understood
as preparatory, voluntary, and non-exclusive assurance mechanisms.

The ORC WG **CRA Attestations** specification (see `orcwg/cra-attestations`) is developing a framework for this purpose. This
chapter is an overview of the current state of this work.

### Definition

For the purposes of this document, a Voluntary Security Attestation is:

**A scoped, dated, verifiable, and reusable statement describing the security posture, governance, processes, and supporting
evidence associated with a free and open source software project.**

In the stewardship context, such an attestation may be issued or maintained by:

- The steward of the project
- The project itself, where appropriate
- A third party, such as a manufacturer, researcher, auditor, or ecosystem body
- A combination of these actors, depending on the eventual attestation model

An attestation should identify who makes the statement, what project or release it covers, what claims are being made, what
evidence supports those claims, and what limitations apply.

Attestations are not equivalent to:

- CE marking
- CRA conformity assessment
- Certification under the Cybersecurity Act
- A legal guarantee of security
- A transfer of manufacturer responsibility to the steward
- A warranty that the software is free from vulnerabilities

Instead, attestations serve as:

- Transparency mechanisms for open source security practices
- Evidence packages for manufacturer due diligence
- A bridge between community-based development and regulatory compliance
- A possible operational and funding model for stewardship activities
- A way to reduce duplicative compliance requests across the ecosystem

### Relationship to Steward Obligations

Voluntary Security Attestations should be understood as an evidence layer built on top of stewardship practices, not as a
replacement for those practices.

The primary obligation of a steward remains the Article 24 cybersecurity policy. That policy should describe how the steward and
project foster secure development, vulnerability handling, voluntary reporting, and information sharing. An attestation can then
summarise, structure, and evidence how those practices are applied to a specific project, release stream, support period, or time
interval.

In practical terms:

- The **cybersecurity policy** describes the intended process.
- The **project implementation** shows how the process is applied.
- The **attestation** packages selected claims and evidence for reuse.
- The **manufacturer** remains responsible for assessing whether the component is suitable for integration into its product.

Attestations may also support cooperation with Market Surveillance Authorities by making relevant documentation easier to locate,
interpret, and verify.

### Core Characteristics

To be effective, attestations should exhibit the following properties.

#### Clear Scope

An attestation should state precisely what it covers. This may include:

- The project name and repository
- The steward or issuing entity
- The relevant release, version range, branch, or support period
- The date of issuance
- The period of validity or review cadence
- Any excluded components, forks, plugins, optional modules, or deployment configurations

This is particularly important because open source projects may be used in many contexts that the steward does not control.

#### Verifiability

Attestations should be based on documented processes and supporting evidence. Evidence may include:

- Published cybersecurity policies
- `SECURITY.md` files
- Coordinated vulnerability disclosure processes
- Security advisories
- CVE or EUVD records
- Release notes
- SBOMs or dependency files
- Signed releases
- Access control and release management procedures
- Public governance documents
- Build provenance or reproducible build information, where available

Where possible, evidence should be referenced by stable URLs, content hashes, cryptographic signatures, or other means that allow
later verification.

#### Standardisation

Attestations should follow a common structure and vocabulary. Standardisation is necessary to avoid replacing one compliance
burden with many inconsistent forms.

A useful attestation model should define:

- Common claim categories
- Evidence expectations
- Versioning rules
- Revocation or supersession rules
- Machine-readable fields
- Human-readable explanations
- A vocabulary for limitations and exclusions

#### Machine-Readability

Where feasible, attestations should be available in machine-readable form, with a human-readable rendering for project communities
and downstream users.

Machine-readability would support integration with:

- SBOM formats
- Vulnerability databases
- Advisory formats
- Dependency analysis tools
- Compliance management systems
- Procurement and risk review workflows
- Package registries and repository metadata

The attestation should be capable of being signed, referenced, and redistributed without losing its integrity.

#### Proportionality

The level of detail and assurance should reflect:

- The type of support provided by the steward
- The project’s role in downstream products
- The project’s criticality and deployment scale
- The complexity of the software
- The maturity of the project’s security practices
- Whether the project is mainly used as a component or as a product-like system

A small library should not be expected to produce the same evidence package as a large operating system, language runtime,
database, or platform.

#### Non-Exclusivity

Attestations should not restrict the open nature of the software or create barriers to participation.

They should not:

- Make access to the software conditional on payment
- Prevent unaffiliated use, modification, or redistribution
- Create a private permission layer over open source licensing
- Penalise projects that do not participate
- Require maintainers to assume manufacturer-like obligations

Attestations should complement open source practices rather than replace them.

#### Lifecycle Management

An attestation should not be treated as a static document. It should include processes for:

- Periodic review
- Updating after material changes
- Superseding earlier attestations
- Withdrawing inaccurate attestations
- Correcting errors
- Handling disputed third-party attestations
- Communicating changes to downstream users

### Suggested Content of Attestations

A Voluntary Security Attestation may include the following elements.

#### Identification and Scope

- Name of the project
- Name of the steward or issuing entity
- Project repository, website, and release locations
- Covered versions, branches, or release streams
- Date of issuance
- Review or expiry date
- Attestation profile or assurance level
- Contact point for questions, corrections, or vulnerability reports

#### Steward Role and Support Model

- Identification of the steward and its legal role
- Description of the steward’s support model
- Classification of the steward’s involvement, for example:
  - Non-technical support
  - IT infrastructure support
  - Engineering involvement

- Description of relevant project governance arrangements
- Relationship between steward-level policies and project-level implementation

This helps downstream users understand what the steward can reasonably know, influence, and evidence.

#### Cybersecurity Policy Alignment

- Reference to the Article 24 cybersecurity policy
- Explanation of how the policy is adopted by the project
- Description of how policy changes are proposed, reviewed, and implemented
- Evidence that the policy is publicly available or available to competent authorities upon request
- Description of how the policy fosters secure development, vulnerability handling, voluntary reporting, and information sharing

#### Vulnerability Management Practices

- Security contact and reporting channel
- Coordinated vulnerability disclosure process
- Triage and prioritisation practices
- Treatment of low-quality, abusive, or automated reports
- Remediation and patch development process
- Publication of security advisories
- Use of CVE, EUVD, or other vulnerability identifiers where applicable
- Handling of embargoes and coordinated disclosure timelines
- Processes for receiving reports and fixes from downstream manufacturers

#### Reporting and Coordination

- Processes for determining whether an issue is voluntarily reportable under Article 15
- Processes for determining whether mandatory reporting obligations are triggered, where applicable
- Identification of internal or project-level roles responsible for reporting workflows
- Interaction with CSIRTs, ENISA, and Market Surveillance Authorities where applicable
- User notification practices for vulnerabilities and severe incidents
- Relationship between public advisories, private notifications, and risk-based disclosure

#### Release and Maintenance Practices

- Versioning model
- Release approval process
- Supported branches or release streams
- Security update practices
- Patch management process
- End-of-support communication
- Signing of releases, tags, or artefacts where applicable
- Protection of release infrastructure and credentials
- Changelog or release note practices for security fixes

#### Supply Chain Transparency

- Availability of SBOMs or equivalent dependency information
- Dependency update practices
- Handling of third-party components
- Treatment of optional, bundled, generated, or vendored dependencies
- Identification of known unmaintained or unstewarded dependencies, where feasible
- Processes for dependency vulnerability monitoring
- Build and provenance information, where available

This section should be careful not to imply that a steward is responsible for all transitive dependencies outside its control. The
attestation should distinguish between what the steward controls, what it monitors, and what it merely reports.

#### Security Engineering Practices

Depending on proportionality, an attestation may describe:

- Code review practices
- Test practices
- Security testing or fuzzing
- Static or dynamic analysis
- Dependency scanning
- Access control for repositories and release infrastructure
- Use of branch protection or equivalent controls
- Handling of secrets and credentials
- Build system security
- Maintainer onboarding and offboarding practices

#### Evidence and Verification

For each material claim, the attestation should identify supporting evidence.

Examples include:

- Public policy documents
- Repository configuration
- Security advisory records
- Release artefacts
- SBOM files
- Signed tags or provenance metadata
- Public issue or advisory workflows
- Governance documents
- Maintainer documentation
- Links to relevant project infrastructure

A mature attestation format should separate claims from evidence so that downstream tools can evaluate, reuse, or update the
evidence without rewriting the entire attestation.

#### Limitations and Disclaimers

Each attestation should clearly state its limitations, including:

- It is not a guarantee that the software contains no vulnerabilities.
- It is not a certification or CE marking.
- It does not replace manufacturer due diligence.
- It does not transfer regulatory responsibility from manufacturers to stewards.
- It covers only the stated scope, versions, and time period.
- It may not cover downstream modifications, integrations, forks, or deployment configurations.
- It may not cover dependencies outside the steward’s control.

These limitations are essential to preserve proportionality and avoid creating unrealistic expectations for open source projects.

### Attestation Profiles

A practical attestation model should support multiple profiles, reflecting the diversity of open source projects.

#### Lightweight Attestation

A lightweight attestation may be appropriate for projects that are primarily used as components, libraries, utilities, or
dependencies within larger products.

It could cover:

- Basic project identity and governance
- Security contact information
- Vulnerability reporting process
- Supported release branches
- Basic release practices
- Dependency information
- Availability of advisories
- Basic evidence that security processes exist and are maintained

This profile should be low-cost, largely self-service, and capable of being completed by well-maintained projects without imposing
a heavy compliance burden.

#### Enhanced or Heavyweight Attestation

An enhanced attestation may be appropriate for larger, more critical, or more product-like projects, including platforms,
operating systems, language ecosystems, databases, browsers, runtimes, or projects with substantial downstream commercial use.

It could include:

- Deeper evidence review
- More structured governance documentation
- Stronger supply chain transparency
- More detailed release and support commitments
- Independent review or third-party validation, where appropriate
- Formalised update and withdrawal processes
- More extensive mapping to CRA essential cybersecurity requirements

This profile is likely to require sustained funding, dedicated tooling, and operational support. It should therefore be treated as
an optional higher-assurance model, not as the default expectation for all open source projects.

### Operational Lifecycle

A steward-operated attestation process may follow the lifecycle below.

#### 1\. Scope the Attestation

The steward identifies the project, release stream, support period, and practices covered by the attestation. It also identifies
exclusions, such as unsupported branches, downstream modifications, optional plugins, or dependencies outside its control.

#### 2\. Map Claims to Practices

The steward maps the relevant claims to existing project practices, including the cybersecurity policy, vulnerability handling
process, release practices, and supply chain transparency measures.

#### 3\. Collect Evidence

The steward gathers references to evidence, preferring public, stable, and machine-verifiable artefacts where possible.

#### 4\. Issue the Attestation

The steward publishes the attestation in both human-readable and, where feasible, machine-readable form. The attestation should be
signed or otherwise protected against tampering.

#### 5\. Publish and Distribute

The attestation may be published:

- In the project repository
- On the project or steward website
- Alongside release artefacts
- In package registry metadata
- In SBOM or advisory ecosystems
- Through a dedicated attestation registry, if one emerges

#### 6\. Review and Update

The attestation should be reviewed periodically and updated after material changes, such as:

- Changes in stewardship model
- Changes in security policy
- New release or support policy
- Major infrastructure changes
- Significant vulnerability handling events
- Changes in dependency management practices
- Discovery that a prior claim was inaccurate

#### 7\. Supersede or Withdraw

Where an attestation becomes outdated, inaccurate, or misleading, it should be superseded or withdrawn. The withdrawal process
should preserve transparency while avoiding unnecessary security risk, especially where disclosure could affect unresolved
vulnerabilities.

### Role in the Regulatory Ecosystem

Voluntary Security Attestations may support several regulatory and operational objectives.

#### Under the CRA

Attestations may:

- Support manufacturers’ Article 13(5) due diligence
- Operationalise the Article 25 concept of voluntary security attestation programmes
- Provide structured evidence of Article 24 stewardship practices
- Assist stewards in responding to Market Surveillance Authority requests
- Reduce duplicative due-diligence questionnaires from multiple manufacturers
- Clarify what a steward does and does not control

They do not replace manufacturer obligations, conformity assessment, technical documentation, or CE marking.

#### Under the Cybersecurity Act

Attestations may serve as reusable inputs to cybersecurity certification schemes or conformity assessment processes where open
source components are part of a larger product or service.

They should not be presented as certification unless they are formally recognised within an applicable certification scheme.

#### Under NIS2

Attestations may support coordinated vulnerability disclosure, incident awareness, and information sharing by documenting:

- Security contact points
- Vulnerability handling processes
- Advisory publication practices
- Coordination channels
- Reporting and escalation pathways

They do not determine whether an entity is subject to NIS2 or replace incident reporting obligations under NIS2.

#### In the Context of the AI Act

Where open source components are used in AI systems or AI-related infrastructure, attestations may provide useful transparency on
software governance, vulnerability handling, dependency management, and release practices.

They should not be treated as AI Act compliance artefacts unless the relevant AI Act obligations and guidance expressly support
that use.

### Attestations and the Steward Business Model

Attestations may also support a sustainable and proportionate operational model for stewardship.

Rather than monetising access to the software itself, stewards may provide value through:

- Development and maintenance of assurance frameworks
- Issuance, maintenance, and updating of attestations
- Security policy tooling
- Vulnerability handling infrastructure
- Advisory publication infrastructure
- SBOM and dependency tooling
- Release integrity and signing infrastructure
- Coordination services for manufacturers and downstream users

This model may help fund the security work that manufacturers depend on, without changing the open source licence or restricting
access to the software.

However, safeguards are necessary. Attestation-based funding should not create a de facto paywall around open source software,
exclude unfunded projects from normal participation, or impose manufacturer-like obligations on maintainers who have not accepted
them. Where revenue is generated from attestation services, stewards should consider how it supports the project, its
infrastructure, and where feasible, the security of important dependencies.

### Limitations and Safeguards

To remain compatible with open source principles and the CRA’s proportional approach, attestation models should observe the
following safeguards.

#### No Substitution of Regulatory Responsibility

Manufacturers remain responsible for compliance with their own CRA obligations. An attestation may support due diligence, but it
cannot perform due diligence on behalf of the manufacturer in every product-specific context.

#### No Liability Transfer

Attestations should not be interpreted as guarantees, warranties, certifications, or assumptions of downstream liability by the
steward or project.

#### Transparency Over Formalism

The goal should be meaningful security transparency, not paperwork. A short, accurate, evidence-backed attestation is preferable
to a long document that creates an appearance of assurance without reflecting actual practices.

#### Protection of Open Source Participation

Attestation programmes should avoid creating barriers for smaller projects, volunteer maintainers, individual contributors, or
projects without formal stewards.

#### Careful Treatment of Third-Party Attestations

If third parties are allowed to issue attestations about a project, there should be processes for:

- Identifying the issuer
- Distinguishing third-party claims from steward or project claims
- Correcting inaccurate statements
- Handling disputes
- Preventing misleading commercial uses
- Avoiding market-distorting behaviour

#### Responsible Disclosure

Attestations should not require disclosure of sensitive security information that would increase risk. Evidence models should
allow confidential or delayed disclosure where justified.

### Towards Standardisation and Adoption

Further work is needed to make Voluntary Security Attestations operational at scale.

Priorities include:

- Common specifications and schemas
- A shared vocabulary of claims, evidence, exclusions, and assurance levels
- Integration with SBOM formats and vulnerability advisory formats
- Mechanisms for signing, verifying, superseding, and withdrawing attestations
- Guidance on dependency handling, including transitive and unstewarded dependencies
- Alignment with vulnerability databases, including CVE and EUVD
- Clarification of how attestations may interact with future CRA delegated acts under Article 25
- Exploration of whether and how attestations may be reused in Cybersecurity Act certification schemes
- Development of lightweight and enhanced profiles suitable for different project types
- Processes for third-party attestations and dispute handling
- Funding models that support projects without undermining openness

### Conclusion

Voluntary Security Attestations provide a practical mechanism to operationalise stewardship. They translate open source security
practices into structured, reusable, and verifiable assurance artefacts.

Used carefully, attestations can help manufacturers perform due diligence, help stewards demonstrate their practices, help
authorities understand project security posture, and help open source communities attract support for security work.

Their value depends on proportionality. Attestations should reflect actual practices, avoid transferring regulatory
responsibility, and preserve the openness, scalability, and collaborative nature of free and open source software.

## Cooperation with Market Surveillance Authorities (Article 24(2))

Article 24(2) states:

> Open-source software stewards shall cooperate with the market surveillance authorities, at their request, with a view to
> mitigating the cybersecurity risks posed by a product with digital elements qualifying as free and open-source software.
> Further to a reasoned request from a market surveillance authority, open-source software stewards shall provide that authority,
> in a language which can be easily understood by that authority, with the documentation referred to in paragraph 1, in paper or
> electronic form.

It should be noted that without harmonised expectations on language and jurisdiction, cooperation obligations may impose
disproportionate burdens on globally distributed open source stewards.

### Documentation Requirements

When Market Surveillance Authorities (MSAs) request assistance from a Steward, the Steward shall cooperate with the aim of
mitigating the security risks posed by the Project. The MSA may request:

- A copy of the Security Policy
- Documentation demonstrating the Policy has been applied (e.g., published security advisories, voluntary security attestations,
  or evidence of an ongoing CVD process)

Public publication of the policy (e.g., on the Project website or in the source code repository) fulfils the publication
requirement. However, the regulation requires the policy be provided "in a language which can be easily understood by that
authority," which may imply translation. As most Projects publish policies in English, it would be beneficial if authorities
accepted English. The Commission's draft guidance does not resolve whether English is sufficient in practice. For stewards based
outside the EU, who may have no prior relationship with a specific Member State's MSA, the cost and logistics of maintaining
policy documents in multiple EU languages represent a concrete compliance risk. Until further guidance clarifies the language
expectations, stewards should consider whether their policies and key documentation are available in at least English and, where
feasible, in the language(s) of the Member State(s) most relevant to their projects' user base.

**Recommended practice**: Identify the relevant Market Surveillance Authority for the Project and the Steward, potentially in the
Project's `SECURITY.md`.

### Corrective Actions (Article 52(3))

Article 52(3) states:

> Where a market surveillance authority finds that an open-source software steward does not comply with the obligations set out
> in that Article, it shall require the open-source software steward to ensure that all appropriate corrective actions are taken.

Non-compliance likely means not having a Policy and/or not promoting best practices as required by Article 24(1). The Steward must
have a means to influence the Project.

Possible situations triggering corrective actions include a Project not responding to vulnerability reports or not documenting
fixed vulnerabilities. Note that disagreements between reporters and developers on whether an issue constitutes a vulnerability
are common, as are **AI-generated low-quality reports** (a serious and growing issue requiring developer time). It is therefore
reasonable for the Policy to include a process for handling abusive or low-quality reports.\[^1\]

\[^1\]: Low quality reports are caused, amongst other factors, by the potential reward (e.g., a CVE number or a bounty, which open
        source projects typically do not offer). It is therefore reasonable for the Policy to include a process for handling
        abusive reports.

### Identifying the Relevant MSA

The CRA does not explicitly address how to determine the relevant MSA for a Steward, particularly where the Steward is based
outside the EU. Rules for the identification of the competent MSA are provided in Regulation (EU) 2019/1020 and are expected to be
further elaborated through guidance.

**Open question**: Guidance is needed on determining the appropriate MSA for Stewards based outside the EU and on resolving
language barriers between Projects/Stewards and MSAs.

## Mandatory Reporting Obligations (Articles 14 and 24(3))

Article 24(3) states:

> The obligations laid down in Article 14(1) shall apply to open-source software stewards to the extent that they are involved in
> the development of the products with digital elements. The obligations laid down in Article 14(3) and (8) shall apply to
> open-source software stewards to the extent that severe incidents having an impact on the security of products with digital
> elements affect network and information systems provided by the open-source software stewards for the development of such
> products.

### Reporting Obligations Scaled by Type of Support

The Commission's draft guidance (paragraphs 76–79) confirms that steward reporting obligations are **more limited in scope than
manufacturers'** and are **graduated based on the type of support the steward provides**. This creates a three-tier framework:

**Tier 1 — Non-technical support only** (e.g., branding, governance, community events, collecting donations):

- The steward is, by definition, not involved in the product's development.
- **Not required** to report actively exploited vulnerabilities under Article 14(1).
- **Not required** to report severe incidents under Article 14(3), as it does not provide network and information systems for the
  development of such products.
- However, where the steward becomes aware of an actively exploited vulnerability (e.g., from external sources), it **should**
  share the information with the product's maintainers in accordance with its cybersecurity policy.
- The steward **should consider** voluntary reporting in accordance with Article 15\.

**Tier 2 — IT infrastructure support** (e.g., hosting repositories, providing version control, generating signing keys):

- **Required** to notify ENISA and CSIRTs under Article 14(3) of severe incidents that have an impact on the security of products.
- **Required**, where appropriate, to inform all users (e.g., via a general announcement).
- **Not required** to report actively exploited vulnerabilities under Article 14(1), unless the steward is also involved in
  development.
- **Should** foster the correct handling of vulnerabilities and consider voluntary reporting.

**Tier 3 — Engineering resources** (e.g., employing developers, coordinating development, reviewing/merging code, managing
releases, handling vulnerability reports):

- **Required** to notify under Article 14(1) of actively exploited vulnerabilities it becomes aware of.
- **Required**, where appropriate, to inform all users.
- Where the steward also has a direct relationship with impacted users, **required** to inform them directly under Article 14(8).

**Per-project, not per-entity assessment**: A single steward may fall into different tiers for different projects in its
portfolio. For example, a foundation may provide only governance and branding for one project (Tier 1), host the source code
repository for another (Tier 2), and employ core developers for a third (Tier 3). The Commission's guidance (paragraphs 76–79)
confirms that the applicable obligations are determined per product, based on the type of support the steward provides to that
specific project. A steward's obligations for a Tier 1 project do not escalate merely because it also acts at Tier 3 for a
different project. Stewards supporting multiple projects should therefore document and assess their role, and the corresponding
obligations, for each project individually.

### Actively Exploited Vulnerabilities

Stewards must report actively exploited vulnerabilities only if they are **involved in the development** of the product (Tier 3
above). If the Steward handles only non-development elements (e.g., finances), and the Project takes development decisions
independently, the Steward is not required to report. This matches the typical foundation–project relationship.

In such situations, the Steward has no practical means of becoming aware of an exploited vulnerability unless informed by the
Project. If information comes from external sources and the Steward is not involved in development, it has no legal obligation to
report, but should pass the information to the Project.

Conversely, if the Steward is involved in development and operations, its staff are likely to handle vulnerability reports and
must report exploited vulnerabilities.

### Severe Incidents

The Steward must report severe incidents affecting the **network and information systems it provides** for its hosted Projects
(Tier 2 and Tier 3 above). Examples of qualifying incidents include:

- Intrusions into IT infrastructure leading to unauthorised modification of the version control system (VCS)
- Account takeovers of project maintainers on steward-provided infrastructure
- Leakage of code-signing keys managed by the steward
- Prolonged infrastructure unavailability making development impossible

Stewards that do not manage IT infrastructure for their projects (Tier 1\) are not required to report such incidents.

### Reporting Timelines

When reporting obligations are triggered, stewards must follow the same timelines as manufacturers. The CRA does not provide
differentiated deadlines for stewards; the rationale is that timely notification is equally important regardless of the reporting
entity's role. The graduated nature of steward obligations is reflected in *which* events must be reported (see
[Reporting Obligations Scaled by Type of Support](#reporting-obligations-scaled-by-type-of-support)),
not in the speed of reporting.

- **Early warning notification**: Without undue delay and in any event within **24 hours** of becoming aware.
- **72-hour notification**: Additional information without undue delay and within **72 hours** of becoming aware.
- **Final report**: Within **14 days** after a corrective or mitigating measure is available (for actively exploited
  vulnerabilities), or within **one month** after the 72-hour notification (for severe incidents).

### Notification to Users (Article 14(8))

After becoming aware of an actively exploited vulnerability or severe incident, the Steward must **inform impacted users** of the
vulnerability or incident and any risk mitigation or corrective measures.

Practical means of notifying users include:

- Updating the relevant CVE entry (and, when available, the EUVD entry)
- Publishing a security advisory in human-readable format on the project site
- General announcements via project communication channels

The Commission's guidance (paragraphs 199–200) clarifies that notification should be **risk-based and proportionate**. For
products used in sensitive environments, public disclosure of technical details could itself increase cybersecurity risks.
Manufacturers and stewards may limit initial disclosure to affected users, with broader disclosure once the vulnerability has been
adequately addressed.

If a Steward does not notify users within a reasonable timeframe, the **CSIRT may do so** where it considers this proportionate
and necessary.

### Becoming Aware: When Do Deadlines Start?

The Commission's draft guidance (paragraphs 193–196) clarifies when a steward (or manufacturer) is deemed to have "become aware"
of an actively exploited vulnerability or severe incident, aligning the CRA's concept with NIS 2 (Implementing Regulation (EU)
2024/2690) and GDPR breach notification guidance:

- Where a suspicious event is detected, the steward should assess it **immediately** to determine whether it constitutes an
  actively exploited vulnerability or a severe incident.
- The steward is regarded as having become aware when, after initial assessment, it has a **reasonable degree of certainty** that
  a vulnerability is being actively exploited or that a severe incident has occurred and compromised the security of a product.
- In some cases this will be relatively clear from the outset. In others, it may take some time. However, the emphasis should be
  on **prompt action** to carry out the initial assessment, particularly where the vulnerability may pose a significant risk.

### Process Requirements

Stewards should define:

- Who within the Steward and/or Project is responsible for submitting notifications via the single reporting platform
- How credentials for the reporting platform are handled
- How information flows between the Project's developers and the Steward's reporting personnel

These may be documented in the Security Policy or a separate implementation document.

## Voluntary Reporting (Article 15\)

Article 15 provides that manufacturers, and other natural or legal persons, may voluntarily report to a CSIRT designated as
coordinator or to ENISA:

- Any vulnerability contained in the product (not only actively exploited ones)
- Cyber threats that could lead to a significant cybersecurity risk
- Any incident having an impact on the security of the product
- **Near misses**, situations where exploitation or an incident was possible but avoided

Stewards may both submit voluntary reports and receive reports from CSIRTs/ENISA that originated from voluntary reporting.

Critically, Article 15(5) provides that **voluntary reporting shall not result in the imposition of any additional obligations
upon the natural or legal person to which it would not have been subject had it not submitted that notification**.

This protection is important for encouraging a culture of transparency within the open source ecosystem without fear of escalating
regulatory consequences.

## CSIRT Designation and Coordination

### Determining the Relevant CSIRT

The regulation requires stewards to report to the **CSIRT designated as coordinator**. The relevant CSIRT is that of the Member
State where (in priority order):

1. The Steward has its **main establishment**, the place where decisions on product cybersecurity are predominantly taken
1. If no EU establishment, the Steward's **authorised representative** is established
1. Where a specific Project has a **strong user base** in another Member State, that Member State's CSIRT may also be relevant

### Multiple Projects Under One Steward

As the legislation appears to assume a **single CSIRT per steward**, multiple Projects under the same Steward must share the
determination. It is good practice to explicitly name the designated CSIRT in each Project's standard security documentation
(e.g., `SECURITY.md`).

Given the global nature of open source usage, different CSIRTs will likely receive reports about the same Project, and rules for
routing reports will be necessary.

### ENISA's Role

ENISA may play multiple roles in the steward reporting framework:

- As a **"CSIRT of last resort"** for stewards without a clear national alignment in the EU
- As a **coordinator** when multiple CSIRTs receive reports about the same project
- As the operator of the **single reporting platform** used for notifications
- As the maintainer of the **European vulnerability database (EUVD)** established under NIS 2

The NIS 2 Directive (Article 12(1)) also establishes requirements for coordinated vulnerability disclosure, including the
possibility of **anonymous reporting**.

## Upstream Reporting and Sharing Security Fixes

While Article 13(6) is formally an obligation on **manufacturers**, it has important implications for stewards and the broader
open source ecosystem. The Commission's draft guidance (Section 9.2.1) provides detailed interpretation.

### Scope of Upstream Reporting

Manufacturers who integrate FOSS components into their products are required to report vulnerabilities in those components to the
person or entity maintaining them ("reporting upstream"). Key clarifications from the Commission's guidance:

- Manufacturers must report upstream only the **version of the component they integrate**.
- Manufacturers must report only vulnerabilities that exist **in the integrated component itself**, not vulnerabilities that arise
  solely from the interaction between the component and the manufacturer's own code.
- However, where integration reveals security-relevant characteristics of the component not apparent in isolation, manufacturers
  are **encouraged** to communicate this information to the maintainer.

For stewards, this means they may **receive** upstream vulnerability reports from manufacturers integrating their projects' FOSS.
The steward's cybersecurity policy should include processes for receiving and triaging such reports.

### Sharing Security Fixes

Manufacturers who develop a software modification to address a vulnerability in an integrated component must **share that fix**
with the component's maintainer. The Commission's guidance clarifies:

- The fix should be shared in a **machine-readable format** (e.g., via a merge request).
- Where the component is FOSS, the fix should be shared in a manner **compatible with the component's licence**.
- Where the maintainer has **guidelines** on how security fixes should be shared, the manufacturer should follow those guidelines.
- Manufacturers are **not required** to ensure their fixes are accepted by the maintainer, and vice versa.

For stewards, this means establishing clear processes for **receiving and reviewing** security fixes from downstream
manufacturers, and communicating those processes in the project's `SECURITY.md` or contributing guide.

### Forked Components

Manufacturers are not required to report upstream where the component no longer has a maintainer, or where the manufacturer has
**forked** the FOSS component and no longer relies on the original maintainer for new versions or security fixes. However, a
manufacturer that continues to synchronise with the upstream project should not be considered to have forked the component for
this purpose.

## Contributors and Downstream Uses

The Commission's draft guidance (Section 3.4) confirms several important principles for the open source ecosystem:

1. **Contributors are protected**: The CRA does not apply to natural or legal persons who contribute source code to FOSS products
   that are not under their responsibility. Contributing code does not make a contributor a manufacturer or steward.

2. **Manufacturers integrating FOSS do not become responsible for individual component compliance**: Even where they contribute
   code to an integrated FOSS component's maintenance, they do not become the manufacturer of that component.

3. **Integration has no impact on the component's CRA status**: Whether the CRA applies to a FOSS component depends solely on
   whether the entity that publishes it places it on the market. The fact that manufacturers integrate a component into their own
   monetised products has no bearing on the component's own status.

4. **Manufacturers must exercise due diligence**: Under Article 13(5), manufacturers integrating FOSS are required to perform due
   diligence on integrated components. Under Article 13(6), they must report vulnerabilities upstream and share security fixes.

These principles are fundamental for maintaining the collaborative, contribution-based model that characterises open source
development.

## Penalties and Non-Compliance (Article 64(10))

Article 64(10) explicitly **excludes administrative fines** for open source software stewards:

> By way of derogation from paragraphs 3 to 9, the administrative fines referred to in those paragraphs shall not apply to the
> following: \[...\] (b) any infringement of this Regulation by open-source software stewards.

The only enforcement mechanism for stewards is **corrective actions** required by Market Surveillance Authorities under Article
52(3). This is consistent with the CRA's "light-touch and tailor-made" regulatory regime for stewards.

This exclusion applies to all types of non-compliance by stewards, including failure to maintain a cybersecurity policy, failure
to cooperate with MSAs, and failure to meet applicable reporting obligations.

Note that while administrative fines do not apply, stewards may still face indirect forms of liability, including reputational
impacts, and contractual expectations from downstream users.

## Illustrative Scenarios

The following scenarios are hypothetical and meant to illustrate the principles described above. They combine scenarios from the
original whitepaper with additional scenarios drawn from the Commission's draft guidance.

### Scenario A: Individual developer with donations, no steward

Individual developer A publishes a FOSS tool and includes a link to collect voluntary donations. Companies B, C, and D integrate
the FOSS into their products and make voluntary donations to support ongoing maintenance.

**Result**: The FOSS is not placed on the market. Developer A has **no obligations** under the CRA (natural person, no commercial
activity). Companies B, C, and D must exercise **due diligence** under Article 13(5).

### Scenario B: Not-for-profit foundation as steward

Not-for-profit foundation F publishes a FOSS component for integration into other commercial products. Foundation F provides
sustained support to ensure the project's long-term viability. Companies A, B, and C integrate the FOSS into their products.

**Result**: As Foundation F is a not-for-profit entity, the FOSS is not placed on the market. Foundation F is the **steward** and
subject to Article 24 obligations. Companies A, B, and C must exercise **due diligence** under Article 13(5).

### Scenario C: Company as steward for internally developed FOSS

Company A develops a FOSS component for integration into its own products, publishes it separately under its own name, and
actively maintains it, but does not charge for its use or monetise it in other ways. Companies B, C, and D integrate the FOSS into
their products.

**Result**: The FOSS is not placed on the market. Company A is not the manufacturer but is the **steward**. Companies B, C, and D
must exercise **due diligence**.

### Scenario D: Company as manufacturer for paid FOSS

Company A publishes a FOSS under its own name and offers it as a paid version including technical assistance and performance
optimisation. Developers from other companies contribute to the FOSS's maintenance.

**Result**: Company A is the **manufacturer**. Contributing companies have no obligations for that specific FOSS (but must
exercise due diligence if integrating it into their own products).

### Scenario E: Foundation providing only non-technical stewardship

Foundation G manages branding, governance rules, and community events for several FOSS projects. It collects membership fees but
does not host infrastructure or employ developers working directly on the code.

**Result**: Foundation G is a **steward** (Tier 1 — non-technical support) for the projects it sustains. It must maintain a
cybersecurity policy under Article 24(1) and cooperate with MSAs under Article 24(2). It is **not required** to report actively
exploited vulnerabilities or severe incidents, as it is not involved in development and does not provide network and information
systems. It should share relevant information it receives with project maintainers.

### Scenario F: Foundation providing IT infrastructure

Foundation H hosts source code repositories, provides CI/CD infrastructure, and manages code-signing keys for several FOSS
projects. Development is done primarily by community volunteers and corporate contributors.

**Result**: Foundation H is a **steward** (Tier 2 — IT infrastructure) for the projects it sustains. It must report **severe
incidents** affecting its infrastructure under Article 14(3). It should foster vulnerability handling and consider voluntary
reporting.

### Scenario G: Foundation with engineering involvement

Foundation J employs developers who coordinate development, review and merge code, manage releases, and handle vulnerability
reports for a critical FOSS library.

**Result**: Foundation J is a **steward** (Tier 3 — engineering resources) for that library. It must report **actively exploited
vulnerabilities** under Article 14(1) and inform impacted users under Article 14(8).

### Scenario H: Dual role (steward and manufacturer)

Company K publishes a FOSS database engine under its own name, offering both a paid "enterprise" version (with support and
additional features) and a free "community" version. The community version is freely available to all.

**Result**: Company K is the **manufacturer** of the enterprise version (placed on the market in the course of a commercial
activity). Company K is the **steward** of the community version (not placed on the market). Different obligations apply to each
version.

### Scenario I: Service provider customising FOSS for a client

A consultancy helps a customer deploy a FOSS project on the customer's infrastructure. As part of the engagement, the consultancy
adapts configuration files, writes integration scripts, and adjusts default settings to fit the customer's environment. The
consultancy does not modify the FOSS's core functionality or security-relevant behaviour.

**Result**: The consultancy is **not** placing the FOSS on the market, as it does not perform a substantial modification (see
Commission guidance, paragraph 56 and Example 13). The original steward's (or maintainer's) role is unaffected. The customer who
deploys the resulting product in the course of a commercial activity may have obligations as a manufacturer for the product as a
whole, including due diligence under Article 13(5).

### Scenario J: Consultancy performing a substantial modification of FOSS

A consultancy takes a FOSS project and, as part of a client engagement, replaces the authentication subsystem with a proprietary
module and adds a remote management interface not present in the original software. These changes fundamentally alter the
product's security risk profile and intended purpose.

**Result**: The modifications likely constitute a **substantial modification** within the meaning of Article 3(30). In accordance
with Article 22, the consultancy (or the client, depending on who makes the modified product available on the market) is
considered the **manufacturer** of the modified product and must comply with the CRA in its entirety for that product. The
original steward's role in relation to the unmodified FOSS is unaffected. This scenario illustrates that the boundary between
"service provider doing customisation" and "manufacturer performing a substantial modification" depends on whether the changes
affect compliance with the essential cybersecurity requirements or modify the product's intended purpose.

## Open Questions and Areas Requiring Further Guidance

The following questions remain **partially or fully unresolved** despite the Commission's March 2026 draft guidance:

### Resolved or substantially clarified by the Commission's guidance

1. **Steward vs. manufacturer boundary**: The guidance provides detailed criteria and a flowchart for determining when FOSS is
   placed on the market (Section 3.2 of the guidance).
1. **Not-for-profit exemption**: Clarified that not-for-profit entities are not placing FOSS on the market even when monetising.
1. **Dual roles**: Confirmed that the same entity can hold different roles for different projects.
1. **Graduated reporting**: Confirmed that reporting obligations scale with the type of support provided.
1. **"Becoming aware" threshold**: Aligned with NIS 2 and GDPR precedent.
1. **Sustained support**: Examples provided of what constitutes sustained support.

### Technical and Operational Open Questions

Despite the clarifications provided in the Commission’s draft guidance, several practical and operational questions remain
unresolved and would benefit from further guidance or standardisation:

1. **Cross-border CSIRT selection and coordination**: Uncertainty remains regarding how to determine the appropriate CSIRT for
   stewards without an EU establishment, and how multiple CSIRTs should coordinate when the same project is used across several
   Member States.
1. **Language requirements for regulatory interaction**: It is unclear whether Market Surveillance Authorities (MSAs) and CSIRTs
   will systematically accept documentation and communication in English, or whether translations into national languages will be
   required in practice.
1. **Routing and deduplication of vulnerability reports**: As multiple actors (manufacturers, researchers, CSIRTs) may report the
   same vulnerability, mechanisms are needed to avoid duplication, ensure efficient triage, and prevent overload on stewards and
   project maintainers.
1. **Operational integration with ENISA systems:** Further clarity is needed on how stewards will interact with ENISA’s single
   reporting platform and the European vulnerability database (EUVD), including authentication, workflows, and access management.
1.  **Scope of “fostering” obligations**: The obligation to “foster” secure development and vulnerability handling remains open to
   interpretation, particularly regarding whether it applies only to the project’s internal practices or also to downstream
   integration by manufacturers.
1. **Interaction with remote data processing solutions (RDPS)**: Additional guidance is needed on how steward obligations apply
   where open source software includes or depends on remote services, especially in light of broader CRA provisions on remote data
   processing.
1. **Handling of low-quality or automated vulnerability reports**: With the increase of automated scanning and AI-generated
   reports, stewards require practical mechanisms to filter, prioritise, and manage low-quality submissions without undermining
   coordinated vulnerability disclosure.

### Strategic Priorities for the Evolution of Stewardship

Beyond these operational questions, the introduction of the steward role raises broader structural considerations for the EU
digital regulatory framework.

#### Towards a coherent cross-regulatory concept of stewardship

While the Cyber Resilience Act introduces the steward role, similar governance functions are only implicitly addressed in
instruments such as the NIS2 Directive and the EU AI Act. A lack of alignment across these frameworks risks fragmentation and
inconsistent expectations.

**Priority**: Develop a horizontal and interoperable understanding of stewardship as an ecosystem-level governance function across
EU digital legislation.

#### Integrating stewardship into EU cybersecurity certification frameworks

The current certification system under the EU Cybersecurity Act does not recognise open source stewards as contributors to
assurance.

**Priority**: Enable the use of steward-generated artefacts (e.g. attestations) within certification and conformity assessment
processes, supporting scalable and reusable assurance for open source components.

#### Establishing a sustainable and operational stewardship model

The CRA defines obligations but does not provide mechanisms to support the long-term sustainability of stewardship activities.

**Priority**: Promote operational and economic models for stewardship, including:

- Shared infrastructure
- Service-based approaches (e.g. attestations)
- Public-private support mechanisms

#### Providing lifecycle clarity and legal predictability

The absence of guidance on how entities enter, transition within, or exit the steward role creates uncertainty.

**Priority**: Develop lifecycle principles and transition guidance, particularly for:

- Steward / manufacturer role changes
- Entry and exit conditions
- Transitional responsibilities

#### Evolving towards a risk-based and proportionate model

The current framework primarily distinguishes obligations based on the type of support provided.

**Priority**: Complement this approach with risk-based criteria, such as:

- Criticality of the software
- Scale of deployment
- Dependency centrality

#### Bridging open source practices and regulatory compliance

A gap persists between how open source security is managed in practice and how compliance is demonstrated in regulated
environments.

**Priority**: Develop standardised, machine-readable, and reusable artefacts that:

- Reflect real-world development practices
- Support regulatory compliance
- Enable automation and interoperability

Addressing both the operational open questions and the strategic priorities identified above is essential to ensure that the
steward role evolves into a coherent, scalable, and effective governance mechanism supporting Europe’s cybersecurity and digital
resilience objectives.

## References

### Primary legal instruments

- **Regulation (EU) 2024/2847** of the European Parliament and of the Council of 23 October 2024 on horizontal cybersecurity
  requirements for products with digital elements (Cyber Resilience Act). OJ L, 2024/2847, 20.11.2024.
- **Directive (EU) 2022/2555** of the European Parliament and of the Council of 14 December 2022 on measures for a high common
  level of cybersecurity across the Union (NIS 2 Directive). OJ L 333, 27.12.2022.
- **Commission Implementing Regulation (EU) 2024/2690** of 17 October 2024 laying down rules for the application of Directive (EU)
  2022/2555.
- **Commission Implementing Regulation (EU) 2025/2392** setting out the technical description of the categories of important and
  critical products.
- **Regulation (EU) 2019/881** on ENISA (the European Union Agency for Cybersecurity) and on information and communications
  technology cybersecurity certification (EU Cybersecurity Act).
- **Regulation (EU) 2024/1689** of the European Parliament and of the Council laying down harmonised rules on artificial
  intelligence (Artificial Intelligence Act).
- **Regulation (EU) 2022/2065** on a Single Market for Digital Services (Digital Services Act).
- **Regulation (EU) 2023/2854** on harmonised rules on fair access to and use of data (Data Act).

### Commission guidance

- **European Commission, Draft Guidance on the application of Regulation (EU) 2024/2847 (Cyber Resilience Act)**. Ref.
  Ares(2026)2319816 — 03/03/2026. Published for public consultation.
- **European Commission, CRA Implementation FAQs** (December 2025). Available via the Commission's CRA implementation website.

### ORC WG resources

- ORC WG CRA FAQ: [https://cra.orcwg.org/faq/](https://cra.orcwg.org/faq/)
- ORC WG CRA Steward FAQ: [https://cra.orcwg.org/faq/stewards/](https://cra.orcwg.org/faq/stewards/)
- ORC WG CRA Attestations specification: [https://github.com/orcwg/cra-attestations](https://github.com/orcwg/cra-attestations)
- ORC WG Vulnerability Management Specification:
  [https://github.com/orcwg/vulnerability-management-spec](https://github.com/orcwg/vulnerability-management-spec)
- ORC WG CRA Hub: [https://github.com/orcwg/cra-hub](https://github.com/orcwg/cra-hub)

### Other references

- Commission notice — The 'Blue Guide' on the implementation of EU product rules 2022\. OJ C 247, 29.6.2022, pp. 1–152.

---

*This document is Deliverable D3.5 of the ORC Working Group's Cyber Resilience SIG. It is maintained at
<https://github.com/orcwg/orcwg/blob/main/cyber-resilience-sig/whitepapers/stewards-and-cra.md>*
