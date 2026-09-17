# 5. Unterseiten-Struktur (Beispiele + Aufgaben-IDs)

<aside>
🏷️

**Seiten-ID:** `section_unterseiten_beispiele`

</aside>

### Lesefassung (Kurz)

- Diese Seite zeigt die **Beispiel-Struktur** für Fachseiten.
- Pro Fachseite:
    - erst **Themenübersicht**,
    - dann pro Thema ein Block mit **Formel-Refs**,
    - darunter **Beispielaufgaben** (ohne Lösung), die auf Formeln verweisen.
- info_leseansicht_unterseiten ￨ Was du hier findest
    - id: info_leseansicht_unterseiten
    - Ein durchgängiges Muster für Seiten, Themen und Aufgaben
    - Beispiel „NTG – Physik“ inklusive 3 Themen + Aufgabenformat

---

- info_prinzip_unterseiten | Prinzip: Unterseiten-Struktur (Beispiele)
    - id: info_prinzip_unterseiten
    - Prinzip: Jede Fachseite enthält
        - Themenübersicht (topic_* IDs)
        - Themen-Blöcke (je Thema ein Toggle mit `info_*`)
        - Beispielaufgaben (task_ *IDs) mit `ref: formula_*`
- info_ntg_physik | NTG – Physik (Beispielstruktur)
    - id: page_fach_ntg_physik
    - info_fach_themen | Themen (IDs)
        - id: info_fach_themen
        - id: topic_kinematik | Kinematik: Bewegungslehre (s, v, t, a; freier Fall; Wurf)
        - id: topic_dynamik | Dynamik: Kräfte, Newton, Reibung, schiefe Ebene, Gleichgewicht
        - id: topic_erhaltung | Erhaltungssätze: Impuls, Energie, Stoßvorgänge
        - id: topic_kreis | Kreisbewegung: Zentripetalkraft, Kurvenfahrt
    - topic_gleichfoermige_bewegung | Thema: Gleichförmige Bewegung
        - id: topic_gleichfoermige_bewegung
        - formel_refs:
            - ref: formula_s_v_t
            - ref: formula_v_s_t
            - ref: formula_t_s_v
        - task_bewegung_1a | Beispielaufgabe (ohne Ergebnis)
            - id: task_bewegung_1a
            - Kontext: Gabelstapler fährt konstant durch eine Halle.
            - Gegeben: Geschwindigkeit (km/h), Strecke (m)
            - Gesucht: Zeit (s)
            - Rechenweg (Prosa):
                1. Umrechnen: km/h → m/s
                2. Formel wählen: `ref: formula_t_s_v`
                3. Werte einsetzen, Einheit prüfen
    - topic_beschleunigte_bewegung | Thema: Gleichmäßig beschleunigte Bewegung
        - id: topic_beschleunigte_bewegung
        - formel_refs:
            - ref: formula_v_at
            - ref: formula_s_1_2at2
            - ref: formula_v2_2as
            - ref: formula_v_v0_at
        - task_bewegung_2b | Beispielaufgabe (mittlerer Schwierigkeitsgrad)
            - id: task_bewegung_2b
            - Kontext: Förderband beschleunigt aus dem Stillstand.
            - Gegeben: Zielgeschwindigkeit, Beschleunigung
            - Gesucht: Zeit und Strecke
            - Rechenweg (Prosa):
                1. Zeit über `ref: formula_v_at` bestimmen
                2. Strecke über `ref: formula_s_1_2at2` bestimmen
                3. Plausibilität: Größenordnung prüfen
    - topic_freier_fall_wurf | Thema: Freier Fall und Wurf
        - id: topic_freier_fall_wurf
        - formel_refs:
            - ref: formula_fall_s_1_2gt2
            - ref: formula_fall_v_gt
            - ref: formula_fall_v2_2gh
            - ref: formula_waag_x_v0t
            - ref: formula_waag_y_1_2gt2
        - task_freier_fall_3b | Beispielaufgabe (ohne Zahlenlösung)
            - id: task_freier_fall_3b
            - Kontext: Werkzeug fällt von einer Höhe.
            - Gegeben: Fallhöhe, $g$
            - Gesucht: Fallzeit, Aufprallgeschwindigkeit, ggf. km/h
            - Rechenweg (Prosa):
                1. Fallzeit: `ref: formula_fall_s_1_2gt2` nach $t$ umstellen
                2. Geschwindigkeit: `ref: formula_fall_v_gt`
                3. Optional: Umrechnen m/s → km/h
    - id: info_ntg_physik
    - page-id: page_fach_ntg_physik
    - info_ntg_physik_themen | Themenübersicht
        - id: info_ntg_physik_themen
        - section-id: ntg_physik_themen
        - topic-id: topic_kinematik | Kinematik: Bewegungslehre (s, v, t, a; freier Fall; Wurf)
        - topic-id: topic_dynamik | Dynamik: Kräfte, Newton, Reibung, schiefe Ebene, Gleichgewicht
        - topic-id: topic_erhaltung | Erhaltungssätze: Impuls, Energie, Stoßvorgänge
        - topic-id: topic_kreis | Kreisbewegung: Zentripetalkraft, Kurvenfahrt
    - info_topic_gleichfoermig | Thema: Gleichförmige Bewegung
        - id: info_topic_gleichfoermig
        - topic-id: topic_gleichfoermige_bewegung
        - Formeln:
            - ref: formula_s_v_t
            - ref: formula_v_s_t
            - ref: formula_t_s_v
        - info_task_bewegung_1a | Aufgabe: Gabelstapler (Zeit berechnen)
            - id: info_task_bewegung_1a
            - task-id: task_bewegung_1a
            - Kontext: Gabelstapler fährt konstant durch eine Halle.
            - Gegeben: Geschwindigkeit (km/h), Strecke (m)
            - Gesucht: Zeit (s)
            - Rechenweg (Prosa):
                1. Umrechnen: km/h → m/s
                2. Formel wählen: `ref: formula_t_s_v`
                3. Werte einsetzen, Einheit prüfen
    - info_topic_beschleunigt | Thema: Gleichmäßig beschleunigte Bewegung
        - id: info_topic_beschleunigt
        - topic-id: topic_beschleunigte_bewegung
        - Formeln:
            - ref: formula_v_at
            - ref: formula_s_1_2at2
            - ref: formula_v2_2as
            - ref: formula_v_v0_at
        - info_task_bewegung_2b | Aufgabe: Förderband (Zeit & Strecke)
            - id: info_task_bewegung_2b
            - task-id: task_bewegung_2b
            - Kontext: Förderband beschleunigt aus dem Stillstand.
            - Gegeben: Zielgeschwindigkeit, Beschleunigung
            - Gesucht: Zeit und Strecke
            - Rechenweg (Prosa):
                1. Zeit über `ref: formula_v_at` bestimmen
                2. Strecke über `ref: formula_s_1_2at2` bestimmen
                3. Plausibilität: Größenordnung prüfen
    - info_topic_fall_wurf | Thema: Freier Fall & Wurf
        - id: info_topic_fall_wurf
        - topic-id: topic_freier_fall_wurf
        - Formeln:
            - ref: formula_fall_s_1_2gt2
            - ref: formula_fall_v_gt
            - ref: formula_fall_v2_2gh
            - ref: formula_waag_x_v0t
            - ref: formula_waag_y_1_2gt2
        - info_task_freier_fall_3b | Aufgabe: Fallhöhe (ohne Zahlenlösung)
            - id: info_task_freier_fall_3b
            - task-id: task_freier_fall_3b
            - Kontext: Werkzeug fällt von einer Höhe.
            - Gegeben: Fallhöhe, $g$
            - Gesucht: Fallzeit, Aufprallgeschwindigkeit, ggf. km/h
            - Rechenweg (Prosa):
                1. Fallzeit: `ref: formula_fall_s_1_2gt2` nach $t$ umstellen
                2. Geschwindigkeit: `ref: formula_fall_v_gt`
                3. Optional: Umrechnen m/s → km/h
