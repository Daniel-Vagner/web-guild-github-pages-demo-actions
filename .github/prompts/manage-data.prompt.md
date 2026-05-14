---
description: "Create or update a JSON data file and wire it to a component"
---
# Manage Static Data

For Blazor WASM apps hosted on static hosting (GitHub Pages), data is served from JSON files in `wwwroot/data/`.

## When adding new data:
1. Create a JSON file in `wwwroot/data/` with a descriptive name.
2. Create a model class (private sealed, inside the component's `@code` block, or in a shared `Models/` folder if reused).
3. Inject `HttpClient` and fetch with `Http.GetFromJsonAsync<T[]>("data/filename.json")`.
4. Ensure `HttpClient` is registered in `Program.cs` with `BaseAddress` set to `builder.HostEnvironment.BaseAddress`.

## When updating existing data:
1. Edit the JSON file directly.
2. Verify the structure matches the model class.
3. Build to verify no issues.

## Conventions:
- Use `DateOnly` for dates (format: `yyyy-MM-dd` in JSON).
- Use PascalCase for JSON property names (System.Text.Json default).
- Keep data files small — they're downloaded by the client.
