###  9 June 2025
##  Agenda

| Min | Agenda Topics | Moderator |
| --: | ----- | --- |
|   0 | Welcome & approve [previous minutes](https://github.com/orcwg/orcwg/pull/103) | Tobie |
|   5 | [Pending action items](#pending-action-items) from last SIG call | Tobie |
|  10 | CRA Expert Group updates | [Expert Group Liaisons][] |
|  15 |  | |
|  20 |  | |
|  25 | ESOs updates | [ESO Liaisons][] |
|  30 |  | |
|  35 | Vulnerability Handling TF update | Vulnerability Handling TF leads |
|  40 | Resource Inventory TF update ([#228](https://github.com/orcwg/cra-hub/pull/228)) | Inventory TF leads |
|  45 | BSI / FSFE questionnaire update | Tobie |
|  50 | FAQ TF update | FAQ TF leads |
|  55 | AOB | |

## Pending action items

- [ ] Open PR to add statements on CVEs to deliverables plan & get SIG started on this.
- [ ] Continue work on infrastructure facilitating coordination around standardization.
- [X] Open pull request to create vulnerability handling task force and share on the mailing list: _[#104](https://github.com/orcwg/orcwg/pull/104)_
- [X] Start thread with volunteers for BSI/FSFE questionnaire


<details>
<summary><b>Participants </b></summary>

* Tobie Langel (UnlockOpen/Eclipse Foundation)  
* Juan Rico (Eclipse Foundation)  
* Mathias Schindler (GitHub)  
* Shanda Giacomoni (Eclipse Foundation)  
* Dirk-Willem van Gulik (the Apache Software Foundation)  
* Dick Brooks (Business Cyber Guardian)  
* Becky Hepper (Seagate)  
* Olle E. Johansson (Edvina / OWASP)  
* Henry Haverinen (Cyberismo)  
* Roman Zhukov (Red Hat)  
* Alistair Woodman (Erlang Ecosystem System (EEF))  
* Rebecca Rubul (Rust Foundation)  
* Jakub Zelenka (PHP Foundation)  
* Daniel Thompson (Tauri)  
* Sal Kimmich (GadflyAI)  
* Vicky Risk (ISC.org)  
* Dan Appelquist (Samsung / OpenSSF Global Cybersec Policy WG)  
* Salve J. Nilsen (CPANSec)  
* Jeremy Stanley (Spec Committee, OpenInfra Foundation, SPI)  
* CRob (OpenSSF)   
* Simon Phipps (SWH/Meshed Insights)  
* Æva Black

</details>


## Minutes

### Welcome & approve previous minutes (Tobie)

* [https://github.com/orcwg/orcwg/pull/103](https://github.com/orcwg/orcwg/pull/103)  
* No objection. merging.	

### Pending action items from last SIG call (Tobie)

- [ ] Open PR to add statements on CVEs to deliverables plan & get SIG started on this.  
  - No progress. This needs help  
- [ ] Continue work on infrastructure facilitating coordination around standardization.  
  - Not much progress.  
- [x] Open pull request to create vulnerability handling task force and share on the mailing list: \#104  
  - Waiting on the Github team being approved (see [orcwg/.eclipsefdn#6](https://github.com/orcwg/.eclipsefdn/pull/6)).
  - [ ] Tobie to organize first vulnerability handling TF call
  - Anyone missing, add your name below ([intital list)](https://github.com/orcwg/orcwg/blob/main/cyber-resilience-sig/minutes/2025-05-26-mom-cyber-resilience-sig.md#esos-updates):  
      - Jeremy Stanley <jeremy@openinfra.dev>
      - Sal kimmich <salkimmich@gmail.com>
      - Olle E. Johansson <oej@edvina.net>
      - Dick Brooks <dick@businesscyberguardian.com>
      - Arnout Engelen <engelen@apache.org>
  - [X] Tobie to add missing folks to Vulnerability handling TF GH team  
- [x] Start thread with volunteers for BSI/FSFE questionnaire  
  - Vicky, Roman, and Michael (from BSI) met  
  - Not designed as a replacement for LF’s survey  
  - Input OK as is.  
  - BSI will take it from here.  
  - Main focus is determining whether people are accurately identifying their role under the CRA.  
  - Possible output: come up with some canonical example cases (challenge is this might constitute legal advice).  
  - [ ] Tobie to close workstrand

### CRA Expert Group updates (Expert Group Liaisons)

* Two meetings last week  
  * Open Source workstream  
  * Brussels plenary  
* Minutes are not yet public  
* The CRA expert group meeting on Open Source Guidance (Tobie)  
  * Subset of the CRA expert group  
  * Tobie is positive to work done in this group  
  * Output possible from Commission in Q4 this year (guess) although may be as early as Q3  
  * Dan: Can we get output faster? We need to communicate to the community.  
* Dirk: Small group of us live with Common Criteria. EUCC takes a lot of time for the commission. What do we think?  
  * Discussion postponed \- separate meeting with preparation  
  * Dirk to email the mailing list with an update.  
  * EUCC risks being part of horizontal standards if we don’t act strongly  
  * Some background: https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements\_en

### ESOs updates (ESO Liaisons)

* Plenary in Brussels with updates, not many new aspects presented  
* There were no ETSI meetings last week  
* CEN Project Teams are at different states of progress  
  * PT1 is a full draft  
  * PT2 is essentially rebooting  
  * PT3 is now under active drafting  
    * Open source contribution made  
* PT1 looking at integration of third party components   
* PT3 is looking at an annex on open source stewards  
* ETSI Special Task Force (EU funded rapporteurs):  
  * Contractors retained to work on verticals are now ready to start & kick-off this week  
  * First milestone June 30 

### Vulnerability Handling TF update (Vulnerability Handling TF leads)

* Goals:
  * Help coordinate input to CEN/CENELEC PT 3
  * Provide input to the SIG and Cyber Resilience Practices Project on [deliverables plan](../deliverables.md) and [proposed specs](../deliverables.md#4-specifications)
  * Possible white paper on vulnerability handling 

### Resource Inventory TF update (\#228) (Inventory TF leads)

* No progress made  
* Document nearly finished

### BSI / FSFE questionnaire update (Tobie)

* Action item closed (see above)

### FAQ TF update (FAQ TF leads)

* Task force call Friday 13.30 CEST

### AOB (Tobie)

* CVE update (Dirk-Willem)  
  * ENISA is now much more on the ball \- and has now a single point in the org for this.  
  * ENISA has some understanding how crucial this system is (And having a single one) for the CRA/SBOMs.  
  * CNAs and reporters keep the system running  
    * I.e. there is a negotiation aspect as to what is a vulnerability, how is it described, what is its scope.  
    * Reports and those with the vulnerability do not have the same view of this  
    * CNAs and the hierarchy \`up’ are key to finding a balance / enforce some industry standard minimal levels of \`sanity’ (so that not every CVE has the description \`security review item discrepancy’).  
    *  this is not well understood within the EC yet \- when they talk to our community they generally talk to people on the operational coal face \- for whom the final outcome of that delicate balance is what they care/hear about \- i.e. the issues numbers. So the process before that is not stressed/all that much visible  
  * Concrete outcomes?  
    * Large knowledge gap  
    * It’s going to take a while before we get to a place where we can explain this  
* GVIP update (OEJ): [https://github.com/gvip-project/](https://github.com/gvip-project/)  
  * Mailing list: [cve@owasp.org](mailto:cve@owasp.org) Ping Olle to be added  
  * Series of webinars starting fairly soon  
  * Looking for stakeholders outside of the open source community right now  
  * Dirk will help Olle find the right Enisa contact for this conversation/workshop/talk  
* OpenSSF short guide for maintainers (2 pages)

### CRA Mondays

- Remember this is on zoom today: [https://eclipse.zoom.us/j/85385310037?jst=2](https://eclipse.zoom.us/j/85385310037?jst=2) 

[SIG Leads]: https://github.com/orcwg/orcwg/tree/main/cyber-resilience-sig#leads
[ESO Liaisons]: https://github.com/orcwg/orcwg/tree/main/cyber-resilience-sig#cen-cenelec-wg-9
[Expert Group Liaisons]: https://github.com/orcwg/orcwg/tree/main/cyber-resilience-sig#cra-expert-group

  
