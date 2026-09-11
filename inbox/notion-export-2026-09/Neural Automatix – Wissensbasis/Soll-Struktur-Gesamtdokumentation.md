# Soll-Struktur-Gesamtdokumentation

Bereich: A-Werkzeug/Bauplan
Schutzklasse: intern
Soll-Knoten: G-Governance
Status: Draft

# Soll-Struktur – Neuordnung der Gesamtdokumentation (Zielgliederung)

**Erstelldatum (fix):** 10.07.2026, 05:28 (Europe/Berlin)

**Letzte Aktualisierung:** 10.07.2026, 05:28 (Europe/Berlin)

**Status:** Draft

**Zweck:** Verbindliche Zielgliederung ("Soll-Struktur"), gegen die der bestehende, unübersichtliche Dokumentenstand neu geordnet, zerlegt und einsortiert wird. Grundlage für das Refactoring der Dokumentation und für die spätere Überführung aller Begriffe ins Begriffsmodell.

**Fehlt (kurz):** Zuordnung jedes bestehenden Dokuments zu genau einem Zielknoten (Migrationsmatrix) + Entscheidung, welche Inhalte in der bestehenden SD-Wissensbasis bleiben und nur referenziert werden + Dubletten-Liste aus dem Ist-Stand.

**KI-Referenz:** SOLL-STRUKTUR-GESAMTDOKUMENTATION

Update-Historie (Evolution)

| Zeitpunkt (TZ) | Änderung |
| --- | --- |
| 10.07.2026, 05:28 (Europe/Berlin) | Initiale Zielgliederung aus den fünf Input-Blöcken; Konzept/Domäne/Implementierung als durchgängige Achse |

Standard: siehe Dokumentations-Styleguide (Global). Diese Soll-Struktur ist eine Landkarte, kein Inhaltsdokument — die eigentlichen Inhalte bleiben in ihren Fachdokumenten und werden hier nur verortet (verlinken statt duplizieren).

## Leitprinzip: die durchgängige Achse

ID: SOLL-ACHSE-0001

Das zentrale Ordnungsprinzip der gesamten Dokumentation sind drei Ebenen, die jeden inhaltlichen Bereich gleich durchziehen:

- **Konzept** – die allgemeine, domänenunabhängige Vorgehensweise (das Warum und der Rahmen). Abgeleitet aus Struktur/Organisation, bestem Wissen (Fachliteratur, Ausbildung), praktischer Erfahrung → Best Practices → prüffähiges Regelwerk.
- **Domäne** – dieselbe Vorgehensweise angewandt auf eine Fachabteilung/Fachaufgabe (z. B. KI-gestützte Softwareentwicklung); hier entstehen die abteilungsspezifischen Kernprozesse.
- **Implementierung** – die Umsetzung am konkreten Anwendungsfall mit echten Daten (Multi-Agentic Workflow, Scrum, Human-in-the-Loop).

Regel für das Aufräumen: Jeder Bereich unten wird nach Möglichkeit in genau diese drei Ebenen gegliedert. Wo im Ist-Stand die Trennung fehlt, ist sie herzustellen. Ein Chunk/Abschnitt gehört zu genau einer Ebene.

## A – Gründung

ID: SOLL-A-GRUENDUNG-0001

Die betriebswirtschaftlich-formale Ebene der Firmengründung. Adressat u. a. IHK, Jobcenter, Förderstellen.

- A1 Gründungsphasen (vor / während / nach) und zugehörige Aufgaben
- A2 Geschäftsmodell & Unternehmensziele (Kurzfassung; Detail in B)
- A3 Businessplan (gutachterreif, förderfähig)
- A4 Finanzplan (drei Szenarien, Kapitalbedarf, Liquidität, Break-Even)
- A5 Marktanalyse (Angebotsseite belegt; Nachfrageseite noch zu belegen)
- A6 Förderung & Finanzierung (Einstiegsgeld §16b, Sachgüter §16c, BAFA, ZIM, KfW; De-minimis; AI-Act-Abgrenzung)
- A7 Nachweise & Einreichung

Bestehende Anknüpfung: Kapitel 1–9 der Gründungsdoku, Kapitel 3a (Finanzszenarien), Kapitel 4a (IHK/Einstiegsgeld).

## B – Unternehmen: Ziele & Konzepte

ID: SOLL-B-KONZEPT-0001

Die strategisch-konzeptionelle Ebene: was das Unternehmen ist und anstrebt.

- B1 Vision & Leitidee: KI-Unterstützung aller Kernprozesse
- B2 Digital-Twin-Konzept (vollständige digitale Abbildung der Firma und ihrer Prozesse)
- B3 Proof-of-Concept-Strategie (eigene Firma als Prototyp und Referenz; Live-Demo)
- B4 Dienstleistungsportfolio (Prozessanalyse, KI-Erweiterung bestehender Prozesslandschaften, Software-Entwicklung)
- B5 Drei-Ebenen-Modell der Problemlösung (Konzept/Domäne/Implementierung als Unternehmensmethodik)

