# Development History (by Version)

*(한글 버전: [HISTORY.md](./HISTORY.md))*

> This document is reference material for the book "Teaching My 25 Years to AI."
> It records what features were added or changed at each version of the skill.
>
> The original development log includes implementation detail such as function names and code structure. Here, that detail has been stripped away, leaving only **what was added or changed at each version**. Chapter 6 and Appendix E of the book turn this history into a narrative.

---

## Three eras at a glance

| Era | Versions | Character |
|------|------|------|
| Birth, first cycle | v1.0 ~ v1.3.5 | Just make it work + first cleanup (~6 days) |
| Feature explosion | v1.4 ~ v1.8.4 | Rapidly adding new tasks (19 types → 47 types) |
| Verification, structure | v1.8.5 ~ v2.5.0 | Feature freeze, make it robust and long-lasting |

---

## Changes by version

**v1.3.6** (2026-05-27) — Established skill design principles (applied from this version on)

**v1.3.7** (2026-05-27) — Feature reinforcement

**v1.4.0** (2026-05-28) — Added multi-contribution comparison/consolidation feature

**v1.4.1** (2026-05-28) — Feature reinforcement

**v1.4.2** (2026-05-28) — Added gap analysis feature

**v1.4.3** (2026-05-28) — Added terminology/definition review feature

**v1.5** (2026-05-29) — Official organization of 19 prompt types — first stable release

**v1.5.1** (2026-05-30) — Structural improvement (breaking change)

**v1.5.2** (2026-05-31) — Structural improvement (breaking change)

**v1.5.3** (2026-06-01) — Direct conversion of WP2/JCA-AI meeting reports

**v1.6.0** (2026-06-01) — Added SG jurisdiction determination feature (WTSA knowledge base + live ITU-T web reference)

**v1.7.0** (2026-06-01) — Added SG response-logic support feature (constructing arguments from a conclusion)

**v1.8.0** (2026-06-04) — Added AAP domestic review opinion drafting feature

**v1.8.1** (2026-06-04) — Fixed real-world defects in the AAP builder

**v1.8.2** (2026-06-04) — PROC Korean-language localization (batches B-4-2~5)

**v1.8.3** (2026-06-04) — Unified quality gate structure

**v1.8.4** (2026-06-05) — External SDO data integration (ISO/IEC + IETF)

**v1.8.5** (2026-06-06) — ★ Built verification infrastructure — no new features, purely "stop it from breaking." (Turning point)

**v1.9.0** (2026-06-07) — Foundation stabilization + key new capability

**v1.9.1** (2026-06-07) — Structural neutralization — isolated refactoring release

**v1.9.2** (2026-06-07) — Connection/expansion — incremental additions on top of the v1.9.1 foundation

**v1.9.3** (2026-06-07) — Redesigned the routing system into a two-axis model mapping requests to tasks

**v2.0.0** (2026-06-07) — ★ Architecture redesign — single engine + declarative specification

**v2.0.1** (2026-06-07) — Stability/documentation cleanup + reduced deployment files to under 200

**v2.0.2** (2026-06-08) — File structure cleanup — moved README/HISTORY to repo root

**v2.1.0** (2026-06-08) — Began decomposing a monolithic module

**v2.2.0** (2026-06-09) — Phase 2: absorbed report-builder header logic

**v2.3.0** (2026-06-09) — Redesigned the review feature — 4 review modes

**v2.3.1** (2026-06-09) — Added a submission-readiness check feature

**v2.3.2** (2026-06-09) — Infrastructure: made principles persistent + L4 docs-sync gate + automated upgrade workflow

**v2.3.3** (2026-06-10) — D-2 completion: unified display-layer severity vocabulary + extended CHK-4 to .py files

**v2.3.4** (2026-06-10) — Fixed a silent error: missing engine path for sg-contribution contact/body insertion

**v2.3.5** (2026-06-10) — Restored test-infrastructure reliability + swept out remaining silent failures

**v2.3.6** (2026-06-10) — Consolidated duplicate code

**v2.4.0** (2026-06-11) — Single-sourced the routing specification + added generation quality gate

**v2.4.1** (2026-06-11) — F4 — per-contributor tracked-changes attribution

**v2.4.2** (2026-06-11) — Aligned output with expectations — NP review redesign (R1) + captured in-use inconsistencies (R2)

**v2.4.3** (2026-06-11) — Small safety-net/hygiene patches — keyword-only arguments, packaging, .doc handling, unified PROMPTS

**v2.4.4** (2026-06-12) — First pass at structural debt reduction — decomposed main(), declared the checklist, eval infrastructure (S1+S2+S4)

**v2.4.5** (2026-06-12) — Cleared real-world bugs (8 found right before a meeting)

**v2.4.6** (2026-06-12) — Auto-generated the prompt list from a single source

**v2.5.0** (2026-06-13) — Cleared structural debt — module decomposition complete

---

## What this history tells us

Tracing the version numbers down, one pattern stands out. At first, **new features** were added almost every version (v1.4 ~ v1.8.4), and then at one point (v1.8.5) feature additions stop. From there, the same feature set is kept while **structural work** continues (v1.9 ~ v2.5).

That second half — where development kept going even after features stopped — turned out to be what made the skill durable enough for long-term use. Chapter 6 (the four acts of the development journey) and Chapter 7 (rethinking the order of development) discuss what this pattern means in more detail.
