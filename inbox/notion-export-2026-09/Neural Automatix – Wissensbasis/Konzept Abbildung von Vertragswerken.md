# Konzept: Abbildung von Vertragswerken

Bereich: B-Wissen
Schutzklasse: intern
Soll-Knoten: B-Konzepte
Status: Draft
Anmerkung: Ebene 1 (Konzept) der Dreiteilung Konzept -> Domaene -> Anwendung. Generische, wiederverwendbare Struktur zur Erfassung beliebiger Vertragswerke. IDs werden nachgelagert per Notion-Regelwerk vergeben.

# Hintergrund und MotivationnDie Sammlung dient dazu, sämtliche privaten Vertragsunterlagen (Größenordnung ca. 10 Verträge, nicht tausende) digital zu erfassen. Primärer Zweck ist ein **digitales Backup** der Papierunterlagen als Absicherung gegen Verlust oder Beschädigung der Originale (z. B. durch Brand, Wasserschaden o. Ä.).nnAuf dieser erfassten Datenbasis sollen anschließend nützliche Funktionen aufsetzen, u. a.:n- Erzeugung wiederkehrenden Schriftverkehrs (z. B. Mahnungen, Anzeigen, Anfragen).n- Überwachung von Handlungsbedarfen und Fristen (z. B. Einhaltung von Kündigungsfristen).n- Prüfung und Nachvollziehbarkeit von Vertragsinhalten (z. B. Deckungsumfang von Versicherungspolicen).n- Dokumentation und Initialisierung der jeweils sinnvollen Schritte je Vertragsfall.nn# Struktur der Ablage (Verschachtelung)nDie drei Ebenen werden als **ineinander verschachtelte Seiten** abgebildet, nicht als getrennte, nur verlinkte Seiten:n- Diese **Konzept-Seite** steht für sich allein und ist in keinen größeren Rahmen eingebunden.n- Jede **Domäne** (z. B. Mietverhältnis) ist eine **Unterseite dieser Konzept-Seite**.n- Jeder **konkrete Anwendungsfall** (z. B. Mietverhältnis Kiefer ↔ Leinenbach) ist wiederum eine **Unterseite der jeweiligen Domänen-Seite**.nnWeitere Domänen (z. B. Internetvertrag, Handyvertrag, Versicherungen wie Haftpflicht und Kfz, Vermögensanlage) werden später als weitere Unterseiten dieser Konzept-Seite ergänzt.n

<aside>
📌

**Zweck**

Diese Seite beschreibt generisch und wiederverwendbar, wie ein beliebiges **Vertragswerk** erfasst, strukturiert und für wiederkehrende Aufgaben (Pflichten, Dokumentation, Schriftverkehr) nutzbar gemacht wird. Sie ist die abstrakteste der drei Ebenen: **Konzept → Domäne → Anwendung**.

</aside>

# Einordnung in die Dreiteilung

Diese Seite ist **Ebene 1 (Konzept)**. Sie steht über den konkreteren Ebenen:

- **Ebene 1 – Konzept (diese Seite):** Vertragswerk allgemein – gilt für jede Vertragsart.
- **Ebene 2 – Domäne:** Konkrete Vertragsart (z. B. Mietverhältnis, Handyvertrag, Internetvertrag, Versicherungspolice).
- **Ebene 3 – Anwendung:** Der reale Einzelfall mit konkreten Fakten und Schriftverkehr.

# Kernbestandteile eines Vertragswerks

Jedes Vertragswerk lässt sich auf wenige, immer wiederkehrende Grundbestandteile zurückführen.

## Vertragsgegenstand

Der Gegenstand, über den der Vertrag geschlossen wird (z. B. eine Wohnung, eine Mobilfunkleistung, ein Versicherungsschutz). Er bestimmt, welche Leistungen und Pflichten überhaupt entstehen.

## Vertragsparteien

Die am Vertrag beteiligten Personen oder Organisationen mit ihren jeweiligen Rollen (z. B. Leistungserbringer/Leistungsempfänger, Vermieter/Mieter, Versicherer/Versicherungsnehmer) sowie ihren Stamm- und Kontaktdaten.

## Pflichten und wiederkehrende Leistungen

Aus dem Vertrag entstehende, oft wiederkehrende Verpflichtungen – insbesondere Zahlungen (Miete, Beiträge, Gebühren), aber auch Instandhaltungs-, Auskunfts- oder Mitwirkungspflichten. Diese Ebene dient dazu, wiederkehrende Tätigkeiten und Fristen zu dokumentieren.

## Ereignisse

Vertragsrelevante Vorkommnisse während der Laufzeit (z. B. Schadensfälle, Mängel, Leistungsstörungen, Änderungen). Ereignisse können Pflichten auslösen oder Ansprüche begründen.

## Schriftverkehr und Dokumente

Der aus Pflichten und Ereignissen entstehende Schriftverkehr (z. B. Mahnungen, Anzeigen, Kündigungen, Anfragen) sowie die zugehörigen Nachweise und Belege. Ziel ist die lückenlose, nachvollziehbare Dokumentation.

# Zweck des Konzepts

Die generische Struktur verfolgt drei Ziele:

- Wiederkehrende Pflichten (v. a. Zahlungen) und Fristen strukturiert erfassen und überwachen.
- Vertragsrelevante Ereignisse nachvollziehbar dokumentieren.
- Auf dieser Basis den notwendigen Schriftverkehr (halb-)automatisiert erzeugen können.

# Typische Anwendungsfälle (Use-Case-Muster)

Aus der Struktur ergeben sich wiederkehrende Use Cases, die in den Domänen und Anwendungen konkretisiert werden:

- Erzeugung von Zahlungsaufforderungen / Mahnschreiben.
- Anzeige von Leistungsstörungen oder Mängeln mit Fristsetzung.
- Geltendmachung von Minderungs- oder Erstattungsansprüchen.
- Anfragen an Dritte (Verwaltungen, Dienstleister, Versicherer).
- Kündigungen und Widersprüche.

# Referenzen

- Ebene 2 (Domäne): Mietverhältnis – siehe zugehörige Domänen-Seite.
- Ebene 3 (Anwendung): Mietverhältnis Kiefer ↔ Leinenbach – siehe zugehörige Anwendungs-Seite.

[](Konzept%20Abbildung%20von%20Vertragswerken/Unbenannt.md)