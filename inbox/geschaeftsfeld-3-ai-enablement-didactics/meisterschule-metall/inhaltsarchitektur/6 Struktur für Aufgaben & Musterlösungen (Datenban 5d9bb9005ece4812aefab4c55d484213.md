# 6. Struktur für Aufgaben & Musterlösungen (Datenbank-Logik)

<aside>
🏷️

**Seiten-ID:** `page_schema_aufgaben`

</aside>

### Lesefassung (Kurz)

- Diese Seite beschreibt, **wie Aufgaben, Rechenwege und Lösungen** strukturiert werden, damit du daraus später ein Aufgabenheft oder eine Datenbank machen kannst.
- Fokus ist: **klare Aufgabenstellung**, **reproduzierbarer Rechenweg**, **saubere Trennung** von Schüler- und Dozentensicht.

<aside>
✅

**Minimalstandard für jede Rechenaufgabe:**

- Kontext (1 Satz)
- Gegeben / Gesucht
- Formel-Refs (`ref: formula_*`)
- Rechenweg in Prosa (nummeriert)
- Ergebnis *optional* (je nach Sichtbarkeit)
</aside>

- info_leseansicht_schema ￨ Entscheidungslogik
    - id: info_leseansicht_schema
    - Aufgaben enthalten: Aufgaben-Text, ggf. Gegeben/Gesucht, Rechenweg in Prosa
    - Lösungen bleiben getrennt (Sichtbarkeit/Filter möglich)
    - Formeln werden nur referenziert (formula_*), nicht kopiert

---

<aside>
🗂️

**Zweck:** Konsistente Datenstruktur für Aufgaben, Lösungen und Referenzen (Formeln/Themen), damit sich Inhalte als Wiki, Druckansicht und später als Datenbank nutzen lassen.

</aside>

<aside>
🏷️

**Seiten-ID:** `page_schema_aufgaben`

</aside>

- info_schema_aufgabe | Schema: Aufgabe-Datensatz (Meta-Struktur)
    - id: schema_aufgabe
    
    <aside>
    🧾
    
    **Empfohlene Felder (DB):**
    
    - `id` (task_*)
    - `fach_id` (page_*)
    - `thema_id` (topic_*)
    - `schwierigkeitsgrad` (A/B/C)
    - `text_aufgabe` (ohne Lösung)
    - `gegeben` (optional, strukturiert)
    - `gesucht` (optional, strukturiert)
    - `schritte_prosa` (strukturierter Rechenweg)
    - `formel_refs` (Liste von formula_*)
    - `musterloesung_kurz` (dozent)
    - `musterloesung_ausfuehrlich` (dozent, optional)
    - `sichtbarkeit` (schueler/dozent)
    - `tags`
    </aside>
    
    - id: info_schema_aufgabe
    - schema-id: schema_aufgabe
    
    <aside>
    🗂️
    
    **Empfohlene Felder (DB):**
    
    - `id` (task_*)
    - `fach_id` (page_*)
    - `thema_id` (topic_*)
    - `schwierigkeitsgrad` (A/B/C)
    - `text_aufgabe` (ohne Lösung)
    - `schritte_prosa` (strukturierter Rechenweg)
    - `formel_refs` (Liste von formula_*)
    - `musterloesung_kurz` (optional, dozent/-in)
    - `tags`
    </aside>
    
- info_schema_formel_link | Verknüpfung: Aufgaben ↔ Formelsammlung
    - id: schema_formel_link
    - Jede Aufgabe enthält `formel_refs` = Liste von `formula_*` (nur Referenzen, keine Kopien).
    - Optional: Rückverlinkung über ein Feld `task_refs` auf der Formelseite (oder automatisiert über Relation, falls DB umgesetzt).
    - id: info_schema_formel_link
    - schema-id: schema_formel_link
    - Jede Aufgabe enthält `formel_refs` = Liste von `formula_*`.
    - Optional: Formelseite erhält je Formel ein Feld `task_refs` (Rückverlinkung).
- info_template_schema | Template: Schema-Block (copy/paste)
    - id: info_schema_export
    - Aufgabenheft: `text_aufgabe`, `gegeben`, `gesucht`, `schritte_prosa`
    - Lösungsskript: zusätzlich `musterloesung_*`
    - Formelsammlung: nur `formula_*`-Blöcke
    - id: info_template_schema
    - info_template_schema_entry | schema_* (Definition)
        - id: info_template_schema_entry
        - schema-id: schema_...
        - Zweck:
        - Felder:
        - Regeln/Validierung:
        - Beispiele/Refs: