# Kapitel 5 – Marktanalyse, Zielgruppe und USP

<aside>
📌

**Status:** Updated (auditierbar, quellenbasiert)

Zweck: Markt, Zielgruppenpriorisierung, USP und Belege **prüffähig** strukturieren.

KI-Referenz: KAPITEL-5-MARKTANALYSE-ZIELGRUPPE-USP

</aside>

<aside>
🕒

**Erstelldatum (fix):** 27.05.2026, 16:11 (Europe/Berlin)

**Letzte Aktualisierung:** 02.07.2026, 05:05 (Europe/Berlin)

</aside>

- Update-Historie (Evolution)
    
    
    | Zeitpunkt (TZ) | Änderung |
    | --- | --- |
    | 02.07.2026, 05:05 (Europe/Berlin) | Markt/ICP/Wettbewerb auditierbar neu strukturiert (Evidence Pack) |
    | 17.06.2026, 17:47 (Europe/Berlin) | Draft-Stand (Anforderungen + fehlende Punkte) |

<aside>
🧾

**Änderungslogik (aus 3 Dokumenten abgeleitet):**  

1) *Beschaffungsplan* definiert Informationsbedarf + Quellen (prüfbarer Plan).  

2) *Faktenmatrix* belegt Kennzahlen (Quelle + Snippet + Datum + Limitations).  

3) *Businessplan-Text* nutzt ausschließlich belegte Fakten und markiert Annahmen.

</aside>

## 5.1 Markt & Bedarf (belegt)

### 5.1.1 Marktlage (Kurztext, einreichungsreif)

Der deutsche KMU-Markt befindet sich 2025/26 in einer aktiven KI‑Adoptionsphase. Destatis weist für 2025 eine KI‑Nutzungsquote von **26 % aller Unternehmen** mit ≥ 10 Beschäftigten aus (kleine Unternehmen 10–49 MA: **23 %**; mittlere 50–249 MA: **36 %**). Die größten Hemmnisse gegen KI‑Adoption sind **fehlendes Wissen (72 %)**, **rechtliche Unsicherheit (62 %)** und **Datenschutzbedenken (60 %)** – und decken damit exakt die typischen Leistungsfelder von KI‑Beratung, Enablement und Implementierungsbegleitung ab. Das ifo Institut bestätigt eine unmittelbare Nachfragepipeline: **18,9 %** der Unternehmen planen in den kommenden Monaten den KI‑Start.

### 5.1.2 Marktdaten – Mini-Faktenmatrix (Auszug)

*(Vollständige auditierbare Faktenmatrix liegt separat als Evidence Pack vor; hier nur die Kernaussagen für Kapitel 5.)*

<aside>
📋

**Audit-Vermerk (Juli 2026):** Diese Faktenmatrix wurde gegen Originalquellen stichprobenartig geprüft. Ergebnis: Die Kernzahlen (Destatis, ifo, BAFA, freelancermap) sind korrekt zitiert. Vier Punkte wurden ergänzt/korrigiert und sind im Dokument mit ⚠️ Audit Juli 2026 markiert: (1) BAFA-Interessenkonflikt-Klausel bei F10, (2) KMU-Zahlen-Divergenz bei F04, (3) neuere ifo-Zahl (54,5%) bei F06, (4) neuer Proxy P06 zum Freelancer-Marktrückgang 2026.

</aside>

| ID | Aussage | Kennzahl | Jahr | Primärquelle |
| --- | --- | --- | --- | --- |
| --- | --- | ---: | ---: | --- |
| M1 | KI-Nutzung in DE-Unternehmen (≥10 MA) | 26% gesamt; 23% (10–49); 36% (50–249) | 2025 | Destatis IKT-Erhebung |
| M2 | Top-Hemmnisse gegen KI | Wissen 72%; Recht 62%; Datenschutz 60% | 2025 | Destatis IKT-Erhebung |
| M4 | Geplante KI-Einführung (Pipeline) | 18,9% planen KI-Start | 2025 | ifo Institut |
| M5 | KMU-Marktgröße (DE) | 3,44 Mio. KMU | 2023 | IfM Bonn |
| M6 | Digitalisierungsausgaben Mittelstand | 31,9 Mrd. € | 2024 | KfW Research |
| M10 | BAFA-Beratungsförderung (KMU) | 50–80% bis 31.12.2026 | 2023–2026 | BAFA / Förderdatenbank |

