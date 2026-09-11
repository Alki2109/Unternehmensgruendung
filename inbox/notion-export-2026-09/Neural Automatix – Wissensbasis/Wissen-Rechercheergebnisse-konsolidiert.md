# Wissen-Rechercheergebnisse-konsolidiert

Bereich: B-Wissen
Schutzklasse: intern
Soll-Knoten: F-Wissen
Status: Draft

# Wissensdokument – Rechercheergebnisse (offene Themen, konsolidiert)

**Erstelldatum (fix):** 10.07.2026, 06:10 (Europe/Berlin)

**Letzte Aktualisierung:** 10.07.2026, 06:10 (Europe/Berlin)

**Status:** Draft

**Zweck:** Formatkonforme Ablage der Perplexity-Rechercheergebnisse zu sieben offenen Themen. Jeder Block ist einem Soll-Struktur-Knoten zugeordnet und Pipeline-fähig aufbereitet (IDs, Quellen als Kurzbeleg, offene Posten markiert). Grundlage für die spätere Begriffsmodell-/DB-Überführung.

**Fehlt (kurz):** Alle mit "n.a." markierten Posten sind offene Recherchelücken und vor Freigabe zu schließen oder als dauerhaft offen zu kennzeichnen + Zahlendivergenzen (KI-Nutzung Destatis vs. ifo) im Businessplan mit Definition/Jahr sauber führen + Rechtsstand AI Act (Digital Omnibus) vor Verwendung erneut prüfen.

**KI-Referenz:** WISSEN-RECHERCHE-OFFENE-THEMEN

Update-Historie (Evolution)

| Zeitpunkt (TZ) | Änderung |
| --- | --- |
| 10.07.2026, 06:10 (Europe/Berlin) | Rechercheertrag formatkonform konsolidiert; Soll-Knoten zugeordnet |

Standard: siehe Dokumentations-Styleguide (Global) und Schreib-/Qualitätsrichtlinie G7. Quellen sind als Kurzbeleg (Herausgeber, Datum) geführt; Originalpassagen wurden in eigenen Worten verdichtet, nicht reproduziert.

Navigation:

| Fachliche ID | Thema | Ziel-Knoten (Soll) |
| --- | --- | --- |
| WIS-DIGITALTWIN-0001 | Digital Twin & DTO | B2 |
| WIS-BPM-0001 | Geschäftsprozessmodellierung BPMN/UML | D3 |
| WIS-USECASE-0001 | Use Case → Workflow → Multi-Agentic | D/E |
| WIS-BEGRIFFE-0001 | Geschäftsprozess/Workflow/Agent | G6 |
| WIS-MARKT-0001 | Nachfrageseite Markt (KMU/KI) | A5 |
| WIS-CHUNK-0001 | Chunking/Retrieval Best Practices | F2 |
| WIS-AIACT-0001 | AI-Act-Pflichten | A6/D |

## Digital Twin & DTO

ID: WIS-DIGITALTWIN-0001

Ein Digital Twin ist eine virtuelle Repräsentation eines physischen Objekts/Systems mit Echtzeit-Datenanbindung; Kernmerkmal ist der bidirektionale Datenaustausch (unterscheidet ihn von Simulation und statischem 3D-Modell) (IBM, 2020; Siemens; Britannica, 2024). Für das eigene Vorhaben maßgeblich ist der **Digital Twin of an Organization (DTO)**: ein dynamisches Softwaremodell einer Organisation, das menschliches und nicht-menschliches Verhalten abbildet – "was tatsächlich getan wird, statt was getan werden soll" (Gartner, Report G00785499, 20.11.2024; DTO-Begriff seit 2017).

Reale Umsetzungen physischer Twins: NASA (Ursprung, Apollo 13), GE Aerospace und Rolls-Royce (Triebwerks-Twins, Predictive Maintenance), Siemens (Produkt-/Produktions-/Service-Twins), Virtual Singapore (Stadt). Nutzen: Simulation, Vorhersage, Optimierung, Was-wäre-wenn; bei Rolls-Royce bidirektionaler "Blue Data Thread".

Technische Voraussetzungen: Datenmodell, Sensorik/Telemetrie, Datenpipeline mit Echtzeit-Sync, Feedback-Kanal, Analytics/KI, Visualisierung (IBM, 2020; Siemens).

Reifegrad (IBM-Modell, 5 Stufen): (1) einmalige 2D/3D-Nachbildung, (2) statisch mit Historie/Alerts, (3) dynamisch mit Echtzeit-Sync und Was-wäre-wenn, (4) interaktiv/vernetzt mehrerer Twins (Mensch im Loop), (5) autonom/Closed-Loop. **Einordnung für das eigene Vorhaben:** "Event-Logging vorhanden" entspricht Stufe 1–2; der DTO ist Zielbild, nicht Ist-Zustand. Im Businessplan als Entwicklungspfad darstellen, nicht als erreicht.

