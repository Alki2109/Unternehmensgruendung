# Wissens-Pipeline-Repo-zu-DB

Bereich: A-Werkzeug/Bauplan
Schutzklasse: intern
Soll-Knoten: F-Wissen
Status: Draft

# Wissens-Pipeline: Vom Repo zur DB (Aufbereitung & Befüllung)

**Erstelldatum (fix):** 10.07.2026, 05:28 (Europe/Berlin)

**Letzte Aktualisierung:** 10.07.2026, 05:28 (Europe/Berlin)

**Status:** Draft

**Zweck:** Verbindliches Ablaufkonzept, wie Inhalte aus dem GitHub-Repo (SSOT) über Obsidian aufbereitet, per Template geprüft, getaggt und schließlich in SQL- und Vektor-DB überführt werden — in einer Reihenfolge, die Re-Embedding und uneindeutiges Tagging vermeidet.

**Fehlt (kurz):** Reale Wahl Embedding-Modell + finale Chunk-Zielgröße (empirisch, Mess-Beispiel) + Umfang des Erst-Begriffsmodells vor dem ersten Tagging-Lauf.

**KI-Referenz:** WISSENS-PIPELINE-REPO-ZU-DB

Update-Historie (Evolution)

| Zeitpunkt (TZ) | Änderung |
| --- | --- |
| 10.07.2026, 05:28 (Europe/Berlin) | Initiales Pipeline-Konzept; Begriffsmodell-first-Tagging, Obsidian als Repo-Ansicht |

Standard: siehe Dokumentations-Styleguide (Global), Soll-Struktur (F Wissensmanagement) und Konsolidierungs-Konzeption. Baut auf dem konsolidierten Repo-Stand auf.

Navigation:

| Fachliche ID | Titel/Label | Typ |
| --- | --- | --- |
| PIPE-OBSIDIAN-0001 | Obsidian als lebende Repo-Ansicht | Kapitel |
| PIPE-REIHENFOLGE-0001 | Verbindliche Reihenfolge (kritisch) | Kapitel |
| PIPE-TEMPLATE-0001 | Template-/Layout-Prüfung | Kapitel |
| PIPE-BEGRIFF-0001 | Begriffsmodell zuerst (Eindeutigkeit) | Kapitel |
| PIPE-TAGGING-0001 | Tagging über Begriffs-IDs | Kapitel |
| PIPE-DB-0001 | Befüllung SQL + Vektor-DB | Kapitel |
| PIPE-READY-0001 | Reifegrad für Vollautomatisierung | Kapitel |

## Obsidian als lebende Repo-Ansicht

ID: PIPE-OBSIDIAN-0001

Empfehlung: Der Obsidian-Vault ist der Repo-Ordner selbst — dieselben Markdown-Dateien, in Obsidian verlinkt und navigierbar. Kein zweiter Datenbestand.

- Das Repo bleibt Single Source of Truth; Obsidian ist nur die Ansicht/Bearbeitungsbrille.
- Verknüpfungen (Wiki-Links, Backlinks) und die Graph-Ansicht helfen beim Erkennen von Zusammenhängen und Dubletten — ohne die Daten zu duplizieren.
- Vorteil: keine Synchronisationskonflikte zwischen Vault und Repo, weil es nur einen Bestand gibt.

## Verbindliche Reihenfolge (kritisch)

ID: PIPE-REIHENFOLGE-0001

Diese Reihenfolge ist unverrückbar, weil ein Schritt vorziehen alles danach entwertet:

1. **Vollständigkeit**: Alle Dokumente liegen konsolidiert im Repo vor (Konsolidierungs-Konzeption abgeschlossen).
2. **Template-/Layout-Prüfung**: Styleguide drüberlaufen lassen — IDs, Hierarchie, Meta-Blöcke (PIPE-TEMPLATE-0001).
3. **Begriffsmodell**: Eindeutiges Vokabular mit IDs steht (PIPE-BEGRIFF-0001).
4. **Tagging**: über Begriffs-IDs (PIPE-TAGGING-0001).
5. **DB-Befüllung**: erst jetzt SQL + Vektor-DB (PIPE-DB-0001).

Begründung: Wird vor Schritt 3/4 eingebettet, muss nach dem Tagging neu eingebettet werden (Re-Embedding) — teuer und fehleranfällig. Unvollständige oder ungetaggte Inhalte erzeugen genau die uneindeutige Verknüpfung, die vermieden werden soll.

