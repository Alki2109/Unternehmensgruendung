# Konsolidierung-und-Migrationsmatrix

Bereich: A-Werkzeug/Bauplan
Schutzklasse: intern
Soll-Knoten: G-Governance
Status: Draft

# Konsolidierungs-Konzeption & Migrationsmatrix (Wissen zusammenführen)

**Erstelldatum (fix):** 10.07.2026, 05:28 (Europe/Berlin)

**Letzte Aktualisierung:** 10.07.2026, 05:28 (Europe/Berlin)

**Status:** Draft

**Zweck:** Verbindliches Vorgehen, um verstreutes Wissen aus drei Quellen (GitHub-Repo, Notion, diese Arbeits-Session) plus weitere Einzelartefakte konfliktfrei in einen aufgeräumten Zielstand zu überführen. Enthält Grundfluss, Konfliktregel und die Migrationsmatrix (Zuordnung Dokument → Soll-Struktur-Knoten + Quelle/Vorrang).

**Fehlt (kurz):** Vollständige Liste aller Einzelartefakte (Organigramm, Digital-Twin-Konzept, Ideensammlungen) mit Dateinamen + reale Repo-Pfade + Bestätigung der Notion-Deltas (welche punktuellen Änderungen sind nur in Notion).

**KI-Referenz:** KONSOLIDIERUNG-MIGRATIONSMATRIX

Update-Historie (Evolution)

| Zeitpunkt (TZ) | Änderung |
| --- | --- |
| 10.07.2026, 05:28 (Europe/Berlin) | Initiale Konzeption: Grundfluss Repo→Staging→Session/Notion, Konfliktregel, Migrationsmatrix |

Standard: siehe Dokumentations-Styleguide (Global) und Soll-Struktur (SOLL-MIGRATION-0001). Diese Konzeption ist die praktische Umsetzung des Migrations-Knotens der Soll-Struktur.

Navigation:

| Fachliche ID | Titel/Label | Typ |
| --- | --- | --- |
| KONS-QUELLEN-0001 | Die drei Quellen & ihr Aktualitätsstand | Kapitel |
| KONS-FLUSS-0001 | Grundfluss (Repo → Staging → Session/Notion) | Kapitel |
| KONS-KONFLIKT-0001 | Konfliktregel (Vorrang je Inhalt) | Kapitel |
| KONS-STAGING-0001 | Staging-Ordner & Quellenvermerk | Kapitel |
| KONS-MATRIX-0001 | Migrationsmatrix | Kapitel |
| KONS-TERMINAL-0001 | Übergabe an die Terminal-Instanz | Kapitel |

## Die drei Quellen & ihr Aktualitätsstand

ID: KONS-QUELLEN-0001

Kein Ort ist durchgängig der neueste — das ist der Kern der Herausforderung:

- **GitHub-Repo** – definierte Single Source of Truth. Enthält das Regelwerk zur KI-getriebenen OO-/Multi-Agent-Softwareerstellung inkl. der Retrospektive-Anweisungen aus dem Building (vor ~4 Wochen). Nicht überall der neueste inhaltliche Stand.
- **Notion** – eigentlicher Alt-Stand, kann aber punktuelle Änderungen enthalten, die im Repo fehlen (Notion-Deltas).
- **Diese Arbeits-Session** – Entstehungsort des Großteils der neuen Erkenntnisse und Dokumente (Soll-Struktur, Richtlinie G7, Kapitel 3a/4a/6a/6b, Regelwerke Meetings/Prompting/ID-Vergabe).
- **Weitere Einzelartefakte** (bei dir lokal) – Organigramm/Unternehmensstruktur, Digital-Twin-Konzept, Anwendungs-/Konzeptideen; konzeptionell detaillierter, aber unfertig.

## Grundfluss (Repo → Staging → Session/Notion)

ID: KONS-FLUSS-0001

Gewählter Grundfluss:

1. **Repo → Staging**: Den Repo-Stand als Ausgangsbasis in den Staging-Ordner exportieren (er trägt die Retrospektive-Anweisungen, die es nur dort gibt).
2. **Session einpflegen**: Die in dieser Session entstandenen Dokumente in den Staging-Ordner überführen; bei thematischer Überschneidung ersetzt der Session-Stand den Repo-Stand (neuer).
3. **Notion-Deltas einpflegen**: Gezielt die punktuellen Notion-Änderungen identifizieren und übernehmen, die weder im Repo noch in der Session enthalten sind — nicht pauschal Notion darüberlegen.
4. **Einzelartefakte einordnen**: Organigramm, Digital-Twin-Konzept etc. den Soll-Struktur-Knoten zuordnen und als Grundlage aufnehmen.
5. **Staging → Zielsystem**: Du kopierst den geprüften Staging-Ordner auf das Hetzner-Ubuntu-System; die Terminal-Instanz führt die definierten Schritte aus (KONS-TERMINAL-0001).

