# 2026-07-27 Pilot Project Portfolio

## Purpose

Define the initial pilot projects that will validate both MKA and APT packaging prototypes during the current 4-6 week internal-collaboration window.

## Pilot Selection Principles

- Pilot projects must be small enough to ship learning quickly.
- Each pilot must produce reusable artifacts for other projects.
- Every pilot must exercise both:
  - MKA process artifacts
  - APT packaging integration concepts
- Audience is internal collaborators (human and agent).

## Pilot 1: Product Manager & Implementation Manager (Agentic MKA)

### Scope
Implement an agentic capability that applies MKA to product governance and implementation execution as distinct but meshed tracks.

### Primary Validation Targets
- MKA governance artifacts can guide product decisions.
- MKA approach artifacts can guide implementation sequencing.
- Product and project processes can be interleaved through roadmap state.

### Prototype Outputs
- A minimal function definition set for Product Manager and Implementation Manager behaviors.
- A milestone/roadmap operating flow that separates governance vs implementation responsibilities.
- At least one worked example of a project using this split.

### APT Packaging Validation
- Package the function definitions and supporting docs as an internal prototype package.
- Test install/use in a containerized project workspace.

## Pilot 2: Google Collaboration Suite (Docs/Sheets/Slides/Drive/Calendar/Tasks)

### Scope
Build agent collaboration contexts and capabilities for Google collaborative tools, using existing *-markdown-sync utilities in Lab as implementation foundations.

### Primary Validation Targets
- Agents can produce and consume collaboration artifacts consistently.
- Human-agent handoff is traceable through MKA artifacts.
- Collaboration workflows can be normalized across document and scheduling tools.

### Prototype Outputs
- Context model for Google collaboration operations (documenting objects, permissions assumptions, workflow events).
- Initial capability list and boundary conditions for agent actions.
- Prototype workflow mappings using markdown-sync and gtask-markdown-sync utilities.

### APT Packaging Validation
- Package at least one collaboration capability bundle with clear dependency metadata.
- Validate reproducible setup in internal test environment.

## Pilot 3: Meeting Secretary Function

### Scope
Deliver a narrowly scoped attendant function for meeting facilitation support and outcome-focused notes capture.

### Primary Validation Targets
- MKA Missives and Roadmap patterns can be applied with low overhead.
- Meeting outcomes can be transformed into project-ready tasks and milestones.
- Notes remain concise, decision-oriented, and reusable.

### Prototype Outputs
- Meeting note template and operating checklist.
- Lightweight summary-to-actions conversion rules.
- Example notes set across multiple meeting topics.

### APT Packaging Validation
- Package Meeting Secretary templates and workflow rules as an internal function package.
- Validate install and invocation consistency in a containerized environment.

## Shared Deliverables Across All Pilots

- Friction log with issue categories: process, tooling, packaging, collaboration.
- Interface map showing where MKA artifacts feed packaging lifecycle.
- Recommendation memo for next rollout phase.

## Out of Scope (Current Window)

- Broad mandate of Karsheft standards across all projects.
- External collaborator onboarding requirements.
- Production-hardening all automation paths.
