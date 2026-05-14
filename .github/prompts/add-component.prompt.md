---
description: "Add a new reusable Razor component (not a page)"
---
# Add New Component

Create a new reusable Blazor component:

1. Ask the user for:
   - Component name
   - Purpose / what it renders
   - Parameters it should accept

2. Create the `.razor` file in an appropriate folder (e.g., `Components/` or `Shared/`).

3. Follow these conventions:
   - Use `[Parameter]` for public inputs
   - Use `[Parameter] public RenderFragment? ChildContent { get; set; }` if it wraps content
   - Keep components focused on a single responsibility
   - Add a scoped `.razor.css` file if custom styling is needed
   - For standalone WASM: do NOT use `@rendermode` directives

4. Build to verify compilation succeeds.
