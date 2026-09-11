# Agenda-PC-Session-Framework-Repo

Bereich: C-Betrieb
Schutzklasse: intern
Soll-Knoten: E-Agentic
Status: Draft

# Agenda – PC-Session Framework & Repo (Arbeitsablauf)

**Erstelldatum (fix):** 10.07.2026, 01:58 (Europe/Berlin)

**Letzte Aktualisierung:** 10.07.2026, 01:58 (Europe/Berlin)

**Status:** Draft

**Zweck:** Konkreter Arbeitsablauf für die heutige PC-Session mit je Was/Warum/Wie pro Schritt. Dient als abarbeitbare Agenda (nach Meetings-Regelwerk: Ziel, Ergebnistyp, Zeitbudget) und als Grundlage für das Protokoll am Ende.

**Fehlt (kurz):** Deine Anpassungen je Punkt (Reihenfolge, Zeitbudget, Streichungen) + Festlegung, ob Punkt 5 heute noch realistisch ist.

**KI-Referenz:** AGENDA-PC-SESSION-FRAMEWORK-REPO

Update-Historie (Evolution)

| Zeitpunkt (TZ) | Änderung |
| --- | --- |
| 10.07.2026, 01:58 (Europe/Berlin) | Initiale Agenda aus den gestern vereinbarten 5 Punkten + vorangestelltem Logging-Grundsatz |
| 10.07.2026, 02:00 (Europe/Berlin) | Pro Punkt eine allgemeinverständliche "Kurz erklärt"-Zeile (Sinn/Aufgabe/Nutzen) ergänzt |
| 10.07.2026, 02:00 (Europe/Berlin) | Punkt 6 (Begriffsmodell & semantische Klassifikation) ergänzt inkl. Eindeutigkeitspflicht, Grenzfall-Rücksprache, Abschlussbericht-Pflicht; NATS/JetStream als Erst-Einträge vorgemerkt |

Standard: siehe Dokumentations-Styleguide (Global) und Meetings-Regelwerk (Agenda-/Protokollpflicht).

Ziel der Session (1 Satz): Wissensstand ins Repo + Retrieval-Schicht steht, generisches Agent-Interface entworfen, sodass ab morgen eine erste einfache Pipeline mit vollständigem Event-Log laufen kann.

Navigation:

| Fachliche ID | Schritt | Ergebnistyp | Zeitbudget (Vorschlag) |
| --- | --- | --- | --- |
| AGD-0-LOGGING | Event-Logging-Grundsatz festlegen | Entscheidung | 20 min |
| AGD-1-TRENNUNG | Konzept/Domäne/Implementierung trennen | Entscheidung + Redaktion | 60 min |
| AGD-2-REPO | Repo-Commit vorbereiten | Artefakt | 45 min |
| AGD-3-RETRIEVAL | Retrieval-Schicht (Vektor+SQL) aufsetzen | Artefakt | 90 min |
| AGD-4-INTERFACE | Agent-Interface generisch designen | Artefakt | 60 min |
| AGD-5-PILOT | Einfaches Projekt starten | Test/Nachweis | offen |
| AGD-6-BEGRIFFE | Begriffsmodell & semantische Klassifikation | Artefakt + Abschlussbericht | offen |

## Punkt 0 – Event-Logging-Grundsatz

ID: AGD-0-LOGGING

**Kurz erklärt:** Ein Event-Log ist ein lückenloses Tagebuch des Systems — jede Aktion wird als Eintrag festgehalten. Sinn: Man kann jederzeit zurückverfolgen, was passiert ist, Fehler finden und das Geschehen später sichtbar machen (dein Digital Twin). Nutzen einer sauberen Umsetzung: belastbare Retrospektive und ein Nachweis, dass das Framework wirklich arbeitet.

**Was:** Vor allem anderen festlegen, dass jede Aktivität, jeder DB-Zugriff, jedes Event und jedes Artefakt geloggt wird (Event-Sourcing-Prinzip). Format und Speicherort (Log-File + DB + Archiv) bestimmen.

**Warum:** Das Log ist rückwirkend nicht rekonstruierbar — läuft es beim ersten Pilotlauf nicht mit, fehlen die Retrospektive-Daten für den Digital Twin und der Tragfähigkeitsnachweis. Muss daher vor Punkt 5 stehen.

**Wie:** Minimales Event-Schema definieren (Zeitstempel, Akteur/Rolle, Event-Typ, Referenz auf Artefakt/Block-ID, Payload/Status). Auf dem NATS/JetStream-Bus jeden Agenten so aufsetzen, dass er sein Event beim Entstehen schreibt. Für heute reicht ein einfacher, aber vollständiger Logger — Visualisierung kommt später als Ansicht darauf.

*Deine Anpassung:* …

## Punkt 1 – Konzept/Domäne/Implementierung trennen

ID: AGD-1-TRENNUNG

