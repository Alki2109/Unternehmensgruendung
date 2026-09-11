# Meetings-und-Besprechungsorganisation

Bereich: B-Wissen
Schutzklasse: intern
Soll-Knoten: G-Governance
Status: Draft

**Erstelldatum (fix):** 07.07.2026, 15:32 (Europe/Berlin)

**Letzte Aktualisierung:** 07.07.2026, 15:32 (Europe/Berlin)

**Status:** Draft

**Zweck:** Verbindliche Governance für alle Besprechungen (Mensch↔Mensch, Mensch↔KI, KI↔KI): kein Meeting ohne Agenda, kein Meeting ohne Protokoll, jede Zuständigkeit und Deadline dokumentiert und wiederauffindbar.

**Fehlt (kurz):** Verknüpfung zu DB-02 (Aufgaben) und DB-05 (Risiken/Entscheidungen) mit realen View-IDs + finales Protokoll-Template als kopierbarer Notion-Block + Abgleich der Block-IDs gegen den zentralen Block-ID-Index (Kollisionsprüfung).

**KI-Referenz:** REGELWERK-MEETINGS-BESPRECHUNGSORGANISATION

Update-Historie (Evolution)

| Zeitpunkt (TZ) | Änderung |
| --- | --- |
| 07.07.2026, 15:32 (Europe/Berlin) | Initiale Erstellung des Meetings-Regelwerks (realer Kapitel-Stil) |

Standard: siehe Dokumentations-Styleguide (Global) – Regel-Template. Dieses Regelwerk ist ein Querschnitts-Governance-Dokument und unterlegt die „Review-Termine" aus Kapitel 6 (Delivery-Lifecycle) sowie den Wochenrhythmus aus Kapitel 8 (Aufgaben & Wochensteuerung) mit verbindlichen Regeln.

Navigation:

| Fachliche ID | Titel/Label | Typ |
| --- | --- | --- |
| MEET-PRINZIP-0001 | Grundprinzipien (kein Meeting ohne …) | Kapitel |
| MEET-TYPEN-0001 | Meeting-Typen & Kadenz | Kapitel |
| MEET-AGENDA-0001 | Agenda-Pflicht (vor dem Termin) | Kapitel |
| MEET-PROTO-0001 | Protokoll-Pflicht (nach dem Termin) | Kapitel |
| MEET-ACTION-0001 | Zuständigkeiten, Deadlines & Action Items | Kapitel |
| MEET-KI-0001 | KI- und Multi-Agenten-Meetings | Kapitel |
| MEET-DOD-0001 | Definition of Done (Meeting) | Kapitel |
| MEET-TMPL-0001 | Kopierbare Templates (Agenda/Protokoll) | Template |

## Grundprinzipien

ID: MEET-PRINZIP-0001

Ein „Meeting" ist jede terminierte Besprechung mit Entscheidungs- oder Abstimmungscharakter — unabhängig von der Dauer und davon, ob Menschen, KI-Agenten oder beide beteiligt sind. Auch ein Sprint-Review, ein Kunden-Discovery-Termin oder ein interner Agenten-Handoff mit Entscheidungsbedarf fällt darunter.

Verbindliche Grundregeln:

- **Kein Meeting ohne Agenda.** Liegt bis zum Start keine Agenda vor, wird der Termin verschoben oder abgesagt (Ausnahme: deklarierter Ad-hoc-Incident, siehe MEET-TYPEN-0001).
- **Kein Meeting ohne Protokoll.** Jedes Meeting erzeugt ein Protokoll-Wissensobjekt mit stabiler ID.
- **Kein Meeting ohne Owner.** Jedes Meeting hat genau eine verantwortliche Person/Rolle (Einberufer = Owner), die für Agenda, Moderation und Protokoll-Fertigstellung haftet.
- **Jede Entscheidung und jedes Action Item ist zugeordnet und terminiert.** Keine offene Zuständigkeit ohne benannten Verantwortlichen und Deadline.
- **Ein Ergebnis, eine Quelle.** Beschlüsse landen als Wissensobjekte in der Dokumentation und in den operativen Datenbanken (DB-02/DB-05), nicht nur im Fließtext.

## Meeting-Typen & Kadenz

ID: MEET-TYPEN-0001

