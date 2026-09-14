# Example Workflow

This example shows the public high-level behavior of Architec on an existing software project.

## Scenario

A user returns to a project and asks:

> What is done, and what should happen next?

## 1. Mission Control

Mission Control reads the compact project status set and current repository evidence. It reports verified position and one procedural next action.

It does **not** invent the next feature.

Example outcome:

```text
Current Sprint: closed
Current Pack: none approved
Repository: available
Validation: previous Sprint evidence present
Next procedural action: open Architect and reconcile the next outcome
```

## 2. Architect

Architect inspects the relevant repository areas, product rules, decisions, risks, and current project state.

It reconciles user intent with repository reality, defines one bounded next outcome, and prepares an Architect Pack only after the required decision gate.

## 3. Builder

Builder receives the approved Pack in a fresh execution context.

Builder:

1. verifies the live repository and delivery context;
2. prepares a bounded implementation plan;
3. stops at the normal code gate;
4. implements only the approved scope;
5. runs the required validation;
6. records evidence and closes the Sprint when acceptance passes.

Builder does not widen scope or invent missing product intent.

## 4. Closeout and resume

After closeout, Mission Control can read the durable project records again and report the new verified position without requiring the user to copy a long handoff between chats.

## Conflict path

If live repository behavior conflicts with durable project truth, Architec does not silently choose one side. The workflow routes to Architect reconciliation before more implementation.

This public example is intentionally simplified. The production Skill contains additional governance, update, migration, validation, and delivery logic that is not published here.
