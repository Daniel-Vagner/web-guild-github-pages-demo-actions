---
description: "Publish Blazor WASM client to GitHub Pages output folder"
---
# Publish to GitHub Pages

1. Build the solution and verify no errors.
2. Run `dotnet publish` on the **Client** (WebAssembly) project with `-c Release`.
3. After publish, copy static assets from the server project's `wwwroot` (`lib/`, `app.css`, `favicon.png`) into the publish output's `wwwroot`.
4. Sync `index.html` as `404.html` for client-side routing fallback.
5. Report the publish output path to the user.

## Important
- The publish output folder should be relative to the workspace root: `publish/`
- Always overwrite existing files when copying assets.
- The `index.html` in the client's `wwwroot` is the source of truth — do not patch it post-publish.
