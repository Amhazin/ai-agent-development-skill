# Workflow Architecture

Architec separates project launch, status, planning, implementation, and governed automation into distinct roles that share one durable project Method.

The production version is private. This document shows only the public high-level design.

## Role model

```text
Project Launcher
      |
      v
Mission Control -> Architect -> Builder
                     ^           |
                     +-----------+

Fly = governed automation of the Architect / Builder loop
```

- **Project Launcher** establishes or resumes the project workspace and starting truth.
- **Mission Control** reads verified status and gives one procedural next action.
- **Architect** reconciles intent with repository reality and prepares one bounded Pack.
- **Builder** implements one approved Pack, validates it, records evidence, and closes an ordinary no-gap Sprint.
- **Fly** automates the same governed loop without changing the underlying authority model.

## Durable truth model

The Method distinguishes four evidence layers:

```text
Repository / Git     -> what exists
Fresh validation     -> what works
DOMAIN / DECISIONS   -> what is intended
Conversation history -> supporting context
```

The goal is to prevent stale chat context from becoming stronger than current project evidence.

## Canonical project records

A governed project can include:

```text
AGENTS.md
INTAKE.md
DOMAIN.md
DECISIONS.md
QUESTIONS.md
RISKS.md
FILE_INVENTORY.md
ROADMAP.md
STATUS.json
STATE.md
ARCHITECT_BRIEFING.md
planning/
  architect-packs/
  sprints/
```

Each record has one clear responsibility so project truth is not duplicated across competing files.

## Simplified lifecycle

```text
Intake / Onboard
      ↓
Mission Control
      ↓
Architect discovery and reconciliation
      ↓
Approved Architect Pack
      ↓
Builder plan and stop gate
      ↓
Implementation
      ↓
Validation and evidence
      ↓
Closeout
      ↓
Mission Control refresh
```

If requirements change, acceptance fails, or repository reality conflicts with durable truth, the workflow returns to Architect reconciliation instead of silently widening implementation scope.

## Context efficiency

Architec uses progressive context loading: identify the current role, load only the relevant Method references, inspect the smallest useful repository surface, reuse durable project state, and expand context only when a real gap requires it.

## Reuse-first decisions

The production Method prefers existing project capability, native framework/platform capability, installed tools or Skills, and mature compatible components before custom implementation.

## Private implementation

The complete production Skill also contains private scripts, templates, validation logic, migration/update behavior, Git delivery policy, and additional routing rules. Those implementation details are intentionally omitted from this public repository.