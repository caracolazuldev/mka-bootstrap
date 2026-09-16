# 2026-09-16 Knowledge Reconciliation Close-out Brief

## Decision

Push and merge `feat/phase3-pilot-operationalization` to `main` **before** implementing remaining reconciliation work.

Phase 3 is one commit (`f38ae67`) ahead of the Phase 2 `main` tip. It adds pilot acceptance contracts, BR-006, BR-007, and ROADMAP M-008 through M-011. That work is complete as *operationalization*, not as pilot execution. Starting M-012 from Phase-2-only `main` would drop those artifacts.

PR create link: https://github.com/caracolazuldev/mka-bootstrap/pull/new/feat/phase3-pilot-operationalization

After that merge, implement **M-012** from `main` using the working spec.

## Selected approach (reaffirmed)

- Canonical execution home: this repository, for the current prototype window.
- Repos stay separate. Knowledge moves from standalone `mka` into bootstrap. Do not merge git histories.
- Do not change installer scripts or the `main`/`install` overlay model in this pass.

Governing plan: [2026-07-27-mka-knowledge-reconciliation-plan.md](2026-07-27-mka-knowledge-reconciliation-plan.md).

## Status

| Phase | Result |
|-------|--------|
| 1 Import | Done. Pilot/kickoff missives and Karsheft seeds are in-tree. |
| 2 Methodology | Done. Manifest / Architecture / Approach boundaries are in architecture and taxonomy docs. |
| 3 Pilot contracts | Done on the Phase 3 branch. Pilots M-008–M-011 remain scoped work. |
| 4 Close-out | Open. This is M-012. |

## Next session: implement M-012

Read in order:

1. `manifest/business-requirements.md` (BR-008)
2. `ROADMAP.md` milestone M-012
3. `docs/developer/phase4-reconciliation-closeout.md`

That spec includes a recommended keep/archive/drop table, maintainer-README framing, artifact-kit confirmation, standalone `mka` freeze note, and overlay verification commands.

Out of scope for that session: implementing pilots M-008–M-011 or changing bootstrap scripts.