Offene Posten: Begriffsursprung strittig (1997 vs. 2002/2010); keine universelle Definition; einzelne GE-Kennzahlen ohne Primärquelle = n.a.; ROI-/Marktzahlen aus Drittstudien (mit Vorsicht).

## Geschäftsprozessmodellierung BPMN/UML

ID: WIS-BPM-0001

Ein BPMN-Geschäftsprozessmodell besteht aus Aktivitäten (Tasks/Sub-Prozesse), Ereignissen (Start/Intermediate/End), Gateways (exklusiv/parallel/inklusiv/ereignisbasiert), Sequenz- und Nachrichtenflüssen, Pools und Lanes (Rollen/Verantwortung) sowie Datenobjekten (Input/Output) (Camunda; OMG BPMN 2.0).

BPMN 2.0 ist der De-facto-Standard für Geschäftsprozessdiagramme (OMG, formal seit Dez. 2010; zugleich ISO/IEC 19510) – verständlich für Fachanwender, aber präzise genug für Übersetzung in Softwarekomponenten. UML ist demgegenüber softwareorientiert (Visualisierung/Spezifikation von Objektsystemen). Faustregel: **BPMN für die fachliche End-to-End-Sicht + Automatisierbarkeit, UML für die technische System-/Softwaresicht** – in der Praxis kombiniert ("BPMN = was das Business tut, UML = wie die Software es tut").

Geschäftsprozesse sind prinzipiell auch im UML-Aktivitätsdiagramm modellierbar, aber verlustfreies Mapping ist nicht trivial (BPMN hat Konstrukte ohne direkte UML-Entsprechung, z. B. inklusive Gateways). BPMN ist zudem als Modellierungs- UND Ausführungswerkzeug ausgelegt, UML-AD nur zur Modellierung.

Offene Posten: "BPMN besser lesbar" empirisch nicht eindeutig (mehrere Studien finden UML-AD mindestens gleich nutzbar); Standardwahl ≠ methodische Überlegenheit.

## Use Case → Workflow → Multi-Agentic

ID: WIS-USECASE-0001

Ein Use Case wird heruntergebrochen, indem er in klar dekomponierbare Teilaufgaben zerlegt und daraus ein Workflow modelliert wird (Schritte, Übergänge, Artefakte, Entscheidungen, Rollen). Grundunterscheidung (Anthropic, Dez. 2024): **Workflows** = LLMs/Tools über vordefinierte Code-Pfade orchestriert; **Agents** = LLM steuert Prozess und Tool-Einsatz dynamisch. Leitprinzip: einfachste Lösung zuerst, Komplexität nur bei Bedarf.

Dekompositions-Muster (Anthropic): Prompt Chaining (fixe Teilschritte), Routing (Klassifikation → Spezialpfad), Parallelization (unabhängige Teilaufgaben/mehrere Perspektiven), Orchestrator-Workers (zentrale Instanz zerlegt dynamisch, delegiert, synthetisiert), Evaluator-Optimizer (eins generiert, eins bewertet, Schleife).

Multi-Agent-Referenzmuster: Orchestrator-Worker (Lead-Agent + spezialisierte Subagenten parallel) (Anthropic, Juni 2025). LangGraph systematisiert: Network, Supervisor, Supervisor (tool-calling), Hierarchical. Skalierungsregel (Anthropic): einfache Faktensuche 1 Agent/3–10 Tool-Calls; Vergleiche 2–4 Subagenten; komplexe Recherche >10 Subagenten.

Handoffs & Artefakt-Verträge: Jeder Subagent braucht Objective, Output-Format, Tool-/Quellen-Hinweise, klare Grenzen (Anthropic). Handoffs werden dem LLM als Tools präsentiert (`transfer_to_<agent>`, optional strukturiertes Input-Schema) (OpenAI Agents SDK). Große Ergebnisse als persistente Artefakte ablegen, nur leichte Referenzen zurückreichen (verhindert "Stille-Post", spart Token).

Offene Posten: synchron vs. asynchron (Lead führt Subagenten aktuell synchron = Engpass); Framework-Nutzung umstritten (kann Debugging erschweren); kein framework-übergreifender Standard für Artefakt-Verträge.

## Geschäftsprozess / Workflow / Agent (Begriffe)

ID: WIS-BEGRIFFE-0001

