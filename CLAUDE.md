# Wochenplaner

Ein Wochen-Essensplaner fürs Handy, komplett auf Deutsch. Man wählt für jeden Wochentag (Mo–So) ein Abendessen und bekommt daraus eine Einkaufsliste, sortiert nach Supermarkt-Bereichen. Die App soll später auf GitHub Pages laufen.

## Funktionen (Version 1)

- **Reiter „Woche“**: pro Tag ein Abendessen per Auswahlliste; Button „Neue Woche“ leert Plan und Häkchen
- **Reiter „Gerichte“**: 8 vegetarische Startrezepte (Mengen für 1 Person) + Formular „Neues Gericht“ mit beliebig vielen Zutaten; eigene Gerichte können gelöscht werden (nicht bearbeitet). Der Supermarkt-Bereich ist nicht vorausgewählt: Bekannte Zutaten bekommen ihn automatisch, sonst muss er gewählt werden (nie still auf „Sonstiges“).
- **Reiter „Einkauf“**: Einkaufsliste aus allen geplanten Gerichten, nach Bereich gruppiert, gleiche Zutaten (Name + Einheit) zusammengezählt, abhakbar; Button „Liste teilen“ (Teilen-Menü am Handy, sonst Zwischenablage, nur offene Einträge)
- Plan, Häkchen und eigene Gerichte bleiben im localStorage erhalten

## Regeln

- **Eine einzige Datei `index.html`** mit HTML, CSS und JavaScript. Keine Frameworks, kein Build-Schritt, keine externen Dateien oder CDNs.
- **Oberfläche komplett auf Deutsch.** Code-Kommentare ebenfalls auf Deutsch.
- **Mobile-first**, schlichtes Design: Grundschrift 18 px, Tippflächen mindestens 48 px hoch.
- **Muster bei jeder Aktion:** Daten ändern → speichern → Anzeige neu malen.
- **Nutzereingaben nur mit `textContent` anzeigen**, nie über `innerHTML`.
- Supermarkt-Bereiche und Einheiten sind **nur an einer Stelle** im Code definiert (Konstanten `BEREICHE` und `EINHEITEN`).

### Supermarkt-Bereiche (feste Reihenfolge)

Obst & Gemüse · Kühlregal · Brot & Backwaren · Trockenware & Konserven · Gewürze & Öle · Tiefkühl · Sonstiges

### Einheiten

g, ml, Stück, Zehe, EL, TL, Prise, Bund, Dose, Packung

## Datenformat

Ein Gericht:

```js
{ id: "s1", name: "Linsen-Dal mit Reis", zutaten: [
  { name: "Rote Linsen", menge: 80, einheit: "g", bereich: "Trockenware & Konserven" }
]}
```

- Startrezepte haben IDs `s1`–`s8`, eigene Gerichte `e` + Zeitstempel.
- `menge` darf `null` und `einheit` leer (`""`) sein, z. B. bei „Salz und Pfeffer“.

localStorage-Schlüssel:

| Schlüssel | Inhalt |
|---|---|
| `wochenplaner.plan` | `{ "mo": "s1", "di": null, … }` |
| `wochenplaner.gerichte` | Array der eigenen Gerichte |
| `wochenplaner.haekchen` | Array von Schlüsseln `"bereich|name|einheit"` (klein geschrieben) |

Kaputte oder fehlende Daten im Speicher dürfen die App nicht abstürzen lassen. Dann wird mit leeren Werten gestartet.

## Hinweis zur Zusammenarbeit

Die Entwicklerin ist Anfängerin. Änderungen bitte in einfachen Worten erklären und kurz sagen, wo im Code sie stehen.