- info_ntg_mathe | NTG – Mathematik (Themenliste)
    - id: info_ntg_mathe
    - page-id: page_fach_ntg_mathematik
    - topic-id: topic_bruch_prozent | Bruch- und Prozentrechnung
    - topic-id: topic_potenzen_wurzeln | Potenzen, Wurzeln, Formelumstellungen
    - topic-id: topic_gleichungen | Lineare und quadratische Gleichungen
    - topic-id: topic_statistik | Grundlagen Statistik (Mittelwert, Varianz, Häufigkeiten)
- info_basis_recht | Basisfach: Rechtsbewusstes Handeln (Themenliste)
    - id: page_fach_ntg_mathematik
    - id: topic_bruch_prozent | Bruch- und Prozentrechnung
    - id: topic_potenzen_wurzeln | Potenzen, Wurzeln, Formelumstellungen
    - id: topic_gleichungen | Lineare und quadratische Gleichungen
    - id: topic_statistik | Grundlagen Statistik (Mittelwert, Varianz, Häufigkeiten)
    - id: info_basis_recht
    - page-id: page_fach_recht
    - topic-id: topic_arbeitsrecht | Arbeitsrecht (Vertrag, Pflichten, Kündigung)
    - topic-id: topic_betriebsverfassung | Betriebsverfassungsrecht (Betriebsrat, Mitbestimmung)
    - topic-id: topic_sozialversicherung | Sozialversicherung (KV, RV, UV)
    - topic-id: topic_arbeitsschutz | Arbeitsschutzrecht
    - topic-id: topic_umweltrecht | Umweltrecht
