---
name: game-abstraction-review
description: Check and safely improve abstraction use in game mechanics, requirements, and scenarios. Detect redundant lists, misleading categories, lost conditions, unsupported additions, and disagreements with implementation. Verify source-to-document coverage when source decisions are available; apply supported fixes within authorized editing tasks.
---

# Abstraction review

## Scope and editing authority

Review the requested text, affected definitions, and the evidence needed to judge its meaning. Follow the project's abstraction-first policy. Use the existing vocabulary and any relevant `GLOSSARY-MAP.md` routing; do not create a competing glossary or inspect every context. If no glossary exists, establish one lazily only within an authorized writing task; multiple established contexts need a minimal map, not duplicated definitions or a new taxonomy of contexts.

In a task to write or improve documentation, apply supported in-scope corrections. In an analysis-only request, including an evaluation without edit authorization, report suggested changes. Do not ask again for permission already granted. Uncertain semantics require a decision regardless of whether file edits are allowed.

Work incrementally. Reuse still-valid discovery/modeling findings instead of invoking another skill or repeating an interview. Trivial edits need a brief local check, not a full report. Do not change code or publish externally.

## 1. Establish independent evidence

Identify the intended scope and the actual source set: accepted discussion statements, referenced source material, approved requirements, glossary entries, and relevant implementation. Read accessible referenced sources; do not ask the user to repeat information you can retrieve. Avoid unrelated repository searches.

Distinguish agreed facts from proposals, rejected alternatives, and explicitly superseded decisions. Follow declared source authority. Surface unresolved source conflicts instead of assuming code, a newer draft, or an assistant's summary wins. Missing history or inaccessible references remain explicit limitations.

Preserve the pre-edit text as the baseline for an editing-equivalence check. That baseline can show whether an edit loses existing content; it cannot independently prove that an earlier discussion was fully captured. Derive source obligations from the source set, not just from the document being reviewed.

## 2. Verify implementation consistency

For claims about existing or changing behavior, inspect relevant code and available tests, including paths needed to understand the claim. Tests encode expectations; they are not automatic approval of the target design. Reuse earlier evidence only while the relevant code, definitions, and assumptions remain unchanged.

State `checked` with scope and method, `not applicable` for an evidenced absence of implementation, or `not verified` for unavailable/insufficient evidence. A static reading is not a successful test run. No tests is not a reason to skip readable code; an unsuccessful search is not proof of absent implementation.

For every new unresolved material discrepancy, show both the intended rule and code/test evidence, the consequence, and the decision needed. Code describes implemented behavior; approved requirements describe intended behavior. Do not silently rewrite one to match the other. Discuss the conflict interactively, or report it as an unresolved finding and withhold dependent semantic corrections. An already-approved intended change can remain a documented implementation gap; do not repeatedly ask the user to reapprove it. Continue independent safe work.

## 3. Check abstraction quality and rewrite equivalence

Find redundant enumerations, missing umbrella concepts, duplicate terminology, undefined or overloaded names, overbroad/narrow categories, and behavior attached to the wrong subject. Separate subtypes from capabilities, states, and conditions. Do not force independent dimensions into a single classification tree.

Prefer an existing concept, then a concept with explicit conditions, then a new name for an already-supported meaning. New membership or behavior choices remain proposals. Supply necessary definitions in the authorized canonical location.

For each wording correction, check the same entities, actors, permissions, timing, quantities, quantifiers, prerequisites, and exceptions. Seek a counterexample. Matching today's list is not enough to replace a closed selection with a category. Preserve concrete scenarios and test parameters. Do not promote subtype behavior to its parent or replace the game's own semantics with real-world assumptions.

Before changing a canonical definition, inspect relevant uses and known cross-context consumers. Do not partially change a shared meaning whose impact is still unresolved or exceeds the authorized edit scope. Retain the precise wording when no safe abstraction is established.

## 4. Check transfer of agreements in both directions

When reviewing synthesized requirements or materially changed mechanics, build a small, task-local coverage mapping from the independent source decisions. Include conditions, exceptions, quantities, timing, permissions, prohibitions, and agreed exclusions, not merely the names of features. Stable IDs are optional; precise file/section or discussion locators are sufficient. No separate tracking system or new permanent report file is required.

- **Source to document:** locate where each in-scope approved rule is preserved. Multiple source statements may map to one exact generalized rule. Flag omitted or altered meaning; respect explicit superseding decisions and scope boundaries.
- **Document to source:** check support for normative claims and concept boundaries. Mark newly invented or unresolved behavior as a proposal, not an agreed fact.

Use only relevant statuses: `covered`, `missing`, `conflicting`, `unsupported`, or `not checked`. Do not claim coverage of unseen discussion or inaccessible sources. The document alone supports an internal check, not independent completeness.

An unambiguously approved, in-scope omission may be restored during authorized editing. Report it as **restoring an agreed requirement**, not as a wording-only rewrite: this changes the incomplete draft while preserving the agreed design. Do not restore rejected, superseded, contradictory, or out-of-scope material.

## 5. Correct, recheck, and report

Apply supported corrections within authority; preserve IDs and unrelated wording. Do not silently choose among conflicting intentions. Recheck changed fragments and affected definitions once for newly introduced problems, not in an unbounded review cycle. If a required definition or correction lies outside write scope, report that dependency rather than leaving an undefined term.

Return a compact result:
- Corrections made or proposed, distinguishing a **wording-only correction** from **restoring an agreed requirement**.
- **Decision needed** findings with location, both sources where relevant, consequence, and a concrete unresolved choice.
- Evidence coverage: sources actually read, implementation-check status/method, and missing evidence. Show the small coverage mapping when transfer checking is material; otherwise report only relevant gaps and a bounded summary.

Keep findings separate from the permanent glossary. Definitions stay compact; mechanics stay in requirements. Preserve the requested prose language and existing concept identifiers. Do not generate architecture or unrelated artifacts.

## Calibration

- All weapons may be dropped: `weapon` can replace an illustrative list.
- A chest permits exactly pistols and rifles: keep the closed selection.
- Only one weapon mode is instant-hit: do not generalize it to every mode.
- A test specifies a pistol with three rounds: preserve the concrete setup.
- An approved source says swapping interrupts reload, but the draft omits that: restore the condition if authorized; do not claim it is merely shorter wording.
- The draft is the only source: check consistency and editing preservation, but explicitly leave transfer from earlier discussion unverified.
