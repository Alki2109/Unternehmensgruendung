# Scrum – Systembeschreibung (Clean)

<aside>
ℹ️

**Abstract/Überblick:** Konsolidierte, prüfbare Systembeschreibung von Scrum (Rollen, Artefakte, Events, Chronologie) als Grundlage für eine spätere operative Anwendung (inkl. Software-Delivery/CI/CD‑Kontext).

</aside>

<aside>
🧷

**Standard:** siehe [Dokumentations-Styleguide (Global) – Regel-Template](https://app.notion.com/p/Dokumentations-Styleguide-Global-Regel-Template-ebb91c6deb1747998a35aa3e0da9d7d2?pvs=21)

**Quelle (Working Notes):** [Neue Anweisungen für Zusammenfassungen ](https://app.notion.com/p/Neue-Anweisungen-f-r-Zusammenfassungen-39c0cb48a954800fb63ed4969f17ac13?pvs=21)

</aside>

<aside>
🕒

**Erstelldatum (fix):** 13.07.2026, 07:09 (Europe/Berlin)

**Letzte Aktualisierung:** 13.07.2026, 07:09 (Europe/Berlin)

</aside>

- Update-Historie (Evolution)
    
    
    | Zeitpunkt (TZ) | Änderung |
    | --- | --- |
    | 13.07.2026, 07:09 (Europe/Berlin) | Initiale Konsolidierung aus Working Notes |

---

## 1) Begriffsmodell (SSOT)

### 1.1 Bausteine

- **Rollen (Accountabilities):** Product Owner, Scrum Master, Developers
- **Events (Rituale):** Sprint, Sprint Planning, Daily Scrum, Sprint Review, Sprint Retrospective
- **Artefakte:** Product Backlog, Sprint Backlog, Increment
- **Commitments:** Product Goal, Sprint Goal, Definition of Done (DoD)
- **Empirische Pfeiler:** Transparenz, Inspektion, Adaption

### 1.2 Arbeitsobjekte (Domänenobjekte)

- **Use Case / Epic:** fachlicher Nutzenrahmen
- **User Story:** kleinster wertorientierter Lieferumfang (vertikaler Schnitt)
- **Task:** konkrete Arbeitsschritte zur Umsetzung einer Story
- **Bug / Tech Debt:** Backlog Items mit Akzeptanzkriterien/DoD‑Anforderungen

---

## 2) Rollen & Verantwortlichkeiten

### 2.1 Product Owner (PO)

**Zweck:** Maximiert Produktwert.

**Verantwortet:**

- Product Goal / Vision‑Richtung und Backlog‑Priorisierung
- Klare Backlog Items (Wert, Akzeptanzkriterien, Reihenfolge)

**Lieferobjekte:** Priorisiertes Product Backlog; Sprint‑Ziele (abgestimmt)

### 2.2 Scrum Master (SM)

**Zweck:** Macht Scrum wirksam.

**Verantwortet:**

- Coaching zu Scrum, Facilitation, Impediment‑Bearbeitung
- Verbesserung von Zusammenarbeit und Systembedingungen

**Lieferobjekte:** Verbesserungsmaßnahmen aus Retros (tracked)

### 2.3 Developers

**Zweck:** Erstellt das Increment.

**Verantwortet:**

- Umsetzung der Sprint‑Backlog Items, technische Qualität, Integration
- Laufende Plananpassung im Sprint Richtung Sprint Goal

**Lieferobjekte:** Increment gemäß DoD (inkl. Tests/Docs im Scope)

---

## 3) Artefakte & Qualitätsregeln

### 3.1 Product Backlog

**Definition:** Geordnete Liste aller bekannten Arbeiten am Produkt.

**Mindestinhalt je Item:** Nutzen/Wert, Akzeptanzkriterien, grobe Größe, relevante Abhängigkeiten.

### 3.2 Sprint Backlog

**Definition:** Sprint Goal + ausgewählte PBIs + Umsetzungsplan (Tasks).

**Regel:** Lebendig; wird täglich angepasst.

### 3.3 Increment

**Definition:** Summe aller „Done“ PBIs des Sprints + vorherige Inkremente; potenziell auslieferbar.

---

## 4) Definition of Done (DoD) & Definition of Ready (DoR)

### 4.1 DoD (verbindlich)

Ein Item ist „Done“, wenn mindestens:

- Implementiert & im Hauptzweig integriert
- Automatisierte Tests vorhanden & grün
- CI/Build erfolgreich; Qualitätsgates erfüllt
- Doku im Scope aktualisiert
- Akzeptanzkriterien erfüllt; ggf. Abnahme erfolgt

### 4.2 DoR (optional)

Ein Item ist „ready“, wenn:

- Ziel/Nutzen und Akzeptanzkriterien klar
- Abhängigkeiten/Constraints bekannt
- Größenordnung sprintfähig

---

## 5) Prozessablauf & Chronologie (Sprint‑Lebenszyklus)

### 5.1 Kontinuierlich: Refinement

**Ziel:** Schneiden, Klären, Vorbereiten.

**Output:** Besser geschnittene Items + aktualisierte Priorisierung.

### 5.2 Sprint (Zeitbox, typ. 1–2 Wochen)

#### 5.2.1 Sprint Planning

**Output:** Sprint Goal + Sprint Backlog.

#### 5.2.2 Daily Scrum

**Ziel:** Synchronisation & Plananpassung.

**Output:** Aktualisierter Tagesplan; sichtbare Impediments.

#### 5.2.3 Sprint Review

**Ziel:** Inkrement zeigen, Feedback, Backlog anpassen.

#### 5.2.4 Sprint Retrospective

**Ziel:** System/Team verbessern.

**Output:** Wenige, verbindliche Verbesserungsmaßnahmen.

---

## 6) Work‑Splitting: Use Case → Story → Tasks

### 6.1 Vertikaler Schnitt (Wertlieferung)

- Use Case/Epic → mehrere Stories (jeweils nutzbarer Teilwert)
- Story → Tasks (Analyse, Implementierung, Tests, Infra, Review, Doku)

### 6.2 User‑Story‑Form

- Als *[Rolle]* möchte ich *[Funktion]*, damit *[Nutzen]*.
- Akzeptanzkriterien: Given/When/Then oder klare Prüfliste.

### 6.3 Sizing‑Leitplanken (Mensch vs. KI)

- **Mensch:** ideal 0,5–1 Tag je Story; >2 Tage → weiter schneiden.
- **KI:** kann Implementierungszeit stark reduzieren, aber Validierung/Review/Abstimmung bleibt limitierend.

---

## 7) 2‑Stunden‑Inkremente (Tageszerlegung)

### 7.1 Ziel

In 2‑Stunden‑Blöcken messbaren Output erzeugen (Liefer‑ oder Lernresultat).

### 7.2 Beispiele für „Done in 2h“

- Kleines Sub‑Feature inkl. Test & Integration
- API‑Endpunkt inkl. Contract‑Test
- Pipeline‑Stufe/Config‑Änderung inkl. Smoke‑Test

### 7.3 Tag‑Mapping (realistisch)

- 3–4 Blöcke à 2h Fokusarbeit + Kommunikation/Overhead.

---

## 8) CI/CD‑Pipeline als Teil der Lieferkette

- Pipeline‑Schritte (Build, Tests, Scans, Deploy) sind Teil der DoD.
- Pipeline/Infra‑Änderungen sind normale Backlog Items (mit Akzeptanzkriterien).

---

## 9) Offene Parameter (für „vollständig & korrekt“ im konkreten Setup)

- Sprintlänge (Standard)
- Tooling (Backlog/Board, CI/CD, Code‑Review)
- Konkrete DoD‑Checkliste (engineering‑spezifisch)
- Wertdefinition/Outcome‑KPIs (PO‑Leitlinien)