## Konfliktregel (Vorrang je Inhalt)

ID: KONS-KONFLIKT-0001

Vorrang wird pro Inhalt entschieden, nicht pauschal pro Quelle:

- **Session gewinnt** bei allen Themen, die hier neu erarbeitet wurden (Gründungskapitel neu, Soll-Struktur, Richtlinie, Regelwerke dieser Session).
- **Repo gewinnt** bei OO-/Multi-Agent-Softwareregelwerk und den Retrospektive-Anweisungen (nur dort vorhanden).
- **Notion gewinnt** nur bei nachweislichen Notion-Deltas (punktuelle Änderungen, die sonst nirgends stehen).
- **Einzelartefakte** sind Grundlage/Ergänzung, wo noch nichts Vergleichbares existiert; überschneiden sie sich, gilt die Session-/Repo-Regel.

Grundsatz: Im Zweifel nichts überschreiben, sondern als Konflikt markieren und vorlegen. Ein überschriebener neuerer Stand ist schwerer wiederherzustellen als ein markierter Konflikt.

## Staging-Ordner & Quellenvermerk

ID: KONS-STAGING-0001

Vorgeschlagene Struktur (an Soll-Struktur A–G angelehnt):

```
/staging/
  A-gruendung/
  B-konzepte/        (Digital-Twin, Vision)
  C-struktur/        (Organigramm, virtuelles Personal)
  D-prozesse/
  E-agentic/         (OO-/Multi-Agent-Regelwerk aus dem Repo)
  F-wissen/          (Styleguide, Chunking, Prompting)
  G-governance/      (Meetings, ID-Vergabe, Richtlinie G7)
  _quelle.md         (pro Bereich: Datei → Herkunft → Stand → Vorrang)
```

Die `_quelle.md` je Bereich ist Pflicht und die praktische Umsetzung der Konfliktregel: Sie hält für jede Datei fest, woher der maßgebliche Stand stammt und was bei Konflikt gilt.

## Migrationsmatrix

ID: KONS-MATRIX-0001

Zuordnung der bekannten Dokumente zu Soll-Struktur-Knoten, Quelle und Vorrang. (Zu ergänzen um die noch nicht gelisteten Einzelartefakte und reale Repo-Pfade.)

| Dokument | Ziel-Knoten | Maßgebliche Quelle | Vorrang/Status |
| --- | --- | --- | --- |
| Gründungsdoku Kapitel 1–9 | A | Notion/Repo | Basis; Session-Kapitel ergänzen |
| Kapitel 3a Finanzszenarien | A4 | Session | Session gewinnt |
| Kapitel 4a IHK/Einstiegsgeld | A6 | Session | Session gewinnt |
| Businessplan V2 / Finanzplan V2 | A3/A4 | Notion | Deltas prüfen, Session-Zahlen einarbeiten |
| Digital-Twin-Konzept | B2 | Einzelartefakt | Grundlage, unfertig |
| Organigramm/Unternehmensstruktur | C1 | Einzelartefakt | Grundlage, unfertig |
| OO-/Multi-Agent-Softwareregelwerk | E | Repo | Repo gewinnt (inkl. Retrospektive) |
| SD-Wissensbasis (KB-…) | E/F | Repo | Repo; via Brücke Kap. 6a referenziert |
| Prompting-Dreischicht (KB-PROMPT-0030) | F6 | Session | Session gewinnt |
| Dokumentations-Styleguide (global) | G1/F1 | Notion/Repo | bestehend, prüfen ob Deltas |
| Meetings-Regelwerk | G3 | Session | Session gewinnt |
| ID-Vergabe-Regelwerk | G4 | Session | Session gewinnt |
| Soll-Struktur | G (Landkarte) | Session | Session gewinnt |
| Schreib-/Qualitätsrichtlinie G7 | G7 | Session | Session gewinnt |

## Übergabe an die Terminal-Instanz

ID: KONS-TERMINAL-0001

Rollen sind klar getrennt: Diese Instanz (hier) formuliert die Inhalte und die Schritt-Anweisungen; die Terminal-Instanz auf dem Hetzner-System führt Datei-/Repo-Operationen aus (Zugriff, den diese Instanz nicht hat).

- Du legst den geprüften Staging-Ordner lokal an und kopierst ihn aufs Zielsystem.
- Anweisungen für die Terminal-Instanz werden je Schritt eindeutig formuliert (was, wohin, welche Konfliktregel).
- Verifikation bleibt bei dir als Human-in-the-Loop: nach jedem Schritt prüfen, ob das Ergebnis stimmt — diese Instanz kann das Zielsystem nicht einsehen.
- Erst nach erfolgreichem Merge folgt der Aufbau von Vektor-/SQL-DB aus dem konsolidierten Stand (Agenda-Punkt 3).