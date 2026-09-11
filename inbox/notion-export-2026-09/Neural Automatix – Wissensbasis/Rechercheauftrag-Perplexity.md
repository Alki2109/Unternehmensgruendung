# Rechercheauftrag-Perplexity

Bereich: B-Wissen
Schutzklasse: intern
Soll-Knoten: F-Wissen
Status: Stable

**Erstelldatum (fix):** 10.07.2026, 05:28 (Europe/Berlin)

**Letzte Aktualisierung:** 10.07.2026, 05:28 (Europe/Berlin)

**Status:** Draft

**Zweck:** Strukturierter Rechercheauftrag für die noch offenen Wissensthemen. Jeder Block ist so gefasst, dass die Ergebnisse anschließend einem Soll-Struktur-Knoten zugeordnet und in die DB eingepflegt werden können. Enthält am Ende einen fertigen Übergabe-Prompt.

**Fehlt (kurz):** Nach der Recherche: Ergebnisse je Block einem Soll-Knoten zuordnen, per Template/Tagging aufbereiten, dann DB-Einpflege (nach Wissens-Pipeline-Reihenfolge).

**KI-Referenz:** RECHERCHEAUFTRAG-PERPLEXITY-OFFENE-THEMEN

Update-Historie (Evolution)

| Zeitpunkt (TZ) | Änderung |
| --- | --- |
| 10.07.2026, 05:28 (Europe/Berlin) | Initiale Themenliste + Übergabe-Prompt |

Standard: siehe Schreib-/Qualitätsrichtlinie G7 (Korrektheit, Belegpflicht). Rechercheergebnisse sind Quellen-belegt zu übernehmen; Programm-/Normnamen gegen Originalquelle prüfen.

Navigation:

| Fachliche ID | Thema | Ziel-Knoten (Soll) |
| --- | --- | --- |
| RECH-DIGITALTWIN-0001 | Digital Twin (Konzept/Beispiele/Benefit) | B2 |
| RECH-BPM-0001 | Geschäftsprozessmodellierung (BPMN/UML) | D3 |
| RECH-USECASE-0001 | Use Case → Workflow → Multi-Agentic | D/E |
| RECH-BEGRIFFE-0001 | Geschäftsprozess vs. Workflow vs. Agent | G6 |
| RECH-MARKT-0001 | Nachfrageseite Marktanalyse | A5 |
| RECH-CHUNK-0001 | Chunking/Retrieval Best Practices | F2 |
| RECH-AIACT-0001 | AI-Act-Pflichten für eigenes Angebot | A6/D |

## Digital Twin

ID: RECH-DIGITALTWIN-0001

Fragen: Was ist ein Digital Twin (klare Begriffs-/Konzepterklärung)? Abgrenzung Digital Twin eines physischen Systems vs. „Digital Twin of an Organization" (DTO). Gibt es Konzept-Beispiele und praktische Umsetzungen (wer hat so etwas real gebaut)? Was ist der konkrete Benefit? Was braucht man technisch zur Umsetzung (Datenmodell, Event-Erfassung, Visualisierung)? Wie weit ist der Weg von „Event-Logging vorhanden" bis „Digital Twin"?

## Geschäftsprozessmodellierung (BPMN/UML)

ID: RECH-BPM-0001

Fragen: Wesentliche Elemente eines Geschäftsprozessmodells (Aktionen/Aktivitäten, Schnittstellen, Input-/Output-Quellen, Rollen). Wann BPMN, wann UML? Eignung von Aktivitätsdiagramm und Komponentensicht für Geschäftsprozesse. Kann man Geschäftsprozesse vollständig in UML abbilden oder ist BPMN der Standard — und warum? Sinnvolle Kombination BPMN (fachlich) + UML (technisch).

## Use Case → Workflow → Multi-Agentic

ID: RECH-USECASE-0001

Fragen: Wie bricht man einen Use Case sauber auf einen konkreten Workflow herunter? Welche Elemente hat ein Workflow (Schritte, Übergänge, Artefakte, Entscheidungen)? Wie bildet man einen Workflow auf einen Multi-Agentic Workflow ab? Best Practices für Agenten-Handoffs und Artefakt-Verträge (einer liefert, der nächste konsumiert).

## Begriffe: Geschäftsprozess vs. Workflow vs. Agent

ID: RECH-BEGRIFFE-0001

