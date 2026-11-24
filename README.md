# Kabinett im Viereck

**Spielen:** https://nb-gsn.github.io/SowiPlanspiel/

<img src="assets/qr-code.png" alt="QR-Code zur Spielseite" width="300">

Planspiel zum **magischen Viereck** (und Achteck) der Wirtschaftspolitik für SOWI, Oberstufe Q1 (NRW, Inhaltsfeld 4: Wirtschaftspolitik).

Vier Kabinette regieren Deutschland von 2027 bis 2031. Startwerte sind echte Daten vom Herbst 2026 (Destatis, Bundesbank, Bundesagentur für Arbeit, Umweltbundesamt, Jahreswirtschaftsbericht). Maßnahmen wirken verzögert, die EZB reagiert auf die Inflation, die Schuldenbremse begrenzt den Haushalt. Zum Schluss deckt die Lehrkraft das „Oktogon“ auf: Umwelt, Verteilung, Arbeitsbedingungen und Ressourcen wurden die ganze Zeit mitgerechnet.

## Bereiche der App

| Bereich | Gerät | Zweck |
|---|---|---|
| Lagebild | Beamer | Deutschland 2026 im Viereck, Werte schätzen und aufdecken, Zeitreihen 2015–2026 |
| Quiz | Handys der Teams | 10 zufällige Fragen: positiv/normativ, Bereiche, Träger, Marktversagen, Zielbeziehungen, Rechnen |
| Planspiel | Beamer | 5 Runden, je Team 2 Maßnahmen pro Jahr, Krisenereignis 2029, Jahresbilanz mit Radar und Wirkungsketten |
| Berater | Handys der Teams | Maßnahmenkatalog mit Wirkungsrichtung (sofort / 1 Jahr / langfristig) |
| Auswertung | Beamer | Rangliste, Verläufe, „Oktogon aufdecken“, Gewichtung aus verschiedenen Blickwinkeln |
| Quellen & Modell | alle | Alle Quellen mit Links, Erklärung der Rechenregeln |

## Auf GitHub Pages veröffentlichen

1. Neues Repository auf GitHub anlegen (hier: `SowiPlanspiel`), öffentlich.
2. Die Dateien `index.html`, `README.md`, `ANLEITUNG.md`, `.nojekyll` und den Ordner `assets` hochladen („Add file → Upload files“).
3. Im Repository: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, Branch `main`, Ordner `/ (root)`, speichern.
4. Nach ca. einer Minute ist die Seite unter https://nb-gsn.github.io/SowiPlanspiel/ erreichbar.

Die App ist eine einzige HTML-Datei ohne Server, ohne Anmeldung und ohne Tracking. Spielstände liegen nur im Browser des Beamer-Rechners (localStorage). Schriftarten werden von Google Fonts geladen; ohne Internet greift eine Systemschrift.

Direktlinks für die Handys: `…/#quiz` und `…/#berater`.

## Inhalte anpassen

Alle Daten stehen oben im `<script>`-Teil von `index.html`:

- `START`, `BASE`, `HISTORY`, `LAGE`, `SOURCES`: Ausgangswerte, Basispfad, Zeitreihen, Quellen
- `MEASURES`: Maßnahmenkatalog mit Wirkungen `fx` (sofort, +1 Jahr, langfristig)
- `EVENTS`: Krisenereignisse für Runde 3
- `QUIZ`: Quizfragen
- `PRESETS`: Gewichtungen der Interessengruppen (Grundlage für die geplante Rollen-Erweiterung)

Lizenzvorschlag: CC BY-SA 4.0.
