# PROMPTS — Real Prompt Examples Used

*(한글 버전: [PROMPTS.md](./PROMPTS.md))*

> This document is reference material for the book "Teaching My 25 Years to AI."
> It is a collection of real prompts given to the skill, discussed in main text Chapter 6 ("The Prompts Were the Skill's History") and Appendix E.

---

## What this document is

This skill operates on natural language instead of complex commands. You don't need to know options like `--type` or `--mode` — you just describe "the task I'm doing right now" the way you'd normally say it. Attaching the same file but writing a different prompt can produce a different output.

Below are **real prompt examples**, organized by category. The internal processing order (how the skill handles each one) is omitted — only the **"here's how you'd phrase it in this situation"** examples are included.

The skill started with nineteen task types and grew to more than seventy as new needs arose. The growth of this list is, in effect, the history of how the skill itself grew. (See Chapter 6 and Appendix E of the book.)

Each example is specific to ITU-T standardization practice, so the subject matter itself may be unfamiliar. What matters isn't the specific content but the approach: **how a recurring task gets expressed in natural language.**

> Note: the skill's actual body (SKILL.md, templates, code) contains content from official ITU documents and is therefore not published. These prompt examples merely describe the task being requested — they are not ITU document content itself — which is why they can be shared.

---

## A. Contribution development

### A-1. Idea → contribution draft

```
"I want to write a contribution on standardizing AI agent interoperability.
 First lay out the problem statement, gap analysis, and a typical use case,
 then draft an SG13 contribution."
```

### A-2. Contribution proposing a revision to an existing draft Recommendation/Supplement

```
"Clause 6.2 of the attached draft Y.3541 doesn't adequately cover
 AI agent functional requirements. Make a revision-proposal contribution
 with this content. Mark the changed parts as revision marks."
```

### A-3. New NP proposal package

```
"I want to propose an AI agent interoperability framework as a new NP.
 First lay out the problem statement, gap analysis, use case, and
 expected deliverable, then put together a contribution + A.1 justification
 + initial draft outline."
```

### A-4. Peer review of a contribution

```
"Review the attached contribution draft from a peer-review perspective.
 Check whether the standardization need, problem statement, gap analysis,
 and action requested are sufficient, and tell me specifically what
 needs improvement."
```

### A-5. MD → final DOCX generation

```
"Now make it a docx."
"Generate the final contribution as a DOCX."
"Finish it as a Word file for submission."
```

### A-6. Editing/supplementing an existing MD

```
"Add a use case to section 3 of this body.md."
"Clean up the requirement wording in 6.2 using shall/should/may keywords."
"Flesh out the references section."
```

### A-7. New contribution (idea → DOCX)

```
"Draft a contribution related to Y.fAgent"
"Write a contribution on agent architecture for SG13 Q17"
```

### A-8. Step-by-step contribution development

```
"Build a contribution on this topic step by step"
```

### A-9. MD pair → DOCX generation

```
"Make a DOCX from this MD pair"
```

### A-10. Consolidating multiple contributions for comparison

```
"Compare these contributions"
"Make a consolidated contribution"
```

---

## B. Meeting review (Rapporteur/Chair)

### B-1. Contribution review from a Rapporteur's perspective

```
"Review the attached contribution from a Rapporteur's perspective.
 Put together the questions likely to come up in the meeting,
 acceptability, what needs to be requested for revision,
 and a possible meeting decision."
```

### B-2. Drafting a Chair's checklist

```
"Make a Chair's checklist for the attached draft Y.3541."
```

### B-3. Position brief on an external document — v1.5.3

```
"Put together our position on the attached proposal document.
 Review it from a security angle."
```

---

## C. Editor drafting

### C-1. Incorporating a contribution into the draft

```
"Incorporate the content of contribution C-2026-007 into the attached
 draft Y.3541 (base document). The meeting agreed to revise clause 6.3.
 Also write up where it was incorporated, the reason for the change,
 and an editor's note."
```

### C-2. Comparing/consolidating multiple contributions — v1.4.0

```
"Compare the attached base draft Y.3541 with the three contributions
 C-001, C-002, and C-003. Lay out the commonalities, differences, and
 conflicts clause by clause, and propose a consolidated text that
 could work as a compromise."
"Consolidate these contributions, marking which proposing administration
 each change came from."
```

### C-3. Consent readiness review

```
"Review the attached draft Y.3541 ahead of requesting consent.
 Check everything: the Author's Guide, references, definitions,
 abbreviations, any unresolved editor's notes, and the Chair's checklist."
```

---

## D. Liaison Statements

### D-1. LS introducing an initial draft

```
"Make an LS introducing the attached initial draft Y.3541 to
 ISO/IEC JTC 1/SC 42. Include information on the related
 standardization project and a request for their views."
```

### D-4. Drafting the LS body first (recipient not yet decided) — v1.8.3

```
"Write the LS body first based on the attached Y.3600.
 The recipient will be decided at the meeting."
```

### D-2. LS introducing consented text

```
"Make an LS introducing the attached Y.3541 consented text to
 3GPP SA2. Include wording requesting further coordination if needed."
```

