# PK-lab

En interaktiv norsk læringsapp for farmakokinetikk og farmakodynamikk. Åpne `index.html` i en moderne nettleser. Hele appen, inkludert anatomibildet, ligger i denne ene filen og fungerer uten installasjon eller eksterne biblioteker.

## Innhold

- Parameterverksted med forbindelser, definisjoner og før–etter-markeringer.
- Enkeltdose, gjentatt dosering, steady state, MEC/MTC og sammenligning av regimer.
- ADME og forenklede lever-/nyrescenarier.
- PK/PD med direkte Emax-modell og forklaring av EC50.
- Proteinbinding: fu, Cu, Ctot, CLint, QH, samt fm og hemming av en metabolismevei.
- Variasjonsbånd og 36 egenformulerte quizoppgaver.
- Lys/mørk modus, tastaturkontroller og lokal lagring av innstillinger.

Appen er en pedagogisk modell med hypotetiske legemiddelparametre. Kliniske doseringsbeslutninger krever legemiddelspesifikk informasjon og klinisk vurdering.

## Faglig grunnlag

Rowland and Tozer’s Clinical Pharmacokinetics and Pharmacodynamics: Concepts and Applications, 5. utgave, Hartmut Derendorf og Stephan Schmidt, særlig kapittel 4, 5, 8, 12 og 17. Oppgaver og forklaringer er nyformulerte. Læreboken, utdrag og originalfigurer distribueres ikke her. Anatomien er en generert generell illustrasjon.

## GitHub Pages

Velg **Settings → Pages → Deploy from a branch → main → /(root)**. Nettstedets startfil er `index.html`. Filen `.nojekyll` gjør at den serveres som en vanlig statisk side.

Det brukes ingen analysetjeneste eller app-backend. Innstillinger lagres i nettleserens localStorage. GitHub håndterer selve nettpubliseringen.
