---
name: game-domain-concept-discovery
description: Discover reusable umbrella concepts and intermediate categories for game mechanics and requirements. Use when designing new domain distinctions or normalizing existing descriptions with concrete-item lists. Complements interactive domain-modeling with scoped abstraction checks, code comparison, and explicit boundaries.
---

# Domain concept discovery

## Role and activation

Find the smallest useful vocabulary for the current mechanics. This is an abstraction-focused check, not a replacement for interactive `domain-modeling`. Use it when concepts or membership boundaries are missing or changing, not for ordinary reuse of settled terms. Follow the project's abstraction-first policy.

Infer the task's purpose; no mode flag is required. Without authorization for new design, default to extracting and normalizing existing meanings:
- **Design:** propose alternatives for unresolved concepts; have consequential membership or behavior choices decided before treating them as requirements.
- **Extract and normalize:** name meanings already supported by existing sources. Flag missing design decisions rather than making them through a wording change.

When working alongside `domain-modeling`, limit it to clarifying terms, testing boundaries through scenarios, comparing claims with code, and maintaining glossary definitions. Keep other document edits, publication, and implementation changes outside that skill's scope. Contribute discovery checks to the same session. Let one discussion resolve each issue and one editor maintain each artifact. Reuse source reads and code checks while still valid. Do not automatically invoke another skill, start a second interview, or depend on its installation.

## Locate context and sources

Use the requested scope and project-authoritative material. Read supplied or referenced requirements, accepted discussion decisions, and relevant definitions. Distinguish approvals, proposals, rejections, and explicit superseding decisions; do not infer approval from silence or from a draft's confident wording.

Honor existing locations. If root `GLOSSARY-MAP.md` exists, follow it to the relevant context glossary and affected related definitions; do not load every context. Otherwise use the existing glossary. For an authorized documentation task with no glossary, create root `GLOSSARY.md` only when the first supported term is ready. When multiple contexts are already established, place terms in their existing locations and add a minimal root map only within write authority. The map records context scope, glossary paths, and known relationships, not duplicate definitions. Do not invent contexts from subclasses or folder names. Resolve ambiguous ownership before writing the affected term; continue unrelated work.

## Procedure

1. **Extract the current distinctions.** Identify entities, actions, relationships, properties, states, and rules. Distinguish examples from closed selections. Keep concise source locators for facts you rely on: requirement IDs, file and section, code symbols, or identifiable accepted statements from the discussion.

2. **Perform the implementation check.** When the topic concerns existing or changing domain behavior, inspect the relevant implementation paths and available tests. Tests are evidence of encoded expectations, not automatic approval of game design. Follow dependencies needed to interpret the claim, without auditing unrelated code. Reuse an earlier check only if its relevant sources have not changed. Pure terminology edits may reuse that evidence.

   Mark the check as `checked` (state scope and static inspection versus execution), `not applicable` (no implementation yet, with a basis), or `not verified` (unavailable or insufficient evidence). Failure to find code is not by itself proof that it does not exist. Missing tests do not prevent code inspection.

   Bring every new unresolved material mismatch into the discussion: show the intended rule, the code/test evidence, its consequence, and the decision needed. Code describes what is implemented; approved requirements describe what is intended. Do not silently make either conform to the other. An explicitly approved future change is a known implementation gap, not a question to reopen. Without an interactive decision, report the conflict and leave dependent semantic changes unresolved; continue supported work.

3. **Reuse and generalize.** Find existing concepts before naming new ones. Look proactively for missing umbrella and intermediate categories needed by a current shared rule. A concept needs meaningful membership criteria, not just today's example list. One member is sufficient if a current rule needs the distinction; hypothetical extensibility alone is not.

4. **Choose boundaries and ownership.** Distinguish `is-a` categories from capabilities, conditions, states, and intentionally named closed sets. Put a property on its actual subject, such as an attack mode rather than every use of a weapon. Keep independent dimensions separate. Do not assume sibling categories are exclusive or exhaustive. Respect fictional project definitions.

5. **Test each useful candidate.** Rewrite a representative rule and probe a boundary or counterexample. Would it improperly include another member, remove an exception, or turn a closed list into an open category? Preserve conditions, quantifiers, and concrete test data. Label invented probe scenarios as hypothetical, not new content. Before changing an existing definition, inspect relevant use sites and known cross-context consumers; defer changes whose wider impact is unresolved or outside authorized scope.

6. **Resolve and capture.** Distinguish `Existing`, `New term` (a supported meaning given a name), and `Proposal` (new or changed semantics). In design work, offer a small set of meaningful alternatives and ask only consequential unresolved questions. In extraction work, preserve uncertain boundaries as findings. Never restart already-resolved questions without new evidence.

   In an authorized writing task, save supported definitions and approved mechanics as they settle: definitions in the canonical glossary, mechanics in the relevant working requirements or draft. Preserve decision status and source locators where needed for a later handoff. If that destination is absent or not writable, return a compact handoff listing the working documents and sections, approved rules not yet transferred with their key conditions, open questions, rejected or superseded alternatives, and limits of the checks. Do not treat the glossary as storage for the discussion. Report any source material you could not inspect.

## Editing and output

Apply supported documentation changes within an editing task's authorized scope; for analysis-only requests, return proposals without writes. A skill invocation does not override read-only or scope limits. Do not modify implementation, publish externally, or generate unrelated artifacts.

Return only useful deltas: concept, status, concise meaning/boundary, source basis, and a representative rewrite when helpful. Include actionable unresolved choices and implementation/source-check limitations. Do not print unchanged concepts or force empty report sections.

The permanent glossary contains compact definitions (normally one or two sentences), relevant distinguishing boundaries, and genuinely confusing aliases when useful. Procedural rules, numerical balance values, evidence tables, exploratory examples, and unresolved proposals belong in requirements or the transient report instead. Use project naming conventions and the requested prose language; otherwise prefer singular English snake_case for concept identifiers.

Stop when this task has sufficient supported vocabulary or the remaining questions are clearly identified. Do not run a full discovery pass again after the same concepts have already been resolved in the shared modeling session.