**Geschäftsprozess** (Gartner): ereignisgesteuerter, End-to-End-Verarbeitungspfad von der Kundenanfrage bis zum Ergebnis für den Kunden – fachliche Ebene, oft abteilungs-/organisationsübergreifend. **Workflow**: operativ/ausführbare Ebene; normative Referenz ist das WfMC Workflow Reference Model (1995, bis heute Basis vieler BPM-Systeme; WfMC 2019 aufgelöst). **(Software-)Agent** (Russell & Norvig): etwas, das seine Umgebung wahrnimmt (Sensoren) und auf sie einwirkt (Aktuatoren); Software-Agent = autonomes Programm, das Aufgaben für Nutzer erledigt. Moderne LLM-Definition (Anthropic): Agents steuern Prozess/Tool-Einsatz dynamisch selbst.

Korrelation: Geschäftsprozess = fachliches Was/Warum (grobgranular, kundenorientiert); Workflow = operative/ausführbare Umsetzung (feingranular, task-orientiert). BPMN ist die Brücke zwischen Prozessdesign und -implementierung. Intern im Agenten: Reasoning, Tool-Nutzung, interner Loop. Extern zwischen Agenten: Kommunikation/Handoffs/Nachrichten (historisch FIPA-ACL, modern Tool-Call-Handoffs, geteilte Message-Listen, Pub-Sub).

Für das Begriffsmodell relevant – Synonyme: AI Agent = Compound AI System; agentic AI = AI Agent; BPMN ≈ ISO/IEC 19510. Homonyme (Achtung, Kollisionsgefahr): "Agent" (KI-Entität vs. autonomes Programm vs. LLM-Agent vs. LangGraph-Node); "Workflow" (WfMC-ausführbar vs. Anthropic-"vordefinierte Code-Pfade"); "Handoff" (OpenAI vs. LangGraph vs. AutoGen); "Task" (CrewAI-Objekt vs. Nachricht vs. Teilaufgabe).

Offene Posten: wörtliche Gartner-Workflow-Definition und Wooldridge-Agent-Definition = n.a. (Quellen blockiert/nicht abgerufen); veraltete Normungsgremien (WfMC, FIPA).

## Nachfrageseite Markt (KMU/KI Deutschland)

ID: WIS-MARKT-0001

KI-Nutzung wächst, ist bei KMU aber deutlich niedriger als bei Großunternehmen. Destatis (IKT-Nutzung 2024, ab 10 Beschäftigte): gesamt 20 %, klein (10–49) 17 %, mittel (50–249) 28 %, groß (ab 250) 48 %. Hemmnisse: fehlendes Wissen 71 %, rechtliche Unklarheit 58 %, Datenschutz 53 %, Datenqualität 45 %. Bitkom (2025, ab 20 MA): 36 % Einsatz, nur 5 % stellen gezielt KI-Fachkräfte ein, 43 % ohne KI-Schulungen. ifo (2026): 54,4 % KI-Software-Nutzung.

**Zahlendivergenz beachten:** Destatis 20 % (2024) vs. ifo 54,4 % (2026) = unterschiedliche Definitionen (enger KI-Begriff vs. inkl. generativer KI), Jahre, Stichproben. Im Businessplan immer mit Quelle, Definition und Jahr führen.

Digitalisierungsausgaben Mittelstand rückläufig: 2023 = 31,9 Mrd. €, 2024 = 23,8 Mrd. € (KfW). KI-Marktvolumen Deutschland: 2024 = 8,2 Mrd. €, 2025 > 10 Mrd. € (Bitkom/IDC). IT-Fachkräftemangel: 2025 rund 109.000 unbesetzte IT-Stellen, Vakanzzeit 7,7 Monate (Bitkom); allgemeiner IT-Stellenmarkt 2024 eingebrochen (−26,2 %, IW Köln), KI-Kompetenznachfrage steigt.

**USP-Einordnung:** Tragende Story = Bedarf da, Wissen fehlt (71 % Hemmnis "fehlendes Wissen"). These "KI-Kompetenz knapper als Softwareentwicklung" nur teilweise belegt (KI-Berufe höher vergütet: Data Scientist 67.000 € vs. Softwareentwickler 54.500 € Median; aber KI-Jobs nur 1,5 % aller Anzeigen, stagnierend). Daher als Kombinationsvorteil (IT + KI + Didaktik selten zusammen) formulieren, nicht als absolute Knappheit.

Offene Posten: isoliertes Marktvolumen "KI-Dienstleistungen für KMU" = n.a. (nur Näherung); direkte Vakanzzeit KI-Spezialist vs. Softwareentwickler = n.a.; freelancermap-Indikatoren nicht verifiziert = n.a.

## Chunking/Retrieval Best Practices

ID: WIS-CHUNK-0001

