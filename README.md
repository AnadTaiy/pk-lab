# PK-lab

An interactive learning app in Norwegian, English and Arabic for pharmacokinetics and pharmacodynamics. Open `index.html` in a modern browser. The entire app, including the anatomical illustration, is contained in this single file and works without installation or external libraries.

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
- A purple browser-tab icon, softer gold organ outlines and a subtle 30-second light tracing the logo's letter contours.
- Basic and advanced views, a guided clearance example, and up to 12 saved workshop scenarios with a two-scenario comparison.
- A shared linear/semi-log graph setting. The compartment lab defaults to a single plasma concentration curve; a particle-derived curve and the full comparison are optional.
- Eliminated particles flow through a channel into a separate collection box. Volume of distribution illuminates the body silhouette while excluding the organs.
- Local PNG and PDF graph/result exports under **My experiments & export**. Prepare the export, then select its download link.
- An About me tab with a compact portrait and the story behind the app.

The app is an educational model using hypothetical drug parameters. Clinical dosing decisions require drug-specific information and clinical judgment.

## About the app

Created by Mohanad Taiy, a pharmacist living in Norway, 2026 – For personal learning. The app began during master's studies in pharmacy at UiT, in connection with FAR-3203, to make central pharmacokinetic models visual and intuitive. Questions and explanations are independently written. The anatomy is a generated general illustration.

The compartment lab offers an IV bolus or oral dose with first-order absorption (F and kₐ), and elimination from the central compartment. First-order curves are calculated analytically; saturation and zero-order kinetics use a positive, mass-conserving numerical method. The particles are a stochastic illustration and may differ slightly from the smooth expected curve. The curve and dosing tab uses oral, linear first-order kinetics.

## GitHub Pages

Choose **Settings → Pages → Deploy from a branch → main → /(root)**. The site entry point is `index.html`. The `.nojekyll` file makes it serve as a regular static site.

There is no analytics service or app backend. Settings are stored in the browser's `localStorage`. GitHub handles the web hosting.

Scenario storage covers the six workshop parameters and renal/hepatic function settings; it does not save every lab's independent controls. Exports capture the visible charts and numeric summaries as an image; PDF text is therefore not selectable. Export files are created locally, without a server upload. A browser must permit downloads to save them.

See [SECURITY.md](SECURITY.md) for the security scope and limitations. The standalone file uses a restrictive Content Security Policy with hashes for its bundled scripts. Rebuilding or editing scripts requires regenerating those hashes.

The initial language is inferred locally from the browser time zone: Norwegian for Norway, Arabic for time zones in Arab countries, and English elsewhere. If the time zone is unavailable, the browser locale is used. This is a regional hint, not verified residence. A manual choice in the 🌐 selector takes priority and is remembered. No geolocation permission or IP lookup is used. Arabic uses right-to-left layout, while formulas and graphs keep their mathematical left-to-right direction. The distribution comparison shows phases and AUC contributions; its phase boundary is an educational marker, not a biological switch.

Search metadata, author information, structured learning-resource data, a canonical URL and `sitemap.xml` are included. These help discovery but do not guarantee indexing or ranking. To request indexing, verify the URL-prefix property `https://anadtaiy.github.io/pk-lab/` in Google Search Console, submit the sitemap and inspect the homepage URL. Bing Webmaster Tools supports a corresponding sitemap submission. A `robots.txt` in this repository's `/pk-lab/` subpath would not control the host, so none is added here.
