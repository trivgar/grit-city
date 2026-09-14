# Grit City Sim Racing

Single-page static site for the sim racing server. One `index.html`, one `css/`,
images in `assets/`. No build step, no dependencies.

| | |
|---|---|
| Repo | `trivgar/grit-city` |
| Hosting | Cloudflare Pages, project `grit-city-sim-racing` — **direct upload**, not git-connected |
| Domain | `gritcitysimracing.com` |

## Deploying

Direct-upload means pushing to GitHub publishes nothing. Deploy explicitly:

```bash
set -a; . ~/.cloudflare.env; set +a
npx wrangler pages deploy . --project-name grit-city-sim-racing --branch main
```

`wrangler login` does not work from WSL — the token in `~/.cloudflare.env` is the
only path, and it needs **Account · Cloudflare Pages · Edit**. `wrangler whoami`
passing proves nothing about deploy rights. Ask before deploying.

## Two checkouts

- `/mnt/c/Users/Trav/grit-city` — branch `main`
- `/mnt/c/Users/Trav/worktrees/grit-city-dev` — branch `dev`, **this one**, and
  the one the phone's `grit` / `gritcity` launcher opens.

Work here on `dev`; merge to `main` when it's ready to publish. Branding assets
(banner, badge, wheel icon) live loose in the repo root with dated filenames.
