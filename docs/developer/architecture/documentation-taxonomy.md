# Documentation taxonomy

Rules for placing and linking documentation in mka-bootstrap and solution repos bootstrapped from it.

## Placement rules

1. **Business intent and governance contract** → `manifest/` (never mandate implementation approach in BRs)
2. **Business requirements index details** → `manifest/business-requirements.md`
3. **Workflow and delivery rationale** → `docs/developer/approach/`
4. **Technical strategy and standards (solution-agnostic)** → `docs/developer/architecture/`
5. **Feature specs (in progress)** → `docs/developer/` (promote when stable)
6. **End-user content** → `docs/user/` (most complete; may be syndicated)
7. **Operations** → `docs/admin/` (link to user docs; avoid duplication)

## MKA boundary rules

- **Manifest** states what must be governed and achieved.
- **Architecture** states what environment and constraints exist.
- **Approach** states how the chosen solution proceeds.

When a document spans multiple boundaries, split it and cross-link rather than blending classes.

## ROADMAP format

- Stage markers: `# ── Stage Name ──` (Completed, Acceptance, Quality Assurance, In Progress, Sprint, Scoping)
- Milestones: `## M-### Title` only — no epics in `##` slots
- Epics live in `manifest/Deep-Backlog.md`

## Index maintenance

Every domain directory should have a README or index listing its contents. Cross-link upward to manifest and architecture docs.

## Deduplication

User documentation is authoritative for shared end-user topics. Admin and developer docs **refer** to user docs rather than copying content.

## Branch-specific README

| Context | README source |
|---------|---------------|
| `main` (maintainer) | Root README.md — product vision, contributor guide |
| `install` (consumer) | Overlay from `docs/developer/references/templates/install-README.md` |
| Solution (post-install) | From `solution-README.md.stub` with tokens resolved |

## Validation

Run `scripts/validate-governance-structure.sh --context main|install|solution` to verify structure.
