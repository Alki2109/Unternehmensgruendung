# Regelwerk-Dokumenten-Abbildung-ID-Vergabe

Bereich: A-Werkzeug/Bauplan
Schutzklasse: intern
Soll-Knoten: G-Governance
Status: Draft

# Regelwerk – Dokumenten-Abbildung & ID-Vergabe (Vollzug)

**Erstelldatum (fix):** 07.07.2026, 15:32 (Europe/Berlin)

**Letzte Aktualisierung:** 07.07.2026, 15:32 (Europe/Berlin)

**Status:** Draft

**Zweck:** Verbindliche **operative Prozedur** für die Vergabe, Prüfung und Registrierung stabiler IDs über alle Dokumentensysteme hinweg. Dieses Regelwerk dupliziert nicht die konzeptionellen Regeln des globalen Styleguides, sondern setzt sie in einen ausführbaren Vollzugs-Prozess um (Vergabe → Kollisionsprüfung → Registrierung).

**Fehlt (kurz):** Reale Ablage/Technik des zentralen ID-Registers festlegen (Notion-DB vs. Datei im Repo) + verantwortliche Rolle benennen + Erst-Import aller bestehenden IDs aus GRUENDUNG- und KB-System ins Register.

**KI-Referenz:** REGELWERK-DOKUMENTEN-ABBILDUNG-ID-VERGABE

Update-Historie (Evolution)

| Zeitpunkt (TZ) | Änderung |
| --- | --- |
| 07.07.2026, 15:32 (Europe/Berlin) | Initiale Erstellung: Vollzugs-Prozedur über beide Doku-Systeme |

Standard: siehe Dokumentations-Styleguide (Global) – Regel-Template. Dieses Regelwerk ist der operative Vollzug zu den konzeptionellen Styleguide-Regeln `DOCSTYLE-HIER-0001` (Hierarchie), `DOCSTYLE-BLOCKID-0001` (ID-Format), `DOCSTYLE-KNOW-0001` (Wissensobjekte/Tagging) und `DOCSTYLE-TEST-0001` (Testbarkeit). Es ist eingeordnet in Kapitel 6b (Standards & Governance).

Navigation:

| Fachliche ID | Titel/Label | Typ |
| --- | --- | --- |
| DOCID-ZWECK-0001 | Abgrenzung zum Styleguide | Kapitel |
| DOCID-SCHEMA-0001 | Zwei ID-Welten & Zuordnung | Kapitel |
| DOCID-PROZESS-0001 | Vergabe-Prozedur (Schritt für Schritt) | Kapitel |
| DOCID-REGISTER-0001 | Zentrales ID-Register (SSOT) | Kapitel |
| DOCID-KOLLISION-0001 | Kollisions- & Qualitätsprüfung | Kapitel |
| DOCID-DOD-0001 | Definition of Done (ID) | Kapitel |

## Abgrenzung zum Styleguide

ID: DOCID-ZWECK-0001

Der globale Styleguide definiert, **wie** IDs aussehen und welche Metadaten ein Wissensobjekt braucht. Dieses Regelwerk definiert, **wie eine ID konkret entsteht, geprüft und eingetragen wird** — die ausführbare Prozedur.

Der Bedarf ist real: In allen bisher erstellten Dokumenten stand im „Fehlt (kurz)"-Feld der Hinweis, dass die vorgeschlagenen Block-IDs gegen einen zentralen Index zu prüfen sind. Dieses Regelwerk schließt genau diese Lücke, indem es den Index (Register) und den Prüfschritt verbindlich macht.

## Zwei ID-Welten & Zuordnung

ID: DOCID-SCHEMA-0001

Im Unternehmen existieren zwei bewusst getrennte, jeweils intern konsistente ID-Welten. Neue Dokumente werden dem passenden System zugeordnet, nicht gemischt:

- **GRUENDUNG-Welt** (Gründungsdoku, Regelwerke): sprechende IDs, z. B. `KAPITEL-6B-STANDARDS-GOVERNANCE`, Block-IDs im Schema `<BEREICH>-<THEMA>-<NNNN>` (z. B. `DOCID-PROZESS-0001`, `MEET-PROTO-0001`).
- **KB-Welt** (AI Driven Software Development Knowledge Base): `Block ID: KB-<KAT>-<NNNN>` (z. B. `KB-PROMPT-0030`) plus Abschnitts-IDs im Schema `CATEGORY_CONTEXT_NAME`.

