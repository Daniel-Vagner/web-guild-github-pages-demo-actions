---
description: "Add a new Razor page/component to the Blazor project"
---
# Add New Page

Create a new Blazor page component with the following guidelines:

1. Ask the user for:
   - Page route (e.g., `/about`)
   - Page title
   - Brief description of content

2. Create the `.razor` file in the `Pages/` folder of the client project.

3. Follow these conventions:
   - Include `@page` directive with the route
   - Include `<PageTitle>` component
   - Use existing layout (do NOT set a custom layout unless asked)
   - For standalone WASM: do NOT use `@rendermode` directives
   - Follow the same code style as other pages in the project

4. If the page needs navigation, add a `<NavLink>` entry in `Layout/NavMenu.razor`.

5. Build to verify compilation succeeds.
