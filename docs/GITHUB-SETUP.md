# GitHub setup guide for Jent Innovations

Everything here is a one-time setup. Items marked **you** need account-owner access; the Claude GitHub App cannot change these.

## 1. Put each app in its own private repo (you)
1. github.com/new. Name it after the app. **Private**. Don't add a README or .gitignore yet.
2. From the project folder on your Mac: `git init`, copy in the right template (`docs/templates/app-repo/` for iOS, plus `docs/templates/unity-repo/` for Unity), `git add .`, `git commit -m "Initial commit"`, then the `git remote add origin ...` and `git push -u origin main` lines GitHub shows.
3. **Before the first commit, check for secrets**: API keys, `.p8`/`.p12` files, provisioning profiles. The templates' `.gitignore` excludes common ones, but check by hand. If a secret ever gets committed, treat it as leaked and rotate it. Deleting it from a later commit does not remove it from history.
4. Unity: run `git lfs install` before the first commit so large assets go through LFS. Free accounts have limited LFS storage and bandwidth; check current limits.

## 2. Turn on security features (you), per repo
Settings → **Advanced Security** (or "Code security"):
- Dependency graph, **Dependabot alerts**, **Dependabot security updates**: on.
- **Secret scanning** and **push protection**: on. Push protection blocks a push containing a recognized secret.
(Names move around; use the repo's Settings search.)

## 3. Protect `main` (you), optional but cheap
Settings → Rules → New branch ruleset for `main`: require a pull request, and require status checks to pass once CI exists. As a solo developer you can still open PRs yourself; the point is CI runs before changes land.

## 4. GitHub Pages for this repo (you)
Settings → Pages → Deploy from a branch → `main` / `/ (root)`. This is what serves the policy URLs. Later, a custom domain is configured on the same page.

## 5. Releases
Tag each shipped version (`v1.2.0`) and publish a Release using `docs/templates/RELEASE_NOTES_TEMPLATE.md`. Record which privacy policy version applied.

## 6. Issues
Copy `docs/templates/app-repo/.github/ISSUE_TEMPLATE/` into each app repo. Keep private app repos' issues for yourself; point public support to `support.html`.
