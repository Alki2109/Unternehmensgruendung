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
| 19.09.2026 (Europe/Berlin) | 12-Monats-Grobgerüst ergänzt (KAP3A-JAHRESUEBERSICHT-0001): Umsatzverlauf, Liquiditätsverlauf (kumuliert) und Kapitalbedarf je Szenario über volle Anlaufperiode statt nur der ersten 3 Monate |
| 07.07.2026, 15:32 (Europe/Berlin) | Initiale Szenariorechnung auf Basis der erhobenen Kosten- und Umsatzannahmen |

Standard: siehe Dokumentations-Styleguide (Global) – Regel-Template. Detailwerte gehören in DB-03 (Finanzplanung); dieses Kapitel ist der lesbare Rechenstand zu Kapitel 3.

Navigation:

| Fachliche ID | Titel/Label | Typ |
| --- | --- | --- |
| KAP3A-FIXK-0001 | Fixkosten (monatlich) | Kapitel |
| KAP3A-UMSATZ-0001 | Umsatz & Szenarien | Kapitel |
| KAP3A-BREAKEVEN-0001 | Break-Even & Deckung | Kapitel |
| KAP3A-KAPITAL-0001 | Kapitalbedarf & Anlauf | Kapitel |
| KAP3A-JAHRESUEBERSICHT-0001 | 12-Monats-Grobgerüst (Umsatz, Liquidität, Kapitalbedarf) | Kapitel |
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

## 12-Monats-Grobgerüst (Umsatz, Liquidität, Kapitalbedarf)

ID: KAP3A-JAHRESUEBERSICHT-0001

Erweiterung der obigen 3-Monats-Anlaufrechnung auf ein volles Geschäftsjahr. Fixkosten konstant mit 2.605 €/Monat angesetzt (Annahme; steigt real mit GKV-Einkommensabhängigkeit und Steuerlast, siehe Annahmen unten). Ramp-up Monat 1–3 wie oben (0/3/5 abrechenbare Tage im realistischen Szenario); ab Monat 4 wird die jeweilige Szenario-Auslastung (6/8/10 Tage/Monat) als Dauerzustand angenommen. Tagessatz konstant 800 €.

| Monat | Tage konserv. | Tage realist. | Tage optim. | Umsatz konserv. | Umsatz realist. | Umsatz optim. |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| 1 | 0 | 0 | 0 | 0 € | 0 € | 0 € |
| 2 | 2 | 3 | 4 | 1.600 € | 2.400 € | 3.200 € |
| 3 | 4 | 5 | 6 | 3.200 € | 4.000 € | 4.800 € |
| 4–12 (je Monat) | 6 | 8 | 10 | 4.800 € | 6.400 € | 8.000 € |

**Liquiditätsverlauf (kumulierter Saldo Umsatz − Fixkosten, vor Einkommensteuer):**

| Monat | kumuliert konserv. | kumuliert realist. | kumuliert optim. |
| --- | ---: | ---: | ---: |
| 1 | −2.605 € | −2.605 € | −2.605 € |
| 2 | −3.610 € | −2.810 € | −2.010 € |
| 3 | −3.015 € | −1.415 € | 185 € |
| 4 | −820 € | 2.380 € | 5.580 € |
| 5 | 1.375 € | 6.175 € | 10.975 € |
| 6 | 3.570 € | 9.970 € | 16.370 € |
| 7 | 5.765 € | 13.765 € | 21.765 € |
| 8 | 7.960 € | 17.560 € | 27.160 € |
| 9 | 10.155 € | 21.355 € | 32.555 € |
| 10 | 12.350 € | 25.150 € | 37.950 € |
| 11 | 14.545 € | 28.945 € | 43.345 € |
| 12 | 16.740 € | 32.740 € | 48.740 € |

**Break-Even-Lesart (Ergänzung zu KAP3A-BREAKEVEN-0001):**

- *Monatlicher* Break-Even (3,3 Tage/Monat) wird im konservativen wie im realistischen Szenario bereits ab Monat 3 laufend überschritten.
- *Kumulierter* Break-Even (Startkapitallücke ausgeglichen) wird konservativ in Monat 5, realistisch in Monat 4, optimistisch bereits in Monat 3 erreicht.

**Kapitalbedarf über die volle Anlaufphase (nicht nur Monat 1–3):** Maßgeblich ist die tiefste kumulierte Lücke im Jahresverlauf, nicht nur der 3-Monats-Wert. Diese liegt in allen drei Szenarien in Monat 2: konservativ **−3.610 €**, realistisch **−2.810 €**, optimistisch **−2.010 €**. Zusammen mit den Einmalkosten (1.530 €) ergibt sich ein Kapitalbedarf von **5.140 € (konservativ)** bis **3.540 € (optimistisch)**. Mit dem bereits ausgewiesenen 3-Monats-Liquiditätspuffer (7.815 €) bleibt die frühere Gesamt-Kapitalbedarfsgröße von **rund 12.000–13.000 €** als konservative Zielgröße bestehen.

Hinweis: Diese Jahresrechnung ist ein Grobgerüst auf Basis der bestehenden Annahmen (Tagessatz, Auslastungsstufen, konstante Fixkosten). Sie ersetzt keine Steuer-/Rechtsformberatung und keine reale GKV-/RV-Bestätigung (siehe Annahmen unten).

## Annahmen & offene Punkte

ID: KAP3A-ANNAHMEN-0001

- GKV 500 € ist Planannahme (einkommensabhängig; in der Niedrigphase eher weniger, mit steigendem Gewinn mehr). Echtes Kassenangebot einholen.
- RV (100 €, Mindestbeitrag) und ALV (95 €) sind Platzhalter; Regelbeitrag RV wäre deutlich höher (frei wählbar).
- Einkommensteuer je Szenario noch nicht gerechnet (Rechtsform/USt mit Steuerberatung klären).
- Auslastung 6/8/10 Tage ist eine Startannahme; freelancermap-Gespräche zur Nachfrageseite sollen sie belegen.
- Marktenge (ca. 150 vergleichbare Anbieter) stützt den USP, nicht die Nachfrage — Nachfragebelege separat führen.
- Website/Logo, Steuerberatung (ca. 50–150 €/Mon), Betriebshaftpflicht (ca. 100–300 €/Jahr) sind noch als real belegte Werte zu ergänzen.
- Kein Steuer-/Finanzberatungsersatz: verbindliche Zahlen über Steuerberatung, Kasse und Jobcenter.