# Konzept: Multi-Agent-Architektur & Avatar-Organigramm (Digital Twin)

Bereich: B-Wissen
Schutzklasse: intern
Soll-Knoten: E-Agentic
Status: Draft
Anmerkung: Konzept/To-Do – noch nicht verifiziert, einziger Mitarbeiter aktuell Alexander selbst. Erweiterung des bestehenden Wissensstands um konkrete Multi-Agent-Szenarien.

> **Hinweis:** Dies ist ein Konzept-Entwurf (Draft), noch nicht final verifiziert. Entstanden aus der laufenden Architektur-Diskussion zur Pipeline Notion → GitHub → SQL/pgvector → Obsidian und zur Digital-Twin-Erweiterung.
> 

# Ziel

Ein voll umfängliches digitales Abbild der Firma (Digital Twin), das die gesamte Organisation – Abteilungen, Mitarbeiter, Arbeitsabläufe, Schnittstellen – als KI-Agenten/Avatare abbildet, obwohl aktuell nur eine reale Person (Alexander) die Firma trägt.

# Bausteine

## 1. Market-Intelligence-Agent

Eigene Agenten-Rolle (neben Architect/Developer/QA), die laufend strukturierte Branchendaten (Destatis, ifo, Statista, News-Feeds) einliest und daraus Kandidaten-Profile für Zielkunden ableitet. Kein einmaliger Recherche-Task, sondern ein Agent mit eigenem Gedächtnis in der Wissensbasis.

## 2. Use-Case-Matching per Embedding

Bestehende Konzept-Artefakte (Prozessdigitalisierung, -automatisierung, -optimierung) werden gegen Branchenprofile embedded und über pgvector gematcht. Damit entsteht dynamische Bedarfsermittlung ohne manuell vorgegebene Regeln.

## 3. Avatare / Abteilungen

Jede Domäne (Marketing, Vertrieb, Umsetzung, ...) erhält einen Agenten mit klar abgegrenztem Kontextfenster. Kommunikation über NATS/JetStream (Pub/Sub). Ein Bedarfsfall wird als Nachricht durch die Kette gereicht (Market-Intelligence → Vertrieb-Avatar → Architect), nicht zentral vorgegeben.

# Offene Punkte / To-Do (aktuell gänzlich unbearbeitet)

- **Organigramm fehlt vollständig**: Abteilungsleiter-Ebene, Mitarbeiter-Ebene, Rollendefinitionen pro Avatar.
- **Wiederkehrende Arbeitsabläufe** je Avatar/Rolle noch nicht spezifiziert.
- **Schnittstellen zwischen Avataren** (Datenformat, Trigger, Eskalationspfade) noch nicht definiert.
- **Avatar-Charakterisierung**: visuelle Darstellung + Rollenkonsistenz ("im Charakter bleiben"), inkl. Repräsentation von Geschlechtervielfalt im Organigramm – offene Frage, siehe gesonderte Diskussion.
- **Priorität**: Diese Ausbaustufe soll möglichst schnell erreicht werden, bevor der Wissensbestand deutlich weiterwächst.

# Bezug zur Gesamt-Roadmap

Sobald ein erster lauffähiger Twin-Prototyp steht, dient er als Testkonzept, um zu prüfen, ob fremde Kompetenzbereiche (z. B. Marketing) über das gleiche Konzept abgebildet werden können – Grundlage für die Auswahl konkreter Use Cases unterschiedlicher Komplexitätsstufen für Proof-of-Concept und Business-Plan-Vorstellung.