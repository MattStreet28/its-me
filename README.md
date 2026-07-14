# Mathias Strasser – Portfolio

Persönliche Portfolio-Website: Agile Coach, Scrum Master & Release Train Engineer mit über 15 Jahren Erfahrung in Automotive, Energy, Financial Services und Telekommunikation – plus eigene KI- und No-Code/Low-Code-Projekte als Beleg technischer Breite.

Komplett "vibecoded" im Terminal mit [Claude Code](https://claude.com/claude-code) – kein Framework, kein Build-Schritt.

## Struktur

Statisches Multi-Page-HTML/CSS, ein gemeinsames Stylesheet für alle Seiten:

```
index.html            Startseite: Hero, Haltung, Werdegang, Projekt-Übersicht
discogs.html           Projekt: Discogs Sammlung Viewer
rfp-checker.html        Projekt: RFP Analyzer
health-check.html       Projekt: Squad Health Check Coach
ki-workshop.html        Projekt: KI Workshop
styles.css             gemeinsames Stylesheet (Custom Properties, BEM-artige Klassen)
styleguide.md          Design-Tokens (Farben, Typografie, Spacing)
```

Bild-Assets liegen projektweise in eigenen Ordnern (`Discogs/`, `Health Check/`, `RFP Analyzer/`, `Workshop/`, `Badges/`).

## Lokal starten

Keine Dependencies, kein Build – einfach über einen simplen HTTP-Server ausliefern (für relative Pfade/Fonts nötig, `file://` reicht meist auch):

```bash
python3 -m http.server 8766
```

Danach `http://localhost:8766` öffnen.

## Design

- Typografie: [Crimson Pro](https://fonts.google.com/specimen/Crimson+Pro) (Serif, Headlines), [Plus Jakarta Sans](https://fonts.google.com/specimen/Plus+Jakarta+Sans) (Sans, Fließtext), [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) (Mono, Akzente)
- Farb-, Typo- und Spacing-Tokens als CSS Custom Properties in `styles.css`, dokumentiert in `styleguide.md`
- Mobile-first, responsive über `@media`-Breakpoints bei 600px / 1024px

## Kontakt

[mathias.strasser@gmx.de](mailto:mathias.strasser@gmx.de) · [LinkedIn](https://linkedin.com/in/mathias-straßer)
