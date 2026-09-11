# Rueckblick-Fahrplan-Session

Bereich: C-Betrieb
Schutzklasse: intern
Soll-Knoten: G-Governance
Status: Draft

# Rückblick & Fahrplan – Session-Artefakte nach Bereich und Reihenfolge

**Erstelldatum (fix):** 12.07.2026, 00:20 (Europe/Berlin)

**Letzte Aktualisierung:** 12.07.2026, 00:20 (Europe/Berlin)

**Status:** Draft (Orientierungs- und Fahrplan-Dokument)

**Zweck:** Überblick über alle in dieser Session entstandenen Artefakte, aufgeteilt nach Bereich und Verwendungszweck, mit klarer Bearbeitungsreihenfolge. Beantwortet: Was gehört wohin, was ist zuerst dran, wie ist mit jedem Teil zu verfahren.

**Fehlt (kurz):** Reale Repo-Pfade + Schutzklassen (G8) je Dokument + vollständige Migrationsmatrix (Einzelartefakte).

**KI-Referenz:** RUECKBLICK-FAHRPLAN-SESSION

Update-Historie (Evolution)

| Zeitpunkt (TZ) | Änderung |
| --- | --- |
| 12.07.2026, 00:20 (Europe/Berlin) | Initialer Rückblick mit Bereichsaufteilung und Reihenfolge |

Standard: siehe Dokumentations-Styleguide (Global), Soll-Struktur und Artefakt-Inventar-Session.

## Die drei Bereiche auf einen Blick

ID: RB-BEREICHE-0001

Die Artefakte zerfallen in drei Verwendungsbereiche:

- **Bereich A – Werkzeug/Bauplan fürs Aufräumen:** Regeln und Landkarte, nach denen umstrukturiert wird. Wird zuerst angewendet, nicht eingespeist.
- **Bereich B – Inhaltliches Wissen (nummerierte Teile + Businessplan):** der eigentliche Wissensstand, der ins Repo und später in die DB kommt.
- **Bereich C – Betrieb/Praktisches:** Domain, Logo, Agenda – begleitende Handlungsdokumente, kein DB-Stoff.

## Reihenfolge (kritisch)

ID: RB-REIHENFOLGE-0001

Deine eigene Einschätzung ist richtig: erst umstrukturieren, dann Wissen einspeisen. Konkret:

1. **Bereich A anwenden** – Soll-Struktur als Landkarte nehmen, Migrationsmatrix vervollständigen, Konsolidierung durchführen (Merge der drei Quellen). Ergebnis: aufgeräumter Repo-Stand.
2. **Template-/Begriffs-/Tagging-Schritte** aus der Wissens-Pipeline – erst danach ist der Stand DB-fähig.
3. **Bereich B einspeisen** – die inhaltlichen Dokumente in den aufgeräumten Stand einsortieren und (nach Pipeline-Reihenfolge) in die DB überführen.
4. **Bereich C** läuft parallel/unabhängig (Domain ist erledigt, Logo folgt später, Agenda steuert die PC-Session).

Grund: Wissen einspeisen, bevor Struktur und Begriffsmodell stehen, erzeugt genau die Nacharbeit (Re-Tagging, Re-Embedding), die vermieden werden soll.

## Bereich A – Werkzeug/Bauplan fürs Aufräumen

ID: RB-BEREICH-A-0001

Diese Teile werden **angewendet**, nicht eingespeist. Sie sind das Regelwerk der Umstrukturierung.

| Datei | Rolle | Verfahren |
| --- | --- | --- |
| [Soll-Struktur-Gesamtdokumentation.md](http%3A//Soll-Struktur-Gesamtdokumentation.md) | Ziel-Landkarte A–G | Referenz für die Einsortierung aller Inhalte |
| [Konsolidierung-und-Migrationsmatrix.md](http%3A//Konsolidierung-und-Migrationsmatrix.md) | Merge-Plan + Zuordnungstabelle | Matrix vervollständigen, dann Merge ausführen (Terminal-Instanz) |
| [Wissens-Pipeline-Repo-zu-DB.md](http%3A//Wissens-Pipeline-Repo-zu-DB.md) | Ablauf bis zur DB | Schritt-für-Schritt-Anleitung für die Einspeisung |
| [Schreib-und-Qualitaetsrichtlinie-G7.md](http%3A//Schreib-und-Qualitaetsrichtlinie-G7.md) | Sprach-/Prüfregeln | gilt für alle Dokumente beim Überarbeiten |
| [IP-Schutz-Konzept-G8.md](http%3A//IP-Schutz-Konzept-G8.md) | Schutzklassen, IP-Regeln | Schutzklasse je Dokument vergeben |
| [Regelwerk-Dokumenten-Abbildung-ID-Vergabe.md](http%3A//Regelwerk-Dokumenten-Abbildung-ID-Vergabe.md) | ID-Vergabe-Prozedur | beim Einsortieren IDs gegen Register prüfen |

## Bereich B – Inhaltliches Wissen (ins Repo/DB)

ID: RB-BEREICH-B-0001

Der eigentliche Wissensstand. Kommt nach dem Aufräumen ins Repo und dann in die DB.

| Datei | Ziel-Knoten | Verfahren |
| --- | --- | --- |
| [Businessplan-1.0.0-rc.md](http%3A//Businessplan-1.0.0-rc.md) | A3 | Hauptdokument Gründung; noch Finanzzahlen/Belege für "Stable" |
| [Kapitel-3a-Finanzplan-Szenarien.md](http%3A//Kapitel-3a-Finanzplan-Szenarien.md) | A4 | in Businessplan-Umfeld einordnen |
| [Kapitel-4a-IHK-und-Einstiegsgeld-Pfad.md](http%3A//Kapitel-4a-IHK-und-Einstiegsgeld-Pfad.md) | A6 | Handlungsleitfaden Behörden |
| [Use-Case-Uebersicht-und-Referenzprojekte.md](http%3A//Use-Case-Uebersicht-und-Referenzprojekte.md) | A5/D | Marktkenntnis + Referenzprojekt-Plan |
| [Wissen-Rechercheergebnisse-konsolidiert.md](http%3A//Wissen-Rechercheergebnisse-konsolidiert.md) | mehrere (WIS-…) | recherchiertes Wissen, nach Pipeline einspeisen |
| [Rechercheauftrag-Perplexity.md](http%3A//Rechercheauftrag-Perplexity.md) | mehrere | erledigt; als Beleg/Historie ablegen |
| [23-Prompting-Framework-Drei-Schichten.md](http%3A//23-Prompting-Framework-Drei-Schichten.md) | F6 | Regelwerk für die KI-Arbeit |
| [Kapitel-6a-Delivery-Methodik-KI-Softwareentwicklung.md](http%3A//Kapitel-6a-Delivery-Methodik-KI-Softwareentwicklung.md) | D/E | Brücke zur SD-Wissensbasis |
| [Kapitel-6b-Standards-und-Governance.md](http%3A//Kapitel-6b-Standards-und-Governance.md) | G | Einordnung der Regelwerke |
| [Meetings-und-Besprechungsorganisation.md](http%3A//Meetings-und-Besprechungsorganisation.md) | G3 | Governance-Regelwerk |

## Bereich C – Betrieb/Praktisches

ID: RB-BEREICH-C-0001

Begleitende Handlungsdokumente, kein DB-Stoff.

| Datei | Rolle | Status/Verfahren |
| --- | --- | --- |
| [Domain-Registrierung-Neural-Automatix.md](http%3A//Domain-Registrierung-Neural-Automatix.md) | Domain-Anleitung | .ai registriert; DNS auf Hetzner + .de/.eu offen |
| [Logo-Vorgaben-Neural-Automatix.md](http%3A//Logo-Vorgaben-Neural-Automatix.md) | Logo-Vorgaben | wartet auf Zeichnungen (spätere Session) |
| [Agenda-PC-Session-Framework-Repo.md](http%3A//Agenda-PC-Session-Framework-Repo.md) | Ablaufplan PC-Session | steuert die technische Umsetzung |
| [Artefakt-Inventar-Session.md](http%3A//Artefakt-Inventar-Session.md) | Gesamtinventar | Checkliste beim Ablegen |

## Nicht einpflegen (ersetzte Zwischenstände)

ID: RB-OBSOLET-0001

- [Prompt-Engineering-KB-Dreischicht-Regelwerk.md](http%3A//Prompt-Engineering-KB-Dreischicht-Regelwerk.md) → ersetzt durch [23-Prompting-Framework-Drei-Schichten.md](http%3A//23-Prompting-Framework-Drei-Schichten.md)
- [Businessplan-A5-Markt-B2-Vision.md](http%3A//Businessplan-A5-Markt-B2-Vision.md) → aufgegangen in [Businessplan-1.0.0-rc.md](http%3A//Businessplan-1.0.0-rc.md)

## Konkret als Nächstes

ID: RB-NEXT-0001

1. Migrationsmatrix vervollständigen (deine Einzelartefakte + Repo-Pfade eintragen).
2. Merge der drei Quellen über die Terminal-Instanz (Repo → Staging → Session/Notion).
3. Erst-Begriffsmodell aufsetzen (Flaschenhals für Tagging).
4. Danach: Wissen (Bereich B) nach Pipeline-Reihenfolge in die DB.
5. Parallel: Businessplan auf "Stable" (Finanzzahlen, Belege, Referenzprojekte); DNS/Nebendomains.