# FICSIT Component Calculator

A zero-backend Satisfactory component calculator designed for GitHub Pages.

## What it does

- Enter an item and quantity.
- Recursively expands the production chain.
- Shows the exact intermediate quantities needed.
- Shows the raw/base materials.
- Rounds to whole craft cycles by default (important because Satisfactory recipes craft in discrete cycles).
- Supports alternate recipes from the loaded dataset.
- Runs entirely in the browser; no server or API key is required.

## Deploy to GitHub Pages

1. Create a new GitHub repository, e.g. `satisfactory-component-calculator`.
2. Upload `index.html` and `README.md`.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Choose the `main` branch and `/ (root)`.
6. Save. GitHub will give you the Pages URL.

The site loads recipe data directly from the public `KirkMcDonald/satisfactory-calculator` data file at runtime. That file is a community-maintained dataset and contains items and recipes, including alternate recipes. The app is deliberately structured so the data source can be swapped later for a pinned/current dataset.

## Next upgrades I would add

- Per-minute mode.
- Machine counts and power draw.
- A full expandable dependency table.
- Recipe selection at every level, not just the target.
- Save/load plans with localStorage.
- Shareable URLs.
- A "what can I make with these resources?" mode.
- Pin a specific Satisfactory game-data version instead of tracking the community dataset's moving `master` branch.


### Somersloop 2× mode
The calculator includes an optional **Use Somersloops (2× production)** setting. When enabled, eligible production recipes are calculated at full 2× production amplification: the recipe output is doubled while its input requirements per cycle remain unchanged. Non-amplifiable buildings such as miners, extractors, and packagers are not modified. This matches Satisfactory's full Somersloop production amplification behavior.