Die Typen sind an Kapitel 6 (Delivery-Lifecycle) und Kapitel 8 (Wochensteuerung) angelehnt. Da das Unternehmen aktuell solo geführt ist (Geschäftsführer + Human-in-the-Loop), sind viele „Meetings" strukturierte Selbst- oder Mensch↔KI-Termine — das Protokoll bleibt trotzdem Pflicht, weil es die Wissensbasis speist.

- **Wochen-Review & -Planung** (wöchentlich, Fr): Abgleich gegen Prüfraster, Planung der Folgewoche. Anknüpfung an Kapitel 8.
- **Daily-Check** (arbeitstäglich, kurz): Statt Status-Runde ein Deviation-Check — was steht, wo staut sich Arbeit, wo ist ein KI-Agent blockiert. Protokoll minimal (Abweichungen + nächster Schritt).
- **Kunden-Discovery / Sprint-Review** (projektabhängig): terminiert im Delivery-Lifecycle (Kapitel 6). Volles Protokoll inkl. Abnahme-/Scope-Bezug.
- **Entscheidungs-Meeting** (bei Bedarf): wenn ein Beschluss mit Tragweite ansteht (z. B. Förderpfad, Anmeldung, irreversible Schritte). Beschluss wird in DB-05 gespiegelt.
- **Ad-hoc-Incident** (ungeplant): einzige Ausnahme von der Agenda-Vorabpflicht. Nachbedingung: Innerhalb von 24 h wird ein Protokoll nacherstellt.

## Agenda-Pflicht (vor dem Termin)

ID: MEET-AGENDA-0001

Die Agenda liegt **vor** dem Termin vor und ist ein eigenes Wissensobjekt (oder Kopf des Protokoll-Objekts). Mindestinhalt:

- Titel, Datum/Zeit (Europe/Berlin), Owner, Teilnehmer (inkl. beteiligter KI-Agenten/Modelle).
- Ziel des Meetings in 1–2 Sätzen (was soll am Ende entschieden/geliefert sein).
- Tagesordnungspunkte mit je einem erwarteten Ergebnistyp (Entscheidung / Info / Abstimmung).
- Benötigte Vorbereitung / verlinkte Wissensobjekte (Block-IDs).
- Zeitbudget je Punkt (optional, empfohlen bei > 3 Punkten).

Regel: Punkte ohne definierten Ergebnistyp werden gestrichen oder in einen Info-Anhang verschoben — das hält die Agenda entscheidungsorientiert.

## Protokoll-Pflicht (nach dem Termin)

ID: MEET-PROTO-0001

Jedes Meeting erzeugt genau ein Protokoll-Wissensobjekt mit Meta-Block (Erstelldatum, Letzte Aktualisierung, Status) und `KI-Referenz`-ID nach Muster `MEET-PROTO-YYYYMMDD-<kurz>`. Pflicht-Metadaten je Protokoll (gemäß DOCSTYLE-KNOW-0001): Objekt-ID, Titel, Objekttyp = Protokoll, Überblick (1–3 Sätze), Parent (dieses Regelwerk bzw. das Projekt), Children (erzeugte Action Items), Tags.

Pflicht-Inhalt:

- Anwesende (Menschen + KI-Agenten/Modelle mit Rolle).
- Behandelte Agenda-Punkte und Ergebnis je Punkt.
- **Beschlüsse** (klar als solche markiert, mit Begründung, wenn nicht trivial).
- **Action Items** (siehe MEET-ACTION-0001).
- Offene Punkte / Vertagtes (mit Grund).
- Verweise auf erzeugte oder geänderte Wissensobjekte (Block-IDs).

Regel: Das Protokoll ist spätestens am selben Tag DoD-konform (Meta-Block + Beschlüsse + Action Items). Ein reiner Chat-/Transkript-Mitschnitt ist **kein** Protokoll — er kann als Quelle angehängt werden, ersetzt aber nicht die strukturierte Verdichtung.

## Zuständigkeiten, Deadlines & Action Items

ID: MEET-ACTION-0001

Jedes Action Item ist ein eigenständig referenzierbares Objekt mit mindestens:

- Kurztitel (imperativ: „X erstellen", „Y prüfen").
- **Verantwortliche(r)** (genau eine Rolle/Person; bei KI-Ausführung zusätzlich der menschliche Owner, der abnimmt).
- **Deadline** (Datum, Europe/Berlin).
- Status (offen / in Arbeit / erledigt / vertagt).
- Verknüpfung: gehört zu Protokoll-ID X, betrifft Wissensobjekt/DB-Eintrag Y.

Regeln:

- Action Items werden in die operative Aufgaben-DB (DB-02) übernommen — das Protokoll ist die Quelle, DB-02 bleibt Single Source of Truth für den Aufgabenstatus (Konsistenz mit Kapitel 8).
- Beschlüsse mit strategischer Tragweite werden zusätzlich in DB-05 (Risiken/Entscheidungen) gespiegelt.
- Kein Action Item ohne Verantwortliche(n) UND Deadline. Fehlt eines von beiden, gilt es als nicht vergeben und bleibt Verantwortung des Meeting-Owners.

## KI- und Multi-Agenten-Meetings

ID: MEET-KI-0001

Wenn KI-Agenten an einem Meeting beteiligt sind oder ein Handoff zwischen Agenten Entscheidungscharakter hat, gelten dieselben Regeln — mit Präzisierungen:

- **Rolle statt Modell im Protokoll.** Vermerkt wird die Rolle (z. B. Analyse-Agent), nicht primär das Modell. Das konkrete Modell ist ein austauschbarer Parameter und wird optional als Zusatzinfo geführt (konsistent zum „Rolle-nicht-Modell"-Prinzip der Systemarchitektur).
- **Human-in-the-Loop-Gate.** Beschlüsse mit Außenwirkung (Kundenkommunikation, Anmeldung, Ausgaben, irreversible Schritte) sind erst gültig nach menschlicher Freigabe durch den Owner.
- **Confidence-/Abweichungsvermerk.** Meldet ein Agent niedrige Sicherheit oder eine Abweichung, wird das im Protokoll als offener Punkt geführt und eskaliert — nicht stillschweigend übernommen.
- **Nachvollziehbarkeit.** Für KI-erzeugte Ergebnisse werden Quelle/Prompt-Kontext so weit referenziert, dass die Entscheidung später prüfbar ist.

## Definition of Done (Meeting)

ID: MEET-DOD-0001

Ein Meeting gilt als „fertig", wenn:

- Agenda existierte vor dem Termin (oder Ad-hoc-Ausnahme dokumentiert).
- Protokoll-Wissensobjekt mit Meta-Block, Beschlüssen und Action Items existiert.
- Jedes Action Item hat Verantwortliche(n) + Deadline und ist in DB-02 übernommen.
- Strategische Beschlüsse sind in DB-05 gespiegelt.
- Parent/Child-Beziehungen und Tags gesetzt; Protokoll im Index auffindbar.
- Bei KI-Beteiligung: Human-in-the-Loop-Freigaben für außenwirksame Beschlüsse dokumentiert.

## Kopierbare Templates

ID: MEET-TMPL-0001

Agenda (Startpunkt):

```
Titel: …
Datum/Zeit: DD.MM.YYYY, HH:MM (Europe/Berlin)
Owner: …
Teilnehmer (inkl. KI-Agenten/Rollen): …
Ziel (1–2 Sätze): …
TOP 1 – … | Ergebnistyp: Entscheidung/Info/Abstimmung | Vorbereitung: [Block-ID]
TOP 2 – … | Ergebnistyp: … | Vorbereitung: …
```

Protokoll (Startpunkt):

```
KI-Referenz: MEET-PROTO-YYYYMMDD-<kurz>
Erstelldatum (fix): DD.MM.YYYY, HH:MM (Europe/Berlin)
Letzte Aktualisierung: DD.MM.YYYY, HH:MM (Europe/Berlin)
Status: Draft
Objekttyp: Protokoll
Überblick (1–3 Sätze): …
Parent: [Projekt/Regelwerk-ID]   Tags: meet, protokoll, <domäne>

Anwesende (Mensch + KI-Rollen): …
Ergebnisse je TOP:
  - TOP 1 → …
Beschlüsse:
  - B1: … (Begründung: …)  → ggf. DB-05
Action Items:
  - A1: <Titel> | Verantwortlich: … | Deadline: DD.MM.YYYY | Status: offen → DB-02
Offene Punkte / Vertagt:
  - …
Referenzen (Block-IDs): …
```