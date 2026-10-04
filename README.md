# Wochenplaner 🥕

Ein gemütlicher Essensplaner fürs Handy: Für jeden Wochentag ein Abendessen auswählen und daraus automatisch eine Einkaufsliste bekommen, sortiert nach den Bereichen im Supermarkt.

**👉 App öffnen: [lara-kristin-dev.github.io/wochenplaner](https://lara-kristin-dev.github.io/wochenplaner/)**

## Funktionen

- **Woche planen**: Montag bis Sonntag je ein Abendessen auswählen. „Neue Woche“ leert Plan und Häkchen.
- **8 vegetarische Startrezepte**: Mengen für 1 Person, z. B. Linsen-Dal, Chili sin Carne oder Gnocchi-Spinat-Pfanne.
- **Eigene Gerichte**: Name und beliebig viele Zutaten eintragen. Bekannte Zutaten werden automatisch dem richtigen Supermarkt-Bereich zugeordnet. Eigene Gerichte lassen sich auch wieder löschen.
- **Einkaufsliste**:
  - Sie entsteht automatisch aus allen geplanten Gerichten.
  - Gleiche Zutaten werden zusammengezählt (2 × 1 Zwiebel = 2 Zwiebeln).
  - Die Einträge sind nach Bereichen gruppiert: Obst & Gemüse, Kühlregal, Brot & Backwaren, Trockenware & Konserven, Gewürze & Öle, Tiefkühl, Sonstiges.
  - Alles lässt sich abhaken.
- **Liste teilen**: Am Handy öffnet sich das Teilen-Menü (z. B. WhatsApp oder Notizen), am Computer wird die Liste in die Zwischenablage kopiert. Geteilt werden nur die noch offenen Einträge.
- **Merkt sich alles**: Plan, Häkchen und eigene Gerichte bleiben nach dem Neuladen erhalten.

## Tipp fürs Handy

Die Seite im Handy-Browser öffnen und im Browser-Menü **„Zum Startbildschirm hinzufügen“** wählen. Dann hat der Wochenplaner ein eigenes Symbol wie eine richtige App.

## Wo sind meine Daten?

Alles wird nur **im Browser auf deinem Gerät** gespeichert (localStorage). Es gibt kein Konto und keinen Server, und nichts wird hochgeladen. Deshalb gilt:

- Handy und Computer haben jeweils ihren eigenen Plan.
- Löscht man die Browserdaten, sind auch Plan, Häkchen und eigene Gerichte weg.

## Technik

- Eine einzige Datei: [`index.html`](index.html) mit HTML, CSS und JavaScript
- Keine Frameworks, kein Build-Schritt, keine externen Dateien
- Gehostet mit GitHub Pages: Jede Änderung auf `main` ist nach 1–2 Minuten online

## Lokal ausprobieren

Repository herunterladen und `index.html` per Doppelklick im Browser öffnen. Mehr braucht es nicht.

```bash
git clone https://github.com/lara-kristin-dev/wochenplaner.git
```

Die Projektregeln und das Design (Farben, Schriften) stehen in der [`CLAUDE.md`](CLAUDE.md).
