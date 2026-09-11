# Kapitel-6b-Standards-und-Governance

Bereich: B-Wissen
Schutzklasse: intern
Soll-Knoten: G-Governance
Status: Draft

**Erstelldatum (fix):** 07.07.2026, 15:32 (Europe/Berlin)

**Letzte Aktualisierung:** 07.07.2026, 15:32 (Europe/Berlin)

**Status:** Draft

**Zweck:** Einordnung der verbindlichen Regelwerke, die **vor** der Gründung definiert werden, weil sie Querschnittsanliegen (Cross-Cutting Concerns) bedienen und die Voraussetzung dafür sind, dass KI-Einsatz reproduzierbar gute Ergebnisse liefert. Dieses Kapitel fasst die Regelwerke kurz zusammen und verweist auf die maßgeblichen Dokumente — es dupliziert deren Inhalte nicht.

**Fehlt (kurz):** Notion-Links (statt nur IDs) einsetzen, sobald alle Regelwerke im selben Workspace verlinkt sind + Abgleich der Block-IDs gegen den zentralen Block-ID-Index (Kollisionsprüfung) + Prüfen, ob Repo-Stände neuer sind als die zitierten Notion-Fassungen.

**KI-Referenz:** KAPITEL-6B-STANDARDS-GOVERNANCE

Update-Historie (Evolution)

| Zeitpunkt (TZ) | Änderung |
| --- | --- |
| 07.07.2026, 15:32 (Europe/Berlin) | Initiale Erstellung: Standards/Governance als Konzeptions-Baustein eingeordnet |

Standard: siehe Dokumentations-Styleguide (Global) – Regel-Template. Dieses Kapitel schließt an Kapitel 6 (Delivery-Lifecycle) und Kapitel 6a (Delivery-Methodik/SD-KB) an und liegt bewusst vor der operativen Steuerung (Kapitel 8).

Navigation:

| Fachliche ID | Titel/Label | Typ |
| --- | --- | --- |
| KAP6B-WARUM-0001 | Warum Standards vor der Gründung | Kapitel |
| KAP6B-DOKU-0001 | Dokumentations-Styleguide (global) | Kapitel |
| KAP6B-MEET-0001 | Meetings & Besprechungsorganisation | Kapitel |
| KAP6B-PROMPT-0001 | Prompting-Framework (Drei Schichten) | Kapitel |
| KAP6B-SDKB-0001 | AI-Driven-Software-Development-KB | Kapitel |
| KAP6B-STATUS-0001 | Status & offene Punkte | Kapitel |

## Warum Standards vor der Gründung

ID: KAP6B-WARUM-0001

Die hier genannten Regelwerke sind keine nachgelagerte Fleißarbeit, sondern eine bewusste Vorleistung der Konzeptionsphase. Der Grund: Sie bedienen Cross-Cutting Concerns — Anliegen, die quer durch alle Bereiche laufen (Dokumentation, Besprechungen, Prompting, Delivery) und nicht einem einzelnen Prozess zugeordnet werden können.

Einheitliche Standards sind zugleich die Voraussetzung dafür, dass KI überhaupt qualitätsgesichert eingesetzt werden kann: Nur wenn Dokumente gleich strukturiert sind (stabile IDs, Chunking-fähig), Entscheidungen protokolliert und auffindbar sind und Prompts nach festen Mustern entstehen, liefern KI-Agenten reproduzierbar brauchbare Ergebnisse statt schwankender Einzelfälle. Diese Standards werden daher definiert, bevor der operative Betrieb (und die Gründung) startet.

Die Regelwerke leben in ihren jeweiligen Systemen und werden hier nur eingeordnet und verlinkt (Single Source of Truth: verlinken statt duplizieren).

## Dokumentations-Styleguide (global)

ID: KAP6B-DOKU-0001

Der globale Dokumentations-Styleguide ist der verbindliche SSOT für den Aufbau aller wissenstragenden Dokumente: Pflicht-Meta-Block (Erstelldatum, Letzte Aktualisierung, Update-Historie, Europe/Berlin), Abstract ohne Heading, ToC- und Navigations-Tabelle, stabiles Block-ID-Schema, Wissensobjekt-Metadaten (Objekt-ID, Titel, Typ, Überblick, Parent/Child, Tags) und ein Tagging-Modell für die spätere Vektor-DB.

