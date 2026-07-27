# MKA Gap Analysis and Bootstrap Sequencing

**Milestone:** M2 — MKA Gap Analysis and Bootstrap Sequencing
**Team:** Gap Analysis Team (Archivist · Gap Analyst · Sequencer)
**Status:** Draft

---

## Part 1: Inventory of Achieved Components

*Persona: Archivist*

### Foundational Documents (Locked Archive)

| Component | Location | Status |
|-----------|----------|--------|
| MKA framework | [Conception/mka-product-management-framework.md](../../Conception/mka-product-management-framework.md) | Complete (locked) — defines knowledge domains, milestone lifecycle, text-first philosophy |
| Core brainstorm | [Conception/Brainstorm.md](../../Conception/Brainstorm.md) | Complete (locked) — working thesis, 6 core concepts, 11 foundational principles, 5-layer cross-walk model, 3 meta packages, 5-phase bootstrap roadmap, 6 next documents |
| Mythology foundation | [Conception/Mythology/](../../Conception/Mythology/) | Complete (locked) — Karsheft-report.md (6 mythological traits), pronunciation guide, Persian source notes |
| Minimal JS Framework | [Conception/Minimal JS Framework.md](../../Conception/Minimal%20JS%20Framework.md) | Complete (locked) — Directus + Vite + Vanilla JS proto-widget pattern |

### Active Project Infrastructure

