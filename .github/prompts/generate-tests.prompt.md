---
description: "Generate unit tests for a component or service"
---
# Generate Tests

Create unit tests following best practices:

## Conventions:
- Use **bUnit** for Blazor component tests
- Use **xUnit** as the test framework
- Use **NSubstitute** or **Moq** for mocking
- Follow Arrange-Act-Assert pattern
- Name tests: `MethodName_Scenario_ExpectedResult`
- One assertion per test (prefer focused tests)
- Mock all external dependencies (HttpClient, services, etc.)

## Steps:
1. Identify the target class/component to test.
2. Determine test scenarios (happy path, edge cases, error handling).
3. Create test file in the test project following the same namespace structure.
4. Build and run tests to verify they pass.

## For Blazor components:
- Test rendered markup with `cut.Find()` / `cut.FindAll()`
- Test parameter binding
- Test event handlers with `cut.Find("button").Click()`
- Mock injected services
