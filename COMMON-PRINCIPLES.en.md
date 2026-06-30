# Common Working Principles

*(한글 버전: [COMMON-PRINCIPLES.md](./COMMON-PRINCIPLES.md))*

> This document is reference material for the book "Teaching My 25 Years to AI."
> It lays out the working principles followed at every version while developing the skill, discussed in the main text Chapter 6 ("Automating the Repetitive Development Work Too") and Appendix G.
>
> These principles started out as a checklist that a human read and followed. As versions progressed, much of it was automated into code. What follows strips out implementation detail so an outside reader can follow the principles themselves. File names and script names are real examples from this particular skill; in your own field, they'll be named differently.

---

## 1. Five core principles

### Principle 1 — Unverified changes are debt

After touching any code, run the tests without exception. Even a one-line fix gets re-verified end to end. Deferring verification only means paying a larger cost later.

> Corresponds to Principle 1 in Chapter 7 of the book.

### Principle 2 — Protect a single source of truth

Information that appears in multiple places — like a version number — gets one designated source (e.g. a `VERSION` file), and everything else is kept in sync with it. Any mismatch is treated as a deployment incident. Information scattered across multiple places will inevitably drift apart.

> Corresponds to Principle 5 in Chapter 7 of the book.

### Principle 3 — No silent errors

Errors are never swallowed silently. When something is missing or wrong, surface specifically what task needed what, and why. A result that looks fine on the surface but is wrong underneath is the most dangerous failure mode.

> The vigilance emphasized repeatedly in Chapters 6 and 7 of the book.

### Principle 4 — Domain judgment outranks code structure

Domain truth is never bent for implementation convenience. When making the code cleaner conflicts with following the field's actual rules correctly, the latter wins.

> Corresponds to Principle 6 in Chapter 7 of the book.

### Principle 5 — Define "done" in code

Whether something was "left out" is never left to human memory. The code itself checks whether everything required for release was included according to the rules, whether the version matches, and whether the file count is within limits. People miss things; code doesn't.

---

## 2. Skill design principles

*(Applied from v1.3.6 onward)*

- **SKILL.md holds only routing logic and output policy.** Detailed rules are split out into a `references/` folder.
- **Requests are processed in the order "user prompt + attachment state → workflow selection → output decision."** (e.g. routing in `SKILL.md` → the matching workflow file → output generation)
- **Natural language is prioritized over CLI options.** Phrases like "as a revision mark," "review this," or "incorporate this" are interpreted before flags like `--type` or `--mode`.
- **The same attached file can yield different outputs depending on the prompt.** The prompt determines the task, not the file.
- **At the draft stage, generate MD + a readiness check first; create the DOCX only after user confirmation.** Never jump straight to the final document.
- **A weak, standalone phrase alone ("take a look," "review this") gets a low confidence score.** The more business context provided alongside it, the more accurately it routes to the right workflow.

---

## 3. Testing — follow the stages in order

Every time code is changed, the following sequence is followed. No step is skipped.

**Step 1: Immediately after a code change**

Run unit and integration tests. (e.g. pytest in `tests/unit/`, `tests/integration/`) Do not proceed if this step fails.

**Step 2: E2E quality tests — mandatory**

Run the full set of prompt scenarios end to end and verify that the output matches intent. If it fails, fix and rerun. (e.g. `tests/e2e/` + full scenario verification via `run_tests.py`)

**Step 2.5: Prompt routing regression test — mandatory**

Confirm that representative prompts still route to the correct workflow. If a new prompt entry was added, this test must be expanded as well. (e.g. `tests/unit/test_prompts_routing.py`)

**Step 3: Full pytest run + save results**

Run the full test suite and keep the results. This becomes the baseline for checking regressions in the next version.

**Step 3.5: Run regression verification infrastructure** *(from v1.8.5 onward)*

Run golden snapshots (L1), structural invariants (L2), and the routing baseline (L3) together in one pass. (e.g. `run_all.py` → any failures block release) Before this tooling existed, this was checked manually.

**Step 4: Add E2E tests for new features**

Any new feature added must come with a matching test. A feature without a test can silently break in a later change.

---

## 4. Packaging principles

The rules followed when building the deployment ZIP. These are taken directly from real practice.

**Must be included in the deployment ZIP:**
- Only the contents of the `skill/` folder
- `PROMPTS.md` / `PROMPTS.ko.md` (required — used for skill registration)

**Must never be included in the deployment ZIP:**
- `tests/`, `eval/`, `logs/`, `dist/` — development-only, not needed by users
- `README.md`, `HISTORY.md` — repo-root only (including these wastes file count in the deployment package)

**★ The 200-file limit** *(mandatory from v2.0.0 onward)*

The skill registration system rejects a ZIP if it contains more than 200 files. Before packaging, always count the number of files (excluding directories) under `skill/` and confirm it's 200 or fewer. If approaching 190, treat it as a warning and look for a structural reduction.

This constraint is what triggered a major structural cleanup in v2.0.1. (See Appendix E of the book.)

---

## 5. Manual verification checklist

Items that automation doesn't catch get checked by hand before release. Below is the checklist used in practice.

### Structure / version

- [ ] Does the `VERSION` file match `__version__` in the code? (e.g. `__version__` in `build_itu_doc.py`)
- [ ] Does the version noted in `SKILL.md` match `VERSION`?
- [ ] Are `PROMPTS.ko.md` and `PROMPTS.md` in sync?
- [ ] Is the file count under `skill/` 200 or fewer?

### Tests / regression

- [ ] Did `run_all.py` (or the equivalent regression script) pass with zero failures?
- [ ] Was an E2E test written for any newly added feature?
- [ ] If a new PROMPTS entry was added, was the routing regression test also updated?
- [ ] Does the same input produce the same output as the previous version? (golden snapshot comparison)

### Deployment packaging

- [ ] Does the deployment ZIP exclude `tests/`, `eval/`, `logs/`, `dist/`?
- [ ] Does the deployment ZIP exclude `README.md`, `HISTORY.md`?
- [ ] Does the deployment ZIP filename follow the naming convention (`ITU-document-creator-<version>.zip`)?
- [ ] Are the full project ZIP (for delivering work product) and the deployment ZIP kept separate?

### Output quality

- [ ] Were 3–5 representative prompts run, and did the output match intent?
- [ ] Do the DOCX output's headers and styling follow the ITU format?
- [ ] Are there any silent failures? Does an error produce a specific message?
- [ ] Does the new feature avoid breaking any existing feature?

### Documentation / history

- [ ] Was this version's change recorded in `HISTORY.ko.md`?
- [ ] Were important design decisions recorded in `CONTRIBUTING.md`?
- [ ] If a new entry was added to `PROMPTS.ko.md`, are the group, number, and version notation correct?

---

## Applying this to your own field

If you find yourself repeatedly building and fixing the same kind of thing, you may need a similar set of common working principles. You probably can't copy the items above verbatim, but you can carry over the structure.

- What verification step do you always run after changing code?
- What must never be left out when you ship something?
- What can code check for you, instead of relying on human memory?

Writing down the answers to these questions is the starting point for your own common working principles.
