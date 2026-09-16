# 2026-09-16 Knowledge Reconciliation Close-out

Final keep/archive/drop record for MKA knowledge reconciliation (M-012 / BR-008). This missive replaces the earlier same-day session brief.

Governing plan: [2026-07-27-mka-knowledge-reconciliation-plan.md](2026-07-27-mka-knowledge-reconciliation-plan.md). Working spec: [docs/developer/phase4-reconciliation-closeout.md](../docs/developer/phase4-reconciliation-closeout.md).

## Decisions

- Canonical execution home for the current prototype window is **mka-bootstrap**, not standalone `mka`.
- Repos stay separate. Knowledge moves into bootstrap. Do not merge git histories.
- Do not change installer scripts or the `main`/`install` overlay model in this pass.
- Phase 3 (`feat/phase3-pilot-operationalization`, merged as `0dd8e13`) is complete as *contracts*. Pilots M-008–M-011 remain scoped work.
- Standalone `mka` is **frozen**: archive of the 2026-07-27 extraction. Do not push it to GitHub as a competing canonical home in this window.
- Karsheft pointer is out of this milestone.

## Keep / archive / drop

| Source concept | Disposition | Bootstrap home | Rationale |
|----------------|-------------|----------------|-----------|
| Manifest / Architecture / Approach document classes | **Keep** (already merged) | `knowledge-management.md`, `documentation-taxonomy.md`, `manifest/README.md` | Phase 2 complete |
| Text-first knowledge (markdown, optional TOML) | **Keep** (already merged) | `knowledge-management.md` | Phase 2 complete |
| Missives as stakeholder record | **Keep** (already merged) | `missives/` | Matches bootstrap taxonomy |
| Drafting-as-root WIP discipline | **Adapt** | `docs/developer/approach/working-doc-promotion.md` | Same intent as working specs at `docs/developer/`; no `Drafting/` folder |
| Roadmap Releases vs current milestones | **Adapt** | `release/` + Completed stage on `ROADMAP.md` | Bootstrap already splits live work from archived close-outs |
| Missive one-version + time-based archive rule | **Adapt** | `missives/README.md` | High-velocity domain; one live version per topic |
| Charter / Control as a required top-level domain | **Drop** | n/a | Conflicts with bootstrap taxonomy (`manifest/` + ROADMAP Acceptance). Do not create `Charter/` |
| MKA case-differentiated domain tree (`Charter/`, `Missives/`, …) as layout | **Drop** | n/a | Root-merge hazard; bootstrap layout is canonical |
| `mka` as canonical GitHub home this prototype window | **Drop** | n/a | Standing constraint: execution home is mka-bootstrap |
| Full remaining prose of `mka/Conception/mka-product-management-framework.md` | **Archive** | Leave source in standalone `mka`; short pointer from architecture docs | Bootstrap milestone model (M-###, stage markers) already supersedes title-only milestones |
| Karsheft seed notes and gap analysis | **Archive** (already imported) | `docs/developer/references/` | Non-normative |
| Lab copy `.attendant/missives/2026-07-27-pm-methodology.md` | **Archive in Lab** | Not imported | Third copy; do not create a fourth |

## Plan item 8 — maintainer README

Implemented: **Relationship to MKA** section on the maintainer `README.md` only. Install README stays a consumer clone/install guide.

## Plan item 9 — domain README wording

**Dropped** verbatim extraction of standalone `mka` domain READMEs (`Charter/`, `Manifest/`, `Missives/`, `Roadmap/`, `Docs/`, `Conception/`). Those files are one-paragraph placeholders and would duplicate or conflict with bootstrap indexes.

Useful bits already land in bootstrap homes: missive one-version + archive in `missives/README.md`; Manifest as governance contract in `manifest/README.md`; Conception archive intent as non-normative `docs/developer/references/`.

## Artifact kit

Existing solution stubs remain the Q3 kit. Added `docs/developer/references/templates/solution-approach-record.md.stub` (Approach is a first-class document class). No Charter stub. Missives stub extended with the one-version + archive rule.

## Status

| Phase | Result |
|-------|--------|
| 1 Import | Done |
| 2 Methodology | Done |
| 3 Pilot contracts | Done; M-008–M-011 remain scoped |
| 4 Close-out | Done in M-012 |

Definition of Done for reconciliation: high-value knowledge is merged, archived, or dropped with rationale; mka-bootstrap remains installable; ROADMAP still holds pilot-executable milestones; canonical home is this repository.
