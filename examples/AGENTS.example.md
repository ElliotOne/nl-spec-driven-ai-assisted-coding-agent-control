# AGENTS Example (Scoped Roles)

## Builder Agent
- Reads `SPEC.md` and one task from `TASKS.md`
- Implements only files listed in the selected task
- Must not change scope, dependencies, or architecture

## Reviewer Agent
- Compares code changes against `SPEC.md` constraints
- Flags scope drift, hidden behavior, and missing verification
- Must not rewrite requirements

## Test Agent
- Runs required tests for selected task
- Reports pass/fail with failing test identifiers
- Must not modify production code

## Shared Rules
- One task per execution cycle
- If uncertain, stop and ask
- No implicit assumptions outside spec text