Chunk-Größe: token-basiert dominiert; belegte Richtwerte ~512–1024 Token. Anthropic-Beispiel 800 Token; LlamaIndex fand 1024 als beste Balance; Databricks produktiv 512. Overlap moderat, Databricks 50 % (256 bei 512). **Ableitung:** 512 Token als robuster, latenz-/speichereffizienter Startwert; 1024 wenn Faithfulness/Relevancy Priorität; finale Festlegung per A/B-Test auf eigenem Datensatz.

Hybrid-Retrieval + Reranking ist State of the Art: Vektor + BM25 schlägt Vektor allein; Reranker über überfetchte Kandidatenmenge (Anthropic: Top-150 → Top-20). Contextual Retrieval (Kontext 50–100 Token je Chunk voranstellen) senkt Fehlerrate deutlich. Mehr Kontext ist nicht automatisch besser ("lost in the middle").

pgvector: HNSW als Default (bessere Speed-Recall-Balance, kein Trainingsschritt); IVFFlat nur bei sehr großem Volumen/knappem Speicher. Distanzmetrik passend zum Embedding-Modell (meist Cosinus `<=>`). Metadaten-Filter über Index auf Filterspalte + iterative Index-Scans. HNSW-Defaults: m=16, ef_construction=64, ef_search=40.

Hinweis für kleine Wissensbasen: Bei < 200.000 Token rät Anthropic, ganz auf RAG zu verzichten und alles in den Prompt zu geben – vor DB-Aufbau prüfen, ob die eigene Basis diese Schwelle überschreitet.

Offene Posten: keine universelle Chunk-Größe (abhängig von Dokumenttyp/Embedding/Query); allgemeiner Overlap-Prozentwert aus Primärquelle teils n.a.; semantisches Chunking noch experimentell.

## AI-Act-Pflichten

ID: WIS-AIACT-0001

Keine Rechtsberatung – Rechercheüberblick; maßgeblich sind Amtsblatt-Fassung und offizielle Leitlinien.

Grundregel (VO (EU) 2024/1689): Inkrafttreten 01.08.2024, allgemeine Geltung ab 02.08.2026 (gestufte Ausnahmen). Bereits gültig: verbotene Praktiken + KI-Kompetenz (02.02.2025), Governance/GPAI (02.08.2025).

**Für einen KI-Dienstleister mit Agenten auf Kunden-/Mitarbeiterdaten:**

- Ab 02.08.2026 unmittelbar: **Transparenzpflichten Art. 50** – KI-Interaktion offenlegen (Chatbots/Agenten), synthetische Inhalte maschinenlesbar kennzeichnen, Deepfakes offenlegen. Betrifft das Avatar-Konzept direkt.
- **Hochrisiko** (u. a. Beschäftigung/HR, Anhang III Nr. 4): Anbieterpflichten (Art. 16) bzw. Betreiberpflichten (Art. 26/27). Geltung durch "Digital Omnibus" voraussichtlich auf 02.12.2027 verschoben – aber noch nicht rechtskräftig (Parlament 16.06.2026 und Rat 29.06.2026 zugestimmt, Amtsblatt ausstehend). Bei Nichtannahme vor 02.08.2026 gilt der ursprüngliche Zeitplan.
- Parallel gilt weiter die DSGVO.

**Strategische Einordnung:** AI Act ist für das eigene Angebot ein Geschäftsfeld (Kunden brauchen Compliance-Unterstützung), kein Fördertopf. Eigene Transparenzpflicht (Art. 50) von Anfang an erfüllen. Weiterhin auf 02.08.2026 vorbereiten, bis der Omnibus förmlich angenommen ist.

Offene Posten: verbindlicher Status Digital Omnibus (noch nicht in Kraft); Timing Art. 50(2) maschinenlesbare Kennzeichnung (Einzelquelle); Kommissions-Leitlinien zu Art. 6 (Stand n.a.); nationale Umsetzung Deutschland/BNetzA (n.a.).

## Reihenfolge der Weiterverarbeitung

ID: WIS-PIPELINE-0001

Empfohlene Einpflege-Reihenfolge in Begriffsmodell und DB (gemäß Wissens-Pipeline): (1) Begriffe WIS-BEGRIFFE-0001 → G6 zuerst (eindeutige Vokabeln, Synonyme/Homonyme klären), (2) Prozesswissen WIS-BPM-0001 → D3 und WIS-USECASE-0001 → D/E, (3) technisches Wissen WIS-CHUNK-0001 → F2 und WIS-DIGITALTWIN-0001 → B2, (4) markt-/compliance-relevantes Wissen WIS-MARKT-0001 → A5 und WIS-AIACT-0001 → A6/D. Alle "n.a."-Lücken vor Freigabe als offene Rechercheposten kennzeichnen.