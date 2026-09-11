# Kapitel-6a-Delivery-Methodik-KI-Softwareentwicklung

Bereich: B-Wissen
Schutzklasse: intern
Soll-Knoten: D-Prozesse
Status: Draft

**Erstelldatum (fix):** 07.07.2026, 15:32 (Europe/Berlin)

**Letzte Aktualisierung:** 07.07.2026, 15:32 (Europe/Berlin)

**Status:** Draft

**Zweck:** Verbindliche Brücke zwischen der Gründungsdoku und der eigenständigen „AI Driven Software Development Knowledge Base" (SD-KB). Dieses Kapitel erklärt, wie der Delivery-Lifecycle aus Kapitel 6 methodisch durch die SD-KB unterlegt wird, ohne deren Inhalte zu duplizieren.

**Fehlt (kurz):** Notion-Links (statt nur Block-IDs) einsetzen, sobald die SD-KB im selben Workspace verlinkt ist + Prüfung, ob die SD-KB im Repo einen neueren Stand hat als die referenzierte Notion-Version (dann Block-IDs/Titel nachziehen).

**KI-Referenz:** KAPITEL-6A-DELIVERY-METHODIK-SD-KB

Update-Historie (Evolution)

| Zeitpunkt (TZ) | Änderung |
| --- | --- |
| 07.07.2026, 15:32 (Europe/Berlin) | Initiale Erstellung des Brücken-Kapitels (verlinkt SD-KB, dupliziert nicht) |

Standard: siehe Dokumentations-Styleguide (Global) – Regel-Template. Dieses Kapitel folgt der Gründungs-Konvention; die referenzierte SD-KB nutzt bewusst ein **eigenes** Regelwerk (Block-ID-Schema `KB-XXX-NNNN`, festes 7-Block-Template, semantische Farb-/Emoji-Logik, 📦-Block-Pattern). Beide Systeme bleiben getrennt konsistent — dieses Kapitel ist die Verbindungsstelle.

Navigation:

| Fachliche ID | Titel/Label | Typ |
| --- | --- | --- |
| KAP6A-ZWECK-0001 | Warum zwei Dokumentationssysteme | Kapitel |
| KAP6A-MAPPING-0001 | Lifecycle-Mapping (Kap. 6 ↔ SD-KB) | Kapitel |
| KAP6A-GOV-0001 | Governance & Human-in-the-Loop | Kapitel |
| KAP6A-SYNC-0001 | Sync-Regel Notion ↔ Repo | Kapitel |
| KAP6A-REF-0001 | Referenzen in die SD-KB | Kapitel |

## Warum zwei Dokumentationssysteme

ID: KAP6A-ZWECK-0001

Die Gründungsdoku beschreibt das Unternehmen (Businessplan, Finanzplan, Förderung, Marktanalyse, Prozesse) für Prüf- und Steuerungszwecke. Die SD-KB beschreibt die **Methodik der Softwareentwicklung selbst** — den vollständigen SDLC von Vision bis Maintenance, mit KI-Agenten-Rollen, Prompt-Bibliothek und Vektor-DB-Anbindung.

Das sind unterschiedliche Zwecke mit unterschiedlichen Lesern (Förderstelle/Bank vs. Entwicklung/KI-Agenten). Deshalb bleiben sie **getrennt** und werden verlinkt, nicht verschmolzen. Das entspricht dem Single-Source-of-Truth-Prinzip: Artefakte verlinken statt duplizieren. Die SD-KB ist damit die methodische Tiefenschicht unter Kapitel 6 (Interner Geschäftsprozess & Delivery-Lifecycle).

## Lifecycle-Mapping (Kapitel 6 ↔ SD-KB)

ID: KAP6A-MAPPING-0001

Die sechs Phasen des Delivery-Lifecycle aus Kapitel 6 werden methodisch durch SDLC-Bereiche der SD-KB abgedeckt. Die SD-KB-Block-IDs sind stabil und dienen als Referenzanker:

