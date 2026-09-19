# Kapitel 3 – Finanzplan

<aside>
📌

Status: Updated (Finanzplan an Evidence Pack gekoppelt)

Zweck: Finanzplan-Logik + Verlinkung auf Bestandteile und Datenbank

KI-Referenz: KAPITEL-3-FINANZPLAN

</aside>

<aside>
🕒

**Erstelldatum (fix):** 27.05.2026, 16:11 (Europe/Berlin)

**Letzte Aktualisierung:** 19.09.2026 (Europe/Berlin)

</aside>

- Update-Historie (Evolution)
    
    
    | Zeitpunkt (TZ) | Änderung |
    | --- | --- |
    | 19.09.2026 (Europe/Berlin) | Link auf Kapitel 3a (Finanzplan-Szenarien mit 12-Monats-Grobgerüst) ergänzt |
    | 02.07.2026, 05:05 (Europe/Berlin) | Evidence-Input + Top-10 offene Finanz-Inputs ergänzt |
    | 17.06.2026, 17:47 (Europe/Berlin) | Draft-Stand (Hub/Verlinkung) |

## Inhalt

### Aktuelle Arbeitsfassung (Single Source of Truth)

- 📊 [Finanzplan V2 Current – Arbeitsfassung 25.05.2026](https://app.notion.com/p/Finanzplan-V2-Current-Arbeitsfassung-25-05-2026-36b0cb48a9548194b8fefc5f026832fa?pvs=21) (Kostenpositionen, Umsatzbausteine)
- 📊 [Kapitel 3a – Finanzplan-Szenarien (Rechenstand, inkl. 12-Monats-Grobgerüst)](Neural%20Automatix%20%E2%80%93%20Wissensbasis/Kapitel-3a-Finanzplan-Szenarien.md) — Kapitalbedarf, Umsatzszenarien, Liquiditätsverlauf und Break-Even über 12 Monate

### Evidence-Input (neu)

Der Finanzplan wird aus zwei Quellen gespeist:

1) **Belegte Marktdaten & Preisanker** (Evidence Pack) → als Plausibilisierung für Umsatz-/Preisannahmen.  

2) **Interne Annahmen** (Stundensatz, Auslastung, Akquise, KV/RV etc.) → explizit als *Annahme*.

**Promptkette / Evidence Pack:** [Prompt Marktfähigkeit](https://app.notion.com/p/Prompt-Marktf-higkeit-3870cb48a9548026aa32cbc0bdf25dc3?pvs=21)

### Offene Inputs (Top 10, für konsistente Zahlen)

*(Diese Liste stammt aus dem aktuellen Evidence Pack; Details siehe Attachments im Thread.)*

1. Finaler Stundensatz/Tagessatz (interne Entscheidung; plausibilisieren über freelancermap-Anker)  
2. Fakturierbare Stunden/Jahr (konservativ planen; Admin/Akquise/Urlaub abziehen)  
3. KV‑Beitrag/Monat (GKV Angebot einholen)  
4. RV/Altersvorsorge‑Beitrag/Monat (Optionen festlegen)  
5. Steuerlogik: Gewerbe vs. Freiberuf, USt‑Regime (mit Steuerberatung klären)  
6. BAFA‑Listung (ja/nein, Timing; falls genutzt als Vertriebshebel)  
7. Toolchain‑Kosten (Abos + API‑Kosten; Listenpreise belegen) – inkl. **LLM‑API‑Kosten, Research‑Tooling (z. B. Perplexity), ggf. Bild/Video‑Tools sowie Hardware‑/GPU‑Kosten**  
8. Akquise‑Kosten/Monat (intern schätzen; Kanäle definieren)  
9. Zahlungsziele & Zahlungseingangstiming (Liquidität)  
10. Break‑Even (Fixkosten ÷ Netto‑Stundensatz) + Puffer

### Struktur (Soll-Logik)

- Kapitalbedarf
- Rentabilität
- Liquidität
- Finanzierung

### Detailwerte / Rechenblöcke (DB-03)

Die Zahlenpflege liegt in der zentralen Datenbank (DB‑03) im Register:

- 🗂️ [‣](https://app.notion.com/p/5328e3aa60e841af8d7044f45a138f65?pvs=21) → DB‑03 Finanzplanung