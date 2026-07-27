# Manifest

Governance and business-requirements artifacts for mka-bootstrap (maintainer context on `main`).

In MKA terms, Manifest is the governance contract and includes or references the business requirements index. Architecture and Approach remain separate document classes under `docs/developer/architecture/` and `docs/developer/approach/`.

## BR ↔ milestone matrix

| BR | Milestone | Description | Done when |
|----|-----------|-------------|-----------|
| BR-001 | M-001 | Documentation taxonomy enforced | `validate-governance-structure.sh --context main` passes |
| BR-002 | M-002 | Milestone workflow + agent skills routable | `sync-skill-stubs.sh --check` passes |
| BR-003 | M-003 | Install/bootstrap scripts produce valid solution repo | `./scripts/test/run-local-harness.sh bootstrap` passes |
| BR-004 | M-004 | `install` default branch publishable from `main` | `./scripts/test/run-local-harness.sh publish` passes |
| BR-005 | M-005 | Consumer clone + install.sh path verified end-to-end | GitHub install + mka-solution-testing documented |

## Contents

| File | Purpose |
|------|---------|
| [business-requirements.md](business-requirements.md) | BR-### acceptance criteria |
| [personas.md](personas.md) | Maintainer and consumer personas |
| [roadmap-processes.md](roadmap-processes.md) | Sprint cadence and release workflow |
| [glossary.md](glossary.md) | Shared terms |
| [Deep-Backlog.md](Deep-Backlog.md) | Epics and future themes (not ROADMAP `##` slots) |
