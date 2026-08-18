# Regulatory Affairs, From First Principles

An interactive field guide for new Regulatory Affairs professionals — 16 modules that
each take three angles on a topic: a concept explainer, a hands-on game, and a
real-world case or tool.

**Live site:** https://sripad-hs.github.io/regulatory-first-principle/

Created by [Sripad HS](https://www.linkedin.com/in/hssripad/).

## What's inside

33 slides covering the arc of a drug's regulatory life:

| Module | Topic |
| --- | --- |
| 1 | What Regulatory Affairs really is |
| 2 | The global map of regulatory authorities |
| 3 | Drug discovery, step by step |
| 4 | Regulatory strategy |
| 5 | The first gate: IND / CTA |
| 6 | The four clinical phases |
| 7 | CMC — Chemistry, Manufacturing & Controls |
| 8 | Submissions and the CTD |
| 9 | Regulatory Operations |
| 10 | Regulatory Intelligence |
| 11 | Review pathways and timelines |
| 12 | Post-approval lifecycle management |
| 13 | Safety signals after launch |
| 14 | Commercial plans and regulatory input |
| 15 | Why "approved" differs by region |
| 16 | One molecule, many functions |

It ends with a scored quiz that tallies points earned across every game.

## Using it

- **Navigate:** arrow keys, or the on-screen controls in the corner.
- **Present:** the fullscreen button hides the HUD and chrome for projection.
- Score and streak carry across the whole session, so run it start to finish.

## Repo layout

```
index.html                   the entire guide — self-contained HTML/CSS/JS
.nojekyll                    serve files as-is, no Jekyll processing
.github/workflows/pages.yml  builds and deploys the site on push
```

The only external request is the Google Fonts stylesheet; everything else is
inlined, so the file opens standalone from disk too.

## Publishing setup

One manual step, once — GitHub will not let a workflow enable Pages on its own:

**Settings → Pages → Build and deployment → Source → GitHub Actions**

Until that is set, every run fails at `configure-pages` with *"Get Pages site
failed ... verify that the repository has Pages enabled"*. After setting it,
re-run the workflow from the **Actions** tab; the run prints the live URL when it
finishes, and every later push deploys automatically.

(`actions/configure-pages` has an `enablement: true` option that sounds like it
removes this step, but creating a Pages site requires admin rights that
`GITHUB_TOKEN` cannot be granted — it fails with *"Resource not accessible by
integration"*. Automating it would mean storing a personal access token, which is
more setup than the one-time toggle.)

Pages on a **private** repo also requires a paid plan. This repo is public, so
that does not apply today — but making it private on a free plan would break the
deploy.

## Local preview

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

Or just open `index.html` in a browser.
