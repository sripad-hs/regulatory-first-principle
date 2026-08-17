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

The workflow deploys on every push, but GitHub needs to be told to use it once:

**Settings → Pages → Build and deployment → Source → GitHub Actions**

After that, check the run under the **Actions** tab — it prints the live URL when
it finishes.

## Local preview

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

Or just open `index.html` in a browser.
