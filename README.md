# PK-lab

An interactive learning app in Norwegian, English and Arabic for pharmacokinetics and pharmacodynamics. The hosted version uses `index.html` plus two locally hosted image files in `assets/`. Its HTML stays comfortably below Googlebot’s 2 MB crawl limit, while browsers can cache the images across updates. It works without installation or external libraries. A separate standalone HTML export embeds the images for offline sharing.

## Contents

- Parameter workshop with relationships, definitions and before/after change markers.
- Pulsing organ illumination with a brighter light traveling around each selected organ's contour.
- Single-dose, repeated-dose and steady-state views with MEC/MTC thresholds and regimen comparison.
- Multiple-dose regimen lab: oral or instantaneous input, accumulation curves, peak/trough/average concentrations, body amounts, loading dose, and step-by-step calculations. A therapeutic-window planner checks both concentration limits after rounding to a dose increment.
- ADME and simplified liver- and kidney-function scenarios.
- PK/PD with a direct Emax model and an explanation of EC₅₀.
- Protein binding: fu, Cu, Ctot, CLint and QH, plus fm and inhibition of a metabolic pathway.
- Compartment lab with one- and two-compartment models, 320 particles and a synchronized concentration curve.
- First-order, zero-order and Michaelis–Menten saturation kinetics in the compartment lab.
- A floating lab in the parameter workshop, distribution-phase comparison and C₀ starting profiles.
- Uncertainty bands and 108 original quiz questions with topic filters and explanations.
- 56 interactive formula cards with clickable symbols, algebraic rearrangement, units, proportionality, numerical examples and step-by-step derivations.
- Always-on dark mode, keyboard controls and local settings saved in the browser.
- A purple browser-tab icon, translucent gold organ outlines and a black line tracing the logo's letter contours before fading out after 30 seconds. The logo returns to the parameter workshop.
- All advanced controls are available directly, without a level switch. Workshop connections have a damped spring motion and a single, crisp light pulse each time a parameter is selected.
- A shared linear/semi-log graph setting, with semi-log selected by default. The compartment lab defaults to a single plasma concentration curve; a particle-derived curve and the full comparison are optional.
- Oral absorption and elimination use the same smooth particle movement: gather at an outlet, follow a channel, then disperse in the destination box. The underlying kinetic events are unchanged.
- Vd and D illuminate the body below the chin and the boundary around the organ cavity, excluding the face and organs. The illuminated body area becomes less transparent as Vd increases and more transparent as Vd decreases. A soft illuminated area accompanies the translucent gold contours, which keep their animation phase when switching selections.
- Reset the entire compartment lab or just its timeline. The workshop reset button appears only when its parameters differ from their defaults.
- Nine reproducible compartment examples cover rapid/slow distribution, fixed-fraction and fixed-amount elimination, low-dose saturation, slow absorption, reduced clearance, and high-dose IV/oral saturation. The two 12-hour saturation cases move from approximately zero-order elimination to approximately first-order elimination at around 8.4 hours, with reference markers on the curve. Semi-log scaling reveals the low-concentration tail.
- Simple kinetic-order experiments compare 100 → 80 → 64 mg (20% per hour) with 100 → 80 → 60 mg (20 mg per hour). Each uses one compartment and an IV bolus, with the amount eliminated during the last complete hour shown alongside the simulation.
- Strong amber and cyan-blue lines distinguish zero- and first-order elimination. Under Michaelis–Menten elimination the colour blends continuously with saturation; approximate labels use C/Km ≥ 10 and C/Km ≤ 0.1. The detailed explanation is collapsible. Absorption and distribution can still affect the observed curve shape.
- An About me tab at the far right, with a compact portrait and the story behind the app.

The app is an educational model using hypothetical drug parameters. Clinical dosing decisions require drug-specific information and clinical judgment.

## About the app

Created by Mohanad Taiy, a pharmacist living in Norway, 2026 – For personal learning. The app began during master's studies in pharmacy at UiT – The Arctic University of Norway, in connection with FAR-3203, to make central pharmacokinetic models visual and intuitive. Questions and explanations are independently written. The anatomy is a generated general illustration.

The compartment lab offers an IV bolus or oral dose with first-order absorption (F and kₐ), and elimination from the central compartment. First-order curves are calculated analytically; saturation and zero-order kinetics use a positive, mass-conserving numerical method. The particles are a stochastic illustration and may differ slightly from the smooth expected curve. The curve and dosing tab uses oral, linear first-order kinetics.

## GitHub Pages

Choose **Settings → Pages → Deploy from a branch → main → /(root)**. The site entry point is `index.html`. The `.nojekyll` file makes it serve as a regular static site.

There is no analytics service or app backend. Settings are stored in the browser's `localStorage`. GitHub handles the web hosting.

Named scenario storage, file exports and introductory workshop shortcuts have been removed. Ordinary parameter and language preferences are still remembered locally.

See [SECURITY.md](SECURITY.md) for the security scope and limitations. The standalone file uses a restrictive Content Security Policy with hashes for its bundled scripts. Rebuilding or editing scripts requires regenerating those hashes.

The initial language is inferred locally from the browser time zone: Norwegian for Norway, Arabic for time zones in Arab countries, and English elsewhere. If the time zone is unavailable, the browser locale is used. This is a regional hint, not verified residence. A manual choice in the 🌐 selector takes priority and is remembered. No geolocation permission or IP lookup is used. Arabic uses right-to-left layout, while formulas and graphs keep their mathematical left-to-right direction. The distribution comparison shows phases and AUC contributions; its phase boundary is an educational marker, not a biological switch.

Search metadata, author information, structured learning-resource data, a canonical URL and `sitemap.xml` are included. These help discovery but do not guarantee indexing or ranking. To request indexing, verify the URL-prefix property `https://anadtaiy.github.io/pk-lab/` in Google Search Console, submit the sitemap and inspect the homepage URL. Bing Webmaster Tools supports a corresponding sitemap submission. A `robots.txt` in this repository's `/pk-lab/` subpath would not control the host, so none is added here.

Oral concentration plots highlight the rising absorption phase in green, including repeated dosing. Absorption and elimination occur simultaneously; absorption can continue after Cmax. Saturation examples preserve Michaelis–Menten kinetics throughout the gradual transition.
# Loading and tablet layout

The dark loading screen stays visible until the initial layout and anatomy image are ready. On tablet-sized screens, the workshop spans the page, with a dedicated connection corridor and equal-height cards; anatomy appears below it. Ropes stay still on tablets while retaining the selection pulse. The particle canvas uses a lower pixel density and approximately 30 visual updates per second on medium screens and touch devices. Simulation time remains based on elapsed time. Hidden organ animations pause, and translations update only changed text regions.