Fragen: Präzise, standard-orientierte Definitionen von Geschäftsprozess, Workflow und Agent. Wie korrelieren Geschäftsprozess und Workflow (Ebene, Granularität)? Was ist „intern im Agenten" vs. „extern zwischen Agenten"? Ziel: eindeutige Begriffe für das Begriffsmodell (Synonyme/Homonyme benennen).

## Nachfrageseite Marktanalyse

ID: RECH-MARKT-0001

Fragen: Wie groß ist die Nachfrage nach IT-/KI-Dienstleistungen für KMU in Deutschland (aktuelle Zahlen, Quellen)? Nachfrage nach KI-Spezialisten (Stellenausschreibungen, freelancermap-Indikatoren, Fachkräftemangel-Studien). Belege für die These, dass KI-Kompetenz knapper ist als allgemeine Softwareentwicklung. Ziel: die bisher unbelegte Nachfrageseite mit belastbaren Zahlen füllen (förderrelevant).

## Chunking/Retrieval Best Practices

ID: RECH-CHUNK-0001

Fragen: Aktuelle Best Practices für Chunk-Größe bei RAG (Zeichen vs. Token vs. semantische Chunks). Wann lohnt Overlap? Hybrid-Retrieval (SQL-Filter + Vektor) — bewährte Muster. pgvector-spezifische Empfehlungen. Ziel: die offene Chunk-Zielgröße empirisch fundiert festlegen.

## AI-Act-Pflichten für eigenes Angebot

ID: RECH-AIACT-0001

Fragen: Welche konkreten Pflichten treffen ab 02.08.2026 einen KI-Dienstleister, dessen Agenten mit Kunden-/Mitarbeiterdaten arbeiten? Transparenz-/Kennzeichnungspflichten (Art. 50) für KI-generierte Inhalte und Avatare. Was gilt für „Piloten" mit echten Daten? Abgrenzung Hochrisiko vs. nicht. Ziel: AI-Act nicht als Förder-, sondern als Compliance-/Geschäftsfeld-Wissen.

## Übergabe-Prompt für Perplexity

ID: RECH-PROMPT-0001

Folgenden Text an Perplexity übergeben (nach Bedarf Blöcke einzeln, für tiefere Antworten):

```
Rolle: Du bist ein Fachrechercheur. Antworte strukturiert, mit Quellenangaben (Titel, Herausgeber, Datum) und klarer Trennung von belegten Fakten und Einschätzungen. Wo Zahlen genannt werden, gib die Quelle und das Datum an. Deutschsprachig.

Recherchiere zu folgenden Themen jeweils getrennt:

1) Digital Twin: klare Definition; Abgrenzung Digital Twin (physisch) vs. Digital Twin of an Organization (DTO); reale Umsetzungsbeispiele; konkreter Nutzen; technische Voraussetzungen.

2) Geschäftsprozessmodellierung: wesentliche Elemente (Aktivitäten, Schnittstellen, Input/Output, Rollen); Vergleich BPMN vs. UML-Aktivitätsdiagramm; warum BPMN Standard für Geschäftsprozesse ist; sinnvolle Kombination BPMN + UML.

3) Vom Use Case zum Workflow zum Multi-Agent-Workflow: Vorgehen zum Herunterbrechen; Elemente eines Workflows; Best Practices für Agenten-Handoffs und Artefakt-Übergaben.

4) Begriffsklärung: präzise Standard-Definitionen von Geschäftsprozess, Workflow und (Software-)Agent; Korrelation Geschäftsprozess/Workflow; Unterschied agent-intern vs. agent-extern.

5) Nachfrage nach IT-/KI-Dienstleistungen für KMU in Deutschland: aktuelle Marktzahlen, Fachkräftemangel bei KI-Kompetenz, Belege mit Quelle und Datum.

6) RAG Best Practices: optimale Chunk-Größe (Zeichen/Token/semantisch), Overlap, Hybrid-Retrieval (SQL + Vektor), pgvector-Empfehlungen.

7) EU AI Act ab 02.08.2026: konkrete Pflichten für einen KI-Dienstleister mit Kunden-/Mitarbeiterdaten; Transparenzpflichten (Art. 50) für KI-Inhalte und Avatare; Regeln für Pilotbetrieb mit echten Daten.

Gib je Thema: (a) Kurzantwort, (b) Details mit Quellen, (c) offene/strittige Punkte.
```