**Kurz erklärt:** Es geht darum, drei Arten von Inhalt auseinanderzuhalten — das Warum (Konzept), die fachlichen Regeln (Domäne) und die konkrete Umsetzung (Implementierung). Sinn: klare Struktur statt Vermischung. Nutzen: Die Suche findet gezielt das Richtige, weil ein Wissens-Häppchen genau eine Ebene enthält und nicht Konzept und Code durcheinanderwirft.

**Was:** Alle gestern/vorgestern erstellten Dokumente einmal durchgehen und je Baustein zuordnen: Konzept (das Warum/Modell), Domäne (fachliche Regeln), Implementierung (konkrete Umsetzung).

**Warum:** Du wolltest diese drei Ebenen sauber getrennt haben; aktuell sind sie teils vermischt. Nur sauber getrennte Dokumente gehen sauber ins Retrieval (ein Chunk = eine Ebene), sonst mischt die Vektorsuche Konzept und Implementierung.

**Wie:** Pro Dokument/Abschnitt ein Tag setzen (konzept | domäne | implementierung), konsistent mit dem Tagging-Modell des Styleguides. Wo ein Abschnitt zwei Ebenen mischt, trennen oder verlinken. Keine Vollüberarbeitung — Zuordnung und offensichtliche Trennschnitte reichen; Feinschliff später.

*Deine Anpassung:* …

## Punkt 2 – Repo-Commit vorbereiten

ID: AGD-2-REPO

**Kurz erklärt:** Ein Repository (GitHub) ist ein versionierter Speicher — es merkt sich jede Änderung und wer sie wann gemacht hat. Sinn: eine einzige verbindliche Quelle der Wahrheit für alle Dokumente. Nutzen: Von hier aus wird die Suchdatenbank gebaut; ohne diesen Schritt hat die spätere Retrieval-Schicht keine geordnete Grundlage.

**Was:** Den gesamten aktuellen Wissensstand (Gründungsdoku-Kapitel, Regelwerke, SD-Wissensbasis) commit-fähig ins GitHub-Repo bringen.

**Warum:** Das Repo ist die versionierte Single Source of Truth; erst von dort wird die Vektor-/SQL-DB gebildet. Solange die Dokumente nur lokal/in Notion liegen, kann das Retrieval nicht darauf aufbauen.

**Wie:** Dateien in die Repo-Struktur einsortieren (getrennte Repos Wissen/Code, wie geplant). Block-IDs gegen den zentralen Index prüfen (offener Punkt aus allen Kapiteln). Über deine Terminal-Instanz committen — ich bereite die Dateien vor, der Commit selbst läuft bei dir (ich habe keinen Repo-Zugriff).

*Deine Anpassung:* …

## Punkt 3 – Retrieval-Schicht aufsetzen

ID: AGD-3-RETRIEVAL

**Kurz erklärt:** Die Retrieval-Schicht ("retrieve" = heraussuchen) ist der Bibliothekar des Systems: Sie sucht bei jeder Frage nur die passenden Wissens-Häppchen heraus und gibt genau die an das KI-Modell — statt ganze Dokumente. Sinn: Das Modell liest nicht die ganze Aktenwand, sondern nur die drei relevanten Seiten. Nutzen: schneller, günstiger, präziser — das behebt direkt die Langsamkeit vom letzten Mal. Zwei Teile arbeiten zusammen: die Vektor-DB (findet inhaltlich Ähnliches) und die SQL-Schicht (filtert exakt, z. B. nur eine bestimmte Domäne).

**Was:** Vektor-DB (pgvector) + SQL-Schicht aufbauen und aus den Repo-Dokumenten befüllen (Chunking nach Block-IDs).

**Warum:** Das ist die Lösung für das Langsamkeitsproblem von letztem Mal — nur der relevante Chunk kommt in den Prompt, nicht das ganze Dokument. Ohne diese Schicht wiederholt sich die Verzögerung.

**Wie:** Chunking-Strategie aus dem Vektor-DB-Mapping-Konzept der SD-Wissensbasis übernehmen. Embeddings erzeugen, Block-ID als Metadatum je Chunk mitführen (für Rückverweis). Hybrid-Retrieval (SQL-Filter + Vektor-Ähnlichkeit) testen mit ein paar Beispiel-Queries: kommt der richtige Chunk zurück?

*Deine Anpassung:* …

## Punkt 4 – Agent-Interface generisch designen

ID: AGD-4-INTERFACE

**Kurz erklärt:** Ein Interface ist ein verbindlicher Bauplan/Vertrag: Er legt fest, welche Methoden jeder Agent haben muss, ohne vorzuschreiben, wie er sie intern löst. Sinn: Der Kern des Frameworks kennt nur den Vertrag, nicht die konkreten Agenten. Nutzen: Neue Agenten kann man später anstecken, ohne den Kern zu ändern — genau dein "nie erweitern müssen" (Open-Closed-Principle). Entspricht dem, was du aus C++ als abstrakte Basisklasse / aus Java als Interface kennst.

**Was:** Das abstrakte Agent-Interface entwerfen, von dem alle konkreten Agenten erben (Open-Closed-Principle).

**Warum:** Damit später neue Agenten hinzukommen, ohne den Framework-Kern zu ändern — genau dein „nie erweitern müssen". Der Kern erwartet den abstrakten Typ, konkrete Agenten implementieren die deklarierten Methoden.

