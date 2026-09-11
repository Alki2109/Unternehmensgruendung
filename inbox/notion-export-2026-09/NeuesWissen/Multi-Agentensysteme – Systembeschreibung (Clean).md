# Multi-Agentensysteme – Systembeschreibung (Clean)

<aside>
ℹ️

**Abstract/Überblick:** Konsolidierte, prüfbare Systembeschreibung von **Multi‑Agentensystemen** (Agentenbegriff, Charakteristika, interner Agent‑Workflow, Orchestrierung/Team‑Zusammenspiel, Kommunikation/Interfaces, Actions/Events) inkl. minimalem Referenz‑Setup und typischen Use‑Cases. Fokus: als Baustein für ein eigenes Workflow-/Orchestrierungs‑Framework („Pipes“/Pipeline‑Denke).

</aside>

<aside>
🧷

**Standard:** siehe [Dokumentations-Styleguide (Global) – Regel-Template](https://app.notion.com/p/Dokumentations-Styleguide-Global-Regel-Template-ebb91c6deb1747998a35aa3e0da9d7d2?pvs=21)

**Quelle (Working Notes):** Notizfoto im Thread ("Multi-agentic workflow")

</aside>

<aside>
🕒

**Erstelldatum (fix):** 13.07.2026, 07:25 (Europe/Berlin)

**Letzte Aktualisierung:** 13.07.2026, 07:25 (Europe/Berlin)

</aside>

- Update-Historie (Evolution)
    
    
    | Zeitpunkt (TZ) | Änderung |
    | --- | --- |
    | 13.07.2026, 07:25 (Europe/Berlin) | Initiale Konsolidierung (Definition, Agent-Workflow, Orchestrierung, Kommunikation, Minimal-Setup, Referenzen) |

Navigation (maschinenlesbar):

| Fachliche ID | Titel/Label | Ziel | Typ |
| --- | --- | --- | --- |
| MAS-01 | Begriffsmodell (SSOT) | (dieses Dokument) | Kapitel |
| MAS-02 | Agent (Charakteristik & Definition) | (dieses Dokument) | Kapitel |
| MAS-03 | Workflow innerhalb eines Agenten | (dieses Dokument) | Kapitel |
| MAS-04 | Zusammenspiel / Orchestrierung | (dieses Dokument) | Kapitel |
| MAS-05 | Kommunikation, Schnittstellen, Actions, Events | (dieses Dokument) | Kapitel |
| MAS-06 | Minimal-Setup (Rollen) + Beispiel-Workflow | (dieses Dokument) | Kapitel |
| MAS-07 | Framework-Entscheidung: „Pipes“ (Module, Prozesse, Abläufe) | (dieses Dokument) | Kapitel |
| MAS-08 | Use-Cases / Komponenten-Sicht | (dieses Dokument) | Kapitel |
| MAS-09 | Beispiele, Tutorials, Diagramme (Linkliste) | (dieses Dokument) | Kapitel |

---

## 1) Begriffsmodell (SSOT)

ID: MAS-01

### 1.1 Kurzdefinition

Ein **Multi‑Agentensystem (MAS)** ist ein System aus **mehreren (teil‑)autonomen Agenten**, die über definierte **Kommunikationswege** kooperieren, um Ziele zu erreichen, die ein einzelner Agent nur ineffizient oder unzuverlässig lösen würde.

### 1.2 Warum „multi“ (Motivation)

- **Spezialisierung:** unterschiedliche Stärken/Tools/Prompts pro Agent.
- **Komplexität beherrschbar machen:** Zerlegung in überprüfbare Teilresultate.
- **Robustheit:** Cross‑Check, Redundanz, Guardrails.
- **Parallelisierung:** unabhängige Teilaufgaben parallel.
- **Nachvollziehbarkeit:** Rollen/Outputs klarer als „ein Agent macht alles“.

---

## 2) Agent (Charakteristik & Definition)

ID: MAS-02

Ein Agent ist (im hier relevanten Sinn) eine Einheit, die:

- **Ziele/Intents** verfolgt,
- **Zustand/Memory** halten kann (kurz/ lang, strukturiert),
- **Wahrnehmung** hat (Input: User, Datenquellen, Events),
- **Planung/Entscheidung** trifft (Policy/Prompt/Regeln),
- **Actions/Tools** ausführen kann,
- und **Outputs** produziert (Artefakte, Updates, Calls, Entscheidungen).

Abgrenzung:

- „Agent“ ≠ nur Chatbot; entscheidend sind **Zustand + Handlungsfähigkeit**.

---

## 3) Workflow innerhalb eines Agenten (grundlegend)

ID: MAS-03

### 3.1 Generischer Agent‑Loop

1. **Perceive** (Input aufnehmen): Anfrage, Kontext, Events, Daten.
2. **Interpret** (Problem-/Zielklärung): Constraints, Definition of Done.
3. **Plan** (Plan/Teilziele): Tasks, Tool‑Calls, Hand‑offs.
4. **Act** (Ausführen): Tools/Actions, Daten schreiben/lesen.
5. **Observe** (Resultat bewerten): Erfolg/Fehler, Evidenz sammeln.
6. **Reflect / Update State**: Memory/Artefakte aktualisieren.
7. **Decide next**: weitermachen, eskalieren, an anderen Agent übergeben.

### 3.2 Charakteristische Qualitätsmerkmale

- **Deterministische Teiloutputs** (wo möglich), z. B. Struktur/Schema.
- **Evidenzbasierung:** Quellen/Logs/IDs statt „nur Text“.
- **Begrenzte Autorität:** Guardrails, Policy, Review‑Pflicht.

---

## 4) Zusammenspiel / Orchestrierung (Team‑Workflow)

ID: MAS-04

### 4.1 Orchestrierungs-Patterns (SSOT-Begriffe)

- **Supervisor/Manager:** ein koordinierender Agent verteilt Arbeit, sammelt Ergebnisse.
- **Hierarchisch:** Manager → Spezialisten → Sub‑Spezialisten.
- **Peer‑to‑Peer / Netzwerk:** Agenten handeln Übergaben untereinander aus.
- **Router/Dispatcher:** Routing nach Intent/Kategorie/State.
- **Blackboard:** gemeinsamer Arbeits‑/Status‑Speicher (Artefakt‑Zentralpunkt).

### 4.2 Warum mehrere Agenten nutzen (aus der Notiz)

- „Zusammenspiel“ als Kern: klare Verantwortlichkeiten, weniger Kontextüberladung, bessere Testbarkeit.

---

## 5) Kommunikation, Schnittstellen, Actions, Events

ID: MAS-05

### 5.1 Kommunikation (Grundformen)

- **Message Passing:** Agent A → Agent B (mit Kontextpaket).
- **Shared State/Blackboard:** Agenten schreiben/lesen gemeinsamen Zustand.
- **Handoff:** explizite Übergabe inkl. Erwartung/DoD.

### 5.2 Schnittstellen (Interfaces)

- **Tool-/Action‑Interface:** standardisierte Calls (z. B. „search“, „create/update artifact“, „run code“).
- **Daten‑Interface:** Dokumente/DBs als SSOT (Notion, SQL, Vektorindex).
- **Event‑Interface:** Ereignisse triggern Flows (z. B. neue Aufgabe, Statuswechsel, Zeit, Webhook).

### 5.3 Actions (was wird ausgeführt?)

Typische Actions:

- Daten holen (Search/RAG), Daten validieren
- Artefakte erzeugen (Docs, Tickets, Code, Tests)
- Updates durchführen (Properties, Status, Verlinkungen)
- Entscheidungen treffen (Route/Stop/Retry/Eskalation)

### 5.4 Events (was ist ein Event?)

Ein **Event** ist ein strukturierter Auslöser (Zeitpunkt/Änderung/Signal), der einen Flow startet oder fortsetzt (z. B. „Task created“, „Build failed“, „User replied“, „Timer elapsed“).

---

## 6) Minimal-Setup (Rollen) + Beispiel-Workflow

ID: MAS-06

### 6.1 Minimal‑Team (3–5 Agenten)

1. **Supervisor/Orchestrator:** zerlegt Ziel, verteilt Tasks, aggregiert.
2. **Research‑Agent:** sammelt Quellen/Beispiele, extrahiert Fakten.
3. **Engineer/Builder‑Agent:** setzt um (Tools, Code, Automationen), erzeugt technische Artefakte.
4. **Reviewer/QA‑Agent:** prüft Konsistenz, Risiken, Definitionen, Styleguide‑Konformität.
5. *(optional)* **Scribe/Doc‑Agent:** finalisiert Doku (IDs, ToC, Navigation, Evolution).

### 6.2 Beispiel‑Workflow („Wie sieht dein Workflow aus?“)

**Input:** „Baue ein neues Wissensobjekt“

1) Supervisor definiert Scope & DoD → erstellt Plan

