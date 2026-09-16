# 2026-07-27 MKA Knowledge Reconciliation Plan

Imported from Lab `.attendant/missives/` as the governing stakeholder record for knowledge reconciliation. Status as of 2026-09-16: Phases 1–3 are executed in this repository; remaining close-out is M-012. See [2026-09-16-knowledge-reconciliation-closeout.md](2026-09-16-knowledge-reconciliation-closeout.md) and [docs/developer/phase4-reconciliation-closeout.md](../docs/developer/phase4-reconciliation-closeout.md).

## Decision Context

Canonical execution repository: mka-bootstrap.

Goal: reconcile high-value MKA knowledge artifacts from mka into mka-bootstrap without disrupting existing bootstrap/install functionality.

## Standing Constraints (from consolidation review)

Canonical execution home is mka-bootstrap for the current prototype window. Repos stay separate; knowledge moves into bootstrap. This is not a history merge.

Rejected alternatives:
- Staged import of bootstrap into mka under a `bootstrap-engine/` prefix.
- Direct root merge of the two histories.
- Cherry-pick scripts into mka while leaving knowledge split.

Why not a root merge (still binding):
- Parallel domain trees (`Manifest` vs `manifest`, `Missives` vs `missives`, `Docs` vs `docs`) would split governance authority.
- File overlap is small (practically `README.md`), but naming conventions would create conceptual duplication.

Install branch is an overlay, not a separate product tree. Live diffs from `main` are typically:
- `README.md`
- `ROADMAP.md`
- `manifest/business-requirements.md`

Knowledge edits to those files must be published through the existing overlay contract. Do not treat ROADMAP or BR updates as "docs-only" if they change the consumer install surface.

Bootstrap operational surface to leave intact unless a later milestone explicitly gates a change:
- `install.sh`
- `scripts/bootstrap-solution.sh`
- `scripts/publish-to-install.sh`
- `scripts/validate-governance-structure.sh`
- `scripts/sync-skill-stubs.sh`
- `docs/developer/references/templates/`
- `scripts/test/` harness

## Scope

In scope:
- Governance and methodology knowledge from mka.
- Pilot-planning artifacts relevant to current 4-6 week objectives.
- Historical/seed materials that support traceability.

Out of scope:
- Replacing or restructuring working bootstrap scripts in this pass.
- Renaming mka-bootstrap core taxonomy or branch model.
- Large cross-repo code moves without milestone gating.

## Reconciliation Principles

1. Preserve operational continuity first.
2. Merge by intent, not by filename parity.
3. Keep one authoritative location per concept after merge.
4. Archive superseded drafts rather than deleting context.
5. Keep all changes milestone-scoped and testable.

## Source-to-Destination Mapping

### A. Foundational Methodology

1. Source: mka/Conception/mka-product-management-framework.md
- Destination: mka-bootstrap/docs/developer/architecture/knowledge-management.md
- Action: merge concepts into architecture guidance, preserving bootstrap branch-context details already present.
- Additional destination: mka-bootstrap/docs/developer/approach/milestone-workflow.md
- Action: align milestone semantics where needed.

2. Source: mka/Docs/mka-methodology-baseline.md
- Destination: mka-bootstrap/docs/developer/architecture/documentation-taxonomy.md
- Action: merge domain distinctions (Manifest, Architecture, Approach) and text-first database posture.

### B. Pilot and Strategy Artifacts

3. Source: mka/Missives/2026-07-27-pilot-project-portfolio.md
- Destination: mka-bootstrap/missives/2026-07-27-pilot-project-portfolio.md
- Action: import as stakeholder record.
- Additional destination: mka-bootstrap/ROADMAP.md
- Action: convert portfolio into 2 to 4 concrete M-### milestones under Scoping.

4. Source: mka/Roadmap/2026-Q3-prototype-roadmap.md
- Destination: mka-bootstrap/ROADMAP.md
- Action: merge as scoped milestones, preserving existing completed milestone history.

5. Source: mka/Missives/2026-07-27-kickoff-note.md
- Destination: mka-bootstrap/missives/2026-07-27-mka-standalone-kickoff-context.md
- Action: archive as context note, labeled historical.