Wirkung als Cross-Cutting Concern: Er stellt sicher, dass jedes Dokument im ganzen Unternehmen gleich strukturiert und maschinell auffindbar ist — die Grundlage für RAG/semantische Suche.

Referenz: Dokumentations-Styleguide (Global) – Regel-Template (`DOCSTYLE-…`).

## Meetings & Besprechungsorganisation

ID: KAP6B-MEET-0001

Verbindliche Governance für alle Besprechungen (Mensch↔Mensch, Mensch↔KI, KI↔KI): kein Meeting ohne Agenda, kein Meeting ohne Protokoll, jede Zuständigkeit und Deadline dokumentiert. Beschlüsse fließen in die operativen Datenbanken (Aufgaben, Risiken/Entscheidungen); bei KI-Beteiligung gilt ein Human-in-the-Loop-Gate für außenwirksame Beschlüsse.

Wirkung als Cross-Cutting Concern: Er sorgt dafür, dass Entscheidungen nachvollziehbar, zugeordnet und terminiert sind — quer über alle Projekte und Abteilungen. Anknüpfung an Kapitel 6 (Review-Termine) und Kapitel 8 (Wochenrhythmus).

Referenz: Regelwerk – Meetings & Besprechungsorganisation (`MEET-…`).

## Prompting-Framework (Drei Schichten)

ID: KAP6B-PROMPT-0001

Verbindliches Drei-Schichten-Modell fürs Prompting: **Allgemein** (universelle Best Practices) × **Domäne** (Software, Text, Bild/Video) × **Modell** (herstellerspezifisch, austauschbar). Die Schichten werden in fester Reihenfolge kombiniert; die volatilste Modellschicht ist entkoppelt und austauschbar, ohne die anderen anzufassen. Das Regelwerk liegt in der AI-Driven-Software-Development-Wissensbasis und ordnet die bestehende Prompt Library als Software-Domäne ein.

Wirkung als Cross-Cutting Concern: Es standardisiert, wie KI angesprochen wird — über alle Domänen hinweg — und reduziert Prompt Drift und Halluzinationsrisiko.

Referenz: 23 Prompting Framework (Drei-Schichten-Regelwerk) (`KB-PROMPT-0030`).

## AI-Driven-Software-Development-KB

ID: KAP6B-SDKB-0001

Eigenständige Wissensbasis mit dem vollständigen SDLC (Vision bis Maintenance), KI-Agenten-Rollen, Prompt Library, ADRs und einem Konzept für die Hybrid-Speicherung (relational + Vektor-DB). Sie ist die methodische Tiefenschicht unter Kapitel 6 und über das Brücken-Kapitel 6a mit realen Block-IDs angebunden.

Wirkung als Cross-Cutting Concern: Sie liefert die reproduzierbare Methodik, nach der Software-/KI-Dienstleistungen erbracht werden — für interne wie für Kundenprojekte.

Referenz: Kapitel 6a – Delivery-Methodik & KI-Softwareentwicklung sowie die SD-KB (`KB-…`, Einstieg `KB-DASH-0001`, Index `KB-REF-0026`).

## Status & offene Punkte

ID: KAP6B-STATUS-0001

- Alle in diesem Kapitel genannten Block-IDs sind Vorschläge und gegen den zentralen Block-ID-Index zu prüfen (Kollisionsfreiheit).
- Verweise nutzen derzeit IDs; sobald die Regelwerke im selben Notion-Workspace liegen, sind echte Links zu ergänzen.
- Repo vs. Notion: Bei Abweichung ist die Repo-Fassung autoritativ (siehe Kapitel 6a, Sync-Regel).
- Noch nicht als eigenes Regelwerk erfasst, aber geplant: Dokumenten-Abbildung/ID-Vergabe als eigener Abschnitt (aktuell im Styleguide mitgeführt).