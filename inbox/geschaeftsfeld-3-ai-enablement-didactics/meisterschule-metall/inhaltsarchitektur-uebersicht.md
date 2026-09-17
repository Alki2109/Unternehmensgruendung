# Meisterschule Metall – Inhaltsarchitektur Website

<aside>
🧭

**Startseite (Wiki):** Von hier aus erreichst du alle Inhalte zur „Meisterschule Metall“.

**Leselogik:** Diese Seite ist die menschenlesbare Übersicht. Die „technischen“ Inhalte (IDs, Copy/Paste-Templates) bleiben darunter weiterhin als Toggles erhalten.

</aside>

### Schnellstart (für Menschen)

- **Ich will verstehen, was das ist:** [1. Startseite „Meisterschule Metall“](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/1%20Startseite%20%E2%80%9EMeisterschule%20Metall%E2%80%9C%20b7337d08b45d461d98245a930b87ded1.md)
- **Ich will Struktur & Rahmenbedingungen:** [2. Aufbau und Rahmenbedingungen](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/2%20Aufbau%20und%20Rahmenbedingungen%2061406f7e3c42433a8d921bb00818f844.md)
- **Ich will die Fächer/Module als Einstieg:** [3. Fachübersicht (Module)](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/3%20Fach%C3%BCbersicht%20(Module)%2070a7240cde954e269422789492789e06.md)
- **Ich will Formeln nachschlagen:** [4. Zentrale Formelsammlung (mit IDs)](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/4%20Zentrale%20Formelsammlung%20(mit%20IDs)%2032381164467080a69f1fd1e66ef3bc17.md)
- **Ich will sehen, wie Unterseiten/Themen/Aufgaben aufgebaut sind:** [5. Unterseiten-Struktur (Beispiele + Aufgaben-IDs)](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/5%20Unterseiten-Struktur%20(Beispiele%20+%20Aufgaben-IDs)%20dec9f3df36ff48ceaabdd54cdc22c66c.md)
- **Ich will die Datenlogik für Aufgaben/Lösungen:** [6. Struktur für Aufgaben & Musterlösungen (Datenbank-Logik)](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/6%20Struktur%20f%C3%BCr%20Aufgaben%20&%20Musterl%C3%B6sungen%20(Datenban%205d9bb9005ece4812aefab4c55d484213.md)
- **Ich will den Export/Druck verstehen:** [7. Export / Drucklogik (Aufgaben vs. Lösungen)](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/7%20Export%20Drucklogik%20(Aufgaben%20vs%20L%C3%B6sungen)%20cedcc43360ba4a179041e5b3044445d4.md)
- info_leseansicht_kurz  Kurzüberblick (menschenlesbar)
    - id: info_leseansicht_kurz
    - **Ziel:** Inhalte so strukturieren, dass sie gleichzeitig
        - als **Wiki** nutzbar sind,
        - als **Bausteine** wiederverwendet werden können,
        - und **exportfreundlich** (PDF) bleiben.
    - **Prinzip:** 1 Thema = 1 Seite (`topic_*`). Aufgaben referenzieren Formeln über `ref: formula_*`.
    - **Technik-Schicht:** Stabile IDs (`page_*`, `module_*`, `topic_*`, `task_*`, `formula_*`, `schema_*`) sorgen dafür, dass Verweise robust bleiben.

---

<aside>
✅

**So nutzt du das Wiki (Kurz):**

- 1 Thema = 1 Seite (mit `topic_*`)
- Aufgaben referenzieren Formeln über `ref: formula_*`
- Inhalte stehen in eigenständigen Toggles `info_*` (Copy/Paste-fähig)
</aside>

<aside>
🖨️

**Export-Fokus (PDF):**

- Formeln nur als Equation: $…$
- Lösungen über separate Blöcke/Seiten „ausblendbar“ halten
</aside>

## Navigation

- info_nav_unterseiten | Inhaltsarchitektur (Unterseiten)
    - id: info_nav_unterseiten
    - Orientierung: Nummerierung ist nur für Menschen; die stabilen IDs sind `page_*` / `section_*` / `topic_*` / …
    
    ---
    
    1. 
    
    [0. Meta / Root](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/0%20Meta%20Root%2082adf9c062c440989897b1699995ba25.md)
    
    1. 
    
    [1. Startseite „Meisterschule Metall“](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/1%20Startseite%20%E2%80%9EMeisterschule%20Metall%E2%80%9C%20b7337d08b45d461d98245a930b87ded1.md)
    
    1. 
    
    [2. Aufbau und Rahmenbedingungen](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/2%20Aufbau%20und%20Rahmenbedingungen%2061406f7e3c42433a8d921bb00818f844.md)
    
    1. 
    
    [3. Fachübersicht (Module)](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/3%20Fach%C3%BCbersicht%20(Module)%2070a7240cde954e269422789492789e06.md)
    
    1. 
    
    [4. Zentrale Formelsammlung (mit IDs)](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/4%20Zentrale%20Formelsammlung%20(mit%20IDs)%2032381164467080a69f1fd1e66ef3bc17.md)
    
    1. 
    
    [5. Unterseiten-Struktur (Beispiele + Aufgaben-IDs)](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/5%20Unterseiten-Struktur%20(Beispiele%20+%20Aufgaben-IDs)%20dec9f3df36ff48ceaabdd54cdc22c66c.md)
    
    1. 
    
    [6. Struktur für Aufgaben & Musterlösungen (Datenbank-Logik)](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/6%20Struktur%20f%C3%BCr%20Aufgaben%20&%20Musterl%C3%B6sungen%20(Datenban%205d9bb9005ece4812aefab4c55d484213.md)
    
    1. 
    
    [7. Export / Drucklogik (Aufgaben vs. Lösungen)](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/7%20Export%20Drucklogik%20(Aufgaben%20vs%20L%C3%B6sungen)%20cedcc43360ba4a179041e5b3044445d4.md)
    

## Standards (für Wiederverwendbarkeit)

- info_standards_bausteine | Bausteine, IDs, Referenzen
    - id: info_standards_bausteine
    - Jede Seite besteht aus einklappbaren Info-Blöcken (Toggles). Jeder Block ist autark.
    - Jeder Info-Block hat eine eindeutige Kennung `info_*` (in der Toggle-Überschrift) und beginnt innen mit `id:`.
    - Bestehende IDs bleiben erhalten: `page_*`, `section_*`, `module_*`, `hb_*`, `topic_*`, `task_*`, `formula_*`, `schema_*`.
    - Formeln: immer als LaTeX-Equation notieren (Notion-Math): $…$.
- info_workflow_referenzieren | Workflow: Referenzieren statt Kopieren
    - id: info_workflow_referenzieren
    - Aufgaben/Beispiele referenzieren Themen über `ref: topic_*`.
    - Aufgaben-Seiten referenzieren Formeln ausschließlich über `ref: formula_*`.
    - Text-Bausteine werden über eigene `info_*`-IDs referenziert (im Text z. B. `ref: info_*`).
- info_template_copy_paste | Template: Info-Block (copy/paste)
    - id: info_template_copy_paste
    - info_example_id | Beispiel-Blocktitel
        - id: info_example_id
        - Kontext:
        - Inhalt:
        - Verweise: ref: …

[NTG – Physik](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/NTG%20%E2%80%93%20Physik%2049ff5ae6da564383b93ff54a1f3eec5d.md)

[NTG – Mathematik](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/NTG%20%E2%80%93%20Mathematik%20ec8d448ffd1645fdace8642ba3d9cd9f.md)

[Rechtsbewusstes Handeln](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/Rechtsbewusstes%20Handeln%20f4ba29e4296b470d88af5d60ab626ad3.md)

[Betriebswirtschaftliches Handeln](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/Betriebswirtschaftliches%20Handeln%202af37818f3eb4e27b8e8c211ca621267.md)

[Betriebstechnik](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/Betriebstechnik%203ddb242244ee4053a7d00f73b736a207.md)

[Fertigungstechnik](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/Fertigungstechnik%20b56a2c703d9948a29f693858e52213e1.md)

[Montagetechnik](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/Montagetechnik%2014a5984a7d264d3e8fb43c70a4e8d6d9.md)

[OCR](Meisterschule%20Metall%20%E2%80%93%20Inhaltsarchitektur%20Website/OCR%20befdde207cb343f5994cc37921789c4a.md)