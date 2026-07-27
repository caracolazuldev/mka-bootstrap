# ── Completed ──

## M-001 Establish documentation taxonomy, indexes, and Deep Backlog

Closed in v0.1.0. See [release/v0.1.0.md](release/v0.1.0.md).

## M-002 Author governance skills, platform stubs, and AGENTS.md

Closed in v0.1.0. See [release/v0.1.0.md](release/v0.1.0.md).

## M-003 Implement install.sh, bootstrap-solution.sh, init, validate, sync-skill-stubs

Closed in v0.1.0. See [release/v0.1.0.md](release/v0.1.0.md).

## M-004 Implement publish-to-install.sh; establish main/install branch model

Closed in v0.1.0. See [release/v0.1.0.md](release/v0.1.0.md).

## M-005 Publish v0.1.0; dogfood install path → mka-solution-testing

Closed in v0.1.0. Reference install documented in [missives/2026-06-09-mka-solution-testing-reference-install.md](missives/2026-06-09-mka-solution-testing-reference-install.md).

# ── Scoping ──

## M-006 Reconcile MKA knowledge artifacts (Phase 1 import)

Import low-risk knowledge artifacts from the standalone mka repository into mka-bootstrap without changing bootstrap/install mechanics. This milestone covers missive context imports, seed reference preservation, and traceability setup for subsequent methodology integration work.

Done when:
- Pilot and kickoff missives are imported under `missives/`.
- Karsheft seed references are imported under `docs/developer/references/`.
- `scripts/validate-governance-structure.sh --context main` passes.

## M-007 Reconcile MKA methodology boundaries (Phase 2 integration)

Integrate MKA distinctions across architecture and taxonomy guidance so Manifest, Business Requirements Index, Architecture, and Approach remain explicit and auditable document classes.

Done when:
- `docs/developer/architecture/knowledge-management.md` defines MKA boundary distinctions.
- `docs/developer/architecture/documentation-taxonomy.md` includes placement and split rules for Manifest, Architecture, and Approach.
- `manifest/README.md` reflects governance-contract semantics and cross-links the boundary model.
- `scripts/validate-governance-structure.sh --context main` passes.

<!-- Next sprint milestones go here as ## M-### Title -->
