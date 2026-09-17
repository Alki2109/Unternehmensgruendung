# 4. Zentrale Formelsammlung (mit IDs)

<aside>
🏷️

**Seiten-ID:** `page_formelsammlung`

</aside>

### Lesefassung (Kurz)

- Diese Seite ist dein **Formel-Nachschlagewerk**.
- Jede Formel steht als **Equation** und hat eine **stabile ID** (`formula_*`).

<aside>
🧮

**Wie du mit Formeln arbeitest (prüfungsnah):**

1. **Größen klären:** Was ist gegeben, was wird gesucht?
2. **Einheiten prüfen:** km/h → m/s, kJ → J, …
3. **Formel wählen:** passende `formula_*`.
4. **Umstellen** (falls nötig) und **einsetzen**.
5. **Plausibilität**: Größenordnung, Einheiten, Vorzeichen.
</aside>

- info_leseansicht_formeln ￨ Nutzung in der Praxis
    - id: info_leseansicht_formeln
    - Beim Lernen: Themenbereich öffnen und Formeln vergleichen.
    - Beim Aufgabenbauen: Formel-ID notieren (z. B. `ref: formula_v_s_t`).
    - Beim Export: Formeln bleiben „sauber“, weil nichts dupliziert wird.

---

<aside>
📌

**Nutzung:** In Aufgaben/Unterseiten Formeln nie „abschreiben“, sondern über `ref: formula_*` referenzieren (z. B. `ref: formula_v_s_t`).

</aside>

- info_formeln_kinematik | Kinematik – Bewegungslehre
    - id: info_formeln_kinematik
    - section-id: formulas_kinematik
    - info_formeln_kinematik_gleichfoermig | Gleichförmige Bewegung
        - id: info_formeln_kinematik_gleichfoermig
        - section-id: formulas_kinematik_gleichfoermig
        - formula-id: formula_s_v_t
            
            $s = v \cdot t$
            
        - formula-id: formula_v_s_t
            
            $v = \frac{s}{t}$
            
        - formula-id: formula_t_s_v
            
            $t = \frac{s}{v}$
            
    - info_formeln_kinematik_beschleunigt | Gleichmäßig beschleunigte Bewegung (Start aus Ruhe)
        - id: info_formeln_kinematik_beschleunigt
        - section-id: formulas_kinematik_beschleunigt
        - Hinweis: Start aus Ruhe: $v_0 = 0$
        - formula-id: formula_s_1_2at2
            
            $s = \frac{1}{2} \cdot a \cdot t^2$
            
        - formula-id: formula_v_at
            
            $v = a \cdot t$
            
        - formula-id: formula_v2_2as
            
            $v^2 = 2 \cdot a \cdot s$
            
    - info_formeln_kinematik_allgemein | Allgemeiner Start mit Anfangsgeschwindigkeit $v_0$
        - id: info_formeln_kinematik_allgemein
        - section-id: formulas_kinematik_allgemein
        - formula-id: formula_s_v0_t_1_2at2
            
            $s = v_0 \cdot t + \frac{1}{2} \cdot a \cdot t^2$
            
        - formula-id: formula_v_v0_at
            
            $v = v_0 + a \cdot t$
            
        - formula-id: formula_a_v_v0_t
            
            $a = \frac{v - v_0}{t}$
            
    - info_formeln_freier_fall | Freier Fall (ohne Luftwiderstand)
        - id: info_formeln_freier_fall
        - section-id: formulas_kinematik_freier_fall
        - formula-id: formula_fall_s_1_2gt2
            
            $s = \frac{1}{2} \cdot g \cdot t^2$
            
        - formula-id: formula_fall_v_gt
            
            $v = g \cdot t$
            
        - formula-id: formula_fall_v2_2gh
            
            $v^2 = 2 \cdot g \cdot h$
            
    - info_formeln_waag_wurf | Waagerechter Wurf
        - id: info_formeln_waag_wurf
        - section-id: formulas_kinematik_waagerechter_wurf
        - formula-id: formula_waag_x_v0t
            
            $x = v_0 \cdot t$
            
        - formula-id: formula_waag_y_1_2gt2
            
            $y = \frac{1}{2} \cdot g \cdot t^2$
            
        - formula-id: formula_waag_v_sqrt
            
            $v = \sqrt{v_0^2 + (g \cdot t)^2}$
            
