# Schweizer Feiertage

Kantonale und nationale Feiertage der Schweiz — als JSON, pro Jahr und pro Kanton.

## Daten

| Datei | Inhalt |
|-------|--------|
| `holidays.json` | Kanonische Definitionen: Name (DE/FR/IT), Typ, Kantone |
| `2000.json` – `2040.json` | Alle Feiertage mit berechnetem Datum pro Jahr |
| `by_canton/2026/ZH.json` | Nur die Feiertage eines bestimmten Kantons |

## Zahlen

- **23** Feiertage (national, kantonal, kantonsspezifisch)
- **26** Kantone
- **2000–2040** vorberechnet

## Beispiel

### Alle Feiertage eines Jahres

```json
// 2026.json
[
  {
    "id": "neujahr",
    "name_de": "Neujahr",
    "name_fr": "Nouvel An",
    "name_it": "Capodanno",
    "date": "2026-01-01",
    "cantons": ["AG", "AI", "AR", "BE", "BL", "BS", "FR", "GE", "GL", "GR", "JU", "LU", "NE", "NW", "OW", "SG", "SH", "SO", "SZ", "TG", "TI", "UR", "VD", "VS", "ZG", "ZH"]
  },
  ...
]
```

### Kanonische Definition

```json
// holidays.json (Auszug)
{
  "id": "fronleichnam",
  "name_de": "Fronleichnam",
  "name_fr": "Fête-Dieu",
  "name_it": "Corpus Domini",
  "type": "movable",
  "offset": 60,
  "cantons": ["AG", "AI", "FR", "GR", "JU", "LU", "NW", "OW", "SO", "SZ", "TI", "UR", "VS", "ZG"]
}
```

## Feiertage nach Kanton

| Kanton | Anzahl | Besonderheiten |
|--------|--------|----------------|
| AG | 13 | Fronleichnam, Allerheiligen, Mariä Empfängnis |
| AI | 12 | Fronleichnam, Mariä Himmelfahrt, Allerheiligen, Mariä Empfängnis |
| AR | 8 | Protestantisch, kein Fronleichnam |
| BE | 9 | Berchtoldstag, kein Fronleichnam |
| BL | 9 | Tag der Arbeit |
| BS | 9 | Tag der Arbeit |
| FR | 13 | Zweisprachig, katholische Feiertage |
| GE | 9 | Genfer Bettag, Wiederherstellung der Republik |
| GL | 11 | Näfelser Fahrt, Allerheiligen |
| GR | 15 | Dreikönigstag, Josefstag |
| JU | 13 | Unabhängigkeitstag (23. Juni) |
| LU | 14 | Josefstag |
| NE | 10 | Fest der Republik (1. März) |
| NW | 13 | Josefstag |
| OW | 13 | Katholische Feiertage |
| SG | 9 | Allerheiligen |
| SH | 10 | Tag der Arbeit |
| SO | 14 | Josefstag |
| SZ | 14 | Dreikönigstag, Josefstag |
| TG | 10 | Tag der Arbeit |
| TI | 15 | Dreikönigstag, Peter und Paul |
| UR | 14 | Dreikönigstag, Josefstag |
| VD | 9 | Bettagsmontag |
| VS | 9 | Kein Karfreitag, kein Ostermontag, kein Pfingstmontag |
| ZG | 14 | Josefstag |
| ZH | 10 | Tag der Arbeit |

## Bewegliche Feiertage

Einige Feiertage hängen vom Osterdatum ab:

| Feiertag | Berechnung |
|----------|-----------|
| Karfreitag | Ostersonntag − 2 Tage |
| Ostermontag | Ostersonntag + 1 Tag |
| Auffahrt | Ostersonntag + 39 Tage |
| Pfingstmontag | Ostersonntag + 50 Tage |
| Fronleichnam | Ostersonntag + 60 Tage |

Sonderfälle:
- **Bettagsmontag (VD)**: Montag nach dem 3. Sonntag im September
- **Genfer Bettag (GE)**: Donnerstag nach dem 1. Sonntag im September
- **Näfelser Fahrt (GL)**: Erster Donnerstag im April

## Hinweise

- Diese Liste enthält **gesetzliche Feiertage** (arbeitsfrei). Halbe Feiertage und regionale Bräuche (Fasnacht, Zibelemärit, etc.) sind nicht enthalten.
- In Kantonen mit gemischter Konfession (z.B. AG, GR, FR) gelten einzelne Feiertage nur in bestimmten Gemeinden. Diese Datei bildet die **kantonale Regel** ab.
- Quelle: [SECO Feiertagsliste (PDF)](https://www.seco.admin.ch/dam/seco/de/dokumente/Arbeit/Arbeitsbedingungen/Arbeitsgesetz%20und%20Verordnungen/Feiertage-Schweiz.pdf.download.pdf/Anhang_Feiertage_de.pdf), [BJ Feiertagsverzeichnis (PDF)](https://www.bj.admin.ch/dam/bj/de/data/publiservice/service/zivilprozessrecht/kant-feiertage.pdf), kantonale Gesetzgebung.

## Lizenz

[MIT](LICENSE)

---

Gepflegt von [Milk Interactive](https://milkinteractive.ch) — [hello@milkinteractive.ch](mailto:hello@milkinteractive.ch)
