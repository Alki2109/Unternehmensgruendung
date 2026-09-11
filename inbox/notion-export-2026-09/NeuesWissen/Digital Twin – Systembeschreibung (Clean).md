# Digital Twin – Systembeschreibung (Clean)

<aside>
ℹ️

**Abstract/Überblick:** Konsolidierte, prüfbare Systembeschreibung des Konzepts „Digital Twin“ (Begriffsursprung, Definitionen/Abgrenzungen, Bausteine/Architektur, Reifegradmodell, Use-Cases, Qualitäts-/Governance-Aspekte) als Grundlage für eine spätere operative Anwendung (inkl. „Digital Twin“ für Organisation/Prozesse/Software).

</aside>

<aside>
🧷

**Standard:** siehe [Dokumentations-Styleguide (Global) – Regel-Template](https://app.notion.com/p/Dokumentations-Styleguide-Global-Regel-Template-ebb91c6deb1747998a35aa3e0da9d7d2?pvs=21)

**Referenz-Layout (Analog):** [Scrum – Systembeschreibung (Clean)](Scrum%20%E2%80%93%20Systembeschreibung%20(Clean)%201bc9a480e1e64ed48e6ef5dd8a23ec27.md)

</aside>

<aside>
🕒

**Erstelldatum (fix):** 13.07.2026, 07:17 (Europe/Berlin)

**Letzte Aktualisierung:** 13.07.2026, 07:17 (Europe/Berlin)

</aside>

- Update-Historie (Evolution)
    
    
    | Zeitpunkt (TZ) | Änderung |
    | --- | --- |
    | 13.07.2026, 07:17 (Europe/Berlin) | Initiale Konsolidierung (Definitionen, Abgrenzungen, Reifegrad, Use-Cases) |

Navigation (maschinenlesbar):

| Fachliche ID | Titel/Label | Ziel | Typ |
| --- | --- | --- | --- |
| DTWIN-01 | Begriffsmodell (SSOT) | (dieses Dokument) | Kapitel |
| DTWIN-02 | Bausteine / Architektur | (dieses Dokument) | Kapitel |
| DTWIN-03 | Reifegrad / Wandel | (dieses Dokument) | Kapitel |
| DTWIN-04 | Use-Cases & Nutzenhypothesen | (dieses Dokument) | Kapitel |
| DTWIN-05 | Qualität, Governance, Risiken | (dieses Dokument) | Kapitel |
| DTWIN-06 | Offene Parameter (für „vollständig & korrekt“ im konkreten Setup) | (dieses Dokument) | Kapitel |

---

## 1) Begriffsmodell (SSOT)

ID: DTWIN-01

### 1.1 Kern-Definition

Ein **Digital Twin** ist ein **dynamisches, datengetriebenes digitales Abbild** einer realen (oder auch rein digitalen) Entität (Objekt/System/Prozess), das den Zustand fortlaufend aktualisiert, Verhalten modelliert und Entscheidungen/Steuerung unterstützt.

### 1.2 Ursprung / Herkunft (Kurz)

- Historisch stark aus Engineering/Aerospace/Industrial-IoT geprägt (Modellierung + Betriebssignale/Telemetry)
- Popularisiert als Produkt-/Lifecycle-orientiertes Konzept in PLM/Manufacturing (u. a. Michael Grieves, frühe 2000er)

### 1.3 Abgrenzungen (präzise Begriffe)

- **Digital Model:** statisches Modell, keine automatische Datenkopplung.
- **Digital Shadow:** automatische Datenflüsse primär *vom* physischen System *ins* digitale Abbild (Beobachtung).
- **Digital Twin:** (je nach Reife) zusätzlich **Feedback-Schleife**: Analyse/Simulation/Optimierung → Empfehlungen/Automationen → Wirkung zurück ins System („closed loop“).

### 1.4 Gegenteil (Gegenbild)

- **„Null digital / voll analog“:** keine strukturierte Erfassung, keine durchgängige Nachverfolgbarkeit, keine konsistente Datenbasis.

---

## 2) Bausteine / Architektur

ID: DTWIN-02

### 2.1 Minimal-Set (aus Implementierungssicht)

1. **Twin-Entität & Scope** (was genau wird abgebildet? Grenzen, Schnittstellen)
2. **Identität** (stabile IDs, Versionierung, Lifecycle)
3. **Datenquellen** (Sensorik, Logs, Events, Tickets, Dokumente, ERP/CRM, manuelle Erfassung)
4. **Zustandsmodell** (Zustandsvariablen, Zeitreihen, Ereignisse)
5. **Verhaltensmodell** (Regeln, Simulation, ML/Reasoning)
6. **Auswertungs-/Entscheidungsschicht** (KPIs, Anomalien, Prognosen, What-if)
7. **Aktionsfähigkeit** (Workflows, Guardrails, Human-in-the-loop, Automationen)
8. **Governance** (Datenqualität, Rechte, Audit, SSOT, Nachvollziehbarkeit)

### 2.2 Datenfluss-Muster

- **Beobachten:** Real → Digital (Shadow)
- **Simulieren:** Digital + Modelle → Hypothesen/Prognosen
- **Steuern:** Entscheidung/Policy → Real (Twin, „closed loop“)

---

## 3) Wandel / Reifegradmodell (von „null digital“ bis „voll digitalisiert“)

ID: DTWIN-03

### 3.1 Stufenmodell (pragmatisch)

1. **0 – Null digital (analog):** keine systematische Erfassung, Wissen verteilt.
2. **1 – Punktuell digital:** einzelne Tools, wenig Integration, geringe Prozesssicht.
3. **2 – Prozessdigitalisierung:** Kernprozesse digital abgebildet, aber Lücken/Brüche.
4. **3 – Integriert & messbar:** Systeme verknüpft, konsistente IDs, Metriken.
5. **4 – Digital Shadow:** Live-/Near-live Daten fließen ins Abbild; Analysen möglich.
6. **5 – Digital Twin (closed loop):** Rückkopplung/Steuerung mit Audit & Guardrails.

### 3.2 Idealbild („Soll-Zustand“ aus deiner Notiz)

**Voll digitalisiert** bedeutet hier: **Erfassung aller relevanten Prozesse End-to-End**, sodass Zustände, Abhängigkeiten, Durchlaufzeiten, Qualitätskennzahlen und Entscheidungen nachvollziehbar werden.

---

## 4) Use-Cases & Nutzenhypothesen

ID: DTWIN-04

### 4.1 Engineering/Industrie (klassisch)

- Condition Monitoring, Predictive Maintenance
- Simulation/Optimierung von Anlagen/Produkten
- Qualitätsanalyse, Root-Cause, Lifecycle-Tracking

### 4.2 Software/Organisation/Prozesse (übertragene Sicht)

- „Twin“ eines Delivery-Systems (Backlog → CI/CD → Betrieb): Flusskennzahlen, Bottlenecks, Risiken
- Prozess-Transparenz (E2E), Compliance/Audit, Entscheidungsunterstützung
- Szenarioanalyse („Was passiert, wenn wir Teamzuschnitt/WIP/Tooling ändern?“)

---

## 5) Qualität, Governance, Risiken

ID: DTWIN-05

- **Datenqualität:** Vollständigkeit, Aktualität, Konsistenz, Provenienz
- **Modellrisiken:** falsche Annahmen, Drift, Überanpassung, Scheingenauigkeit
- **Sicherheit/Rechte:** Zugriff auf Telemetrie, PII, Betriebsgeheimnisse
- **Nachvollziehbarkeit:** Entscheidungen/Automationen müssen auditierbar sein

---

## 6) Offene Parameter (für „vollständig & korrekt“ im konkreten Setup)

ID: DTWIN-06

- Was ist die *Twin-Entität* in deinem Kontext (Organisation? Produkt? Prozesslandkarte? „virtuelles Bürogebäude“)?
- Welche Datenquellen sind tatsächlich verfügbar (und in welcher Qualität/Frequenz)?
- Welche Aktionen sind erlaubt (nur Empfehlung vs. Automation)?
- Welche Governance-Regeln gelten (SSOT, Rollen, Audit, Datenschutz)?