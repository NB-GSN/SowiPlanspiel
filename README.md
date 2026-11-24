# Kabinett im Viereck

**Spielen:** https://nb-gsn.github.io/SowiPlanspiel/

<img src="assets/qr-code.png" alt="QR-Code zur Spielseite" width="300">

Planspiel zum **magischen Viereck** (und Achteck) der Wirtschaftspolitik für SOWI, Oberstufe Q1 (NRW, Inhaltsfeld 4: Wirtschaftspolitik).

Jede Dreiergruppe ist ein Kabinett aus Finanz-, Wirtschafts- und Arbeits-/Sozialministerium und regiert auf dem eigenen Gerät Deutschland von 2027 bis 2031. Jedes Ressort schlägt verdeckt eine Maßnahme vor, dann verhandelt das Kabinett und beschließt zwei Maßnahmen. Startwerte sind echte Daten vom Herbst 2026 (Destatis, Bundesbank, Bundesagentur für Arbeit, Umweltbundesamt, Jahreswirtschaftsbericht). Maßnahmen wirken verzögert, die EZB reagiert auf die Inflation, die Schuldenbremse begrenzt den Haushalt. Zum Schluss deckt die Lehrkraft das „Oktogon“ auf: Umwelt, Verteilung, Arbeitsbedingungen und Ressourcen wurden die ganze Zeit mitgerechnet.

## Bereiche der App

| Bereich | Gerät | Zweck |
|---|---|---|
| Lagebild | Beamer | Deutschland 2026 im Viereck, Werte schätzen und aufdecken, Zeitreihen 2015–2026 |
| Quiz | Team-Geräte | 10 zufällige Fragen: positiv/normativ, Bereiche, Träger, Marktversagen, Zielbeziehungen, Rechnen |
| Team-Spiel | ein Gerät pro Dreiergruppe | 5 Jahre: verdeckte Ressort-Vorschläge → Kabinettssitzung mit Konfliktanzeige → Beschluss → Bilanz mit Ressort-Punkten und Ergebniscode |
| Berater | Team-Geräte | Maßnahmenkatalog mit Wirkungsrichtung (sofort / 1 Jahr / langfristig) |
| Vergleich | Beamer | Kurswort für die Krise, Rundentimer, Ergebniscodes eintragen, Rangliste, „Oktogon aufdecken“, Gewichtung aus verschiedenen Blickwinkeln |
| Quellen & Modell | alle | Alle Quellen mit Links, Erklärung der Rechenregeln |

Ohne Server: Die Team-Geräte und der Beamer sind nicht verbunden. Die Teams nennen ihren kurzen Ergebniscode, die Lehrkraft trägt ihn am Beamer ein.

## Auf GitHub Pages veröffentlichen

1. Neues Repository auf GitHub anlegen (hier: `SowiPlanspiel`), öffentlich.
2. Die Dateien `index.html`, `README.md`, `ANLEITUNG.md`, `.nojekyll` und den Ordner `assets` hochladen („Add file → Upload files“).
3. Im Repository: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, Branch `main`, Ordner `/ (root)`, speichern.
4. Nach ca. einer Minute ist die Seite unter https://nb-gsn.github.io/SowiPlanspiel/ erreichbar.

Die App ist eine einzige HTML-Datei ohne Server, ohne Anmeldung und ohne Tracking. Spielstände liegen nur im Browser des jeweiligen Geräts (localStorage). Schriftarten werden von Google Fonts geladen; ohne Internet greift eine Systemschrift.

Direktlinks: `…/#team`, `…/#quiz`, `…/#berater`, `…/#vergleich`.

## Inhalte anpassen

Alle Daten stehen oben im `<script>`-Teil von `index.html`:

- `START`, `BASE`, `HISTORY`, `LAGE`, `SOURCES`: Ausgangswerte, Basispfad, Zeitreihen, Quellen
- `MEASURES`: Maßnahmenkatalog mit Wirkungen `fx` (sofort, +1 Jahr, langfristig)
- `EVENTS`: Krisenereignisse für Runde 3
- `QUIZ`: Quizfragen
- `ROLES`: die drei Ressorts mit ihren Zielen
- `PRESETS`: Gewichtungen der Interessengruppen im Vergleich

Lizenzvorschlag: CC BY-SA 4.0.