| Component | Location | Status |
|-----------|----------|--------|
| Brainstorm manifest | [Brainstorm/README.md](../README.md) | Complete — 12 brainstorm projects, all with team assignments |
| Project roadmap | [Roadmap.md](../../Roadmap.md) | Active — 10 milestones, Sprint 1 in progress (M1–M4) |
| Brainstorm subfolders | [Brainstorm/*/](../) | Complete — 12 subfolders, each with README.md |
| Seed notes | 7 subfolders | Complete — mka-roadmap, apt-container-poc, package-system-design, cross-walk-interop, mempalace-mka-integration, trust-security-licensing, developer-experience |

### Reference Implementation

| Component | Location | Status |
|-----------|----------|--------|
| MemPalace | [Research/mempalace/](../../Research/mempalace/) | Functional — hierarchical memory system (Wings→Rooms→Closets→Drawers), pluggable backends, entity detection, knowledge graph, conversation mining |

### M1 Deliverables (Sprint 1, Phase 1)

| Component | Location | Status |
|-----------|----------|--------|
| Agent execution model | [project-teams/agent-execution-model.md](../project-teams/agent-execution-model.md) | Complete — session constraints, communication, instantiation, supervision, tools documented |
| MKA generalization | [project-teams/mka-generalization.md](../project-teams/mka-generalization.md) | Complete — validated against Theaters; terminology mapping produced; recommends single generalized framework |
| Charter template | [project-teams/charter-template.md](../project-teams/charter-template.md) | Complete — reusable template with composition, memory seeds, scope, coordination, constraints |
| Pilot sprint report | [project-teams/pilot-sprint-report.md](../project-teams/pilot-sprint-report.md) | Complete — M2 charter instantiated; template evaluated; 3 minor refinements identified |

---

## Part 2: Gap Assessment

*Persona: Gap Analyst*

### 6 "Immediate Next Documents" (from Conception/Brainstorm.md)

| Document | Status | Addressed By | Severity |
|----------|--------|-------------|----------|
| Project charter | **Not created.** The Roadmap + brainstorm READMEs serve a similar purpose but no formal charter document exists. | No dedicated milestone. Consider adding to M1 scope or creating as part of Sprint Review. | Low — functional equivalent exists across multiple files |
| Package manifest specification | **Not created.** No format defined. | M5 (Package System Concepts) | High — blocks package creation beyond PoC |
| Maintainer handbook | **Not created.** M1's charter template and execution model are precursors but not a handbook. | No dedicated milestone. Could emerge from M5 + M8 (Trust). | Medium — needed before external maintainers join |
| Repository layout specification | **Not created.** No repo structure for packages defined. | M5 (Package System Concepts) partially; full spec may need its own work item | Medium — needed for real package publishing |
| Governance constitution | **Not created.** Conception describes governance conceptually but no formal constitution exists. | M8 (Trust Architecture) partially; full governance likely needs a future milestone | Medium — needed before governance pilot (Phase 4) |
| Licensing position | **Not created.** Conception states "closed-source during bootstrap" but no formal position document. | M8 (Trust Architecture) | Medium — needed before any code is published |

### 3 Initial Meta Packages

| Meta Package | Status | Gap | Addressed By |
|-------------|--------|-----|-------------|
| Package Maintainer | **Partially addressed.** M1 defines team model and charter template. Missing: formal product management processes, knowledge management conventions, participation rules as a package. | Formalization as a package | M5 (Package Design) + future work |
| Repository Infrastructure | **Nothing beyond concept.** No manifest format, versioning, repo layout, signing, or cross-walk metadata. | Everything | M3 (PoC), M5 (Package Design), M6 (Cross-walk), M8 (Trust) |
| Governance Program | **Nothing beyond concept.** No maintainer roles, acceptance criteria, voting, conflict resolution, or deprecation policy defined. | Everything | M8 (Trust) partially; likely needs a dedicated future milestone |

### Known Gaps (from mka-roadmap/README.md)

| Gap | Severity | Milestone(s) | Notes |
|-----|----------|-------------|-------|
| No formal package format or manifest schema | **Critical** | M5 | Blocks all real package work beyond PoC |
| No cross-walk adapter implementations | **High** | M6 | Blocks multi-harness support |
| No container deployment tooling | **High** | M3 (PoC in progress) | PoC will produce first container artifacts |
| No governance program beyond conceptual description | **Medium** | M8 + future | Needed before external contributors |
| No team deployment infrastructure | **Addressed** | M1 (complete) | Charter template + execution model delivered |
| MKA not yet applied to Karsheft's own knowledge management | **Medium** | M2 (this milestone) + ongoing | Gap analysis is itself an application of MKA; full application requires MemPalace integration (M7) |

### Gaps Not Covered by Any Current Milestone

| Gap | Description | Recommendation |
|-----|------------|----------------|
| No formal project charter | Conception lists it as "Immediate Next Document" but no milestone addresses it | Low priority — Roadmap + brainstorm manifest serve the function. Revisit if external stakeholders need a formal charter. |
| No maintainer handbook | Conception lists it; no milestone produces one | Defer to after M5 + M8. Could be a Sprint 3+ deliverable. |
| Governance Program meta package | M8 covers trust/licensing but not the full governance program (roles, voting, conflict resolution, succession) | Consider a dedicated milestone in Sprint 3+ after trust model exists |

---

## Part 3: Brainstorm-to-Phase Mapping and Sequencing Validation

*Persona: Sequencer*

### Validated Mapping

| Bootstrap Phase | Brainstorms | Milestones | Sprint |
|----------------|------------|------------|--------|
| 1. Define the language | Package System Design, Theaters, Karsheft Identity | M4, M5 | S1 (M4), S2 (M5) |
| 2. Define the process | Project Teams, MKA Non-Technical, Developer Experience | M1, M10 | S1 (M1), S2+ (M10) |
| 3. Build infrastructure | APT PoC, MemPalace–MKA, Cross-walk Interop | M3, M6, M7 | S1 (M3), S2+ (M6, M7) |
| 4. Pilot governance | Trust/Security/Licensing, Agent-Skill Libraries | M8, M9 | S2+ |
| 5. Publish first distro | (depends on all above) | Future | S3+ |

### Alignment Assessment

The current Roadmap milestone ordering **largely aligns** with the bootstrap sequence, with the following observations:

**Well-aligned:**
- M1 (Teams) and M4 (Theaters/Identity) correctly start in Sprint 1 — they define language and process (Phases 1–2)
- M5 (Package Design) comes after M3 (PoC) — learning from hands-on experience before formalizing
- M6 (Cross-walk) depends on M5 (Package Design) — correct, need canonical format before adapters

**Tension points:**
- M3 (APT PoC) is Phase 3 infrastructure work happening in Sprint 1, before Phase 1 language is fully defined (M5). This is intentional — the PoC informs the formal language. But the PoC team should be cautious about establishing conventions that M5 might override.
- M8 (Trust) depends on M3 but is Phase 4 work. This is correct — you need to see the infrastructure before securing it.
- M10 (Developer Experience) spans Phase 2 and Phase 3 concerns. Its positioning after M3 and M5 is appropriate.

**No reordering recommended.** The current milestone sequence respects the bootstrap phases while allowing practical learning (PoC before formalization). The dependency map accurately reflects these relationships.

### Critical Path

```
M1 → M2 → M3 → M5 → M6
                 ↘ M8
```

This is the longest dependency chain: Team Model → Gap Analysis → PoC → Package Design → Cross-walk. It defines the minimum timeline for reaching multi-harness support.

**Parallel work opportunities already captured:**
- M4 parallel with M2 (Sprint 1)
- M8 parallel with M5 (after M3)
- M7 parallel with M6 (after M5)
- M9 after M7
- M10 after M3 + M5

### Dependency Map Validation

The dependency map in Roadmap.md is accurate. No changes needed.

---

## Summary of Findings

1. **Strong foundation exists.** The Conception archive, MemPalace reference, brainstorm manifest, and M1 deliverables provide substantial groundwork.

2. **Critical gaps are package infrastructure.** No manifest format, no repo layout, no cross-walk adapters. M3 (PoC) and M5 (Package Design) are correctly prioritized to address this.

3. **Governance is the longest-horizon gap.** The Governance Program meta package is only partially covered by existing milestones. A dedicated milestone should be planned for Sprint 3+.

4. **Bootstrap sequence alignment is good.** No reordering needed. The current Roadmap respects the 5-phase bootstrap while allowing practical learning to feed formal definitions.

5. **Three documents from Conception's "Immediate Next" list have no dedicated milestone:** project charter, maintainer handbook, and repository layout specification. The first is low-priority (functional equivalents exist). The latter two should be addressed in Sprint 2+ planning.
