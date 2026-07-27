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

## M-008 Pilot Alpha: Product Manager & Implementation Manager (Agentic MKA)

Operationalize the Product Manager and Implementation Manager pilot as the first execution lane for MKA-first delivery. The pilot must prove governance and implementation tracks can remain distinct while interleaving through roadmap state.

Done when:
- A pilot acceptance contract is documented in `manifest/pilot-acceptance-contracts.md`.
- At least one worked example shows Product-vs-Implementation handoff via MKA artifacts.
- A prototype package descriptor and dependency note exists for internal containerized installation.
- Validation evidence is logged in `missives/`.

## M-009 Pilot Beta: Google Collaboration Suite (Docs/Sheets/Slides/Drive/Calendar/Tasks)

Operationalize collaborative tooling contexts for human-agent workflows across Google collaboration surfaces, using markdown-sync utilities as implementation foundations.

Done when:
- A pilot acceptance contract is documented in `manifest/pilot-acceptance-contracts.md`.
- Capability boundaries and workflow context model are documented and testable.
- At least one collaboration capability bundle is prepared for package-style installation and internal testing.
- Validation evidence is logged in `missives/`.

## M-010 Pilot Gamma: Meeting Secretary Function

Operationalize a narrowly scoped meeting secretary function that captures concise outcomes and converts discussions into actionable project artifacts.

Done when:
- A pilot acceptance contract is documented in `manifest/pilot-acceptance-contracts.md`.
- Meeting output templates and summary-to-action rules are defined.
- A prototype package path is documented and tested for consistent invocation in containerized workflow.
- Validation evidence is logged in `missives/`.

## M-011 Cross-pilot validation synthesis and rollout recommendation

Consolidate pilot results into a friction log and rollout memo, with explicit recommendations on next-sprint standardization scope.

Done when:
- A cross-pilot friction log exists with categories for process, tooling, packaging, and collaboration.
- An MKA-to-APT interface map is documented.
- A next-phase recommendation memo is published in `missives/`.

<!-- Next sprint milestones go here as ## M-### Title -->
