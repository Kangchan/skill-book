# Teaching My 25 Years to AI — Reference Materials

*(한글 버전: [README.md](./README.md))*

This repository contains reference materials for the book **"Teaching My 25 Years to AI — A Domain Expert's Field Notes on Building AI Skills"** (『나의 25년을 AI에게 가르치다』).

The book follows a telecommunications standardization expert as he turns 25 years of professional experience into an AI skill. ITU-T standardization work serves as the case study, but the core of the story is a universal method: **how do you translate domain expertise in any field into an AI skill?**

---

## Who this book is for

I wrote this book with two kinds of readers in mind.

**Leaders considering adopting skills in their organization** — so that even without writing code or building a skill themselves, they can judge what an AI skill is and whether it's worth adopting.

**Practitioners who want to build a skill themselves** — so they can see what questions to ask and how to design a skill when translating domain knowledge into one.

The main text is written to be accessible to anyone, and this repository holds the underlying material for readers who want to go deeper.

---

## Materials in this repository

| File | Content | Where it connects in the book |
|------|------|-------------------|
| [PROMPTS.en.md](./PROMPTS.en.md) | Real prompt examples given to the skill (70+ tasks, by category) | Chapter 6, Appendix E |
| [HISTORY.en.md](./HISTORY.en.md) | Version-by-version history of features added and changed (v1.3.6 ~ v2.5.0, 42 versions) | Chapter 6, Appendix E |
| [COMMON-PRINCIPLES.en.md](./COMMON-PRINCIPLES.en.md) | The common working principles followed at every version, plus a manual verification checklist | Chapter 6, Appendix G |

All of these materials are about **how the skill was built and managed** — not the *content* of the standards documents the skill processes, but a record of *how it was developed*.

**PROMPTS** is a collection of real input examples — "here's how you'd phrase it in this situation." **HISTORY** is a version-by-version record showing how features kept being added whenever a new task came up, and the point at which that stopped and the focus shifted to solidifying the structure instead. **COMMON-PRINCIPLES** is the checklist built to make sure nothing was missed with each version bump — something a human first read and followed by hand, and later something the code ran automatically.

---

## What is not published, and why

The body of the skill itself — the full specification (SKILL.md), document templates, and processing code — is not published in this repository.

The reason for that is itself one of the lessons of this book. I built this skill based on official ITU (International Telecommunication Union) documents — drafting guidelines, templates, procedural rules — and it contains portions of that content. Since this is ITU's intellectual property, publishing the full skill would amount to redistributing that material.

**When you move domain knowledge into an AI skill, you have to look carefully at the copyright and licensing in that field.** Some knowledge can be freely carried over; some knowledge requires respecting the rights of its source. What this repository does and does not include is one example of that distinction.

I designed and wrote the three materials published here (PROMPTS, HISTORY, COMMON-PRINCIPLES) myself, and they do not contain the content of ITU documents.

---

## Version of these materials

The materials in this repository are current as of the time the book was written (skill v2.5.0).

---

## About the book

- **Title**: 나의 25년을 AI에게 가르치다 (Teaching My 25 Years to AI)
- **Subtitle**: 도메인 전문가의 스킬 개발 실전기 (A Domain Expert's Field Notes on Building AI Skills)
- **GitHub**: https://github.com/Kangchan/skill-book
