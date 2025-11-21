---
SIG: Cyber Resilience SIG
Task force:
Document type: White paper
Number: 3.5
Status: ✍️ Work in Progress
Input to: EU Guidance, Implementing Act, Harmonised standards
Relevant liaisons: EU Commission, CRA Expert Group, CEN/CENELEC, Market Surveillance
License: CC-BY 4.0
---

# Open Source Software Stewards and CRA Whitepaper

## Abstract

The Cyber Resilience Act (CRA) defines a new category of organizations, Open Source Stewards (Stewards hereafter). It also defines obligations
for them that are different from those of other categories like manufacturers.

This whitepaper will aim at elaborating on the obligations, restrictions, and penalties that will be imposed to Stewards.

From the elaboration on the legal text, we will outline the missing pieces / documents / procedures that Stewards need to have to fulfil their obligations.

The goal is NOT to provide a definition or guidance about who is and who is not a steward for an Product with Digital Element qualifying as Open Source Software.

This document is NOT legal guidance, but the current understanding of the CRA by its contributors.

## Status of this document

This is a draft document and may be updated, replaced or obsoleted at any time. It is inappropriate to cite this document as other than
a work in progress. Publication of this document as a draft does not imply endorsement by the Eclipse Foundation, Open Regulatory Working Group Members, or contributors.

## Obligations of Open Source Stewards

Open Source Stewards are defined in the CRA as a separate group of actors, different from Manufacturers. A Steward must be a legal person
(a registered legal entity such as a for-profit or non-profit company, a foundation, etc) and is also different from the Open Source Project itself.

Under the CRA, Stewards have specific obligations related to Open Source projects they are Stewards for.

A formal relationship between any given Open Source Project and their Steward, is something these two may have to establish themselves.
For example, a Steward organization may already be performing a supporting role for the project due to ownership of intellectual property,
for historical reasons, or because the project leadership has entered into an agreement with a Steward organization explicitly, or because
the project was originally founded as such.

### Security Policy

Stewards shall put in place and document a cybersecurity policy that applies to their Projects. That policy has goal of:
- encourage developing of secure 'products with digital elements'[^pwdnote]
- effective handling of vulnerabilities by developers of that product including documenting, addressing and remediating vulnerabilities,
and sharing of information concerning discovered vulnerabilities in the Open Source community
- describe the Project's vulnerability reporting and handling processes, including policies regarding voluntary reporting to and
coordination with a national CSIRT (see below)

