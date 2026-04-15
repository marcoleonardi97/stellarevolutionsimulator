# Stellar Evolution Simulator

Interactive web-based simulator for exploring the lifecycle of stars. Designed for educational use, it provides a simplified but physically motivated view of stellar evolution across different masses and metallicities. Try it [here](https://marcoleonardi97.github.io/stellarevolutionsimulator/)

## Overview

This project visualizes how stars evolve over time using two main diagrams:

- **Hertzsprung–Russell (HR) Diagram** — shows the star’s surface temperature vs luminosity
- **Core Evolution Diagram** — tracks central temperature vs central density

The simulation animates a star’s full lifecycle, from formation to final remnant, while displaying physical parameters and stage descriptions in real time.

## Features

- Adjustable **stellar mass** (0.8–20 M☉)
- Adjustable **metallicity (Z)**
- Real-time **evolution animation**
- Interactive **timeline navigation**
- Dual visualization:
  - HR diagram (log T_eff vs log L)
  - Core evolution (log T_c vs log ρ_c)
- Stage-by-stage **physical explanations**
- Live display of:
  - log T_eff
  - log L/L☉
  - log T_c
  - log ρ_c

## Stellar Phases Included

- Pre-Main Sequence (Hayashi track)
- Main Sequence (pp-chain / CNO cycle)
- Subgiant Branch
- Red Giant Branch
- Helium Flash (low-mass stars)
- Horizontal Branch / Core He Burning
- Asymptotic Giant Branch (AGB)
- Final stages:
  - White Dwarf (low/intermediate mass)
  - Core Collapse / Supernova (massive stars)

## Controls

- **Mass slider** — sets initial stellar mass
- **Metallicity slider** — adjusts composition
- **Speed slider** — controls animation rate
- **Play / Pause / Reset** — simulation control

Clicking stages in the timeline jumps directly to that phase.

## Model Notes

This is not a full stellar evolution code (e.g. MESA), but a **parametric approximation** based on known scaling relations:

- Main sequence lifetime:  
  \( t_{MS} \propto M^{-2.5} \)

- Luminosity scaling:  
  \( L \propto M^{4} \)

- Metallicity effects:
  - Lower Z → hotter, slightly more luminous stars

Core evolution tracks include approximate regimes:
- Ideal gas
- Degenerate matter (non-relativistic / relativistic)
- Radiation-dominated regions

## Technical Details

- Pure **HTML + CSS + JavaScript**
- Uses **Canvas API** for rendering
- No external dependencies
- Responsive layout (basic mobile support)

### Key Components

- `buildStages()` — generates evolutionary tracks
- `getPointOnStage()` — interpolates motion along tracks
- `drawHR()` / `drawCore()` — rendering logic
- Animation loop via `requestAnimationFrame`

## Usage

1. Open `index.html` in a browser  
   or deploy via GitHub Pages

2. Adjust mass and metallicity

3. Press **Play** to start evolution

## Deployment (GitHub Pages)

- Push repository to GitHub
- Enable Pages from the repository settings
- Set source to `main` branch (root)

The simulator will run directly in the browser.

## Limitations

- Simplified physics (not numerically solved stellar structure equations)
- No mass loss, rotation, or binaries
- Tracks are approximations, not observational fits

## Purpose

Built as a visualization tool to:
- Develop intuition for stellar evolution
- Connect HR diagram motion to core physics
- Provide a bridge between analytic scaling relations and full simulations

## License

Open for educational and personal use.