2) Research liefert: Definitionen, Patterns, Referenzen

3) Builder erzeugt Struktur/Artefakt (z. B. Seite, Schema)

4) Reviewer prüft: Widersprüche, Lücken, Governance

5) Scribe schreibt final in SSOT‑Format + Update‑Historie

---

## 7) Framework-Entscheidung: „Pipes“ (Module, Prozesse, Abläufe)

ID: MAS-07

**Ziel:** Ein eigenes Workflow‑/Orchestrierungs‑Framework, das Multi‑Agenten‑Teams als **Pipelines („Pipes“) aus Modulen** abbildet.

### 7.1 Begriff „Pipe“ (Arbeitsdefinition)

Eine **Pipe** ist eine definierte Abfolge von **Stages/Modulen**, die über **ein gemeinsames State‑Objekt** (oder ein Event‑Log) verbunden sind. Jede Stage hat:

- Input‑Schema
- Output‑Schema
- DoD/Guards
- Retry/Timeout/Fehlerpfade

### 7.2 Module (Bausteine)

- **Orchestrator** (Routing, Scheduling)
- **State Store** (Blackboard, Memory, Artefakte)
- **Tool Layer** (Actions/Integrationen)
- **Observability** (Logs, Traces, Evaluations)
- **Policy/Governance** (Rechte, Audit, Data Boundaries)

