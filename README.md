# nl-spec-driven-ai-assisted-coding-agent-control

An educational, markdown-only repository demonstrating **spec-driven AI-assisted coding** and **agent control boundaries** for production workflows.

This project focuses on one core idea: the model should execute only what a versioned specification allows.

## Overview

Most AI coding failures in production come from implicit decisions made during execution.

This repository demonstrates a controlled alternative:

- Define intent, scope, and constraints in a spec first
- Break work into deterministic tasks
- Separate planning from execution
- Enforce human approval gates for boundary crossings
- Keep agent authority explicit and narrow

Everything in this project is designed to be source-of-truth documentation that can be used directly in real coding workflows.

## What This Repository Demonstrates

- `SPEC.md` as an execution contract, not narrative documentation
- `TASKS.md` as deterministic, verifiable execution units
- `AGENTS.md` as behavior constraints for coding agents
- Example templates for production reuse under `examples/`
- Human-in-the-loop control via explicit execution gates

## Repository Type

This is a **markdown-only control-plane project**.

- No application code
- No framework dependency
- No orchestration runtime requirement

The artifacts are intended to be copied into real repositories and used during AI-assisted implementation.

## Quick Start

1. Read `SPEC.md` for global rules.
2. Read `TASKS.md` and pick one task.
3. Read `AGENTS.md` to enforce execution behavior.
4. Use `examples/` templates to scale the workflow.
5. Execute one task at a time and validate against spec constraints.

## Project Structure

```text
.
+-- AGENTS.md
+-- README.md
+-- SPEC.md
+-- TASKS.md
+-- examples/
|   +-- AGENTS.example.md
|   +-- EXECUTION_GATE.example.md
|   +-- SPEC.example.md
|   +-- TASKS.example.md
```

## Core Files

### `SPEC.md`
Defines context, scope, and non-negotiable constraints.

### `TASKS.md`
Defines deterministic units of work and verification criteria.

### `AGENTS.md`
Defines execution behavior for agents (one task at a time, ask when uncertain).

## Example Templates

### `examples/SPEC.example.md`
A production-grade spec template including scope boundaries, escalation conditions, and change-control flow.

### `examples/TASKS.example.md`
Deterministic task templates with file lists, concrete requirements, and verifiable checks.

### `examples/AGENTS.example.md`
Scoped multi-agent role definitions (Builder, Reviewer, Test) with shared control rules.

### `examples/EXECUTION_GATE.example.md`
A human approval checklist for scope, constraints, verification, and traceability.

## Recommended Execution Flow

1. Update the spec before implementation.
2. Approve boundaries and escalation conditions.
3. Execute exactly one task.
4. Validate output against task verification and spec constraints.
5. If requirements change, modify spec first, then continue.

## Notes

- Keep specs short and explicit to reduce ambiguity.
- Treat anything not written in spec or tasks as out of scope.
- Use examples as templates, not fixed policy.

## License

See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome. Good extensions include:

- More domain-specific spec templates
- Additional deterministic task patterns
- Reviewer checklists for common risk categories
- Practical migration guides from prompt-first to spec-driven workflows
