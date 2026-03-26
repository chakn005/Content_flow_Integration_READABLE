# Content_flow_Integration_READABLE

Read-only snapshot of the Cross‑Alliance E2E Integration Console (same behavior as `readonly.html` in the main [Content_flow_Integration](https://github.com/chakn005/Content_flow_Integration) project).

**Live site:** [https://chakn005.github.io/Content_flow_Integration_READABLE/](https://chakn005.github.io/Content_flow_Integration_READABLE/)

This repository must include **`index.html`**, **`app.js`**, and **`styles.css`** at the root. If the site loads but looks broken, confirm those three files are committed and pushed.

---

## Push updates to GitHub

From this repository’s directory on your machine:

```bash
git add -A
git status   # expect: index.html, app.js, styles.css, .nojekyll, README.md, .github/workflows/deploy-pages.yml
git commit -m "Update read-only site"
git push origin main
```

### If `git push` fails with “Permission denied (publickey)”

Your `origin` is probably using **SSH** (`git@github.com:...`) without a working key. Switch to **HTTPS** and sign in (browser or Personal Access Token):

```bash
git remote set-url origin https://github.com/chakn005/Content_flow_Integration_READABLE.git
git push -u origin main
```

---

## Publishing options (pick one)

### A. GitHub Actions (this repo’s workflow)

1. **Settings → Pages → Build and deployment**
2. Set **Source** to **GitHub Actions** (not “Deploy from a branch” unless you disable the workflow below).
3. Push to `main`. Open **Actions** → latest **Deploy GitHub Pages** run.
4. If the job waits for **approval**, open the run → **Review deployments** → approve **github-pages** (first time only; you can relax this under **Settings → Environments → github-pages**).

### B. Deploy from branch (no Actions)

1. **Settings → Pages → Build and deployment**
2. Set **Source** to **Deploy from a branch** → **main** → **/** (root).
3. Remove or disable `.github/workflows/deploy-pages.yml` so you do not use two publishers at once.
4. Push static files to `main`; GitHub will serve `index.html` from the root.

---

## Update from the main project

In your **content-integration-flow** clone:

```bash
bash scripts/sync-readable-pages.sh
```

Then copy or commit the updated files from `Content_flow_Integration_READABLE/` into **this** repository and push (see above). The source HTML flag is `readonly.html` in the main repo (copied to `index.html` here).