- info_basis_bwl | Basisfach: Betriebswirtschaftliches Handeln (Themenliste)
    - id: page_fach_recht
    - id: topic_arbeitsrecht | Arbeitsrecht (Vertrag, Pflichten, Kündigung)
    - id: topic_betriebsverfassung | Betriebsverfassungsrecht (Betriebsrat, Mitbestimmung)
    - id: topic_sozialversicherung | Sozialversicherung (KV, RV, UV)
    - id: topic_arbeitsschutz | Arbeitsschutzrecht
    - id: topic_umweltrecht | Umweltrecht
    - id: info_basis_bwl
    - page-id: page_fach_bwl
    - topic-id: topic_vwl | Volkswirtschaftliche Grundlagen
    - topic-id: topic_orga | Aufbau- und Ablauforganisation
    - topic-id: topic_entgelt_kvp | Entgeltfindung, KVP
    - topic-id: topic_kostenrechnung | Kostenrechnung
- info_technik_faecher | Technik-Fächer (Themenliste)
    - id: page_fach_bwl
    - id: topic_vwl | Volkswirtschaftliche Grundlagen
    - id: topic_orga | Aufbau- und Ablauforganisation
    - id: topic_entgelt_kvp | Entgeltfindung, KVP
    - id: topic_kostenrechnung | Kostenrechnung (Karten/Träger/Rechnung)
    - id: info_technik_faecher
    - section-id: section_technik_faecher
    - info_betriebstechnik | Betriebstechnik
        - id: info_betriebstechnik
        - page-id: page_fach_betriebstechnik
        - topic-id: topic_maschinen | Kraft- und Arbeitsmaschinen
        - topic-id: topic_instandhaltung | Instandhaltung, Wartung, Inspektion
        - topic-id: topic_energie_medien | Energieversorgung & Medien
        - topic-id: topic_steuerung_regelung | Steuerungs- und Regelungstechnik (Grundlagen)
    - info_fertigungstechnik | Fertigungstechnik
        - id: info_fertigungstechnik
        - page-id: page_fach_fertigungstechnik
        - topic-id: topic_fertigungsverfahren | Spanen, Umformen, Fügen
        - topic-id: topic_cnc | CNC-Technik, numerische Steuerungen
        - topic-id: topic_automation | Automatisierungssysteme
    - info_montagetechnik | Montagetechnik
        - id: info_montagetechnik
        - page-id: page_fach_montagetechnik
        - topic-id: topic_montageplanung | Montageaufträge planen
        - topic-id: topic_montagesysteme | Automatisierte Montagesysteme
        - topic-id: topic_fmea | FMEA
- info_template_thema | Template: Themen-Block (copy/paste)
    - id: section_technik_faecher
    - page_fach_betriebstechnik | Betriebstechnik
        - id: page_fach_betriebstechnik
        - id: topic_maschinen | Kraft- und Arbeitsmaschinen
        - id: topic_instandhaltung | Instandhaltung, Wartung, Inspektion
        - id: topic_energie_medien | Energieversorgung & Medien (Strom, Druckluft, Hydraulik)
        - id: topic_steuerung_regelung | Steuerungs- und Regelungstechnik (Grundlagen)
    - page_fach_fertigungstechnik | Fertigungstechnik
        - id: page_fach_fertigungstechnik
        - id: topic_fertigungsverfahren | Spanen, Umformen, Fügen
        - id: topic_cnc | CNC-Technik, numerische Steuerungen
        - id: topic_automation | Automatisierungssysteme (Roboter, Transfersysteme)
    - page_fach_montagetechnik | Montagetechnik
        - id: page_fach_montagetechnik
        - id: topic_montageplanung | Montageaufträge planen
        - id: topic_montagesysteme | Automatisierte Montagesysteme
        - id: topic_fmea | FMEA (Fehler-Möglichkeits- und Einflussanalyse)
    - id: info_template_thema
    - info_template_topic_block | topic_* (mit Aufgaben)
        - id: info_template_topic_block
        - topic-id: topic_...
        - Formeln: ref: formula_...
        - info_template_task | task_* (Aufgabe)
            - id: info_template_task
            - task-id: task_...
            - Kontext:
            - Gegeben:
            - Gesucht:
            - Rechenweg (Prosa):