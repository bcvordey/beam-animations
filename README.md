# Beam-Obstacle Contact and DNC Transition Visualizer

This repository hosts a GitHub Pages visualization of beam-obstacle contact simulations. The page presents side-by-side animations that show how a deformable beam transitions into contact with obstacle constraints under the DNC condition, including the penetration response observed as the obstacle stiffness changes.

The exhibit is intended to make the simulation results easier to inspect, compare, and present. In particular, it highlights the contrast between soft obstacles and increasingly hard obstacles by varying the stiffness parameter `kappa` from `0.1` to `1000`.

## Live animation page

View the deployed visualization here:

<https://bcvordey.github.io/beam-animations/>

Source repository:

<https://github.com/bcvordey/beam-animations>

## What the page demonstrates

- Single-obstacle beam contact under the DNC condition for different `kappa` values.
- The change in penetration behavior as the obstacle stiffness increases from soft contact to hard contact.
- Two-boundary-obstacle contact cases for different `beta` settings.
- Distributed obstacle contact cases with the same stiffness sweep.
- Synchronized 2x2 comparisons that make the effect of stiffness and model parameters easier to see across simulations.

## Animation groups

- Page 1: single obstacle, `beta = 0.1`, with `kappa = 0.1`, `10`, `100`, and `1000`.
- Page 2: single obstacle DNC cases, including `beta = 1` examples and stronger-load cases marked with `f = -5`.
- Page 3: two boundary obstacles, `beta = 1`, with the full `kappa` sweep.
- Page 4: two boundary obstacles, `beta = 5`, with the full `kappa` sweep.
- Page 5: distributed obstacle set, `beta = 1`, with the full `kappa` sweep.

## Viewer controls

- Use `Prev` and `Next` to move between animation groups.
- Use the numbered buttons to jump directly to a page.
- Use `Pause`, `Restart`, and `Sync` to compare animations more precisely.
- Keyboard shortcuts are also supported: left/right arrows change pages, `R` restarts the active page, and number keys jump to pages.

## Repository contents

- `index.html` contains the full static viewer, layout, navigation, video synchronization, and time overlays.
- The `.mp4` files are the beam-obstacle simulation animations displayed by the page.
- `.github/workflows/static.yml` deploys the static page to GitHub Pages from the `main` branch.

## Local preview

From this folder, open the page in a browser:

```bash
open index.html
```

You can also double-click `index.html` in Finder to view the same animation dashboard locally.

## Suggested citation-style description

This project provides a public interactive visualization artifact for beam-obstacle contact simulations, demonstrating DNC transition behavior and stiffness-dependent penetration response across soft, hard, boundary, and distributed obstacle configurations.
