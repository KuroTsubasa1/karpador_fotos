# Karpador Fotos

Static-Site für **Karpador Fotos** — Anime-Convention-Foto-Crew mit Bauchladen, mobilem Drucker und ein paar gehäkelten Magikarp-Mützen. Live: [karpador-fotos.de](https://karpador-fotos.de).

Das Projekt ist gleichzeitig Marketing-Vehikel für die Mutterfirma **[3D Print Shop Harm](https://3dps.space/)** — alle Bauchladen-Schilder, Karpador-Logos und Sticker werden im 3DPS-Studio gedruckt.

---

## Tech

- **Static HTML/CSS/JS**, kein Build-Step, keine Framework-Abhängigkeit
- Google Fonts: Fredoka (Display) · Nunito (Body) · Caveat (Hand)
- Externe Libs (CDN, nur wo nötig):
  - `qrcode-generator@1.4.4` — lokale QR-Generierung auf der Visitenkarten-Seite
  - `html-to-image@1.11.13` — PNG-Export der Visitenkarten

## Seiten

| Pfad | Zweck |
|---|---|
| `/index.html` | Home mit Hero, Foto-Wiederfinden-CTA, How-it-works-Teaser, Instagram-CTA, Galerie-Teaser, Spenden-Teaser, Events-Teaser |
| `/so-funktionierts.html` | Vier Schritte ausführlich + FAQ |
| `/galerie.html` | Bilder-Grid + BTS „Aus dem Druckerstudio" (3DPS-Branding) |
| `/spenden.html` | Letztjähriges Plüschtier-Ziel (erreicht) + aktuelles Japan-Ziel 2026 |
| `/events.html` | Tour-Daten (Polaris 2025 vergangen · DoKomi 2026, Polaris 2026 kommend) |
| `/ueber-uns.html` | Crew-Story, Karpador-Trio (mit Avataren), dunkle 3DPS-Mutterfirma-Sektion |
| `/kontakt.html` | Form (POST an pocket.lasseharm.space) + Direktkontakt-Karten. Liest `?topic=…` und preselectet Dropdown |
| `/business-card.html` | Visitenkarten-Vorschau & Druckvorlage. PNG-Download (Vorderseite, Rückseite, A6 Hochkant für Social-Share). Druck = A4 mit 10 Karten |
| `/business-card-3dps.html` | Mutterfirma-Visitenkarte mit 3DPS-Branding |
| `/brand.html` | Brand-Guide (Farbpalette, Typo, Logo-Varianten, Tone of Voice) — nicht in Nav verlinkt |
| `/how-it-works-print.html` | A3-Druckvorlage fürs Bauchladen-Schild (2 × A4 Querformat) mit Header + 4 Schritten + Japan-Spendenziel-Banner |

## Brand-Identity

Vollständig in `brand.html` dokumentiert. Kurzfassung:

- **Karpador-Palette** (`styles.css :root`):
  Orange `#FF7A1A` · Deep `#E85D04` · Yellow `#FFD23F` · Pink `#FF6B9D`
  · Aqua `#4ECDC4` · Cream `#FFF8E7` · Ink `#1A1B3A`
- **3DPS-Lime** (Mutterfirma-Akzent): `#6DAF46` (`--lime`), aus dem Logo extrahiert
- **Schriften**: Fredoka 600/700 (Display), Nunito 400/600/700 (Body), Caveat 700 (Hand-Akzent)
- **Style-Sprache**: dicke schwarze Outlines (1.2-3 mm im Print, 2-3 px digital) + 3D-Block-Shadows
  (`box-shadow: Npx Npx 0 var(--ink)`) für den verspielten, leicht-cartoon Look

## Assets

```
assets/
├── logo.svg              Karpador-Maskottchen mit Kamera-Linse als Pupille
├── wordmark.svg          Maskottchen + „KARPADOR FOTOS" Schriftzug
├── favicon.svg           Browser-Icon
├── avatar-fotograf.svg   Crew-Avatar (Karpador + Kamera)
├── avatar-drucker.svg    Crew-Avatar (Karpador + Drucker + Headphones)
├── avatar-sidekick.svg   Crew-Avatar (Wasser-Tropfen-Charakter)
├── icon-{camera,fish,heart,print}.svg   How-it-works Icons
├── 3dps-logo.png         3DPS-Logo (512×512 PNG, 228 KB)
├── 3dps-logo.webp        3DPS-Logo (WebP, 28 KB) — fürs Web
└── wave.svg              dekoratives Wellen-Element
```

