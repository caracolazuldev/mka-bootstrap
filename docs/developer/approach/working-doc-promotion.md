# Working document promotion

Checklist for graduating an in-progress spec from `docs/developer/` working status to a stable home.

WIP belongs at `docs/developer/` top level. Do **not** add a `Drafting/` folder. That top-level slot is the bootstrap equivalent of MKA drafting-as-root: messy in-progress work is allowed there, and it must be promoted, merged, or dropped rather than left to accumulate.

## When to promote

- Acceptance criteria are defined and testable
- Content is no longer expected to change daily
- Links from manifest BRs or ROADMAP milestones exist

## Promotion checklist

1. **Classify** — approach (rationale), architecture (constraints), or user/admin (audience-facing)?
2. **Move or merge** — relocate to the correct layer; do not leave duplicate copies
3. **Update indexes** — domain README, manifest links, ROADMAP milestone body
4. **Dedupe** — if user-facing, ensure admin/dev docs link rather than repeat
5. **Validate** — `validate-governance-structure.sh --context main`

## Naming

Use kebab-case filenames. Prefer descriptive names over ticket IDs in filenames.

## WIP hygiene

- Completed or abandoned drafts should leave `docs/developer/` top level.
- Historic brainstorms do not stay as working specs; digest them into approach/architecture or a missive, then remove the working copy.
- After milestone acceptance, promote the spec or archive it (release note + pointer). Do not keep a second live copy.

## Anti-patterns

- Leaving stale working copies after promotion
- Adding a `Drafting/` (or similar) root folder
- Putting epics directly on ROADMAP as `##` headings
- Duplicating user documentation in admin docs
