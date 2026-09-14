---
name: architec-showcase
description: Public showcase of an AI Agent Skill for launching, governing, building, resuming, and safely updating software projects with role-based workflow routing and durable project state.
---

# Architec — Public Showcase

This file is a deliberately simplified portfolio version of the production Skill.

It demonstrates the operating model without publishing the full production routing rules, update/migration logic, scripts, templates, or project-specific safeguards.

## Operating model

Use one canonical project Method across roles. Behavior changes by role; project truth does not.

| Role | Responsibility |
| --- | --- |
| **Project Launcher** | Choose the starting path, collect Intake, create/update Method files, and provide one procedural handoff. |
| **Mission Control** | Read the compact project status set and report verified position plus one procedural next action. |
| **Architect** | Reconcile intent with repository reality, decide the next approved outcome, and write one bounded implementation Pack. |
| **Builder** | Implement one approved Pack, validate it, record evidence, and close an ordinary no-gap Sprint. |
| **Fly** | Automate the same governed Architect ↔ Builder loop while preserving material stop gates. |

## Routing rules

Use project state and user intent to select the smallest appropriate next workflow.

- New idea, website, template, or onboarding request → **Project Launcher**
- Plain-language status or resume request → **Mission Control**
- New outcome, changed requirement, repair, or material reconciliation → **Architect**
- Approved current Pack → **Builder**
- Governed automation request → **Fly**
- Material conflict between live repository reality and durable project truth → **Architect reconciliation before implementation**

Do not invent the next product outcome merely because a project is ready for more work.

## Shared invariants

Treat these as distinct authorities:

1. Repository and Git — what exists
2. Fresh validation — what works
3. Durable product decisions — what is intended
4. Chat/history — context only until corroborated

Never downgrade working implementation to match stale documentation.

Keep these states distinct:

```text
Implemented
Committed
Tested
Validated
Reviewed
Approved
Done
```

## Durable handoff

Files carry project truth; chats coordinate work.

A typical governed project keeps a compact status pointer and human-readable state alongside product rules, decisions, risks, roadmap, Architect Packs, and Sprint evidence.

The production Skill uses this durable structure to let fresh AI contexts resume work without relying on chat history alone.

## Context-efficiency rule

Read only what the current role needs.

Prefer:

1. existing project capability;
2. native framework/platform capability already in use;
3. trusted installed tool or Skill;
4. mature compatible library/component;
5. minimal adaptation;
6. custom implementation only when necessary.

Search first, then open the smallest relevant set of files. Avoid rebuilding context already available in durable project records.

## Safety boundary

Before Brownfield or risky work, verify repository root, branch, HEAD, worktree state, relevant source/test/config entry points, and overlap with existing user work.

Do not silently discard unrelated changes, rewrite Git history, expose secrets, deploy, publish externally, or perform destructive operations without explicit authority.

For auth, payment, permissions, migrations, sensitive data, or financial/inventory behavior, require explicit boundaries and failure-path evidence.

## Completion rule

A successful implementation is not automatically `Done`.

Validate the approved acceptance criteria, preserve evidence, close the correct delivery boundary, and update the durable project state before advancing.

## Intentionally omitted from this public version

The complete production Skill also contains private:

- detailed role and routing rules;
- scaffold/update/migration implementation;
- Git delivery modes and synchronization policy;
- state-management scripts;
- validation tooling;
- templates and project-control records;
- recovery and compatibility logic;
- additional safety and closeout behavior.

The production version is maintained privately.
