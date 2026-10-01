# PK-lab

An interactive learning app in Norwegian, English and Arabic for pharmacokinetics and pharmacodynamics. Open `index.html` in a modern browser. The entire app, including the anatomical illustration, is contained in this single file and works without installation or external libraries.

## Contents

- Parameter workshop with relationships, definitions and before/after change markers.
- Single-dose, repeated-dose and steady-state views with MEC/MTC thresholds and regimen comparison.
- ADME and simplified liver- and kidney-function scenarios.
- PK/PD with a direct Emax model and an explanation of EC₅₀.
- Protein binding: fu, Cu, Ctot, CLint and QH, plus fm and inhibition of a metabolic pathway.
- Compartment lab with one- and two-compartment models, 320 particles and a synchronized concentration curve.
- First-order, zero-order and Michaelis–Menten saturation kinetics in the compartment lab.
- A floating lab in the parameter workshop, distribution-phase comparison and C₀ starting profiles.
- Uncertainty bands and 108 original quiz questions with topic filters and explanations.
- 56 interactive formula cards with clickable symbols, algebraic rearrangement, units, proportionality, numerical examples and step-by-step derivations.
- Always-on dark mode, keyboard controls and local settings saved in the browser.

The app is an educational model using hypothetical drug parameters. Clinical dosing decisions require drug-specific information and clinical judgment.

## About the app

Created by Mohanad Taiy, 2026 – For personal learning. Questions and explanations are independently written. The anatomy is a generated general illustration.

The compartment lab offers an IV bolus or oral dose with first-order absorption (F and kₐ), and elimination from the central compartment. First-order curves are calculated analytically; saturation and zero-order kinetics use a positive, mass-conserving numerical method. The particles are a stochastic illustration and may differ slightly from the smooth expected curve. The curve and dosing tab uses oral, linear first-order kinetics.

## GitHub Pages

Choose **Settings → Pages → Deploy from a branch → main → /(root)**. The site entry point is `index.html`. The `.nojekyll` file makes it serve as a regular static site.

There is no analytics service or app backend. Settings are stored in the browser's `localStorage`. GitHub handles the web hosting.

Choose the language with the 🌐 selector at the top. Arabic uses right-to-left layout, while formulas and graphs keep their mathematical left-to-right direction. The distribution comparison shows phases and AUC contributions; its phase boundary is an educational marker, not a biological switch.