### D-3. Reviewing and responding to an incoming LS — v1.5.3

```
"Review the attached incoming LS from SC 42.
 Summarize the main content, action requested, deadline,
 the responsible Question/WP, and whether a response is needed."
```

---

## E. Document quality review

### E-1. Author's Guide verification

```
"Verify the attached draft Y.3541 against the Author's Guide.
 Classify the issues found into errors/warnings/recommendations."
```

### E-2. Style check (lint)

```
"Before turning this body.md into a contribution, check it first for
 any ITU-T style rule violations."
```

### E-3. Automatic correction

```
"Fix everything in the attached draft that can be automatically corrected
 (missing Annex opener, table header style, etc.)."
```

### E-4. Terminology/definition review — v1.4.3

```
Review the following term and definition against Annex B.
If there's an issue, specify which Annex B clause it violates,
and also provide a suggested revision.

3.2.1 agentic AI: an AI system that uses AI agents to perform tasks.
3.2.2 AI agent: a component of agentic AI that executes actions autonomously.
```

### E-5. DEF-08 — Checking a specific term against the ITU Terms DB

```
Check whether "cloud computing" already has a definition in an
ITU-T Recommendation.
If so, tell me the source Recommendation and the original wording
of the definition.
```

### E-6. Real-time SG/Work Programme lookup

```
Check whether there's a work item currently in progress in SG13
on the topic "cloud computing FaaS."
```

### E-9. Feedback on a mismatch with expectations

```
"That's not it. What I expected was substantive critique plus
 a Korean/English direction for the revision."
"That format won't work for the meeting — redo it as 3 sections."
```

---

## F. Other tasks

### F-1. Korean manuscript → contribution translation

```
"Translate the attached Korean manuscript into a draft English SG13
 contribution, using standard ITU-T terminology and phrasing."
```

### F-2. Drafting A.1/A.13 justifications

```
"Based on the attached contribution, make an A.1 NWI justification."
"Make an A.13 justification for revising Y.3541."
```

### F-3. Reference formatting / abbreviation extraction

```
"Format the reference list in this body.md according to
 ITU-T Author's Guide §8.2."
"Automatically extract the list of abbreviations from this body.md."
```

### F-4. Gap analysis — v1.4.2

```
"Do a gap analysis of the current state of AI network management
 standards in the TSAG A.SupplSGA format.
 Cover ITU-T, ISO/IEC, IETF, and ETSI activities."
```

### F-5. DOCX → MD conversion

```
"Convert this docx to md."
"Extract this contribution's content as markdown."
"Pull the text of this Recommendation's body out as text."
```

### F-6. ISO/IEC + IETF standards lookup

```
"Are there any AI agent-related standards in SC 42?"
"How far does SC 38's coverage of cloud computing go?"
"What standards does ISO have related to AI transparency?"
"Tell me the current state of ISO digital twin standards"
"Is SC 42 currently developing any standards?"
"What is ISO/IEC 42001?"
"What is IEC/ISO JTC 3? How does it relate to ITU-T?"
"Fill in the ISO-related work for this A.13"
```

### F-7. IETF I-D/RFC lookup

```
"Find RFC 9110"
"Tell me about the latest HTTP-related IETF I-D"
```

### F-8. ISO/IEC standards lookup

```
"Give me the SC 42 AI standards list"
"Tell me about ISO/IEC 22123"
```

### F-9. ITU MyWorkspace lookup

```
"Look up SG13's recent LSs"
"Give me the list of Q17/13 contributions"
```

### F-10. Question ToR lookup

```
"Tell me Q17/13's ToR"
"Show me SG13's list of Questions"
```

---

## G. JCA-AI meeting reports

### G-1. JCA-AI agenda → draft report (DOCX)

```
"Make a draft meeting report from the attached JCA-AI agenda."
```

### G-2. Checking the JCA report quality gate

```
"Check whether there's anything wrong with the JCA report I just made."
```

---

## H. WP2/13 meeting reports

### H-1. WP2/13 agenda → draft report (DOCX)

```
"Make a draft meeting report from the attached WP2/13 agenda."
```

### H-2. General meeting notes → meeting report

```
"Turn these meeting notes into a meeting report."
"Summarize today's Q17/13 sub-group meeting outcomes."
"Write up this meeting's results as a report."
```

### H-3. Checking the WP2 report quality gate

```
"Check whether the phrase 'Approval of' in the WP2 report I just made
 has been changed to R21."
```

---

## I. SG jurisdiction/scope determination (WTSA knowledge base) *(added from v1.6)*

### I-1. Determining jurisdiction at the Question level

```
"Does this contribution fall under Q17/13 or Q18/13?"
"Which Question(s) of SG13 does contribution C482 overlap with?"
```

### I-2. Determining boundaries between SGs

```
"Does this proposal fall under SG13 or SG20?"
"This contribution came from another SG — point out where it overlaps with SG13"
```

### I-3. Confirming jurisdiction by Recommendation number

```
"Confirm whether Y.3520 falls under SG13"
"Which SG does the Y.4000 series belong to?"
```

