# Kapitel-3a-Finanzplan-Szenarien

Bereich: B-Wissen
Schutzklasse: vertraulich
Soll-Knoten: A-Gründung
Status: Draft

# Kapitel 3a – Finanzplan-Szenarien (Rechenstand)

**Erstelldatum (fix):** 07.07.2026, 15:32 (Europe/Berlin)

**Letzte Aktualisierung:** 07.07.2026, 15:32 (Europe/Berlin)

**Status:** Draft

**Zweck:** Durchgerechneter Szenariostand (konservativ/realistisch/optimistisch) für Kapitel 3 (Finanzplan): Fixkosten, Umsatz, Break-Even, Deckung und Kapitalbedarf. Dient als Tragfähigkeitsnachweis für IHK und Jobcenter (Einstiegsgeld).

**Fehlt (kurz):** Einkommensteuer-Last je Szenario (Rechtsform/USt mit Steuerberatung) + echtes GKV-Angebot + finale RV/ALV-Beträge + freelancermap-Nachfragebelege + Website/Steuerberatung/Betriebshaftpflicht als reale Werte statt Annahmen.

**KI-Referenz:** KAPITEL-3A-FINANZPLAN-SZENARIEN

Update-Historie (Evolution)

| Zeitpunkt (TZ) | Änderung |
| --- | --- |
| 07.07.2026, 15:32 (Europe/Berlin) | Initiale Szenariorechnung auf Basis der erhobenen Kosten- und Umsatzannahmen |

Standard: siehe Dokumentations-Styleguide (Global) – Regel-Template. Detailwerte gehören in DB-03 (Finanzplanung); dieses Kapitel ist der lesbare Rechenstand zu Kapitel 3.

Navigation:

| Fachliche ID | Titel/Label | Typ |
| --- | --- | --- |
| KAP3A-FIXK-0001 | Fixkosten (monatlich) | Kapitel |
| KAP3A-UMSATZ-0001 | Umsatz & Szenarien | Kapitel |
| KAP3A-BREAKEVEN-0001 | Break-Even & Deckung | Kapitel |
| KAP3A-KAPITAL-0001 | Kapitalbedarf & Anlauf | Kapitel |
| KAP3A-ANNAHMEN-0001 | Annahmen & offene Punkte | Kapitel |

## Fixkosten (monatlich)

ID: KAP3A-FIXK-0001

| Block | Positionen | Summe/Monat |
| --- | --- | --- |
| Privat (Lebenshaltung) | Miete 500, Nebenkosten 200, Internet 60, Telefonie 40, Lebensmittel 450, Auto laufend 100 | 1.350 € |
| Vorsorge/Versicherung | GKV 500 (Planannahme), BU+Spar 300, RV freiwillig 100 (Mindest, Platzhalter), ALV freiwillig 95 (Platzhalter) | 995 € |
| Betrieb (Tools/API) | Perplexity 20, Claude 20, Hugging Face 20, GitHub 0, freelancermap Pro 120, KI-API/Token-Puffer 80 | 260 € |
| **Fixkosten gesamt** |  | **2.605 €** |

Hinweis: Die KI-API-/Token-Kosten sind variabel und steigen, sobald die Produktions-Pipeline mehr läuft. Der Puffer (80 €) ist eine vorsichtige Startannahme, keine belegte Zahl.

## Umsatz & Szenarien

ID: KAP3A-UMSATZ-0001

Annahmen: Stundensatz ~100 € (Spanne 80–120 €), 8-Stunden-Tag → Tagessatz 800 €. Abrechenbare Tage/Monat in der Startphase konservativ angesetzt (nicht jeder Kundentag ist abrechenbar; Akquise/Admin/Fahrten sind unbezahlt).

