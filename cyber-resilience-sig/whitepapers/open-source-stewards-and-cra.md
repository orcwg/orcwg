# Open Source Software Stewards and CRA Whitepaper

The Cyber Resilience Act (CRA) defines a new category of organizations, Open Source Stewards (Stewards hereafter). It also defines obligations for them that are different from those of other categories like manufacturers.

This whitepaper will aim at elaborating on the obligations, restrictions, and penalties that will be imposed to Stewards.

From the elaboration on the legal text, we will outline the missing pieces / documents / procedures that Stewards need to have to fulfil their obligations.

The goal is NOT to provide a definition or guidance about who is and who is not a steward for an Product with Digital Element qualifying as Open Source Software.

TODO: Add a note that this is not legal guidance, but the current understanding of the CRA

## Obligations of Open Source Stewards

TODO: List obligations of Open Source Stewards from different articles of the CRA

### Cybersecurity Policy — Article 24(1)

Stewards shall put in place and document in a verifiable manner a cybersecurity policy.

That policy shall foster:
- the development of a secure product with digital elements
- an effective handling of vulnerabilities by the developers of that product
- the voluntary reporting of vulnerabilities as laid down in Article 15 (vulnerability or incident ​​to a CSIRT designated as coordinator or ENISA)

That policy shall, in particular, include aspects related to:
- Documenting vulnerabilities
- Addressing vulnerabilities                                    
- Remediating vulnerabilities 
- Promote the sharing of information concerning discovered vulnerabilities within the open-source community
- Enable the reporting of vulnerabilities to the project (or to the Steward) by any manufacturer integrating such project in their product, in accordance with the obligations of manufacturers under Article 13(6).

### Collaboration with Market Surveillance authorities — Article 24(2)

Stewards shall cooperate with the market surveillance authorities (MSA hereafter), at their request, with a view to mitigating the cybersecurity risks posed by a PwDE they are the steward of.

Steward must be ready to provide to MSA, at their reasoned request, the documentation about their Cybersecurity Policy. Documentation can be produced in paper or electronic form.

### Reporting Obligations — Article 24(3)

#### CSIRT designated as coordinator

Steward must know who is their CSIRT designated as coordinator (CSIRTdaC hereafter). The CSIRTdaC is the one from the Member State where (in order of priority):
- the Steward has their main establishment. Main establishment is where the decisions related to the cybersecurity of its products with digital elements are predominantly taken
- the Steward has the establishment with the highest number of employees in the Union

If the Steward has no main establishment in the Union, the CSIRTdaC is the one from the Member State in which:
- the authorised representative acting on behalf of the Steward for the highest number of PwDE of that Steward is established
- the highest number of users of PwDE of that Steward are located

#### Notifications

Steward must notify simultaneously to the CSIRdaC and to ENISA, via the single reporting platform (Article 16): 
- Any actively exploited vulnerability (AEV) contained in the PwDE — article 14(1)
- Any severe incident (SevInc) having an impact on the security of the PwDE that it becomes aware of. — article 14(3)

Stewards don’t have a delay for reporting avtively exploited vulnerabilities or severe incidents.

After becoming aware of any event listed above, the Steward must inform the impacted users of the PwDE, and where appropriate all users of — article 14(8)
that vulnerability or incident of any risk mitigation and corrective measures that the users can deploy to mitigate the impact of that vulnerability or incident, 
where appropriate in a structured, machine-readable format that is easily automatically processable.

### Required Guidance

TODO: list required guidance, best practices that stewards should follow

### From Article 24

- Specification about how to demonstrate that the policy is put in place
- How to record it and store it such that an independent party can check that the policy exists (version-controlled documents, maintaining a change log, ...)
- It covers the required topics (scheduling regular reviews)
- It’s actually being followed (tying policy statements to evidence)

Specification on what it means for a policy to foster the development of secure PwDE: policy must list methodologies of risk assessment, secure by design, secure by default, and secure SDLC
an effective handling of vulnerabilities by the developers of that product: policy must contain description of CVD process

Format of the Security Policy

### From Article 14(8)

- The advisory format and content (CSAF, VEX etc)

### From Article 16

- How Stewards become aware of actively exploited vulnerabilities
- How Stewards become aware of severe incidents

### From Article 24(3)

- How to identify the CSIRT

## Restrictions

Steward cannot affix the CE marking on the PwDE they publish - recital 19

## Penalties

Where a MSA finds that a Steward does not comply with its obligations, MSA must require Steward to ensure that all appropriate corrective actions are taken. As a result, Stewards must ensure that all appropriate corrective action is taken in respect of their obligations.

Steward cannot be subject to administrative fines for any infringement of the CRA — Article 64(10b)

### Glossary

CRA - Cyber Resilience Act
CVD - Coordinated Vulnerability Dislosure
PwDE - Product with Digital Elements (as defined by the CRA)

### Contributors

TODO: List contributors of the document

### References

TODO: list useful references, previous work, talks etc including items from the Inventory and FAQ