**Wie:** Entscheidung ABC (`abc.ABC` + `@abstractmethod`, wie C++-Header) vs. `typing.Protocol` (strukturell, ohne Vererbungszwang) — an deinem konkreten Fall entscheiden. Pflichtmethoden deklarieren (z. B. `handle`, `capabilities`, Event-Schreiben aus Punkt 0). `mypy` als Vertrags-Prüfer einplanen, da Python die Verträge nicht erzwingt.

*Deine Anpassung:* …

## Punkt 5 – Einfaches Projekt starten

ID: AGD-5-PILOT

**Kurz erklärt:** Ein Pilot ist ein bewusst kleiner Testlauf, bevor man groß startet. Sinn: prüfen, ob die neuen Teile (Suche + Vertrag + Log) im Zusammenspiel funktionieren. Nutzen: Fehler zeigen sich an einem harmlosen Mini-Fall statt später im automatisierten Dauerbetrieb — ein Proof of Concept im Kleinen.

**Was:** Einen ersten, bewusst einfachen Pipeline-Lauf mit einem einzelnen Agenten gegen die neue Retrieval-Schicht — mit vollständigem Event-Log.

**Warum:** Proof of Concept im Kleinen: belegt, dass Retrieval + Interface + Logging zusammenspielen, bevor Multi-Agent und „Pipeline offen lassen" folgen.

**Wie:** Ein Mini-Projekt mit klarem, testbarem Ziel wählen. Erst ein Agent, nicht Multi-Agent. Prüfen: Kommt der richtige Chunk? Wird jedes Event geloggt? Ist das Ergebnis brauchbar? Realismus: Ob das heute noch drankommt, hängt an Punkt 3/4 — ggf. auf morgen schieben.

*Deine Anpassung:* …

## Punkt 6 – Begriffsmodell & semantische Klassifikation

ID: AGD-6-BEGRIFFE

**Kurz erklärt:** Ein Begriffsmodell ist ein zentrales Wörterbuch des Wissens — jeder Fachbegriff wird einmal sauber gefasst, mit erklärendem Text hinterlegt und mit anderen Begriffen in Beziehung gesetzt (Oberbegriff, Unterbegriff, verwandt, Synonym). Sinn: ein eindeutiger Begriff je Inhalt, keine Dubletten. Nutzen: Erst dadurch findet das System dokumentenübergreifend Ähnlichkeiten und Cross-Cutting Concerns und kann sie referenzieren — die Grundlage für Transferwissen (eine Erkenntnis aus einem Dokument taucht im passenden anderen Kontext wieder auf).

**Was:** Nach der Umstrukturierung (Punkt 1) das gesamte Dokumentenwerk systematisch durchlaufen, in jedem Teildokument die Begrifflichkeiten sauber ermitteln und ins gemeinsame Begriffsmodell übernehmen. Dabei semantische Beziehungen setzen (aufbauend auf dem bereits vorhandenen SKOS-basierten Glossar-/Konzeptmodell der SD-Wissensbasis).

**Warum:** Ohne eindeutige, verknüpfte Begriffe bleibt Wissen in Einzeldokumenten isoliert. Semantische Klassifikation ist die Voraussetzung dafür, dass die Retrieval-Schicht dokumentenübergreifend das Richtige findet und Zusammenhänge über Dokumentgrenzen hinweg sichtbar werden.

**Wie:**

- Jedes Teildokument durchgehen, Fachbegriffe extrahieren, in das zentrale Begriffsmodell überführen.
- Eindeutigkeitspflicht: Es darf nicht mehrere Begriffe für denselben Inhalt geben — ein Inhalt, ein Begriff. Synonyme nur als Alias am Hauptbegriff, nicht als eigener Eintrag.
- Beziehungen setzen (breiter/enger/verwandt/Synonym) nach SKOS-Logik.
- Grenzfall-Regel: Wo unklar ist, ob zwei Begriffe denselben Inhalt meinen, oder wo eine Begrifflichkeit nicht eindeutig erscheint, ist Rücksprache mit dir zu halten — nicht eigenmächtig zusammenführen.
- Pflicht zur Feststellung: Mehrdeutige oder doppelte Begriffe sind aktiv aufzuspüren, nicht nur beiläufig.
- Abschlussbericht: Am Ende ein Bericht, ob das Begriffsmodell aus meiner Sicht noch Schwächen hat und wo genau (offene Dubletten-Verdachtsfälle, unklare Begriffe, fehlende Beziehungen).

**Vorgemerkte Erst-Einträge fürs Begriffsmodell:**

- NATS – Nachrichten-Verteilsystem (Publish/Subscribe-Bus), über den Agenten lose gekoppelt kommunizieren, ohne sich direkt zu kennen.
- JetStream – speichernde Erweiterung von NATS: Nachrichten werden persistiert und sind erneut abspielbar; dient zugleich als Grundlage des Event-Logs (Verbindung zu Punkt 0).

*Deine Anpassung:* …