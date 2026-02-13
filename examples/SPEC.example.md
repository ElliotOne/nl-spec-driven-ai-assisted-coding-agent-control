# SPEC Example (Production Template)

## Context
This system delivers AI-assisted coding with deterministic control.
The specification is the only execution contract.

## Scope
### Included
- Implementations explicitly listed in `TASKS.md`
- Refactors limited to files named in each task
- Test updates that directly validate task requirements

### Excluded
- Architectural redesign
- New dependencies or package upgrades
- CI/CD, infra, or deployment changes
- Data model or schema modifications

## Constraints
### Always
- Keep changes task-scoped and minimal
- Run project tests before marking task complete
- Preserve existing naming conventions and public behavior

### Ask First
- Database/schema changes
- Public API contract changes
- Cross-module refactors beyond task file list
- New environment variables or config keys

### Never
- Commit secrets or credentials
- Modify pipelines or release configuration
- Introduce hidden behavior not stated in spec or task

## Validation Rules
- Every task must map to deterministic checks.
- If a requirement is ambiguous, stop and ask.
- If code passes tests but violates scope, task fails.

## Change Control
When reality conflicts with this spec:
1. Propose a spec change in markdown.
2. Obtain human approval.
3. Update spec first, then execute.