Zuordnungsregel: Software-/SDLC-/Prompt-Methodik → KB-Welt. Gründung, Business, Governance, Cross-Cutting-Regelwerke → GRUENDUNG-Welt. Im Zweifel entscheidet der Hauptzweck des Dokuments (Leserschaft).

## Vergabe-Prozedur (Schritt für Schritt)

ID: DOCID-PROZESS-0001

Für jede neue ID (Seite oder Block) gilt verbindlich:

1. **System bestimmen** (GRUENDUNG vs. KB) nach der Zuordnungsregel oben.
2. **Kandidat-ID bilden** nach dem Format des jeweiligen Systems (Styleguide `DOCSTYLE-BLOCKID-0001` bzw. KB-Style-Guide).
3. **Register-Lookup**: Prüfen, ob die Kandidat-ID bereits im zentralen ID-Register existiert (siehe DOCID-REGISTER-0001).
4. **Bei Kollision**: fortlaufende Nummer erhöhen oder Kontext präzisieren, zurück zu Schritt 3.
5. **Registrieren**: Neuen Eintrag im Register anlegen (am selben Tag — Styleguide-Regel „jede neue Block-ID wird am selben Tag in den Index aufgenommen").
6. **Im Dokument setzen**: ID direkt unter der Überschrift platzieren (`ID:`- bzw. `Block ID:`-Zeile).
7. **Stabil halten**: Nach Anlage wird die ID nicht mehr geändert (Umstrukturieren zieht Register-Pflege nach, ersetzt aber nicht die ID).

## Zentrales ID-Register (SSOT)

ID: DOCID-REGISTER-0001

Das ID-Register ist die Single Source of Truth für alle vergebenen IDs beider Welten. Es ist die Voraussetzung für kollisionsfreie Vergabe und für das spätere KI-Routing/RAG.

Pflichtfelder je Eintrag:

- ID (Block-/Objekt-ID)
- System (GRUENDUNG | KB)
- Dokument/Seite (Titel + Link)
- Überschrift/Kapitelname
- Kurzbeschreibung (1–2 Zeilen, ideal aus dem Überblick)
- Tags/Kategorie
- Parent/Child (soweit relevant)
- Status (Draft/Stable), letzte Änderung

Hinweis: In der KB-Welt existiert dafür bereits der AI Reference Index (`KB-REF-0026`); in der GRUENDUNG-Welt der KI-Referenzindex (Kapitel 9). Beide sind die konkreten Instanzen dieses Registers je System — offener Punkt ist, ob sie logisch zu einem übergreifenden Register zusammengeführt werden (empfohlen: eine gemeinsame Sicht/Tabelle mit Spalte „System").

## Kollisions- & Qualitätsprüfung

ID: DOCID-KOLLISION-0001

Minimal-Checks vor Freigabe einer ID (aus Styleguide `DOCSTYLE-BLOCKID-0001` übernommen und verbindlich gemacht):

- Keine doppelten IDs — global über beide Systeme.
- Jede ID kommt genau einmal im Register vor.
- ID steht direkt unter der Überschrift, nicht mitten im Text.
- Format entspricht dem System (GRUENDUNG- oder KB-Schema).
- Bei Wissensobjekten: Pflicht-Metadaten (Überblick, Parent/Child, Tags) vorhanden.

Die strukturelle Wirksamkeit wird bei Bedarf über das Testmodell `DOCSTYLE-TEST-0001` geprüft (Variante A unstrukturiert vs. B strukturiert, Top-1-Trefferquote).

## Definition of Done (ID)

ID: DOCID-DOD-0001

Eine ID-Vergabe gilt als „fertig", wenn:

- System korrekt bestimmt und Format eingehalten,
- Register-Lookup durchgeführt, keine Kollision,
- Eintrag im zentralen Register am selben Tag angelegt,
- ID im Dokument direkt unter der Überschrift gesetzt,
- bei Wissensobjekten: Überblick, Parent/Child und Tags gepflegt,
- Status im Register gesetzt (Draft/Stable).