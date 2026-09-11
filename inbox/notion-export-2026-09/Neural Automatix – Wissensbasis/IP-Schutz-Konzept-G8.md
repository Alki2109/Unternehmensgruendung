# IP-Schutz-Konzept-G8

Bereich: A-Werkzeug/Bauplan
Schutzklasse: vertraulich
Soll-Knoten: G-Governance
Status: Draft

# IP-Schutz-Konzept (G8)

**Erstelldatum (fix):** 10.07.2026, 05:28 (Europe/Berlin)

**Letzte Aktualisierung:** 10.07.2026, 05:28 (Europe/Berlin)

**Status:** Draft

**Zweck:** Konzept zum Schutz des geistigen Eigentums bei gleichzeitiger, gezielter Außendarstellung. Legt fest, was schützenswert ist, wie öffentlich/vertraulich getrennt wird und mit welchen (organisatorischen, vertraglichen, technischen) Maßnahmen der Schutz erreicht wird.

**Fehlt (kurz):** Anwaltliche Prüfung von NDA-Vorlage und GeschGehG-Absicherung + Klassifizierung jedes bestehenden Dokuments (öffentlich/intern/vertraulich) + Entscheidung, welche Logik serverseitig bleibt.

**KI-Referenz:** IP-SCHUTZ-KONZEPT

Update-Historie (Evolution)

| Zeitpunkt (TZ) | Änderung |
| --- | --- |
| 10.07.2026, 05:28 (Europe/Berlin) | Initiale Erstellung als Governance-Knoten G8 |
| 10.07.2026, 05:40 (Europe/Berlin) | Knoten IP-CODE-0001 (Beispielcode & Referenz-Schnipsel) ergänzt |

Standard: siehe Dokumentations-Styleguide (Global) und Schreib-/Qualitätsrichtlinie G7. Kein Rechtsrat — die vertraglichen Teile sind anwaltlich zu prüfen.

Navigation:

| Fachliche ID | Titel/Label | Typ |
| --- | --- | --- |
| IP-SCHUTZWERT-0001 | Was schützenswert und unique ist | Kapitel |
| IP-RECHT-0001 | Was rechtlich (nicht) schützbar ist | Kapitel |
| IP-KLASSEN-0001 | Klassifizierung öffentlich/intern/vertraulich | Kapitel |
| IP-MASSNAHMEN-0001 | Maßnahmen (organisatorisch/vertraglich/technisch) | Kapitel |
| IP-TECHNIK-0001 | Technischer Schutz: was wirkt, was nicht | Kapitel |
| IP-DEMO-0001 | Sichere Außendarstellung & Live-Demo | Kapitel |
| IP-CODE-0001 | Beispielcode & Referenz-Schnipsel | Kapitel |

## Was schützenswert und unique ist

ID: IP-SCHUTZWERT-0001

Die Einzelbausteine (RAG, Multi-Agent, Event-Sourcing, Scrum, BPMN) sind Standard und nicht schützenswert. Der Wert liegt in Integration und stillem Wissen:

- **Konkrete Orchestrierung**: Modell-zu-Aufgabe-Mapping, Prompting-Dreischicht in eigener Ausprägung, empirisch gefundene Chunk-/Retrieval-Parameter.
- **Betriebswissen aus dem Doing**: Retrospektive-Erkenntnisse, konkrete Fehler-/Lösungsmuster — nicht nachlesbar, erarbeitet.
- **Proof of Concept**: die laufende, vorführbare eigene Firma — verkörpert Durchführung, nicht nur Idee; praktisch nicht kopierbar.

Nicht schützenswert (bewusst offen kommunizierbar): die abstrakte Vision "Firma mit KI-Agenten / Digital Twin".

## Was rechtlich (nicht) schützbar ist

ID: IP-RECHT-0001

- **Ideen/Konzepte/Methoden sind nicht schützbar.** Urheberrecht schützt nur die konkrete Ausdrucksform (Text, Code), nicht die Vorgehensweise dahinter.
- **Patente** scheiden für Software-Geschäftsmethoden in Europa praktisch aus (Kosten, Dauer, Schutzfähigkeit).
- **Geschäftsgeheimnisgesetz (GeschGehG)** ist der zentrale Hebel: Schutz entsteht nur bei nachweisbaren "angemessenen Geheimhaltungsmaßnahmen" (Zugriffsbeschränkung, NDA, Vertraulichkeitskennzeichnung). Der Nachweis ist Pflicht — daher aktiv dokumentieren.
- **Prioritätsnachweis**: Git-Zeitstempel/Versionierung belegen, wann welches Wissen vorlag.

## Klassifizierung öffentlich/intern/vertraulich

ID: IP-KLASSEN-0001

Jedes Dokument bekommt eine Schutzklasse:

- **Öffentlich**: Vision, Nutzenargumente, Konzept-Pitch, ausgewählte Businessplan-Teile, Marketing. Das "Was" und "Warum".
- **Intern**: Arbeitsdokumente ohne Kern-IP (allgemeine Regelwerke, Struktur).
- **Vertraulich (Geschäftsgeheimnis)**: Kern-Wissensbasis, Modell-Mapping-Tabellen, Prompt-Bibliothek-Interna, empirische Parameter, Event-/Retrospektive-Logs. Das "Wie" im Detail.

Regel: Vertrauliche Dokumente werden explizit als vertraulich gekennzeichnet (GeschGehG-Nachweis) und nie ungeschützt herausgegeben. Zwei-Schichten-Kommunikation: nach außen das Was/Warum, nie das Wie im Detail.

## Maßnahmen (organisatorisch/vertraglich/technisch)

ID: IP-MASSNAHMEN-0001