### 7.3 Prozesse/Abläufe (SSOT)

- Trigger/Event → Route → Execute Stage → Validate → Persist → Next Stage

---

## 8) Use-Cases / Komponenten-Sicht (Team, Workflow, Komponenten)

ID: MAS-08

### 8.1 Team‑Use‑Cases

- Research → Synthese → Doku‑Publikation
- Architektur/ADR‑Erstellung mit Review‑Schleife
- Incident‑Analyse (Log‑Sammlung → Hypothesen → Fix → Postmortem)

### 8.2 Komponenten‑Sicht (Checkliste)

- Agentenrollen
- Kommunikationskanäle
- Persistenter State (SSOT)
- Actions/Tools
- Eventing/Trigger
- Safety/Governance

---

## 9) Beispiele, Tutorials, Diagramme (Linkliste)

ID: MAS-09

- LangChain/LangGraph: Multi‑Agent‑Architekturen (Supervisor/Router/Network)
- Microsoft AutoGen: Multi‑Agent Conversation Framework
- CrewAI: Rollen-/Crew‑basierte Orchestrierung
- Event‑Driven MAS Patterns (Analogien zu Microservices)
- „Blackboard pattern“ als Koordinationsmuster

*(Hinweis: Links werden in der nächsten Iteration als kuratierte Referenzen mit kurzen Abstracts ergänzt.)*