---
description: "Diagnose and fix CSS/layout issues in Blazor components"
---
# Fix Layout / Styling

When debugging CSS or layout issues in Blazor:

## Key concepts:
- **Scoped CSS** (`.razor.css`) generates attribute selectors like `[b-xxxxx]` with higher specificity than plain class selectors.
- Global styles in `app.css` or `wwwroot/css/` do NOT have scope attributes — they will lose specificity battles against scoped styles.
- If a global style needs to override a scoped style, it must be moved INTO the scoped `.razor.css` file.

## Debugging steps:
1. Check if the element has a `b-xxxxx` attribute in rendered HTML.
2. If yes, the styles must come from the component's `.razor.css` to match specificity.
3. Verify the `*.styles.css` bundle is referenced in `index.html`.
4. Check `@media` queries are in the correct file (scoped vs global).

## Common pitfalls:
- `flex-direction` in scoped CSS beating a media query in global CSS
- Missing `.styles.css` reference in `index.html`
- `#blazor-error-ui` placed inside the component tree instead of in static `index.html`
