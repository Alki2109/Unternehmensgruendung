# Schreib-und-Qualitaetsrichtlinie-G7

Bereich: A-Werkzeug/Bauplan
Schutzklasse: intern
Soll-Knoten: G-Governance
Status: Draft

# Schreib- & Qualitätsrichtlinie (G7)

**Erstelldatum (fix):** 10.07.2026, 05:28 (Europe/Berlin)

**Letzte Aktualisierung:** 10.07.2026, 05:28 (Europe/Berlin)

**Status:** Draft

**Zweck:** Verbindliche Richtlinie für Sprache, Aufbereitung und Prüfung aller wissenstragenden Dokumente. Legt fest, welches Sprachniveau je Dokumenttyp gilt, wie auf Korrektheit und Vollständigkeit geprüft wird und wie Inhalte am Ende ins Begriffsmodell überführt werden.

**Fehlt (kurz):** Verknüpfung mit realer Prüf-Checkliste je Dokumenttyp + Festlegung, wer (welche Agenten-Rolle) welche Prüfstufe ausführt + Abgleich mit dem Begriffsmodell, sobald dieses existiert.

**KI-Referenz:** RICHTLINIE-SCHREIBEN-QUALITAET

Update-Historie (Evolution)

| Zeitpunkt (TZ) | Änderung |
| --- | --- |
| 10.07.2026, 05:28 (Europe/Berlin) | Initiale Erstellung als Knoten G7 der Soll-Struktur |

Standard: siehe Dokumentations-Styleguide (Global). Diese Richtlinie ergänzt den Styleguide um Sprache und Qualität (der Styleguide regelt Struktur/IDs/Metadaten, diese Richtlinie regelt Wortwahl, Prüfung und Verständlichkeit). Verortet als G7 in der Soll-Struktur.

Navigation:

| Fachliche ID | Titel/Label | Typ |
| --- | --- | --- |
| RL-NIVEAU-0001 | Sprachniveau je Dokumenttyp | Kapitel |
| RL-FOERDER-0001 | Gutachterreife für förderrelevante Dokumente | Kapitel |
| RL-KOMPLEX-0001 | Gebotene Komplexität (keine unnötige Vereinfachung) | Kapitel |
| RL-PRUEF-0001 | Prüfung: Korrektheit & Vollständigkeit | Kapitel |
| RL-BEGRIFFE-0001 | Begriffsüberführung am Ende | Kapitel |
| RL-VERBOTEN-0001 | Sprachliche Fallstricke (nicht verwenden) | Kapitel |

## Sprachniveau je Dokumenttyp

ID: RL-NIVEAU-0001

Nicht jedes Dokument braucht dasselbe Register. Die Richtlinie unterscheidet drei Stufen:

- **Extern/gutachterreif** (Businessplan, Finanzplan, Marktanalyse, Förderanträge): professionell, präzise, sachlich, belegorientiert. So formuliert, dass eine Förderstelle, Bank oder ein Gutachter es ohne Rückfragen als seriös akzeptiert. Details siehe RL-FOERDER-0001.
- **Intern/fachlich** (Regelwerke, Architektur, Wissensbasis): fachlich vollständig, technisch korrekt, mit gebotener Komplexität (RL-KOMPLEX-0001). Keine Marketing-Sprache, keine Vereinfachung um der Zugänglichkeit willen.
- **Erklärend/didaktisch** (Onboarding, Übersichten, Agenda-Kurzerklärungen): allgemeinverständlich mit Alltagsbildern. Nur hier sind vereinfachende Analogien ausdrücklich erwünscht.

Regel: Der Dokumenttyp bestimmt die Stufe, nicht die Tagesform. Ein Dokument mischt die Stufen nicht wahllos; erklärende Einschübe in Fachdokumenten sind als solche erkennbar zu halten.

## Gutachterreife für förderrelevante Dokumente

ID: RL-FOERDER-0001

Für alle Dokumente, die einer externen Stelle vorgelegt werden, gilt:

- Klar, verständlich, auf die wesentlichen Ziele und Kennzahlen fokussiert.
- Belegorientiert: Aussagen mit Quelle/Datum (Evidence-Prinzip aus der bestehenden Faktenmatrix); Annahmen ausdrücklich als Annahme markieren.
- Ziel jeder förderrelevanten Aussage: die **Förderfähigkeit belastbar begründen** — nicht behaupten. Ein Gutachter muss die Förderfähigkeit attestieren können, weil die Argumentation trägt.
- Innovationsgehalt und technisches Risiko explizit herausstellen (2026 Fördervoraussetzung: reine API-Anbindung reicht nicht; echtes technisches Risiko muss erkennbar sein).
- Regulatorik sauber trennen: Der EU AI Act ist eine Pflicht/ein Geschäftsfeld, kein Fördertopf. Fördermittel laufen über eigene Programme (Einstiegsgeld §16b, Sachgüter §16c, BAFA, ZIM, KfW; EU-Ebene GenAI4EU/Horizon/EIC/DIGITAL, für Solo meist konsortialgebunden).
- Formalia mitdenken: Antrag vor Vorhabensbeginn; De-minimis-Grenze (300.000 €/3 Jahre); ggf. Pflicht-Informationsgespräch bei < 1 Jahr Marktbestand.

## Gebotene Komplexität (keine unnötige Vereinfachung)

ID: RL-KOMPLEX-0001

Fachdokumente werden mit der Komplexität geschrieben, die der Sache angemessen ist:

- Technische Details, Schwierigkeiten und Fachbegriffe werden ausgeführt, nicht weggekürzt.
- Didaktische Vereinfachung ist die Ausnahme, nicht die Regel — sie ist nur bei objektiv komplexen Sachverhalten zulässig, wo sie das Verständnis sichert.
- Fachbegriffe werden verwendet (nicht umschrieben), aber beim ersten Auftreten kurz definiert und ins Begriffsmodell überführt (RL-BEGRIFFE-0001).
- Ziel ist Präzision mit guter Erklärbarkeit — verständlich, ohne die fachliche Tiefe zu opfern.

## Prüfung: Korrektheit & Vollständigkeit

ID: RL-PRUEF-0001

Jedes Dokument durchläuft vor dem Status "Stable" eine Prüfung mit mindestens diesen Stufen:

- **Korrektheit:** Sind Fakten, Zahlen, Programm-/Gesetzesnamen und Quellen zutreffend und aktuell? (Beispiel-Lehre: "EU Innovation Act" existiert nicht als Fördertopf — solche Fehler sind aktiv zu finden.)
- **Vollständigkeit:** Sind alle für den Zweck nötigen Aspekte abgedeckt? Offene Punkte im "Fehlt (kurz)"-Feld benannt?
- **Erklärbarkeit:** Ist der Inhalt für den Zieltyp-Leser verständlich aufbereitet (nach RL-NIVEAU-0001)?
- **Konsistenz:** Widerspricht nichts anderen Dokumenten (Zahlen, Begriffe, Regeln)?
- **Mehrmodell-Gegenprüfung** (wo möglich): ein Modell erstellt, ein anderes prüft, Prüfbericht entsteht — konsistent mit dem Iterationsprinzip (Soll-Struktur E6).

Grundsatz: Bei Unsicherheit über einen Fakt wird er recherchiert oder als offen markiert — nie geraten. Falsche Sicherheit ist schädlicher als eine benannte Lücke.

## Begriffsüberführung am Ende

ID: RL-BEGRIFFE-0001

Nachdem die Umstrukturierung eines Bereichs abgeschlossen ist, werden dessen Inhalte durchlaufen, die Fachbegriffe extrahiert und ins zentrale Begriffsmodell überführt (siehe Soll-Struktur G6 / Agenda-Punkt 6):

- Ein Inhalt, ein eindeutiger Begriff; Synonyme nur als Alias.
- Semantische Beziehungen setzen (breiter/enger/verwandt) nach SKOS-Logik.
- Grenzfälle (unklar, ob zwei Begriffe dasselbe meinen) nicht eigenmächtig zusammenführen, sondern zur Klärung vorlegen.
- Abschlussbericht: aktive Feststellung und Benennung verbleibender Schwächen (Dubletten-Verdacht, unklare Begriffe, fehlende Beziehungen).

## Sprachliche Fallstricke (nicht verwenden)

ID: RL-VERBOTEN-0001

In gutachterreifen/förderrelevanten Dokumenten zu vermeiden:

- "Fördertöpfe abgreifen/abschöpfen" → klingt nach Mitnahmeeffekt. Stattdessen: "Kofinanzierung eines Vorhabens mit erkennbarem Innovationsgehalt und technischem Risiko".
- Werbe-/Dringlichkeitsrhetorik ("historische Chance", "jetzt handeln") → gehört nicht in einen sachlichen Businessplan.
- Unbelegte Superlative ("marktführend", "einzigartig") ohne Nachweis.
- Programm-/Gesetzesnamen aus dem Gedächtnis oder aus Werbemails übernehmen → immer gegen die offizielle Quelle prüfen.
- KI-generierte Inhalte für Außenauftritt ohne Kennzeichnung (Transparenzpflicht ab 08/2026).