- **Vertraglich**: NDA mit jedem, der Interna sieht (Kunden bei Tiefeneinblick, Partner, Dienstleister). Anwaltlich geprüfte Vorlage.
- **Organisatorisch**: Vertraulichkeitskennzeichnung, Zugriffsbeschränkung nach Schutzklasse, dokumentierte Geheimhaltung (GeschGehG).
- **Prioritätssicherung**: Git-Historie als Nachweis der Urheberschaft/Zeitpunkt.
- **Technisch (Fundament, siehe IP-TECHNIK-0001)**: sensible Logik serverseitig, Zugang nur über definierte API.
- **Strategisch**: Geschwindigkeit als stärkster Schutz — Early-Bird-Vorsprung durch laufende Umsetzung schlägt jede Verschlüsselung.

## Technischer Schutz: was wirkt, was nicht

ID: IP-TECHNIK-0001

Klarstellung gegen verbreitete Fehlannahmen:

- **Verschlüsselung at rest** (z. B. verschlüsselter Obsidian-Vault, verschlüsseltes Repo) schützt gegen Geräte-/Repo-Diebstahl — NICHT gegen jemanden mit legitimem Zugang, dem man Inhalte zeigt/gibt. Sobald entschlüsselt zum Arbeiten/Vorführen, sind Daten im Klartext.
- **"Verschlüsselter" ausführbarer Code / clientseitiges JS** schützt Logik nicht: Was ausgeführt wird, muss zur Laufzeit im Klartext vorliegen. Clientseitig ist bestenfalls Obfuskation (Hürde, keine Mauer).
- **Was wirklich schützt**: Logik nicht herausgeben — serverseitig auf dem eigenen Server ausführen, nur das Ergebnis über eine API ausliefern. Der Kunde sieht die Ausgabe, nie den Code oder die Orchestrierung.
- **Server-Härtung** (Reverse Proxy, kein Root-Login, nur 80/443 offen) ist gute Basis gegen Angriffe von außen, löst aber nicht das IP-Kernrisiko (legitimer Zugang). Sinnvolle Ergänzungen: SSH nur per Key + non-root, Firewall-Ebene (ufw/nftables), automatische Sicherheitsupdates, fail2ban, getrennte Backups, GitHub-2FA + signierte Commits.

Kurz: Der Obsidian-Vault als Ansicht aufs Repo bleibt sinnvoll für die Arbeit — aber als IP-Schutz zählt nicht seine Verschlüsselung, sondern die Klassifizierung (IP-KLASSEN-0001) und die serverseitige Architektur.

## Sichere Außendarstellung & Live-Demo

ID: IP-DEMO-0001

Die Live-Demo ist das ideale Schutzinstrument: Sie beweist Funktion, ohne die Blaupause zu zeigen.

- Gezeigt wird das Ergebnis (Kunde speist ad hoc ein Dokument ein, findet gezielt Inhalte) — nicht die Mapping-Tabellen, Prompts oder Parameter dahinter.
- Der Ablauf läuft serverseitig; der Kunde interagiert über die Oberfläche/API, sieht die Interna nie.
- Pitch/Marketing bleiben auf der Was/Warum-Ebene; Tiefeneinblick nur unter NDA.
- KI-generierte Inhalte/Avatare im Außenauftritt sind zu kennzeichnen (Transparenzpflicht ab 08/2026) — Schutz und Compliance zusammen denken.

## Beispielcode & Referenz-Schnipsel

ID: IP-CODE-0001

Beispielcode ist der Grenzfall zwischen "Kompetenz belegen" und "Blaupause verschenken". Die Trennlinie verläuft zwischen Muster und Konfiguration:

- **Unbedenklich (Muster):** Code, der ein Standardmuster zeigt (abstraktes Agent-Interface mit ABC, ein NATS-Publish/Subscribe-Beispiel, ein einfacher Chunking-Loop). Das steht so in jedem Tutorial und belegt Handwerk, ohne Einzigartiges zu verraten.
- **Schützenswert (Konfiguration/Betriebswissen):** Modell-zu-Aufgabe-Mapping mit echten Zuordnungen, empirisch gefundene Parameter (Chunk-Größe, Overlap, Schwellenwerte), Prompt-Interna der Dreischicht, die konkrete Agenten-Verschaltung im echten Workflow. Bleibt vertraulich (IP-KLASSEN-0001).

**Lackmustest** je Schnipsel: "Könnte ein Konkurrent damit Wochen an Entwicklungsarbeit sparen?" Ja → Konfiguration, bleibt drin/privat. Nein (zeigt nur saubere Struktur) → kann als Referenz raus.

**Entkernte Referenz-Schnipsel:** Muster mit Platzhaltern statt echter Werte zeigen (z. B. `model_for = {"<rolle>": "<modell-platzhalter>"}` statt der realen Mapping-Tabelle). Beweist Architektur, ohne die Befüllung zu liefern.

**Zweckbezug:**

- Förderantrag/Gutachter: kein lauffähiger Code nötig — Architektur-Auszug, Sequenz-/Komponentendiagramm und ein entkerntes Snippet belegen technische Substanz und "technisches Risiko" ausreichend.
- Kunden-Demo: Ergebnis live zeigen, Code nur unter NDA.

**Repo-Regel (wichtig):** Was in ein öffentliches Repo gelangt, ist unwiderruflich draußen — auch nach Löschen bleibt es in Git-Historie, Forks und Caches. Daher: Default privat; Öffentlichmachen ist eine bewusste Einzelentscheidung pro Datei. Beispielcode erhält dieselbe Schutzklasse wie jedes andere Artefakt (IP-KLASSEN-0001).