### I-4. Drafting a Resolution amendment

```
"Make an amendment to Resolution 98, in the direction of reflecting
 the SG structural change."
"Draft a revision to Resolution 50 — a proposal to expand the
 cybersecurity scope."
```

### I-5. APT WTSA preparatory contribution

```
"Make an APT WTSA preparatory contribution, taking the position
 of defending SG13's jurisdiction over cloud."
```

### I-6. Standalone Question ToR lookup

```
"Pull up the full ToR for Q17/13."
"Show me what Question Q10/20 covers."
"Check the Tasks section of Q18/13."
"Look up the original wording of Q17/13's motivation."
```

### I-7. ITU-T / ISO / IETF data lookup

```
"What's the ITU-T term definition for AI agent?"
"How does SG13 define network slice?"
"Is there an ITU-T definition for 'FaaS'?"
"Tell me the difference between the ITU-T definitions of cloud
 computing and fog computing"
```

---

## J. SG response-logic support *(added from v1.7)*

### J-1. Responding to another SG's contribution — internal email (Mode A)

```
[contribution attached]
"Analyze whether this contribution overlaps with SG13 and write up
 something I can send to the person in charge"
```

### J-2. Constructing an argument from a given conclusion (Mode B)

```
"C482 falls under SG13. Build the argument I can use on the floor"
"This one hits both Q17/13 and Q18/13. Build the supporting rationale"
```

### J-3. Proposing a title revision

```
"Explain why this title conflicts with SG13 and propose a revised title"
"Explain why the subject of this title falls within SG13's scope"
```

### J-4. Responding to a follow-up round

```
"Last time I told them to narrow the scope, and a revision came back.
 The direction is right, but the title is still an issue.
 What should I say this time?"
```

### J-5. International email (English)

```
"Write SG13's position on the FG-City.AI ToR in English"
"An English email recommending the proposer adjust the scope of
 this contribution"
```

### J-6. Differentiated evaluation of a multi-document package

```
"Evaluate C473 and C482 together at the same time"
```

---

## K. AAP domestic review opinions *(added from v1.8)*

### K-1. Consent document → review opinion

```
"Make an AAP review opinion from this consent document. It's AAP-25."
"I'm sending 5 documents to review. Make the review opinion."
"Draft the LC review opinion."
```

### K-2. Preparing a meeting agenda

```
"Prepare the WP2/13 agenda"
"Make a draft report ahead of the meeting"
```

### K-3. Draft LS response

```
"Write a draft response to this LS"
```

### K-4. Processing a received LS and its response

```
"Analyze this LS and also draft a response"
```

### K-5. Full LS handling workflow

```
"Tell me how to handle this LS"
```

### K-6. Generating a meeting report

```
"Write up this meeting's report"
```

### K-7. Korean → ITU English translation

```
"Translate this manuscript into English"
"Turn the Korean contribution into English"
```

### K-8. Upgrade (version upgrade)

```
"(guide MD attached) upgrade to v2.3.3"
"Do the upgrade"
"Bump the version to reflect this change"
```

---

## L. NP defense/attack package *(added from v1.9)*

### L-1. Generating an NP defense package

```
"Make preparation materials for defending the attached Y.aias-reqts
 A.1 at the meeting."
```

---

## M. Policy-comparison-based position derivation *(added from v1.9)*

### M-1. Generating a policy comparison table only

```
Make a table comparing Korea's AI Framework Act, the EU AI Act,
and the US AI EO.
Focus on the parts relevant to ITU-T SG13.
```

### M-2. Comparison table → full pipeline

```
(3 policy documents attached)
Compare Korean, EU, and US AI policy and derive an SG13 NP position.
Go step by step: gap analysis → jurisdiction determination →
position options.
```

### M-3. National-strategy-perspective evaluation

```
(contribution attached)
Evaluate this proposal from a national-strategy perspective.
Which country's policy trend does it follow, and what should
Korea be open to accepting vs. pushing back on?
```

### M-4. Contribution package matrix

```
(5 contributions attached)
Evaluate C480~C484 together as a matrix.
Detect whether they're a series from the same organization, or
a strategy of distributing scope across multiple SGs.
```

### M-5. Strategic/policy analysis of a contribution

```
"Analyze this contribution strategically"
"Lay out the position from a geopolitical perspective"
```

### M-6. Policy comparison → position derivation

```
"Compare Korean, EU, and US AI policy and derive an ITU position"
```

### M-7. Editor-only workflow

```
"Edit this draft from an editor's perspective"
```

---

## How the prompts grew over time

| Period | Categories added |
|------|------------|
| Start | A Contributions · B Review · C Editing · D Liaison Statements · E Quality · F Other · G/H Meeting reports |
| v1.6 | Group I — SG jurisdiction determination |
| v1.7 | Group J — SG response logic |
| v1.8 | Group K — AAP domestic review opinions |
| v1.9 | Group L — NP defense/attack · Group M — policy-comparison-based position derivation |

Every time a new task came up, a new prompt was born, and those prompts accumulated into the skill. The full story is in Chapter 6 and Appendix E of the book.