### C. Seed/Research Traceability

6. Source: mka/Conception/karsheft-mka-gap-analysis-seed.md
- Destination: mka-bootstrap/docs/developer/references/karsheft-mka-gap-analysis-seed.md
- Action: import reference document; no normative authority.

7. Source: mka/Conception/karsheft-mka-seed-notes.md
- Destination: mka-bootstrap/docs/developer/references/karsheft-mka-seed-notes.md
- Action: import reference document; no normative authority.

### D. Repo-level framing docs

8. Source: mka/README.md
- Destination: mka-bootstrap/README.md
- Action: selectively merge strategic framing language about MKA as independent framework, while retaining maintainer/consumer branch guidance.

9. Source: mka/Charter/README.md, mka/Manifest/README.md, mka/Missives/README.md, mka/Roadmap/README.md, mka/Docs/README.md, mka/Conception/README.md
- Destination: mka-bootstrap docs/manifest/missives indexes
- Action: do not copy verbatim. Extract useful wording into existing index files where it improves clarity.

## Execution Plan

### Phase 1: Import and Preserve (Low Risk)

1. Copy pilot and kickoff missive files from mka into mka-bootstrap/missives with historical naming.
2. Copy seed/reference docs into mka-bootstrap/docs/developer/references/.
3. Open one milestone in ROADMAP Scoping for reconciliation effort.

Acceptance checks:
- No script changes yet.
- validate-governance-structure passes for current context.

### Phase 2: Integrate Methodology (Medium Risk)

1. Merge mka methodology baseline and framework distinctions into:
- knowledge-management
- documentation-taxonomy
2. Update manifest references if requirements language changes.

Acceptance checks:
- Documentation remains internally consistent.
- Skill routing remains unaffected.

### Phase 3: Operationalize Pilot Plan (Medium Risk)

1. Translate pilot portfolio into M-### milestones in ROADMAP.
2. Add explicit acceptance criteria referencing:
- MKA artifact usage
- APT packaging validation path

Acceptance checks:
- ROADMAP contains actionable milestone units.
- milestone-lifecycle conventions remain valid.

### Phase 4: Optional Consolidation (Deferred)

1. Evaluate whether mka repo remains as archive or is frozen.
2. If frozen, add a simple note in mka README indicating active development in mka-bootstrap.
3. Record an explicit keep/archive/drop list for MKA methodology that was not merged (Drafting, Charter/Control, missive versioning, Milestones vs Releases) before calling reconciliation done.

Acceptance checks:
- Team has one clear canonical implementation repo.
- Unmerged methodology has a keep, archive, or drop rationale.

## Risks and Mitigations

Risk: Concept drift between imported MKA narrative and bootstrap branch mechanics.
- Mitigation: keep branch model sections untouched unless explicitly refactored.

Risk: ROADMAP bloat from portfolio-level language.
- Mitigation: enforce milestone decomposition into finite M-### items.

Risk: Documentation duplication.
- Mitigation: designate authoritative files at merge time and archive alternatives.

Risk: Knowledge edits to ROADMAP or business requirements drift the install overlay.
- Mitigation: after any change to overlay files, republish or explicitly confirm install-branch contract still holds.

## Proposed First Milestones in mka-bootstrap

Historical proposal from 2026-07-27 (numbering later followed execution phases, not this list):

- M-006 Reconcile MKA methodology baseline into bootstrap architecture docs.
- M-007 Ingest pilot portfolio and define 4-6 week prototype milestone set.
- M-008 Define PM/IM, Google Collaboration, and Meeting Secretary pilot acceptance contracts.

As executed: M-006 = Phase 1 import; M-007 = Phase 2 methodology; M-008–M-011 = pilots and synthesis; M-012 = Phase 4 close-out.

## Definition of Done for Reconciliation

1. All high-value knowledge from mka is either merged, archived, or intentionally dropped with rationale.
2. mka-bootstrap remains fully installable and validated.
3. ROADMAP includes pilot-executable milestones for internal collaborators.
4. No unresolved ambiguity on canonical project home.