## C – Unternehmensstruktur

ID: SOLL-C-STRUKTUR-0001

Die organisatorische Ebene: das digitale Organigramm.

- C1 Organigramm & Fachabteilungen (Marketing, HR, IT, …)
- C2 Rollen: Leitung vs. Ausführung (virtuelles Personal)
- C3 Avatare (Repräsentation, Stimme, KI-Kennzeichnungspflicht ab 08/2026)
- C4 Stellenbeschreibungen → Ableitung der Agenten-Rollen
- C5 Wissenszuordnung je Rolle (allgemein / spezifisch / spezialisiert / kernaufgabenbezogen)

## D – Prozesse & Workflows

ID: SOLL-D-PROZESSE-0001

Die Prozessebene, klar getrennt nach Wertschöpfungsbezug.

- D1 Kernprozesse (extern, wertschöpfend, als Dienstleistung erbringbar)
- D2 Unterstützende Prozesse (intern, auf Anweisung der Geschäftsführung; z. B. Marketing, Personal)
- D3 Prozesslebenszyklus je Prozess: Identifikation → Beschreibung → Modellierung → Digitalisierung
- D4 Schnittstellen & Artefakte (wer liefert, wer konsumiert)
- D5 Events & ausgetauschte Daten

Hinweis: Prozesse, die intern *und* extern vorkommen, werden einmal beschrieben und doppelt referenziert (nicht dupliziert).

## E – Mapping auf Multi-Agentic-Umsetzung

ID: SOLL-E-AGENTIC-0001

Die Umsetzungsebene: wie Geschäftsprozesse auf Agenten abgebildet werden.

- E1 Agentic Workflow als Kommunikationsrahmen (Bus, Data Sources, Artefakte) → NATS/JetStream
- E2 Agenten-Grundbegriffe (Agent intern; Agent im Multi-Agenten-Framework)
- E3 Rollenmodell (Scrum: Product Owner, Developer, Scrum Master; + Unternehmensrollen)
- E4 Modellauswahl & -mapping (Aufgabe → best geeignetes Modell; lokal vs. Cloud; Kostenlogik)
- E5 Software-Lifecycle-Umsetzung (TDD, CI/CD, Schichten Visualisierung/Prozess/Daten; Spezial-Schnittstellen SAP/ERP)
- E6 Iteration & Mehrmodell-Prüfung (eins setzt um, eins prüft, eins berichtet; Soll-/Ist-Zeiten)

Bestehende Anknüpfung: SD-Wissensbasis (KB-…), Agent-Interface-Design (Agenda-Punkt 4).

## F – Wissensmanagement

ID: SOLL-F-WISSEN-0001

Die Wissensebene: Grundlage für schnelle, präzise KI-Zuarbeit.

- F1 Struktur & Hierarchie (Überschriften, Textblöcke, IDs) → Dokumentations-Styleguide
- F2 Chunking-Strategie (Kapitel → ID → Klassifikation unterhalb der Überschrift; Zielgröße empirisch)
- F3 Speicherung: SQL (Metastruktur) + Vektor-DB (semantisch) → Hybrid-Retrieval
- F4 Wissensgraph als Langzeitgedächtnis
- F5 Wissensaufnahme-Prozess (Prüfung auf Korrektheit/Vollständigkeit → Template → IDs → Einspeisung)
- F6 Prompting-Dreischicht (allgemein × Domäne × Modell) → bestehendes Regelwerk KB-PROMPT-0030
- F7 Zerlegungs- & Mess-Beispiel (Zugriffszeiten mit/ohne ID, mit/ohne Vektor-DB)

## G – Querschnitt & Governance

ID: SOLL-G-GOVERNANCE-0001

Die querschnittliche Ebene: Regeln, die überall gelten.

- G1 Dokumentations-Styleguide (global)
- G2 Regelwerk-Konzept (prüffähig, reproduzierbar, messbar)
- G3 Meetings & Besprechungsorganisation (bestehendes Regelwerk)
- G4 ID-Vergabe & Dokumenten-Abbildung (bestehendes Regelwerk)
- G5 Event-Logging / Event-Sourcing (Grundlage Digital Twin & Retrospektive)
- G6 Begriffsmodell & semantische Klassifikation (Abschluss-Schritt; NATS/JetStream als Erst-Einträge)
- G7 Schreib- & Qualitätsrichtlinie (folgt als eigenes Dokument nach dieser Soll-Struktur)

## Nächster Schritt: Migrationsmatrix

ID: SOLL-MIGRATION-0001

Nach Freigabe dieser Soll-Struktur folgt die Migrationsmatrix: eine Tabelle, die jedes bestehende Dokument/jeden Abschnitt genau einem Zielknoten (A–G) zuordnet, Dubletten markiert und offene Lücken (fehlendes Wissen) ausweist. Erst danach wird tatsächlich umsortiert.