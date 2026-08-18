# Regulatory Affairs, From First Principles

An interactive primer for new Regulatory Affairs professionals — 16 modules that
each take three angles on a topic: a concept explainer, a hands-on game, and a
real-world case or tool.

**Live site:** https://sripad-hs.github.io/regulatory-first-principle/

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
index.html                   the entire primer — self-contained HTML/CSS/JS
.nojekyll                    serve files as-is, no Jekyll processing
.github/workflows/pages.yml  builds and deploys the site on push
```

The only external request is the Google Fonts stylesheet; everything else is
inlined, so the file opens standalone from disk too.

## Publishing setup

No manual setup needed. The workflow passes `enablement: true` to
`actions/configure-pages`, so the first run turns Pages on via the API and points
it at the Actions build — then deploys. Watch it under the **Actions** tab; the
run prints the live URL when it finishes.

If you ever want to check or change it by hand, it lives at
**Settings → Pages → Build and deployment**, which should read *GitHub Actions*.

Note that Pages on a **private** repo requires a paid plan (Pro/Team/Enterprise).
This repo is public, so that does not apply — but if it is ever made private on a
free plan, the deploy will start failing.

## Local preview

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

Or just open `index.html` in a browser.