[^pwdnote]: The legal text says *Open-source software stewards shall put in place and document in a verifiable manner a cybersecurity
policy to foster the development of a secure product with digital elements as well as an effective handling of vulnerabilities by the developers of that product.*
There are different possible interpretation: either the "fostering" in the Policy applies to the FOSS project, to the integration
of the FOSS project into Products by Manufacturers, or both. We trace the resolution of this doubt in [a dedicated FAQ entry](https://github.com/orcwg/cra-hub/issues/312)

The Steward may have the policy in paper or electronic form, but it must be "verifiable". As the relationships between
Stewards and their Projects vary, the Policy should take into account their common mode of operations.

Market Surveillance Authorities may request such a Security Policy.

References: Article 24(1)

        Cyber Resilience Act, Article 24(1):
        
        Open-source software stewards shall put in place and document in a verifiable manner a cybersecurity policy to foster 
        the development of a secure product with digital elements as well as an effective handling of vulnerabilities by the 
        developers of that product. That policy shall also foster the voluntary reporting of vulnerabilities as laid down in
        Article 15 by the developers of that product and take into account the specific nature of the open-source software 
        steward and the legal and organisational arrangements to which it is subject. That policy shall, in particular, include
        aspects related to documenting, addressing and remediating vulnerabilities and promote the sharing of information
        concerning discovered vulnerabilities within the open-source community.

In Open Source Projects, Security Policies are public (then the publication requirement is fulfilled) and published on
the Project site and/or included in their source code repository.

In practice, we see two patterns related to security policies:
- Either the supporting organization publishes one, and Projects link to it in their documentation. This may include some minor
clarifications, for example a specific link or email address to report vulnerabilities in that specific Project.
- Or, Projects publish their policies based on the template provided by the supporting organization.

In both cases, both the Steward and the Project will need to check if the Policy they provide includes all needed elements and that it
is followed. In the case the Project does not follow the Policy, the Steward needs to define the way to follow, see the [related FAQ entry](https://github.com/orcwg/cra-hub/issues/292).

As the Policy needs to be followed, the Steward and the Project will need to agree on a way to create the policy and provide changes.
For example, accepting a generic Policy of a Foundation-Steward may be a requirement for creation of a project or accepting that project under that Foundation.

What Stewards and Project will need:
- The published Policy (that is larger in scope than a typical current security policy)
- Evidence that the Policy is followed

What resources could be created to help fulfilling that requirement:
- A description about how to demonstrate that the policy is put in place - how to record it and store it such that an independent
party can check that the policy exists (version-controlled documents, maintaining a change log, ...)
- A description on how to prove that the Policy is actually being followed (tying policy statements to evidence)
- A specification and/or template of the Policy, showing what it means for a policy to foster the development of secure PwDE: 
for example the list of methodologies of risk assessment, secure by design, secure by default, secure SDLC;
and a process for effective handling of vulnerabilities by the developers of that product, description of the CVD process


### Collaboration with Market Surveillance Authorities

When Market Surveillance Authorities request assistance from a Steward related to one of their projects,
the Steward shall cooperate with the goal of mitigating security risk posed by the Project they are a Steward for.

In particular, the Market Surveillance Authority may request a copy of the Security Policy.

When an Open Source Project makes public their Security Policy (for example, by publishing on the Project
site and/or including in the source code repository) then the publication requirement is fulfilled.

However, the regulation also says "in a language which can be easily understood by that authority",
what might mean the language(s) of the country the market surveillance is located. As most Projects and
supporting organization publish their policies in English, it would be useful if those authorities accepted
documents in that language. The language of the country of the Steward may be different than the language
contributors of a given Project speak or understand.

The Market Surveillance Authority may request documentation related to the Security Policy, with the requirement
being "put in place and document in a verifiable manner a cybersecurity policy". In addition to the Policy itself,
it means all other documents showing that the Policy had been applied. It could be for example: the published
advisory (and in general, a list of published advisories) and the documentation of a CVD process in progress
(in case of a wide-impact exploited security vulnerability without a published fix, for example).

If a Market Surveillance Authority finds that a Steward does not comply with its obligations (what probably means
not having the Policy and/or not promoting the best practices), they require Steward to ensure that all appropriate
corrective actions are taken. As a result, Stewards "shall ensure" (formulation from the law) that all appropriate
corrective action is taken in respect of their obligations. It means that the Steward needs to have a way to
influence the Project in question to follow policies. A possible situation may be: not responding to vulnerability
reports, or not documenting fixed vulnerabilities.

The law requires the Steward to take actions, but clearly excludes any fees in the case of non-respect of the
regulation.

References: Article 24(2), Article 64(10b), Article 52(3)

        Cyber Resilience Act, Article 24(2):
        
        Open-source software stewards shall cooperate with the market surveillance authorities, at their request,
        with a view to mitigating the cybersecurity risks posed by a product with digital elements qualifying as
        free and open-source software.

        Further to a reasoned request from a market surveillance authority, open-source software stewards shall
        provide that authority, in a language which can be easily understood by that authority, with the
        documentation referred to in paragraph 1, in paper or electronic form.
        
        Cyber Resilience Act, Article 64(10) "Penalties":
        
        By way of derogation from paragraphs 3 to 9, the administrative fines referred to in those paragraphs shall not apply to the following:
        [...] (b) any infringement of this Regulation by open-source software stewards.
        
        Cyber Resilience Act, Article 52 (3) "Market surveillance and control of products with digital elements in the Union market":

        The market surveillance authorities designated under paragraph 2 of this Article shall also be responsible for carrying out
        market surveillance activities in relation to the obligations for open-source software stewards laid down in Article 24.
        Where a market surveillance authority finds that an open-source software steward does not comply with the obligations set
        out in that Article, it shall require the open-source software steward to ensure that all appropriate corrective actions
        are taken. Open-source software stewards shall ensure that all appropriate corrective action is taken in respect of their
        obligations under this Regulation.
        
What Stewards and Project will need:
- Know what organization is their market surveillance authority

What resources could be created to help fulfilling that requirement:
- A guide on finding out which is the appropriate market surveillance authority for each Steward
- Verifying with market surveillance if they accept policies and communication in a language acceptable
to the Project and the Steward

### Mandatory reporting of exploited vulnerabilities and security incidents

Stewards have an obligation for the mandatory reporting of actively exploited vulnerabilities and severe incidents. However, this obligation
is more limited in scope than the one of manufacturers.

First, Stewards are expected to report actively exploited vulnerabilities if they are involved in the development of the product.
This means that if the Steward is handling other elements than development (for example: finances only, and the Project
is taking development decisions independently), the Steward does not report.

This matches the typical configuration of the relations between Stewards and Projects, when Stewards aren't
directly involved in the development. This is frequently the case for Foundations. In this case, the Steward has also no
way to be aware of such an exploited vulnerability if not informed by the Project

The information that a vulnerability is being exploited might also come from external sources (like security researchers). In this case,
if the Steward is not involved in the development, they have no legal obligation to report. However, they should pass the report
to the Project. It is an open question if the Project needs to report it or not, but it would be the best practice to follow.

On the other hand, if Steward is involved in the development and operations (that could be frequently the case of companies
stewarding Projects they do not monetize), their staff will likely also handle vulnerability reports. In this case
they may receive information on exploitation or detect it directly. In this case, the Steward is required to report
the exploited vulnerability.

Secondly, the Steward is obliged to report serious incidents affecting information systems they provide for the Open Source
projects they host. This applies in a situation where it is the Steward organization managing that infrastructure by its
IT team. An example of such situation might include: the intrusion in the IT infrastructure causing unauthorised modification
of the version control system, taking over of accounts, leaking of their signing keys, or a longer unavailability of the
IT infrastructure making the development impossible.

Stewards that do not handle the IT infrastructure do not report such incidents.

When Stewards are reporting exploited vulnerabilities or severe incidents, they are required to inform affected users (see below).

When reporting, the Steward will use the single reporting platform and do not have a delay for reporting actively
exploited vulnerabilities or severe incidents.

Stewards may receive information of exploited vulnerabilities and incidents from the CSIRT, if the CSIRT receives such information
by the voluntary reporting. In this case, the Steward informs the affected Project.

References: 16, 14(1), 14(3), 14(8), 24(3), 15

        Cyber Resilience Act, Article 24(3) "Obligations of open-source software stewards":
        
        The obligations laid down in Article 14(1) shall apply to open-source software stewards to the extent that they are
        involved in the development of the products with digital elements. The obligations laid down in Article 14(3) and (8)
        shall apply to open-source software stewards to the extent that severe incidents having an impact on the security of
        products with digital elements affect network and information systems provided by the open-source software stewards
        for the development of such products.

        Cyber Resilience Act, Article 14(1) "Reporting obligations of manufacturers":
        
        A manufacturer shall notify any actively exploited vulnerability contained in the product with digital elements that
        it becomes aware of simultaneously to the CSIRT designated as coordinator, in accordance with paragraph 7 of this
        Article, and to ENISA. The manufacturer shall notify that actively exploited vulnerability via the single reporting
        platform established pursuant to Article 16.
        
        Cyber Resilience Act, Article 14(3) "Reporting obligations of manufacturers"

        A manufacturer shall notify any severe incident having an impact on the security of the product with digital elements
        that it becomes aware of simultaneously to the CSIRT designated as coordinator, in accordance with paragraph 7 of this
        Article, and to ENISA. The manufacturer shall notify that incident via the single reporting platform established pursuant
        to Article 16.
        
What Stewards and Projects will need:
- Define a process on who from the Steward and/or Project performs that notification, how to handle credentials (if needed). This could be
in the Steward Security Policy or a separate document that describes the implementation details, as agreed between the Steward and the Project.

What resources could be created to help fulfilling that requirement:
- A guide on filling reports on the common reporting platform

### Informing users about exploited vulnerabilities and security incidents

In case a Steward knows about an actively-exploited vulnerability related to one of their Projects, or a security
incident affecting them or the Project's infrastructure, they are required to inform affected users.
In case of open source project, most reports will likely be public. It might be private at the beginning,
and directed to the exact group of affected persons in case of IT compromise, for example to reset passwords
and verify recent suspicious activity. The best common practice is to publicly disclose that issues after
the Steward and the Project have taken immediate measures.

A typical report contains: information of the vulnerability/incident, any mitigations or measures users can
deploy (for example: disable a feature, reset their password). The text recommends to provide that information
in a machine-readable way. This could be any machine-readable advisory format, for example CSAF. They might also
choose to update the CVE entry for an exploited vulnerability. Most Stewards
will also likely choose to publish the information in human readable format, on a web page or email.

The legal text suggest that this reporting does not need to be immediate, allowing time for analysis of the issue,
verification and deploying fixes. It also suggests that this publication can be done in parallel to the reporting
on the common reporting platform.

If the Steward does not notify users in a reasonable time, the CSIRT can do it, if they find it appropriate.

References: 16, 14(1), 14(3), 14(8), 24(3)

        Cyber Resilience Act, Article 14(8) "Reporting obligations of manufacturers":

        After becoming aware of an actively exploited vulnerability or a severe incident having an impact on the security of
        the product with digital elements, the manufacturer shall inform the impacted users of the product with digital elements,
        and where appropriate all users, of that vulnerability or incident and, where necessary, of any risk mitigation and
        corrective measures that the users can deploy to mitigate the impact of that vulnerability or incident, where appropriate
        in a structured, machine-readable format that is easily automatically processable. Where the manufacturer fails to inform
        the users of the product with digital elements in a timely manner, the notified CSIRTs designated as coordinators may
        provide such information to the users when considered to be proportionate and necessary for preventing or mitigating
        the impact of that vulnerability or incident.

What Stewards and Projects will need:
- Define a method for how a Steward notifies users of exploited vulnerabilities and severe incidents. It can be a specific
web page, mailing list, or a combination of methods.

What resources could be created to help fulfilling that requirement:
- Best practices of notifying users of exploited vulnerabilities and severe incidents

### Voluntary vulnerability reporting

Stewards may voluntarily report vulnerabilities and incidents to a CSIRT or ENISA, or "near misses" (situation when
the exploitation or incident were possible, but avoided), and may receive reports
by the means of CSIRT and/or ENISA that come from voluntary reporting.

References: Article 24(1), 15

        Cyber Resilience Act, Article 24(1) "Obligations of open-source software stewards"
        
        Open-source software stewards shall put in place and document in a verifiable manner a cybersecurity policy to foster the
        development of a secure product with digital elements as well as an effective handling of vulnerabilities by the developers
        of that product. That policy shall also foster the voluntary reporting of vulnerabilities as laid down in Article 15 by the
        developers of that product and take into account the specific nature of the open-source software steward and the legal
        and organisational arrangements to which it is subject.[..]

        Article (15)
        
        1. Manufacturers as well as other natural or legal persons may notify any vulnerability contained in a product
        with digital elements as well as cyber threats that could affect the risk profile of a product with digital
        elements on a voluntary basis to a CSIRT designated as coordinator or ENISA.
        
        2. Manufacturers as well as other natural or legal persons may notify any incident having an impact on the
        security of the product with digital elements as well as near misses that could have resulted in such an
        incident on a voluntary basis to a CSIRT designated as coordinator or ENISA.

        3. The CSIRT designated as coordinator or ENISA shall process the notifications referred to in paragraphs 1 and 2
        of this Article in accordance with the procedure laid down in Article 16.

        The CSIRT designated as coordinator may prioritise the processing of mandatory notifications over voluntary notifications.

        4. Where a natural or legal person other than the manufacturer notifies an actively exploited vulnerability or a
        severe incident having an impact on the security of a product with digital elements in accordance with paragraph 1 or 2,
        the CSIRT designated as coordinator shall without undue delay inform the manufacturer.

        5. The CSIRTs designated as coordinators as well as ENISA shall ensure the confidentiality and appropriate protection
        of the information provided by a notifying natural or legal person. Without prejudice to the prevention, investigation,
        detection and prosecution of criminal offences, voluntary reporting shall not result in the imposition of any additional
        obligations upon a notifying natural or legal person to which it would not have been subject had it not submitted the notification.

        
### A policy to develop secure products

### A policy to effectively handle vulnerabilities

The policy to effectively handle vulnerabilities should be a part of the security policy and include processes of:
- documenting vulnerabilities
- addressing vulnerabilities
- remediating vulnerabilities
- promoting information sharing in the open source community
- enable reporting vulnerabilities to the project (or to the Stewards) by manufacturers including such a project in their product, according to obligations of the Manufacturer.

References: Article 24(1) and 13(6).

#### CSIRT designated as coordinator

The CRA text states that the Steward should perform reporting to the CSIRT designated as coordinator. However, this reporting is always
done via the single reporting platform. The interaction with CSIRTs is two-way. The Steward/Project reports to CSIRT, but the CSIRT also
informs the Steward of potential vulnerabilities and incidents that were reported to the CSIRT.

Stewards must know which CSIRT is their designated coordinator. The CSIRT is the one from the Member State where (in order of priority):
- the Steward has their main establishment. Main establishment is where the decisions related to the cybersecurity of its products with digital elements are predominantly taken
- the Steward has the establishment with the highest number of employees in the Union
- the Steward has the highest number of instances of its software

If the Steward has no main establishment in the Union, the appropriate CSIRT is the one from the Member State in which:
- the authorised representative acting on behalf of the Steward for the highest number of products of that Steward is established
- the highest number of users of products of that Steward are located

In practice, we can assume that the Steward/Project need to report by default to the CSIRT of the country the Steward has its headquarters.

If the Steward has no European official representation, we assume the reporting can be done to one of the CSIRTs of big EU countries (like Germany, France, Spain, Italy etc),
except if the specific Project has a strong user base in another country. This subject should be clarified, especially for Stewards and Projects
that do not have any representation in EU and for cases when there might be a language barier between the CSIRT and the Project.

If the Steward/Project could not figure out the appropriate CSIRT using those rules, we currently assume that they can choose the one that they find the most appropriate.
As the legislation seems to assume one CSIRT for Steward, multiple Projects will need to share the decision on the choice of the CSIRT. It would be the best
practice to take that decision together between all concerned Projects and the Steward representatives.

It will be also a good practice to document which CSIRT is the main one for each Project in the standard security documentation for that Project so it is easy
to find both for anyone who wishes to report a vulnerability, and for contributors to that Project.

Related ORC FAQ entries: [on choice of CSIRT](https://github.com/orcwg/cra-hub/issues/167)

References: 24(3), Directive 2022/2555

        Directive 2022/2555, Article 12(1) "Coordinated vulnerability disclosure and a European vulnerability database":

        Each Member State shall designate one of its CSIRTs as a coordinator for the purposes of coordinated vulnerability disclosure.
        The CSIRT designated as coordinator shall act as a trusted intermediary, facilitating, where necessary, the interaction between
        the natural or legal person reporting a vulnerability and the manufacturer or provider of the potentially vulnerable ICT products
        or ICT services, upon the request of either party. The tasks of the CSIRT designated as coordinator shall include:
        (a) identifying and contacting the entities concerned;
        (b) assisting the natural or legal persons reporting a vulnerability; and
        (c) negotiating disclosure timelines and managing vulnerabilities that affect multiple entities.

        Member States shall ensure that natural or legal persons are able to report, anonymously where they so request, a vulnerability
        to the CSIRT designated as coordinator. The CSIRT designated as coordinator shall ensure that diligent follow-up action is carried
        out with regard to the reported vulnerability and shall ensure the anonymity of the natural or legal person reporting the vulnerability.
        Where a reported vulnerability could have a significant impact on entities in more than one Member State, the CSIRT designated as
        coordinator of each Member State concerned shall, where appropriate, cooperate with other CSIRTs designated as coordinators
        within the CSIRTs network.

What Stewards and Projects will need:
- Documentation which CSIRT is the main one for each Project. This could be in Project's source code files, like SECURITY

What resources could be created to help fulfilling that requirement:
- Clarification of rules on deciding on the main CSIRT to use for non-UE based Stewards
- Clarification of rules on deciding on the main CSIRT is there is a language barier between the Project and the CSIRT

#### Market surveillance authorities

Market surveillance authorities might request information from the Steward on their policies.

Steward must know who is their market surveillance authority. The same rules and question apply, as for the choice of CSIRT.

What Stewards and Projects will need:
- Documentation of the market surveillance authority of the Project and Steward. This could be in Project's source code files, like SECURITY

What resources could be created to help fulfilling that requirement:
- Clarification of rules on deciding on the market surveillance authority to use for non-UE based Stewards
- Clarification of rules on deciding on the market surveillance authority is there is a language barier between the Project and the CSIRT
        
## Restrictions

As Stewards (and open source projects) follow less strict rules than PwDE placed on the market by Manufacturers, Steward cannot affix
the CE marking on the products they publish. It also means that they do not provide the complete CRA documentations for their Projects.

They might have an attestation program that provides equivalent documentation for the use of manufacturers.

References: the Cyber Resilience Act, recital 19:

        [..] legal persons who provide support on a sustained basis for the development of such products which are intended for commercial activities,
        and who play a main role in ensuring the viability of those products (open-source software stewards), should be subject to a light-touch and
        tailor-made regulatory regime. [..] Given that the light-touch and tailor-made regulatory regime does not subject those acting as open-source
        software stewards to the same obligations as those acting as manufacturers under this Regulation, they should not be permitted to affix the CE
        marking to the products with digital elements whose development they support.

### Glossary

- ENISA - European Union Agency for Cybersecurity
- CRA - Cyber Resilience Act
- CSAF - Common Security Advisory Framework
- CSIRT - Computer Security Incident Response Team
- CVD - Coordinated Vulnerability Disclosure
- PwDE or PWD - Product with Digital Elements (as defined by the CRA)
- SDLC - Secure Development Life Cycle

### References

1. [The choice of CSIRT](https://github.com/orcwg/cra-hub/issues/167)
2. [ORC FAQ entries on Open Source Software Stewards](https://github.com/orcwg/cra-hub/blob/main/faq.md#open-source-software-stewards)
3. [FOSDEM 2025 session: CRA Q&A on Open Source Stewards under the Cyber Resilience Act](https://archive.fosdem.org/2025/schedule/event/fosdem-2025-6638-cra-q-a-on-open-source-stewards-under-the-cyber-resilience-act/)

## Acknowledgments

The following people have contributed to this document either directly or indirectly (e.g. by raising questions):

- Mikaël Barbero
- Æva Black
- Arnout Engelen
- Tobie Langel
- Faidon Liambotis
- Jordan Maris
- Salve J. Nilsen
- Juan Rico
- Marta Rybczynska
- Jeremy Stanley
- Mark Thomas
- Daniel Thompson-Yvetot
- Martin von Willebrand

If you have contributed to this document and aren't properly acknowledged or if you want to edit or remove your name, please let us know by [opening an issue](https://github.com/orcwg/orcwg/issues/new) and we will fix this right away.
