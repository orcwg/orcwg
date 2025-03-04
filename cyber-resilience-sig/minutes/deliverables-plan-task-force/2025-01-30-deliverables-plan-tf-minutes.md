# Cyber Resilience SIG - Deliverables Plan Task Force

###  January 30, 2025

In person meeting during the morning and afternoon of the ORC WG Workshop in Brussels.

## Participants

* Tobie Langel (UnlockOpen/Eclipse Foundation)
* Mikael Barbero (Eclipse Foundation)
* Timo Perala (Nokia)
* Jonne Soininen (Nokia)
* Dirk-Willem van Gulik (ASF)
* Thierry Carrez (OpenInfra Foundation)
* Addie Girouard (Varo)
* Brian Fox (ASF / Sonatype)
* ...

## Minutes

### FAQ & Inventory

* Participants noted that the FAQ and Inventory should be mentioned in the deliverables plan
* FAQ answers should embody "industry best practice"

### Scope

* Wise to structure deliverables plan scope & time against the timeline of the standards request to the ESOs (i.e. phasing of types A, B, and C)
* Scope must include other kinds of outputs including input to ESOs
* WG should set up the Friends of ESOs group, which could provide give high-level overview of the harmonized standards work to the WG to help gather input

### Deliverables prioretization

Partcipants went through the categories in the [inventory](https://github.com/orcwg/cra-hub/blob/main/inventory.md) and prioretized relevant deliverables.

* “Secure dev” spec for open source projects based on Type A standard
  * Seems good candidate for spec
* Vulnerability management
  * draft in progress by Eclipse ready to submit to WG, waiting on license approval by Steering Committee
* SBOM
  * Must figure out what the requirements are, and what diff open source communities are willing to do here
  * Noted existing activity in US NTIA, BSI, India, Japan; suggested collecting those in the inventory (tracking in [orcwg/cra-hub#147](https://github.com/orcwg/cra-hub/issues/147))
  * Common issue very security oriented - whereas the win/win in open source is around software lifecycle, upstream origin, provenance and license management (including zero trust/reproducible builds)
  * **Non Problem:** solving the dependency problem; you either ship source -or- a build product; in which case you `know’ what goes in and that (non reproducible, non deterministic) SBOM is known, ‘as is’. The CRA does not require cracking that nut.
  * Next step would be white paper
* Security policy
  * This is harder than just the vulnerability management
  * Also possible spec candidate
* Due diligence requirements for manufacturers
  * What upstream open source can provide on a platter (like README.txt, INSTALL.txt, setup.py, build.xml) to help downstream parties (manufacturers) to comply with the CRA; i.e. feed into the documentation stream for provenance, origin, software lifecycle, latest known upstream vulnerabilities, etc. 

### Drive community input

- WG should set up process for WG member input to the SIG (e.g. in our regular calls) to present on some of these topics
- Figure out how to contribute input to the WG for licensing purposes, but without appearing like this content is endorsed by the WG