- info_formeln_kraefte_energie | Kräfte, Hebel, Impuls, Energie
    - id: info_formeln_kraefte_energie
    - section-id: formulas_kraefte_impuls_energie
    - info_formeln_kraefte | Kräfte
        - id: info_formeln_kraefte
        - section-id: formulas_kraefte
        - formula-id: formula_F_ma
            
            $F = m \cdot a$
            
        - formula-id: formula_Fg_mg
            
            $F_G = m \cdot g$
            
    - info_formeln_reibung | Reibung (Gleitreibung)
        - id: info_formeln_reibung
        - section-id: formulas_reibung
        - formula-id: formula_Fr_muFn
            
            $F_R = \mu \cdot F_N$
            
    - info_formeln_schiefe_ebene | Schiefe Ebene
        - id: info_formeln_schiefe_ebene
        - section-id: formulas_schiefe_ebene
        - formula-id: formula_FH_Fg_sin
            
            $F_H = F_G \cdot \sin(\alpha)$
            
        - formula-id: formula_FN_Fg_cos
            
            $F_N = F_G \cdot \cos(\alpha)$
            
    - info_formeln_hebel_moment | Hebel & Moment
        - id: info_formeln_hebel_moment
        - section-id: formulas_hebel_moment
        - formula-id: formula_hebel_F1l1_F2l2
            
            $F_1 \cdot l_1 = F_2 \cdot l_2$
            
        - formula-id: formula_moment_Fl
            
            $M = F \cdot l$
            
    - info_formeln_impuls | Impuls
        - id: info_formeln_impuls
        - section-id: formulas_impuls
        - formula-id: formula_p_mv
            
            $p = m \cdot v$
            
        - formula-id: formula_impuls_erhaltung_1d
            
            $m_1 v_1 + m_2 v_2 = m_1 v'_1 + m_2 v'_2$
            
        - formula-id: formula_unelast_v_strich
            
            $v' = \frac{m_1 v_1 + m_2 v_2}{m_1 + m_2}$
            
    - info_formeln_energie | Energie, Arbeit, Leistung
        - id: info_formeln_energie
        - section-id: formulas_energie
        - formula-id: formula_Ekin_1_2mv2
            
            $E_{\\text{kin}} = \frac{1}{2} \cdot m \cdot v^2$
            
        - formula-id: formula_Epot_mgh
            
            $E_{\\text{pot}} = m \cdot g \cdot h$
            
        - formula-id: formula_W_Fs_cos
            
            $W = F \cdot s \cdot \cos(\alpha)$
            
        - formula-id: formula_P_W_t
            
            $P = \frac{W}{t}$
            
    - info_formeln_kreisbewegung | Kreisbewegung
        - id: info_formeln_kreisbewegung
        - section-id: formulas_kreisbewegung
        - formula-id: formula_Fz_mv2r
            
            $F_Z = \frac{m \cdot v^2}{r}$
            
- info_formeln_vektoren | Vektoren und Kräftezerlegung
    - id: info_formeln_vektoren
    - section-id: formulas_vektoren_kraeftezerlegung
    - formula-id: formula_Fres_allgemein
        
        $F_{\\text{res}} = \sqrt{F_1^2 + F_2^2 + 2 F_1 F_2 \cos(\alpha)}$
        
    - formula-id: formula_Fx_Fcos
        
        $F_x = F \cdot \cos(\alpha)$
        
    - formula-id: formula_Fy_Fsin
        
        $F_y = F \cdot \sin(\alpha)$
        
- info_template_formel | Template: Formel-Eintrag (copy/paste)
    - id: info_template_formel
    - info_template_formel_entry | formula_* (mit Kontext)
        - id: info_template_formel_entry
        - formula-id: formula_...
        - Bedeutung (kurz):
        - Variablen:
            - $x$ = …
        - Formel:
            
            $...$
            
        - Verweise: ref: topic_... / task_...