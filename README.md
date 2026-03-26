# Content_flow_Integration_READABLE

Read-only, linear snapshot of the [Cross‑Alliance E2E Integration Console](https://chakn005.github.io/Content_flow_Integration/) (same content as `readonly.html` in the main project).

**Live site:** [https://chakn005.github.io/Content_flow_Integration_READABLE/](https://chakn005.github.io/Content_flow_Integration_READABLE/)

## Publishing (GitHub Actions)

1. Open **Settings → Pages** for this repository.
2. Under **Build and deployment**, set **Source** to **GitHub Actions** (not “Deploy from a branch” unless you remove this workflow).
3. Push to `main`. After the workflow succeeds, wait a minute and refresh the Pages URL.

## Updating the site from the main repo

Edits should be made in **`content-integration-flow`** (interactive app + `readonly.html`), then synced here.

In your `content-integration-flow` clone:

```bash
bash scripts/sync-readable-pages.sh
```

Copy the updated contents of `Content_flow_Integration_READABLE/` into this repository (or use your usual mirror process), commit, and push to `main`.
