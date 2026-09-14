# Architec — AI Agent Development Skill

A public portfolio showcase of **Architec**, a custom AI Agent Skill I designed for structured, multi-step software development workflows.

The production Skill is kept private. This repository publishes only a simplified, non-sensitive showcase of its architecture and operating model.

## What problem it addresses

Long-running AI-assisted software projects can lose context, repeat analysis, select the wrong next step, mix planning with implementation, or treat unvalidated work as complete.

Architec is designed to make the agent work from durable project truth, route work to the correct role, preserve explicit stop gates, and keep planning, implementation, review, and recovery separated.

## Core workflow

The Skill uses one canonical Method with different execution roles:

- **Project Launcher** — starts or onboards a project, collects Intake, creates or updates Method files, and provides one procedural handoff.
- **Mission Control** — reads verified project status and reports current position without inventing a new product outcome.
- **Architect** — reconciles intent with repository reality, selects the next approved outcome, and prepares a bounded implementation Pack.
- **Builder** — implements one approved Pack, validates the work, records evidence, and closes an ordinary no-gap Sprint.
- **Fly** — automates the same governed Architect ↔ Builder loop while preserving approval and safety gates.

## Design principles

- Repository and fresh validation outrank chat memory.
- Durable files carry project truth; chats coordinate work.
- Planning, implementation, review, and closeout are separate responsibilities.
- `Implemented`, `Tested`, `Validated`, `Reviewed`, `Approved`, and `Done` are not treated as the same state.
- Existing capabilities are preferred before custom implementation.
- Context is loaded progressively instead of reading the entire project by default.
- High-risk work such as auth, payments, migrations, permissions, and financial/inventory logic requires explicit boundaries and evidence.
- Destructive Git/database actions, deployment, publication, or permission changes require explicit authority.

## Durable project state

The production Method uses a small set of canonical project records, including:

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

`STATUS.json` acts as the compact lifecycle pointer, while `STATE.md` holds human-readable current context and readiness.

## Repository contents

```text
.
├── README.md
├── demo/
│   └── SKILL.md
├── docs/
│   └── architecture.md
└── examples/
    └── example-workflow.md
```

## What is intentionally private

The production version contains additional routing rules, migration/update logic, Git governance, safety handling, templates, validation scripts, and project-control implementation details. Those are intentionally not published here.

This repository exists to demonstrate the design and engineering approach without distributing the full production Skill.

## Areas demonstrated

- AI Agent workflow design
- LLM instruction and role design
- AI-assisted software development
- Project-state management
- Workflow orchestration and routing
- Git-aware delivery governance
- Context-efficiency and durable handoff design
- Validation and closeout discipline

---

Built by **Amir Hossein Azin**.
