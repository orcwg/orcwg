---
SIG: AI Policy and Compliance SIG
Document type: Minutes
Status: 🗓️ Proposed agenda
Date: 2026-08-10
---

## Agenda
| Min | Topic | Moderator |
| --: | ----- | --- |
|   0 | Approve previous minutes | Ciarán |
|   5 | Plan: deliverables list discussion 7 Sep, adoption 21 Sep | Ciarán |
|  10 | AI Act obligations applicable since 2 Aug: art 50 on transparency | Ciarán |
|  15 | CRA interaction, notes on EC's plans | Ciarán |
|  20 | California AB 2013, obligations to describe training data | Ciarán |
|  25 | AI Act standard on logging: prEN 18229-1 | Ciarán |
|  30 | GPAI Code of Practice | Ciarán |
|  35 | ETSI's progress on AIPP, online meeting on 26 Aug | Ciaran |
|  40 | | |
|  45 | AOB | |
|  50 |  | |

Meeting ends at :55.

## Participants
Ciaran O'Riordan
Javier Valiño
Dave Russo
Rachel Foucard
Mathias Schindler
Alistair Woodman
Marcel Kurzmann

## Minutes
1. **Approve previous minutes**.
The minutes of the previous meeting were approved without objection.

2. **Plan: deliverables list discussion 7 Sep, adoption 21 Sep**.
The scheduled September 7 meeting coincides with public holidays in some countries, which could limit attendance for the important discussion on the SIG's scope and deliverables.
  * It was agreed to poll the group via the mailing list and Slack to potentially move the September 7 meeting (e.g., to Wednesday) to ensure adequate participation before the final adoption of the deliverables list scheduled for September 21.
  * The discussion of scope and deliverables should start offline using the slack channel and/or the mailing list as soon as possible to meet the September deadline. A top priority topic selection among the ones discussed in these meetings must be done and the expected deliverables from those priority topics should be identified. The final nature/Technology used on those deliverables can be decided later.

3. **AI Act obligations applicable since 2 Aug: art 50 on transparenc**y.
The group reviewed Article 50, which mandates transparency and watermarking (e.g., informing users they are interacting with AI).
* A Code of Practice on transparency has been developed, divided into Section 1 (for creators/providers) and Section 2 (for deployers/users).
* Past advocacy ensured that the Code of Practice accommodates open source models by not strictly requiring watermarking features to remain intact if it breaks the software.
* There is no open source exemption for Article 50; however, it applies to AI systems, not standalone model weights (which fall under GPAI). Overall, the transparency obligations aim to reduce the compliance burden and appear largely non-controversial.

4. **CRA interaction, notes on EC's plans**.
The intersection of the AI Act and the Cyber Resilience Act (CRA) was discussed, noting the need to coordinate with the ORC Cyber Resilience SIG.
* Generally, if an AI system includes software, it must comply with the CRA. Adhering to the CRA’s stricter cybersecurity requirements will provide a presumption of conformity with the AI Act’s cybersecurity rules.
* However, due to the CRA’s open source exemption, open source AI systems may be exempt from the CRA but will still need to meet the AI Act’s specific cybersecurity requirements.
* Other updates included the expected launch of the ENISA single reporting platform (expected around Sept 11), upcoming ENISA guidance on AI-powered threats (Q3), and a pilot project for a critical open source maintenance instrument later this year.

5. **California AB 2013, obligations to describe training data**.
The group discussed California AB 2013, which has been applicable since January 1, 2026.
* The law requires publishers to provide a summary of training datasets (including copyright status) for AI systems made available to users in California (including via web services).
* This obligation heavily overlaps with Article 53 of the EU AI Act, meaning compliance with the EU framework brings organizations very close to CA compliance.
* A critical difference is that AB 2013 contains no non-commercial exemption. Avoiding the regulation entirely would require geo-blocking California residents.

6. **AI Act standard on logging: prEN 18229-1.**
This topic was briefly introduced, noting it touches upon data collection. As the group has not yet conducted an in depth review, it was agreed to defer this discussion to the next meeting.

7. **GPAI Code of Practice**.
A brief overview of the GPAI Code of Practice was provided.
* Signing a Code of Practice provides a lighter audit regime and demonstrates market confidence, though it lacks the formal legal presumption of conformity provided by a harmonized standard.
* The GPAI Code covers Article 53 (documentation requirements, which has a FOSS exemption) and Article 55 (systemic risk, which does not have a FOSS exemption and mandates red teaming and incident reporting).
* Entities without systemic risk can still voluntarily sign the safety and security chapters to build trust.

8. **ETSI's progress on AIPP, online meeting on 26 Aug**.
ETSI is spearheading a new AI Partnership Project (AIPP) in collaboration with counterparts in South Korea (TTA) and Japan (TTC), mirroring the 3GPP approach for telecommunications.
* This presents strategic advantages for the EU regarding standardizing AI, facilitating data sharing (e.g., leveraging Korean traffic data for autonomous driving training to bypass strict GDPR limits), and semiconductor hardware cooperation.
* An online meeting is scheduled for August 26; SIG members are encouraged to attend to monitor international standardization efforts. Link shared in the meeting chat.

9. **AOB: Collaborative AI Tooling for Regulatory Analysis**. 
A proposal was raised to systematically leverage AI tools (e.g., using LLMs or Retrieval-Augmented Generation) to create a shared "knowledge base" or matrices comparing various EU/US acts and standards.
* It was suggested this could become an official deliverable for the SIG to prevent duplicate effort among members.
* Participants emphasized that any AI generated regulatory output must be heavily fact checked ("trust but verify") to mitigate hallucinations.
* Agreement: The group will continue discussing the methodology for this (e.g., building a shared Git repository with Markdown files) asynchronously and at the next meeting.

10. **AOB: Mailing List Spam Issues**.
It was noted that some participants' Gmail accounts are flagging SIG mailing list traffic as spam. Members are encouraged to add the mailing list email address to their contacts to train the spam filters.

## Action points
* Eclipse Foundation: Explore moving September 7 meeting via Doodle; communicate on mailing list.
* Ciarán: Initiate the discussion via slack/mailing list of scope and deliverables
* Ciarán: Re-add AI Act logging standard (PREN18229-1) to next meeting agenda.
* Marcel: Share a sanitized or illustrative example of Git-based regulatory document analysis workflow to Slack/mailing list.
* All members: Add orc-ai-sig@eclipse.org email to contacts to prevent Gmail spam filtering.
* Interested members: Register for ETSI AIPP online meeting on August 26.
