## Abstraction-first domain modeling

Apply this policy to domain language, game mechanics, requirements, and scenarios, not to code architecture.

1. **Prefer meaningful concepts.** Reuse or identify umbrella concepts and useful intermediate categories instead of repeatedly listing concrete entities. Introduce only distinctions needed by current rules. Preserve the game's own definitions; do not infer behavior from real-world names.

2. **Preserve scope.** A concept, with explicit conditions when necessary, must cover exactly the intended rule. Preserve closed selections, exceptions, quantifiers, concrete examples, and test parameters. Separate subtypes from capabilities, states, and properties; attach behavior to its actual subject.

3. **Use one vocabulary per context.** Follow existing project locations and naming. Read `GLOSSARY-MAP.md` when present and load relevant context glossaries; otherwise use the existing glossary or lazily establish root `GLOSSARY.md`. Map multiple established contexts without duplicating definitions. Do not invent contexts for weapon classes or split files merely because they grew.

4. **Verify against implementation.** For claims about existing or changing domain behavior, inspect relevant code and available tests, or reuse still-valid inspection evidence. Surface every new unresolved material discrepancy for a decision, with both sources. Code describes implemented behavior; approved requirements describe intended behavior. Neither silently overrides the other. Report unavailable evidence or absent implementation; never imply verification.

5. **Preserve agreements.** Capture resolved definitions in the glossary and approved mechanics in the authorized working document as they are settled. During requirement synthesis and reviews of synthesized requirements or materially changed mechanics, check source-to-document coverage and document-to-source support. State missing sources and limitations; the resulting document cannot independently prove its own completeness.

6. **Separate outputs.** Keep definitions compact, including decisive membership boundaries. Keep mechanics in requirements, and analysis and open questions outside the glossary. A supported new name is not a new design decision; proposed changes to meaning or behavior remain unapproved until decided.

7. **Edit within authority.** In writing or improvement tasks, apply supported in-scope documentation corrections without an extra `apply` flag. Analysis-only requests do not authorize edits. Do not silently decide disputed semantics, change code, publish externally, or generate unrelated artifacts.

8. **Work incrementally.** Use `game-domain-concept-discovery` for missing abstractions and `game-abstraction-review` for changed text and source coverage. They complement interactive `domain-modeling`, not a second mandatory modeling process. Reuse valid findings; skip full passes for trivial edits. Inspect affected consumers when definitions change; do not start recursive or project-wide review loops.
