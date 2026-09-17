# Erstellung einer Musterlösung mit Schritt für Schritt, Lösungsweg

<aside>
🧩

Diese Vorlage definiert den **Standard für Musterlösungen** aus OCR‑extrahierten Prüfungsaufgaben: nachvollziehbar, schrittweise, mit Einheiten-Check, Plausibilitätsprüfung, optionaler Skizze und einem konsistenten **Glossar/Begriffsmodell**.

</aside>

## 0) Metadaten (für Ablage/Export)

- Quelle (OCR-Dokument):
- Fach:
- Jahr/Saison:
- Aufgaben-ID (task_*):
- Thema (topic_*):
- Verwendete Formeln (ref: formula_*):
- Didaktik-Level: **D1 / D2 / D3**

## 1) Aufgabenstellung verstehen

- **Kurz paraphrasiert (1–2 Sätze):**
- **Was wird verlangt?** (z. B. „Berechne den Widerstand R“)
- **Wichtige Hinweise/Annahmen:** (z. B. konstante Temperatur, ohmscher Widerstand, Gleichstrom)

## 2) Gegeben / Gesucht (mit Einheiten)

- **Gegeben:**
    - $U = \dots\ \text{V}$
    - $I = \dots\ \text{A}$
    - …
- **Gesucht:**
    - $R = ?\ \Omega$

## 3) Passende Formel(n) auswählen

- **Formel:** Ohmsches Gesetz: $R = \frac{U}{I}$ (ref: formula_ohm_R_U_I)
- **Warum diese Formel passt:** (1 Satz)

## 4) Lösungsschritte (minutiös, nummeriert)

1. **Einheiten prüfen / umrechnen**
    - Prüfe: Volt (V), Ampere (A). Falls mA oder kV gegeben: in Basiseinheiten umrechnen.
2. **Werte einsetzen**
    - $R = \frac{U}{I}$
    - $R = \frac{\underline{\ \dots\ \text{V}\ }}{\underline{\ \dots\ \text{A}\ }}$
3. **Rechnen (sauberer Rechenweg)**
    - $R = \dots\ \Omega$
4. **Ergebnis formulieren (Satz + Einheit)**
    - Der Widerstand beträgt $R = dots Omega$.
5. **Plausibilitätscheck (1–2 kurze Checks)**
    - Größenordnung: Ist der Wert realistisch? (z. B. einige Ohm bis kΩ je nach Kontext)
    - Konsistenz: $\Omega = \frac{\text{V}}{\text{A}}$ erfüllt.

## 5) Ergebnis (kompakt)

- **Endergebnis:** $R = \dots\ \Omega$
- **Optional:** Rundung / signifikante Stellen / Toleranz:

## 6) Grafische Unterstützung (optional, wenn sinnvoll)

- **Skizze/Diagramm-Idee:** (z. B. einfacher Stromkreis mit Spannungsquelle + Widerstand)
- **Beschriftung:** $U$, $I$, $R$
- **Hinweis:** Symbole normgerecht (IEC/DIN), maßstäblich nur wenn erforderlich.

## 7) Didaktische Aufbereitung (D1/D2/D3)

### D1 (einfach, Kl. 7/8)

- Sprachlich vereinfachen, jeden Schritt begründen.
- Typische Stolperstellen: Einheiten, Division.

### D2 (mittel, FOS)

- Standardverfahren, Einheitencheck, kurze Begründung.

### D3 (prüfungsnah, Meister)

- Kompakt, formal, inkl. Plausibilitätsprüfung, ggf. Zusatzfragen/Transfer.

---

# Glossar & Begriffsmodell (für diese Seite / dieses Fach)

<aside>
📚

Ziel: Alle Fachbegriffe/Größen/Einheiten, die in Lösungen vorkommen, werden **einheitlich** erklärt und **in Beziehung** gesetzt. Das reduziert kognitive Last und erhöht Transfer.

</aside>

## A) Glossar (Kurzdefinitionen, 1–2 Sätze)

- **Spannung** $U$ **(Volt, V):** Elektrische Potentialdifferenz; „treibende Ursache“ für Stromfluss.
- **Stromstärke** $I$ **(Ampere, A):** Ladungsfluss pro Zeit; gibt an, wie viel elektrische Ladung pro Sekunde durch einen Leiterquerschnitt fließt.
- **Widerstand** $R$ **(Ohm, $Omega$):** Maß dafür, wie stark ein Bauteil den Stromfluss hemmt; abhängig von Material, Geometrie und Temperatur.
- **Leistung** $P$ **(Watt, W):** Umgesetzte Energie pro Zeit; beschreibt, wie schnell elektrische Energie in andere Energieformen (Wärme, Licht, Bewegung) umgewandelt wird.
- **Energie/Arbeit** $E$ **bzw.** $W$ **(Joule, J):** Umgesetzte Energiemenge.

## B) Einheiten-Zusammenhänge (Merksätze)

- $1\ \Omega = 1\ \frac{\text{V}}{\text{A}}$
- $1\ \text{W} = 1\ \text{V} \cdot 1\ \text{A}$
- $1\ \text{J} = 1\ \text{W} \cdot 1\ \text{s}$

## C) Begriffsmodell (Relationen als „Formel-Netz“)

- Ohmsches Gesetz:
    - $U = R \cdot I$
    - $I = \frac{U}{R}$
    - $R = \frac{U}{I}$
- Leistung in Gleichstromkreisen:
    - $P = U \cdot I$
    - (optional) kombiniert: $P = I^2 \cdot R$ und $P = \frac{U^2}{R}$

## D) Typische Fehlerquellen (für Lernende)

- Einheiten nicht umgerechnet (mA ↔ A, kV ↔ V).
- Formel falsch umgestellt.
- Ergebnis ohne Einheit oder mit falscher Einheit.
- Rundung zu früh (Zwischenergebnisse abschneiden).

## E) Mini-Beispiel (Ohmsches Gesetz: R aus U und I)

**Aufgabe:** Gegeben $U = 12\ \text{V}$ und $I = 2 text{A}$. Gesucht: $R$.

1. Gegeben/Gesucht notieren.
2. Formel wählen: $R = frac{U}{I}$.
3. Einsetzen: $R = frac{12 text{V}}{2 text{A}}$.
4. Rechnen: $R = 6 Omega$.
5. Check: $\Omega = \frac{\text{V}}{\text{A}}$ passt.