- **Intake & Qualifizierung** (Kap. 6/1) → Vision & Project Definition, Stakeholder-Analyse (SD-KB Bereiche 01–02).
- **Discovery Sprint / KI-Prozess-Check** (Kap. 6/2) → Requirements Engineering, Object-Oriented Analysis, Domain Modeling (SD-KB 03–05).
- **Angebot & Scope** (Kap. 6/3) → Architektur, Interfaces/APIs, Data Models (SD-KB 06–08); Entscheidungen als ADR.
- **Umsetzung** (Kap. 6/4) → Implementation Guidelines, Testing & Quality Assurance (SD-KB 10–11, `KB-QA-0015`).
- **Übergabe & Enablement** (Kap. 6/5) → Deployment, Operations & Monitoring (SD-KB 12–13).
- **Betrieb & Weiterentwicklung** (Kap. 6/6) → Maintenance & Evolution (SD-KB 14).

Querschnittlich über alle Phasen: der AI-Driven-Development-Flow (`KB-DASH-0002`), die AI Agent Instructions (`KB-AIAG-0019`) und die Prompt Library (`KB-PROMPT-0020`).

## Governance & Human-in-the-Loop

ID: KAP6A-GOV-0001

Die SD-KB legt eine Grundregel fest, die auch für die Gründungsphase gilt: KI darf Inhalte strukturieren, prüfen und vorschlagen — Entscheidungen, Freigaben und Merge erfolgen nach menschlichem Review (Human-KI-Kollaborationsmodell, `KB-DASH-0004`).

Für die Delivery gilt daraus abgeleitet: Jede Phase hat ein Quality Gate; außenwirksame Schritte (Angebot, Abnahme, Deployment beim Kunden) sind erst nach menschlicher Freigabe gültig. Das ist konsistent mit dem Meetings-Regelwerk (Human-in-the-Loop-Gate bei außenwirksamen Beschlüssen) und mit Kapitel 8 (Definition of Done je Schritt).

## Sync-Regel Notion ↔ Repo

ID: KAP6A-SYNC-0001

Die SD-KB existiert an zwei Orten: als Notion-Workspace (Entstehungsort) und als eingecheckte Fassung im Git-Repository. Für Referenzen aus diesem Kapitel gilt:

- **Autoritativ ist die Repo-Fassung**, sobald sie vom Notion-Stand abweicht (das Repo kann neuere lokale Dateien enthalten, die noch nicht nach Notion zurückgeflossen sind).
- Weichen Block-IDs oder Titel zwischen Repo und Notion ab, werden die Referenzen in diesem Kapitel (KAP6A-REF-0001) nachgezogen.
- Vor einer institutionellen Einreichung wird geprüft, ob die hier zitierten SD-KB-Stände aktuell sind.

Hinweis: Die unten referenzierten Block-IDs stammen aus dem Notion-Export vom Juni 2026 und sind gegen den aktuellen Repo-Stand zu verifizieren.

## Referenzen in die SD-KB

ID: KAP6A-REF-0001

Zentrale Einstiegspunkte der SD-KB (Block-ID → Bereich):

- `KB-DASH-0001` – 00 Dashboard (Einstieg, SDLC-Gesamtüberblick, Navigation)
- `KB-DASH-0002` – 00.1 AI Driven Development Flow (Prozess-Flow)
- `KB-DASH-0004` – 00.3 Human-KI-Kollaborationsmodell (Prinzipien, Rollen, Reviews)
- `KB-QA-0015` – 11 Testing & Quality Assurance (Quality Gates, Test-Gate-Logik)
- `KB-AIAG-0019` – 15 AI Agent Instructions (Agenten-Regeln)
- `KB-PROMPT-0020` – 16 Prompt Library (Prompt-Bausteine)
- `KB-REF-0026` – 19 AI Reference Index (Block-ID → Seite/Kategorie/Link)
- `KB-REF-0029` – 22 Begriffsmodell → Vector-DB-Mapping (Hybrid-Retrieval-Konzept)

Der AI Reference Index (`KB-REF-0026`) ist der maßgebliche Lookup für alle weiteren Block-IDs der SD-KB.