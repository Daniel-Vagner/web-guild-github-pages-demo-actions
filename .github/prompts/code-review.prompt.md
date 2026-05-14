---
description: "Review current file or selection for issues and improvements"
---
# Code Review

Perform a focused code review on the current file or selection:

## Check for:
1. **Correctness** — logic errors, null reference risks, off-by-one errors
2. **Security** — injection risks, exposed secrets, missing input validation
3. **Performance** — unnecessary allocations, N+1 patterns, missing `async`
4. **Maintainability** — unclear naming, overly complex methods, missing error handling
5. **Blazor-specific** — incorrect lifecycle usage, missing `StateHasChanged`, memory leaks from event subscriptions

## Output format:
- List issues by severity (🔴 Critical, 🟡 Warning, 🔵 Info)
- Provide a brief explanation of each issue
- Suggest a fix (but don't apply without confirmation)

## Do NOT:
- Rewrite code that works correctly just for style preference
- Flag issues unrelated to the current file's responsibility
- Suggest changes that would break existing functionality