## Template-/Layout-Prüfung

ID: PIPE-TEMPLATE-0001

Vor dem Tagging läuft die Styleguide-Prüfung über den gesamten Bestand:

- Fehlen IDs? Ist die Hierarchie (Überschriften/Blöcke) korrekt abgebildet?
- Sind Meta-Blöcke (Zeitstempel, Update-Historie) vollständig?
- Sind Wissensobjekt-Metadaten (Parent/Child, Überblick) gesetzt?
- Ergebnis: ein einheitlich strukturierter Bestand, der überhaupt erst sauber chunkbar ist.

## Begriffsmodell zuerst (Eindeutigkeit)

ID: PIPE-BEGRIFF-0001

Das Begriffsmodell muss vor dem Tagging stehen, weil es die Eindeutigkeit sichert — genau gegen die zwei Worst Cases:

- **Synonymie** (gleicher Inhalt, verschiedene Wörter): gelöst, indem alle Schreibweisen als Alias an EINE Begriffs-ID hängen (z. B. "Vektordatenbank", "Vector Store" → eine ID).
- **Homonymie** (gleiches Wort, verschiedene Bedeutung): gelöst, indem jede Bedeutung eine eigene ID bekommt (z. B. "Agent" Software vs. "Agent" Vertrieb).

Vorgehen:

- An übergelagerten Standards orientieren (SKOS für Beziehungen; etablierte Fachterminologie statt Eigenerfindung), um Uneindeutigkeit zu minimieren.
- Ein Inhalt = ein Begriff = eine ID; Synonyme nur als Alias.
- Beziehungen (breiter/enger/verwandt) explizit setzen.

## Tagging über Begriffs-IDs

ID: PIPE-TAGGING-0001

Kernregel gegen deinen Worst Case: **Getaggt wird mit Begriffs-IDs, nicht mit freien Wörtern.**

- Ein Chunk wird mit der/den zutreffenden Begriffs-ID(s) verknüpft, nicht mit einem frei getippten Tag-Text.
- Dadurch kann derselbe Inhalt nicht unterschiedlich getaggt werden — es gibt für ihn nur eine ID.
- Ablauf halbautomatisch: Das System schlägt anhand des Begriffsmodells Tags (IDs) vor, du gibst frei — besonders in der Anfangsphase, bis das Vokabular stabil ist. Danach kann der Automatisierungsgrad steigen.
- Grenzfälle (Begriff unklar / zwei Begriffe evtl. identisch) werden nicht eigenmächtig entschieden, sondern vorgelegt (konsistent mit Begriffsmodell-Regel und Richtlinie G7).
- Ergebnis: Tags sind die Grundlage für semantische Verknüpfung, Cross-Cutting-Concern-Erkennung und Transferwissen über Dokumentgrenzen hinweg.

## Befüllung SQL + Vektor-DB

ID: PIPE-DB-0001

Erst nach vollständiger Aufbereitung, Template-Prüfung und Tagging:

- **Chunking** nach Block-IDs; unterhalb der Überschrift per Text klassifiziert (Styleguide-Logik). Zielgröße empirisch bestimmen (Mess-Beispiel: Zugriffszeiten mit/ohne ID, mit/ohne Vektor-DB).
- **SQL** trägt die Metastruktur (IDs, Hierarchie, Parent/Child, Begriffs-ID-Zuordnung); **Vektor-DB** trägt die Embeddings je Chunk für die semantische Suche.
- Jeder Chunk führt seine Block-ID und Begriffs-IDs als Metadaten mit — für Rückverweis und exakte Filter (Hybrid-Retrieval).
- Embedding-Modell einmal festlegen; bei Wechsel ist Re-Embedding nötig (daher bewusst am Ende).

## Reifegrad für Vollautomatisierung

ID: PIPE-READY-0001

Nach diesem Schritt ist der Stand erreicht, an dem die Dokumentation erstmals hohen Kriterien genügt und die vollautomatisierte Fertigung tragen kann. Erst danach folgen:

1. Implementierung der Unternehmensstruktur (digitales Organigramm, Rollen/Avatare).
2. Implementierung des Multi-Agenten-Ansatzes für ausgewählte Workflows.

Vorher wäre Automatisierung verfrüht — sie würde auf unfertigem, schlecht auffindbarem Wissen aufsetzen und die Langsamkeit/Uneindeutigkeit reproduzieren, die dieses Konzept gerade vermeidet.