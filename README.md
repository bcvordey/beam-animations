# Beam-Obstacle Contact Simulations Under the Damped Normal Compliance Condition

This repository provides a publicly accessible, interactive visualization of beam-obstacle contact simulations governed by the Damped Normal Compliance (DNC) condition. The animations display the dynamic behavior of an Euler-Bernoulli beam vibrating in contact with one or more obstacles, showing how obstacle stiffness and damping parameters affect penetration depth, rebound dynamics, and settling behavior.

These simulations accompany the peer-reviewed publication:

> Saylor, G.; Shillor, M.; Vordey, C. "Model and Simulations of Contact Between a Vibrating Beam and an Obstacle Using the Damped Normal Compliance Condition." *Axioms* 2025, 14(12), 866.

## Live Visualization

View the deployed animation page here:

**[https://bcvordey.github.io/beam-animations/](https://bcvordey.github.io/beam-animations/)**

Source repository:

**[https://github.com/bcvordey/beam-animations](https://github.com/bcvordey/beam-animations)**

## Background

Classical contact models in structural mechanics typically assume either rigid obstacles (the Signorini condition) or purely elastic contact response (the standard Normal Compliance condition). Neither captures the energy dissipation that occurs during real physical contact. The DNC condition addresses this gap by incorporating an explicit damping term into the contact formulation, so the model represents what happens during impact: energy is lost to heat, deformation, and internal friction rather than being recovered elastically.

The mathematical analysis and finite element discretization underlying these simulations are developed in the published paper and in the doctoral dissertation:

> Vordey, C. "Dynamics and Vibrations of an Euler-Bernoulli Beam in Contact with Obstacles under the Damped Normal Compliance Condition." Ph.D. Dissertation, Oakland University, 2026.

The computational solvers used to generate these animations are publicly available in companion repositories:

- **Python solver:** [https://github.com/bcvordey/dnc-beam-python](https://github.com/bcvordey/dnc-beam-python)
- **MATLAB solver:** [https://github.com/bcvordey/beam-contact-solvers](https://github.com/bcvordey/beam-contact-solvers)

## What the Animations Demonstrate

The visualization page presents synchronized side-by-side animations that allow direct comparison of contact dynamics across a systematic range of parameters. The stiffness parameter kappa ranges from 0.1 (soft contact) to 1000 (hard contact), and the damping parameter beta takes values of 0.1, 1, and 5.

Each animation shows the beam displacement over time as it interacts with one or more obstacles. The key physical phenomena visible in the animations include:

- **Penetration depth reduction** as obstacle stiffness increases, transitioning from deep soft-contact penetration to near-rigid response at high kappa values.
- **Accelerated settling** as damping increases, with higher beta values producing faster energy dissipation and shorter transient response.
- **Vibration frequency modification** resulting from the coupled stiffness-damping interaction at the contact interface.
- **Multi-obstacle contact behavior** under boundary and distributed obstacle configurations.

These observations are quantitatively validated in the published paper and provide visual evidence that the DNC model captures physically realistic contact behavior.

## Animation Groups

The page is organized into five groups, each presenting a 2x2 synchronized comparison:

- **Page 1:** Single boundary obstacle, beta = 0.1, with kappa = 0.1, 10, 100, and 1000.
- **Page 2:** Single boundary obstacle under DNC conditions, including beta = 1 cases and stronger loading (f = -5).
- **Page 3:** Two boundary obstacles, beta = 1, with kappa = 0.1, 10, 100, and 1000.
- **Page 4:** Two boundary obstacles, beta = 5, with kappa = 0.1, 10, 100, and 1000.
- **Page 5:** Distributed obstacle set, beta = 1, with kappa = 0.1, 10, 100, and 1000.

## Viewer Controls

The page includes navigation and synchronization controls for precise comparison:

- **Prev / Next** buttons move between animation groups.
- **Numbered buttons** jump directly to a specific page.
- **Pause**, **Restart**, and **Sync** allow frame-level comparison across the four simultaneous animations.
- **Keyboard shortcuts:** Left/right arrows change pages. R restarts the current page. Number keys (1 through 5) jump to pages directly.

## Engineering Relevance

The parameter studies visualized here have direct engineering applications. The stiffness and damping values explored in these animations map to design variables in several domains:

- **MEMS and semiconductor devices**, where micro-scale contact interfaces undergo millions of loading cycles and reliability depends on energy dissipation at contact surfaces.
- **Transportation safety**, where crash detection systems and vehicle structural components involve impact dynamics with finite stiffness and damping.
- **Infrastructure resilience**, where bridge expansion joints, pavement-soil contact, and railway wheel-rail interfaces experience repetitive impact loading.
- **Robotics and prosthetics**, where controlled contact with objects and surfaces requires optimized stiffness-damping parameter selection.

By making these simulation results publicly available and visually accessible, this repository enables researchers and engineers to inspect DNC contact behavior without deriving the mathematics or running the solvers themselves.

## Repository Contents

- `index.html` contains the complete static viewer, including layout, navigation, video synchronization logic, and time overlays.
- `videos/` contains the beam-obstacle simulation animations in .mp4 format.
- `.github/workflows/static.yml` deploys the page to GitHub Pages from the main branch.

## Local Preview

To view the animations locally, open the page in any browser:

```bash
open index.html
```

## Citation

If you use these visualizations or the underlying simulation results in your work, please cite:

```
Saylor, G.; Shillor, M.; Vordey, C. "Model and Simulations of Contact Between
a Vibrating Beam and an Obstacle Using the Damped Normal Compliance Condition."
Axioms 2025, 14(12), 866.
```

## Author

Cornelius Bright Vordey
Ph.D. Candidate, Applied Mathematical Sciences
Oakland University, Rochester, Michigan
ORCID: [0009-0005-1644-9827](https://orcid.org/0009-0005-1644-9827)
