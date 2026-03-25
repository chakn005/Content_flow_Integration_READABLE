# Content_flow_Integration_READABLE

Read-only, linear HTML reference for the [Cross‑Alliance E2E Integration Console](https://chakn005.github.io/Content_flow_Integration/).

- **Pages URL:** https://chakn005.github.io/Content_flow_Integration_READABLE/
- **Source of truth for edits:** mirror `readable.html` in [Content_flow_Integration](https://github.com/chakn005/Content_flow_Integration), then push updates to this repo.

## Fix 404 — enable GitHub Pages

This repo uses **GitHub Actions** to publish (workflow: `.github/workflows/deploy-pages.yml`).

1. Open **Settings → Pages** for this repository.
2. Under **Build and deployment**, set **Source** to **GitHub Actions** (not “Deploy from a branch” unless you disable the workflow).
3. After the first workflow run finishes (**Actions** tab → green check), wait 1–2 minutes and open the Pages URL again.

If **Source** is left on **GitHub Actions** with **no** workflow, or on **Deploy from a branch** with folder **/docs** (while files live in the root), you will get **404**.

### Alternative (branch deploy only)

Set **Source** to **Deploy from a branch** → **main** → **/ (root)** and remove or disable `.github/workflows/deploy-pages.yml` so only one publishing method is active.
