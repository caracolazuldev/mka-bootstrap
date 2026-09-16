# Phase 4 knowledge reconciliation close-out (working spec)

Working spec for **M-012**. Promote to approach or archive after acceptance.

Governing stakeholder record: [missives/2026-07-27-mka-knowledge-reconciliation-plan.md](../../missives/2026-07-27-mka-knowledge-reconciliation-plan.md). Session brief: [missives/2026-09-16-knowledge-reconciliation-closeout.md](../../missives/2026-09-16-knowledge-reconciliation-closeout.md).

This milestone **closes knowledge reconciliation**. It does not execute pilots M-008 through M-011.

## Preconditions

1. `feat/phase3-pilot-operationalization` is merged to `main` (commit `f38ae67` or successor). `origin/main` must include BR-006, BR-007, `manifest/pilot-acceptance-contracts.md`, and ROADMAP M-008 through M-011.
2. Work from `main` (or a branch based on that merge). Do not implement this spec on top of Phase 2-only `main`.
3. Do not change bootstrap scripts, skill stubs, or the `main`/`install` branch model unless a later gated milestone says so.

## Remaining plan items

| Plan item | Status | This milestone |
|-----------|--------|----------------|
| Phase 1 import (missives, Karsheft seeds, M-006) | Done | Move M-006 to Completed |
| Phase 2 methodology boundaries (M-007) | Done | Move M-007 to Completed |
| Phase 3 pilot contracts (M-008–M-011, BR-006/007) | Done as *contracts*; pilots themselves remain scoped | Leave M-008–M-011 in Scoping |
| Mapping item 8: maintainer README framing | Open | Decide and implement |
| Mapping item 9: extract domain README wording into indexes | Open | Extract or drop with rationale |
| Phase 4: freeze/archive standalone `mka` | Open | Decide and implement |
| Unmerged methodology keep/archive/drop list | Open | Publish and apply |
| Q3 artifact kit vs existing templates | Open | Confirm or add one follow-on milestone |
| Install overlay contract after overlay-file edits | Open | Verify before merge |

## Recommended keep / archive / drop

Confirm or amend this table, then publish the final table in the close-out missive. Do not leave DoD #1 of the reconciliation plan untestable.

| Source concept | Disposition | Bootstrap home | Rationale |
|----------------|-------------|----------------|-----------|
| Manifest / Architecture / Approach document classes | **Keep** (already merged) | `knowledge-management.md`, `documentation-taxonomy.md`, `manifest/README.md` | Phase 2 complete |
| Text-first knowledge (markdown, optional TOML) | **Keep** (already merged) | `knowledge-management.md` | Phase 2 complete |
| Missives as stakeholder record | **Keep** (already merged) | `missives/` | Matches bootstrap taxonomy |
| Drafting-as-root WIP discipline | **Adapt** | Expand `docs/developer/approach/working-doc-promotion.md` | Same intent as working specs at `docs/developer/`; do not add a `Drafting/` folder |
| Roadmap Releases vs current milestones | **Adapt** | `release/` + Completed stage on `ROADMAP.md` | Bootstrap already splits live work from archived close-outs |
| Missive one-version + time-based archive rule | **Adapt** | Add `missives/README.md` index with the rule | High-velocity domain; bootstrap currently has no missives index |
| Charter / Control as a required top-level domain | **Drop** for this template | n/a | Conflicts with bootstrap taxonomy (`manifest/` + ROADMAP Acceptance). Do not create `Charter/` |
| MKA case-differentiated domain tree (`Charter/`, `Missives/`, …) as layout | **Drop** | n/a | Root-merge hazard; bootstrap layout is canonical |
| `mka` as canonical GitHub home this prototype window | **Drop** | n/a | Topic 7 / standing constraints |
| Full remaining prose of `mka/Conception/mka-product-management-framework.md` (self-directed-team thesis, Control inventory, milestone title-only style) | **Archive** | Leave source in standalone `mka`; optional short pointer from architecture docs | Bootstrap milestone model (M-###, stage markers) already supersedes title-only milestones |
| Karsheft seed notes and gap analysis | **Archive** (already imported) | `docs/developer/references/` | Non-normative |
| Lab copy `.attendant/missives/2026-07-27-pm-methodology.md` | **Archive in Lab** | Not imported here unless a keep item needs a citation | Third copy; do not create a fourth |

## Maintainer README (plan item 8)

**Recommendation:** add a short **Relationship to MKA** section to the *maintainer* `README.md` only.

Include: MKA is the knowledge practice this template dogfoods; canonical execution home for the current prototype window is this repository; Karsheft consumes MKA and remains a dependent ecosystem; audience is internal collaborators.

Do **not** put that framing in `docs/developer/references/templates/install-README.md`. Install README stays a consumer clone/install guide. That keeps the overlay contract intact.

## Artifact kit (Q3 Milestone 2)

Existing stubs already cover Manifest BR index, ROADMAP, missives index, release note, and solution README:

- `docs/developer/references/templates/solution-business-requirements.md.stub`
- `docs/developer/references/templates/solution-ROADMAP.md.stub`
- `docs/developer/references/templates/solution-missives-README.md.stub`
- `docs/developer/references/templates/solution-release-README.md.stub`
- `docs/developer/references/templates/solution-README.md.stub`

**Gap:** no Charter template (dropped as a folder, above) and no Approach-record template.

**Recommendation:** treat current stubs as the artifact kit. If an Approach record is still wanted, add `docs/developer/references/templates/solution-approach-record.md.stub` in this milestone and link it from `docs/developer/approach/`. Do not add a Charter stub.

## Standalone `mka` repo (Phase 4)

Sibling path: `/home/mzd/Lab/mka`.

**Recommendation:** freeze. Add a short note at the top of `mka/README.md`: active development is in `mka-bootstrap`; this repo is an archive of the 2026-07-27 extraction. Do not push `mka` to GitHub as a competing canonical home in this window.

Karsheft pointer is optional follow-up in `/home/mzd/Lab/karsheft` (out of this repo). If touched, state that MKA execution lives in mka-bootstrap, not nested Karsheft docs.

## Install overlay verification

Live diffs from `main` to `install` are typically `README.md`, `ROADMAP.md`, and `manifest/business-requirements.md`. This milestone will edit at least ROADMAP and BRs, and likely the maintainer README.

Before merge:

```bash
./scripts/validate-governance-structure.sh --context main
./scripts/test/run-local-harness.sh all
```

Do **not** run `scripts/publish-to-install.sh` against origin unless this work is part of a sprint close-out release. Harness `publish` is the overlay check.

## Implementation order

1. Confirm Phase 3 is on the branch you are working from.
2. Finalize the keep/archive/drop table in the close-out missive (amend if the recommendation is wrong).
3. Apply Adapt items: working-doc-promotion expansion, `missives/README.md`, optional architecture pointer to archived methodology.
4. Apply README framing (maintainer only).
5. Extract useful index wording (plan item 9) or record drop in the missive.
6. Artifact-kit confirmation or Approach stub.
7. Freeze note in sibling `mka/README.md`.
8. Update this spec’s status; move M-012 to Acceptance when checks pass; leave pilots in Scoping.

## Out of scope

- Implementing pilot functions (M-008, M-009, M-010)
- Cross-pilot friction log and APT interface map (M-011)
- Script, harness, or skill-stub behavior changes
- Root merge of `mka` and `mka-bootstrap` histories
