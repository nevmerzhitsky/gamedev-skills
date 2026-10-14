# Abstraction-first domain modeling

This package adds two game-domain modeling skills and a policy fragment to an existing agent setup. Use this README for setup and a quick view of how the tools fit together; the policy and skill files contain their operating instructions.

## Package contents

- [AGENTS.fragment.md](AGENTS.fragment.md)
- [skills/game-domain-concept-discovery/SKILL.md](skills/game-domain-concept-discovery/SKILL.md)
- [skills/game-abstraction-review/SKILL.md](skills/game-abstraction-review/SKILL.md)

## Installation

Install both skills from this GitHub repository with the [`skills` CLI](https://github.com/vercel-labs/skills):

```sh
npx skills add https://github.com/nevmerzhitsky/gamedev-skills
```

The CLI installs the skills; it does not add the policy fragment. Append `AGENTS.fragment.md` to the existing `AGENTS.md`; do not replace that file.

For manual installation, copy both skill directories to the location used by your agent. Preserve the directory names, nested `SKILL.md` files, and their YAML metadata. For applications that accept skills as prompts rather than installed directories, copy a skill body without its initial YAML block.

The skills installation path and invocation method depend on the agent application.

## Choosing a workflow

| Task | Start with |
| --- | --- |
| Clarify an unsettled concept | A modeling discussion; `domain-modeling` may help when available. |
| Find a missing umbrella or intermediate concept | `game-domain-concept-discovery`, within the same discussion or as a focused check. |
| Write a rule using settled concepts | The policy in `AGENTS.md`; a new modeling discussion is usually unnecessary. |
| Check or correct a written mechanic, requirement, or scenario | `game-abstraction-review` on the affected text and its relevant sources. |

### New or substantially changing mechanic

```text
Task, decisions, and existing definitions
                    v
Modeling discussion, with domain-modeling when useful
+ discovery checks for missing shared concepts
                    v
Definitions -> glossary; agreed mechanics -> working document
                    v
Draft or refine the mechanic
                    v
Review the changed material
```

### Existing text that needs generalization

```text
Existing text + related definitions and relevant code
                    v
Discovery: extract and normalize the current model
                    v
Update the affected glossary entry or working text
                    v
Review the affected material
```

## Example coverage check

The review skill defines the coverage statuses. This hypothetical example shows what a small result can look like:

| Source decision or claim | Check result |
| --- | --- |
| Switching weapons takes 0.5 seconds | The duration appears in the weapon-switching section: `covered`. |
| Switching weapons interrupts reloading | The condition is absent from the document: `missing`. |
| The document adds invulnerability while switching weapons | No supporting source was found: `unsupported`. |

## Prompt starters

```text
We are designing <mechanic>. Use domain-modeling if available and include game-domain-concept-discovery in the same discussion. Working documents: <glossary and mechanic section>.
```

```text
Apply game-domain-concept-discovery to <section> to extract and normalize the existing model. Sources: <requirements and definitions>. Editable files: <paths, or analysis only>.
```

```text
Apply game-abstraction-review to <section> using <source decisions and related definitions>. Editable files: <paths, or analysis only>.
```

## Dependencies

This archive does not include Matt Pocock's third-party `domain-modeling` skill, its installer, or application-specific settings. Installing this package does not install or configure them. The agent-facing instructions for working alongside that skill are in `skills/game-domain-concept-discovery/SKILL.md`.