| Szenario | Abrechenbare Tage/Mon | Umsatz/Mon | Umsatz/Jahr |
| --- | --- | --- | --- |
| konservativ | 6 | 4.800 € | 57.600 € |
| realistisch | 8 | 6.400 € | 76.800 € |
| optimistisch | 10 | 8.000 € | 96.000 € |

## Break-Even & Deckung

ID: KAP3A-BREAKEVEN-0001

Break-Even = Fixkosten ÷ Tagessatz = 2.605 € ÷ 800 € ≈ **3,3 abrechenbare Tage/Monat**. Ab dieser Auslastung sind die laufenden Kosten gedeckt.

| Szenario | Umsatz/Mon | Fixkosten/Mon | Rest vor Einkommensteuer |
| --- | --- | --- | --- |
| konservativ | 4.800 € | 2.605 € | 2.195 € |
| realistisch | 6.400 € | 2.605 € | 3.795 € |
| optimistisch | 8.000 € | 2.605 € | 5.395 € |

Wichtig: „Rest vor Einkommensteuer" ist noch **kein** verfügbarer Gewinn. Einkommensteuer (und je nach Regime Gewerbesteuer/USt-Abführung) ist abzuziehen; die genaue Last hängt an Rechtsform und USt-Entscheidung (offener Punkt).

Aussage für die Tragfähigkeit: Bereits das konservative Szenario liegt mit 6 Tagen fast beim Doppelten des Break-Even (3,3 Tage). Das Vorhaben ist rechnerisch tragfähig.

## Kapitalbedarf & Anlauf

ID: KAP3A-KAPITAL-0001

Einmalkosten Start: Laptop 1.500 €, Website/Logo 0 € (Eigenleistung), Gewerbeanmeldung ca. 30 € → **1.530 €**.

Anlaufannahme (konservativ, 3 Monate Ramp-up): Monat 1 = 0 abrechenbare Tage, Monat 2 = 3 Tage, Monat 3 = 5 Tage.

| Monat | Umsatz | Fixkosten | Saldo |
| --- | --- | --- | --- |
| 1 | 0 € | 2.605 € | −2.605 € |
| 2 | 2.400 € | 2.605 € | −205 € |
| 3 | 4.000 € | 2.605 € | +1.395 € |

Kumulierte Deckungslücke Anlauf: ~2.810 €. Kapitalbedarf ohne Puffer = 1.530 € + 2.810 € ≈ **4.340 €**. Mit 3-Monats-Liquiditätspuffer (3 × 2.605 €) ≈ **12.155 €**.

Deckung des Kapitalbedarfs: Erspartes (Vorlage vorhanden) + Einstiegsgeld (§ 16b) + ggf. Sachgüter-Zuschuss (§ 16c) für den Laptop. Das Auto ist bewusst nicht enthalten (nur bei Förderkredit, unabhängig von der Gründungsentscheidung).

## Annahmen & offene Punkte

ID: KAP3A-ANNAHMEN-0001

- GKV 500 € ist Planannahme (einkommensabhängig; in der Niedrigphase eher weniger, mit steigendem Gewinn mehr). Echtes Kassenangebot einholen.
- RV (100 €, Mindestbeitrag) und ALV (95 €) sind Platzhalter; Regelbeitrag RV wäre deutlich höher (frei wählbar).
- Einkommensteuer je Szenario noch nicht gerechnet (Rechtsform/USt mit Steuerberatung klären).
- Auslastung 6/8/10 Tage ist eine Startannahme; freelancermap-Gespräche zur Nachfrageseite sollen sie belegen.
- Marktenge (ca. 150 vergleichbare Anbieter) stützt den USP, nicht die Nachfrage — Nachfragebelege separat führen.
- Website/Logo, Steuerberatung (ca. 50–150 €/Mon), Betriebshaftpflicht (ca. 100–300 €/Jahr) sind noch als real belegte Werte zu ergänzen.
- Kein Steuer-/Finanzberatungsersatz: verbindliche Zahlen über Steuerberatung, Kasse und Jobcenter.