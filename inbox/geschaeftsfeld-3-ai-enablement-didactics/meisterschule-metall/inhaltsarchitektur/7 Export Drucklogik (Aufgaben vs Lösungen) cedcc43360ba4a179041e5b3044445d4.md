# 7. Export / Drucklogik (Aufgaben vs. Lösungen)

<aside>
🏷️

**Seiten-ID:** `page_export_logik`

</aside>

### Lesefassung (Kurz)

- Ziel ist ein **sauberer Export** (PDF), ohne doppelte Inhalte.
- Grundidee: **Aufgaben**, **Lösungen** und **Formelsammlung** sind getrennt, damit du je nach Zielgruppe das Richtige ausgeben kannst.

<aside>
🖨️

**3 Export-Typen (praktisch):**

- **Aufgabenheft:** Aufgaben + Rechenweg (ohne Ergebnis)
- **Lösungsskript:** zusätzlich Ergebnisse + Hinweise
- **Formelheft:** nur Formeln (als Anhang oder separat)
</aside>

- info_leseansicht_export ￨ Typische Exporte
    - id: info_leseansicht_export
    - Aufgabenheft: nur Aufgaben + Rechenweg (ohne Ergebnis)
    - Lösungsskript: zusätzlich Musterlösungen, Ergebnisse, Hinweise
    - Formelsammlung: separat oder als Anhang

---

<aside>
🖨️

**Ziel:** Ein konsistenter PDF-Export (Aufgabenheft / Lösungsskript / Formelsammlung), ohne doppelte Inhalte.

</aside>

<aside>
🏷️

**Seiten-ID:** `page_export_logik`

</aside>

- info_export_prinzip | Prinzip: Aufgaben vs. Lösungen trennen
    - id: info_export_loesungsskript
    - Inhalt:
        - Musterlösungen (kurz + ggf. ausführlich)
        - Ergebniswerte und Einheiten
        - Hinweise/Fehlerquellen
    - Empfehlung:
        - Lösungen als eigene Toggles halten (ein-/ausblendbar)
        - Optional: separate Lösungs-Unterseite pro Themenblock
    - id: info_export_prinzip
    - Frontseite: Aufgaben ohne Ergebnis, mit Rechenweg in Prosa.
    - Rückseite/Anhang: Musterlösungen (ein-/ausblendbar).
    - Formelsammlung: separat druckbar oder als Anhang.
- info_export_sichtbarkeit | Sichtbarkeit/Filter (Schüler vs. Dozent)
    - id: info_export_formelsammlung
    - Optionen:
        - separat als „Formelheft“ exportieren
        - oder als Anhang ans Aufgabenheft (wenn gewünscht)
    - Format:
        - jede Formel als Equation $…$
        - pro Formel eine `formula_*`-ID
    - id: info_export_sichtbarkeit
    
    <aside>
    🖨️
    
    **Hinweis:** Die Trennung „Schüler/Dozent“ lässt sich über ein Feld `sichtbarkeit` (z. B. `schueler` / `dozent`) und entsprechende Filter/Ansichten lösen.
    
    </aside>
    
    - Empfehlung: In der Aufgaben-DB zwei Ansichten anlegen:
        - „Schülerdruck“: Filter `sichtbarkeit = schueler`
        - „Dozent“: Filter `sichtbarkeit in (schueler, dozent)`
- info_export_sichtbarkeit | Sichtbarkeit/Filter-Logik (DB oder manuell)
    - id: info_export_sichtbarkeit
    - Trennung „Schüler/Dozent“ lässt sich sauber über ein Feld `sichtbarkeit` (z. B. `schueler` / `dozent`) lösen.
    - Wenn später eine Aufgaben-Datenbank genutzt wird:
        - Views: „Aufgaben (schueler)“, „Lösungen (dozent)", „Druck: Aufgaben", „Druck: Lösungen"
- info_template_export_block | Template: Export-Regel (copy/paste)
    - id: info_template_export_block
    - info_template_export_rule | Regel
        - id: info_template_export_rule
        - Kontext (wo gilt es?):
        - Regel:
        - Umsetzung (DB/View/Seite):