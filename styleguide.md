# Styleguide — Inspired by bradleyziffer.com

> Persönliche Portfolio-Seite von Bradley Ziffer. Gebaut mit Framer.
> Charakter: organisch, intellektuell, handwerklich — minimalistisch mit bewussten Akzenten.

---

## 1. Farben / Color Palette

### Primärfarben

| Name              | Wert                        | Hex         | Verwendung                          |
|-------------------|-----------------------------|-------------|-------------------------------------|
| Almost Black      | `rgb(15, 17, 17)`           | `#0F1111`   | Haupttextfarbe, dunkle Sektionen    |
| True Black        | `rgb(20, 20, 19)`           | `#141413`   | Button-Text, Akzente                |
| White             | `rgb(255, 255, 255)`        | `#FFFFFF`   | Hintergrund (Hero, Body)            |
| Warm Off-White    | `rgb(255, 253, 247)`        | `#FFFDF7`   | Dunkle Sektionen, Footer-Kontrast   |
| Warm Surface      | `rgb(250, 249, 245)`        | `#FAF9F5`   | Button-Hintergrund                  |

### Akzentfarben

| Name              | Wert                        | Hex         | Verwendung                          |
|-------------------|-----------------------------|-------------|-------------------------------------|
| Sky Blue Tint     | `rgba(5, 154, 255, 0.15)`   | —           | Highlight-Overlay auf Hero-Text     |
| Cyan Light        | `rgb(153, 238, 255)`        | `#99EEFF`   | Bild-Akzent / Link-Hintergrund      |
| Cyan              | `rgb(68, 204, 255)`         | `#44CCFF`   | Dekoratives Element                 |
| Terracotta Glow   | `rgba(217, 119, 87, 0.24)`  | —           | Box-Shadow auf CTA-Button           |
| Muted Grey        | `rgb(108, 117, 117)`        | `#6C7575`   | Sekundäre Texte                     |

### Spezial-Effekte

```css
/* Text-Selektion */
::selection {
  background-color: #95E78E;  /* Mintgrün */
  color: #062C02;             /* Dunkelgrün */
}

/* Scrollbar versteckt */
::-webkit-scrollbar {
  width: 0px;
}

/* Font-Rendering */
:root {
  -webkit-font-smoothing: antialiased;
}
```

---

## 2. Typografie / Typography

Die Seite kombiniert drei sehr bewusst gewählte Schriftfamilien für unterschiedliche Stimmungen.

### Schriftarten

| Schrift              | Quelle        | Zweck                                  |
|----------------------|---------------|----------------------------------------|
| **Crimson Pro**      | Google Fonts  | Große Headlines, seriöse Eleganz       |
| **Plus Jakarta Sans**| Google Fonts  | Body, UI-Elemente, Navigation          |
| **VT323**            | Google Fonts  | Retro/Terminal-Akzente (Sektionslabel) |
| **JetBrains Mono**   | Google Fonts  | Code-Ästhetik, Bio-Texte               |

### Typografische Skala

```css
/* Display / Hero Headline */
.hero-title {
  font-family: 'Crimson Pro', serif;
  font-size: 48px;
  font-weight: 300;         /* Light! */
  line-height: 1.09;        /* ~52px */
  letter-spacing: -2.4px;   /* starkes Tight-Tracking */
  color: #0F1111;
}

/* Hero Italic Variant (Keyword-Highlighting) */
.hero-title em {
  font-style: italic;
  font-weight: 300;
  /* gleiche Größe, gleicher Tracking */
}

/* Section Title */
.section-title {
  font-family: 'Crimson Pro', serif;
  font-size: 24px;
  font-weight: 300;
  line-height: 1.09;
  letter-spacing: -1.2px;
  color: #0F1111;
}

/* Large Section Heading */
.large-heading {
  font-family: 'Crimson Pro', serif;
  font-size: 36px;
  font-weight: 300;
  line-height: 1.09;
  letter-spacing: -1.8px;
  color: #0F1111;
}

/* Footer / Closing Statement */
.footer-headline {
  font-family: 'Crimson Pro', serif;
  font-size: 48px; /* gleich wie Hero */
  font-weight: 300;
  /* "Build the world with intention" */
}

/* Body / Fließtext */
.body-text {
  font-family: 'Plus Jakarta Sans', sans-serif;
  font-size: 16px;
  font-weight: 400;
  line-height: 1.6;         /* ~25.6px */
  letter-spacing: -0.32px;
  color: #0F1111;
}

/* Navigation / CTA-Label */
.nav-label {
  font-family: 'Plus Jakarta Sans', sans-serif;
  font-size: 15px;
  font-weight: 500;
  line-height: 1.09;
  letter-spacing: -0.75px;
  color: #FFFFFF;           /* auf dunklem Button */
}

/* Tabellen-Rows / Work History */
.table-row {
  font-family: 'Plus Jakarta Sans', sans-serif;
  font-size: 20px;
  font-weight: 400;
  line-height: 1.09;
  letter-spacing: -1px;
  color: #0F1111;
}

/* Retro/Terminal Label */
.retro-label {
  font-family: 'VT323', monospace;
  font-size: 24px;
  font-weight: 400;
  line-height: 1.15;
  letter-spacing: -1.2px;
  color: #0F1111;
}

/* Bio / Prosa in Monospace */
.mono-text {
  font-family: 'JetBrains Mono', monospace;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.8;
  letter-spacing: -0.7px;
  color: #0F1111;
}
```

### Typografie-Prinzipien

- **Negatives Letter-Spacing** ist ein Kernmerkmal: alle Texte haben `letter-spacing` zwischen `-0.3px` und `-2.4px`
- **Sehr leichte Font-Weights** (300) für große Headlines — Eleganz statt Dominanz
- **Italic für Schlüsselwörter**: bestimmte Begriffe in Headlines werden kursiv gesetzt, nicht fett
- **Serif + Sans-Serif Mix**: Crimson Pro (editorial) trifft Plus Jakarta Sans (modern/UI)
- **Monospace als Persönlichkeitselement**: JetBrains Mono für die persönliche Bio

---

## 3. Layout & Spacing

### Grid / Container

```css
/* Haupt-Wrapper */
.page-wrapper {
  max-width: 810px;          /* centered content */
  margin: 0 auto;
  padding: 0 48px;           /* 48px horizontal padding */
}

/* Body start */
.page-top {
  padding-top: 20px;
}
```

### Sektions-Abstände

```css
/* Hero Section */
.section-hero {
  padding: 32px 0 20px;
}

/* Work / Content Sections */
.section-content {
  padding: 50px 0 70px;
}

/* Trennlinien */
.divider {
  border: none;
  border-top: 1px solid #0F1111;
  opacity: 0.15;             /* subtil */
}
```

### Layout-Muster

- **Single Column** für Text-Sektionen (max 714px Inhaltsbreite)
- **2-Spalten Masonry/Grid** für Projekt-Cards (je ~50% Breite, unterschiedliche Höhen)
- **3-Spalten Grid** für die Mood-Board/Gallery-Sektion
- **Tabellen-Layout** (Flexbox, 3 Spalten) für die Work-History: Titel | Firma | Jahr

---

## 4. Komponenten / Components

### Navigation Bar

```css
.navbar {
  position: fixed;           /* sticky, bleibt oben */
  top: 0;
  width: 100%;
  padding: 20px 48px 0;
  height: ~101px;
  background: transparent;   /* kein Hintergrund! */
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}

/* Logo — animierter Smiley (Lottie/Bild) */
.navbar-logo {
  width: ~72px;
  height: ~81px;
}
```

### CTA-Button (Primär — "Get in touch")

```css
.btn-primary {
  background-color: #141413;  /* fast schwarz */
  color: #FFFFFF;
  font-family: 'Plus Jakarta Sans', sans-serif;
  font-size: 15px;
  font-weight: 500;
  letter-spacing: -0.75px;
  padding: 12px 16px;
  border-radius: 12px;
  border: 0.5px solid rgba(31, 30, 29, 0.4);
  box-shadow:
    rgba(217, 119, 87, 0.24) 0px 40px 80px 0px,
    rgba(217, 119, 87, 0.24) 0px 4px 14px 0px;
  cursor: pointer;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

/* Hover: Arrow/Chevron fliegt rein von links */
.btn-primary:hover {
  /* Arrow-Icon taucht von links auf (absolute positioned) */
  /* via Framer Motion: left: 50% → left: 20px */
}
```

### Pill-Button (Sekundär — "Digital contributions")

```css
.btn-pill {
  background: transparent;
  border: 1px solid #0F1111;  /* CSS Custom Property: --border-color */
  border-radius: 70px;        /* vollständig rund */
  padding: 10px 20px;
  color: #0F1111;
  font-family: 'Crimson Pro', serif;
  font-size: 24px;
  font-weight: 300;
  letter-spacing: -1.2px;
  cursor: pointer;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}
```

### Projekt-Cards

```css
.project-card {
  border-radius: 20px;
  overflow: hidden;
  cursor: pointer;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  /* Kein expliziter Schatten im Ruhezustand */
}

.project-card img,
.project-card video {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 20px;
}
```

### Work History Table

```css
.work-table-row {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding: 20px 0;
  border-bottom: 1px solid rgba(15, 17, 17, 0.15);
}

/* Spalten: Role | Company | Year */
.work-role   { font-size: 20px; }
.work-company{ font-size: 20px; color: #6C7575; }  /* gedimmt */
.work-year   { font-size: 20px; color: #6C7575; }
```

### Gallery / Mood Board

```css
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 8px;
}

.gallery-item {
  border-radius: 10px;
  overflow: hidden;
  aspect-ratio: 1 / 1;
}
```

