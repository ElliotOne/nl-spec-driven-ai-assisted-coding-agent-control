# TASKS Example (Deterministic Units)

## Task 1: Input Validation
Files:
- src/Guardrails/InputValidator.cs
- tests/Guardrails/InputValidatorTests.cs

Requirements:
- Reject empty or whitespace-only input
- Reject input longer than configured max length
- Return deterministic error codes/messages

Verification:
- Unit tests for empty, whitespace, valid, and over-limit inputs pass
- No model call is made for invalid input

## Task 2: Deterministic Policy Refusal
Files:
- src/Guardrails/Policy.cs
- tests/Guardrails/PolicyTests.cs

Requirements:
- Refuse sensitive request categories using rule checks
- Return fixed refusal response for blocked categories

Verification:
- Policy tests pass for allowed and blocked requests
- Blocked requests are refused before any model/tool call

## Task 3: Tool Allowlist Enforcement
Files:
- src/Tools/ToolRegistry.cs
- tests/Tools/ToolRegistryTests.cs

Requirements:
- Execute only allowlisted tools
- Reject unknown tools with deterministic error
- Validate arguments before execution

Verification:
- Tests pass for allowlisted and non-allowlisted tool names
- Invalid arguments fail fast with deterministic error
