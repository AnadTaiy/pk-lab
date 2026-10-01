# PK-lab

En interaktiv norsk læringsapp for farmakokinetikk og farmakodynamikk. Åpne `index.html` i en moderne nettleser. Hele appen, inkludert anatomibildet, ligger i denne ene filen og fungerer uten installasjon eller eksterne biblioteker.

## Innhold

- Parameterverksted med forbindelser, definisjoner og før–etter-markeringer.
- Enkeltdose, gjentatt dosering, steady state, MEC/MTC og sammenligning av regimer.
- ADME og forenklede lever-/nyrescenarier.
- PK/PD med direkte Emax-modell og forklaring av EC50.
- Proteinbinding: fu, Cu, Ctot, CLint, QH, samt fm og hemming av en metabolismevei.
- Kompartmentlab med én/to kompartments, 320 partikler og synkronisert kurve.
- Første orden, nullte orden og Michaelis–Menten-metning i kompartmentlab.
- Flytende lab i parameterverkstedet, sammenligning av distribusjon og C₀-forløp.
- Variasjonsbånd og 108 egenformulerte quizoppgaver med temavalg og forklaringer.
- 56 interaktive formelkort med klikkbare symboler, algebraisk omorganisering, enheter, proporsjonalitet og regneeksempler.
- Lys/mørk modus, tastaturkontroller og lokal lagring av innstillinger.

Appen er en pedagogisk modell med hypotetiske legemiddelparametre. Kliniske doseringsbeslutninger krever legemiddelspesifikk informasjon og klinisk vurdering.

## Om appen

Laget av Mohanad Taiy, 2026 – til egen læring. Oppgaver og forklaringer er egenformulerte. Anatomien er en generert generell illustrasjon.

Kompartmentlab bruker i.v. bolus og eliminasjon fra det sentrale rommet. Førsteordenskurven beregnes analytisk; metning og nullte orden beregnes med en positiv, massebevarende numerisk metode. Partiklene er en stokastisk illustrasjon og kan avvike litt fra den glatte forventningskurven. Kurve- og doseringsfanen bruker fortsatt oral, lineær førsteordens kinetikk.

## GitHub Pages

Velg **Settings → Pages → Deploy from a branch → main → /(root)**. Nettstedets startfil er `index.html`. Filen `.nojekyll` gjør at den serveres som en vanlig statisk side.

Det brukes ingen analysetjeneste eller app-backend. Innstillinger lagres i nettleserens localStorage. GitHub håndterer selve nettpubliseringen.