**Hinweis Messdivergenz:** KI‑Nutzungsquoten variieren je nach Erhebung/Definition (Destatis vs. ifo vs. Eurostat). Im Businessplan gilt Destatis als amtliche Leitquelle; Vergleichswerte werden nur ergänzend verwendet.

## 5.2 Zielgruppe(n) / ICP (Startfokus)

**Arbeitsannahme (intern, zu validieren):** Startfokus auf KMU im Dienstleistungssektor mit 10–100 Mitarbeitenden, die KI‑Einsatz planen oder Hemmnisse „Wissen/Recht/Datenschutz“ haben.

**Segmentvorschlag (v1):**

1) Dienstleistungs‑KMU (Büro-/Backoffice‑Prozesse, Dokumente, E‑Mail‑Workflows)  

2) Handwerksbetriebe (Angebot/Auftrag/Rechnung/Kommunikation, Wissensmanagement)  

3) Bildungsträger / Schulungsanbieter (KI‑Literacy / EU AI Act Art. 4 Nachweise)

## 5.3 Use‑Cases (Problem → Lösung → Nutzen)

### UC1 – KI‑Einführungsberatung (KMU 10–30 MA)

- **Problem:** Kein KI‑Einsatz; Hemmnisse Wissen/Datenschutz/Recht dominieren (Destatis).
- **Lösung:** KI‑Readiness‑Check + Toolauswahl + Einstiegsschulung (½–1 Tag).
- **Nutzen:** schneller Start + Compliance‑fähige Schulungsdokumentation; KPI‑Schätzung als Annahme kennzeichnen.

### UC2 – Prozessautomatisierung (KMU 20–80 MA)

- **Problem:** Manuelle Workflows, Tool‑Brüche, keine interne KI‑Kapazität.
- **Lösung:** Workflow‑Analyse → Automatisierung (Make/n8n/Python) → Doku/Übergabe.
- **Nutzen:** Produktivitätsargument über ifo‑Erwartungswerte; projektspezifische KPI als Annahme.

### UC3 – KI‑Inhouse‑Schulung (EU AI Act Art. 4 Literacy)

- **Problem:** KI wird unstrukturiert genutzt (Shadow‑KI); nur Teil nutzt KI regelmäßig.
- **Lösung:** Schulung + Nachweise + Follow‑up‑Sprechstunde.
- **Nutzen:** KI‑Literacy und kontrollierte Einführung.

## 5.4 Wettbewerb & Preisanker (Kurz)

- **Wettbewerbertypen:** Systemhäuser/Consulting, Agenturen/Boutiquen, Solo‑Freelancer, Tool‑Alternativen, öffentliche Angebote (Mittelstand‑Digital).
- **Preisanker (prüfbar):** freelancermap (Ø ~103–104 €/h; Beratung/Management ~120 €/h). Anbieterpreislisten für Workshops nur als Sekundärquelle kennzeichnen.
- **Wettbewerberanzahl:** keine exakte Zahl seriös; nur Proxy‑Metriken (Plattform‑Zählung/Branchenproxy) und als Proxy deklarieren.

## 5.5 Evidence Pack (Single Source of Truth)

- Evidence Pack / Promptkette: [Prompt Marktfähigkeit](https://app.notion.com/p/Prompt-Marktf-higkeit-3870cb48a9548026aa32cbc0bdf25dc3?pvs=21)
- Beschaffungsplan (Anforderungen + Quellenplan): **siehe Attachment „Beschaffungsplan …“ im Thread**
- Faktenmatrix (auditierbar, 10 Fakten + Proxies + Preisanker): **siehe Attachment „Faktenmatrix …“ im Thread**
- Businessplan‑Textbaustein (aus Evidence Pack abgeleitet): **siehe Attachment „Businessplan …“ im Thread**