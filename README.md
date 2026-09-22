# Grit City Sim Racing

The website for [gritcitysimracing.com](https://gritcitysimracing.com), a
Tacoma-based sim racing community.

[Join the Discord](https://discord.gg/FAmVaD9GeQ)

## What is in here

One static page. There is no build step, no framework and no dependencies.

```
index.html          the whole site
css/style.css       the whole stylesheet
assets/images/      logos, icons and banners
*.png               source artwork, kept at the root deliberately
```

The fonts are Oswald and Roboto, loaded from Google Fonts. Everything else is
local.

## Working on it

Open `index.html` in a browser. That is the entire development loop.

## Deploying

Cloudflare Pages, direct upload, to the `grit-city-sim-racing` project:

```bash
npx wrangler pages deploy . --project-name grit-city-sim-racing --branch main
```

It is not git-connected, so a push does not publish. Deploying is the explicit
command above, and the custom domain `gritcitysimracing.com` is served from that
project.