---

## 5. Animationen / Motion

Die Animationen sind das Herzstück des Designs. Alle basieren auf **Framer Motion** (React), lassen sich aber mit CSS nachbauen.

### Easing / Timing Function

```css
/* Standard-Easing für fast alle Transitions */
--ease-smooth: cubic-bezier(0.4, 0, 0.2, 1);

/* Dauer */
--duration-fast:   200ms;
--duration-normal: 300ms;
--duration-slow:   500ms;
```

### Scroll-Animationen (Reveal on Scroll)

```css
/* Elemente kommen von unten herein */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(24px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.reveal {
  animation: fadeInUp 0.5s cubic-bezier(0.4, 0, 0.2, 1) both;
}
```

### Button Hover — Arrow-Slide

```css
/* "Get in touch" Button: Pfeil-Icon fährt von rechts nach links rein */
.btn-primary .arrow-icon {
  position: absolute;
  left: 50%;
  top: 51%;
  transform: translateY(-50%);
  transition: left 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  white-space: nowrap;
}

.btn-primary:hover .arrow-icon {
  left: 20px;               /* fährt von Mitte nach links */
}
```

### Sticky Logo (Smiley-Face)

```css
/* Das Smiley-Logo folgt dem Scroll und bleibt immer sichtbar */
.logo {
  position: fixed;
  top: 20px;
  left: 48px;
  z-index: 100;
  /* Lottie Animation: Smiley bewegt sich / wackelt */
}
```

### Sticky Nav Button

```css
/* CTA-Button klebt ebenfalls beim Scrollen */
.btn-sticky {
  position: fixed;
  top: 20px;
  right: 48px;
  z-index: 100;
}
```

### Card Hover

```css
.project-card {
  transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1),
              box-shadow 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.project-card:hover {
  transform: scale(1.02) translateY(-4px);
  box-shadow: 0 20px 60px rgba(15, 17, 17, 0.15);
}
```

### Text-Highlighting Highlight (Hero)

```css
/* "software paradigms" hat einen blauen Hintergrund-Highlight */
.highlight {
  background-color: rgba(5, 154, 255, 0.15);
  border-radius: 4px;
  padding: 0 4px;
  /* Animiert via Framer: erscheint beim ersten Render */
}
```

### Typografische Symbole als Dekoration

Bestimmte Zeichen werden als visuelle Elemente genutzt — kein Bild, nur Text/Emoji:
- `⟢` — Pfeil/Zeiger Charakter (neben dem CTA-Button)
- `❋` — Blumen-Asterisk (in Headlines)
- `✳` — Sternchen / Burst-Symbol (in Headlines)
- `— — — — —` — gestrichelte Trennlinie (als Textkette)

---

## 6. Globale Design-Prinzipien

### Visuelles Vokabular

1. **Whitespace ist Inhalt** — großzügige Abstände, keine Überladung
2. **Leichtigkeit** — Light-Weights (300) dominieren die Headlines
3. **Tight Tracking** — negatives Letter-Spacing gibt Texten Charakter
4. **Mix aus Hochkultur und Subkultur** — Serif-Eleganz trifft Terminal-Schrift
5. **Organische Elemente** — Smiley-Logo, Signatur-Bild, handgezeichnet wirkende Akzente
6. **Dunkle Sektionen sparsam** — fast alles ist weiß, der Dark-Footer wirkt wie ein Statement
7. **Keine Borders/Shadows im Standard** — Tiefe entsteht durch Kontrast und Whitespace

### Cursor / Interaktion

```css
/* Alles Klickbare hat cursor: pointer — aber kein custom cursor */
a, button, [role="button"] {
  cursor: pointer;
}
```

### Responsive Haltung

- Klare max-width von `810px` für Inhalte
- Padding von `48px` links/rechts reduziert auf Mobile (~20px)
- Bilder/Cards: auf Mobile von 2-spaltig auf 1-spaltig

---

## 7. CSS-Reset & Basis

```css
/* Reset */
html, body, #main {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

*, *::before, *::after {
  box-sizing: border-box;
  -webkit-font-smoothing: inherit;
}

h1, h2, h3, h4, h5, h6, p, figure {
  margin: 0;
}

/* Hidden Scrollbar */
::-webkit-scrollbar {
  width: 0px;
}

/* Custom Selection */
::selection {
  background-color: #95E78E;
  color: #062C02;
}

/* Font Smoothing */
:root {
  -webkit-font-smoothing: antialiased;
}
```

---

## 8. Google Fonts Import

```css
@import url('https://fonts.googleapis.com/css2?family=Crimson+Pro:ital,wght@0,300;0,400;1,300;1,400&family=Plus+Jakarta+Sans:wght@400;500;600&family=JetBrains+Mono:wght@300;400&family=VT323&display=swap');
```

---

*Styleguide erstellt als Inspiration auf Basis von bradleyziffer.com — Stand Juli 2026*
