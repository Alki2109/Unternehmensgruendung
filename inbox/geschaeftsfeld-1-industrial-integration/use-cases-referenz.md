# Referenz-Anwendungsfälle – Industrial System Integration & Enterprise Connectivity

Praxiserprobte Anwendungsfälle aus ~10 Jahren industrieller Prozess-IT (Walzwerk, Stahlindustrie),
als Grundlage für Portfolio-Darstellung und Kundengespräche. Kein Original-Produktionscode,
sondern aus eigener Erfahrung neu konzipierte, generische Referenzarchitekturen.

## 1. Produktionsfolge-Umplanung bei Störung (Scheduling-Optimierung)

**Problem:** Verzögert sich ein Produkt im Prozess (z. B. Ofenverweildauer +5 Min.), muss die
Ausgangsreihenfolge neu geplant werden – u. a. weil nachfolgende Produkte innerhalb enger
Zeitfenster den nächsten Prozessschritt erreichen müssen (z. B. Kühlkette), sonst drohen
Qualitätsabweichungen.

**Lösungsansatz:** Klassischer Constraint-Solver (z. B. Google OR-Tools) berechnet die optimale
neue Reihenfolge unter den Zeitfenster-Restriktionen. Ein KI-Agent übersetzt das Störungsereignis
in die Solver-Eingabe und erklärt die getroffene Entscheidung in natürlicher Sprache
(Nachvollziehbarkeit für den Bediener) – die eigentliche Optimierung übernimmt bewusst der Solver,
nicht das LLM.

## 2. Ofentemperatur-Überwachung bei Störung (Qualitätsfenster-Einhaltung)

**Problem:** Störungen wie eine klemmende Ofentür verzögern den Ofendurchlauf; bei
hochqualitativen Stählen (z. B. Pipeline-Rohrstahl) gilt ein enges Temperaturfenster
(Toleranz ca. 10–15 °C). Außerhalb des Fensters gilt das Produkt als Ausschuss und muss
zurück in den Hochofen.

**Referenzbeispiel:** Lieferungen von ca. 2 Mio. Tonnen Grobblech für Nord-Stream-Pipelines
(Kunde Gazprom) – hier galten exakt diese engen Qualitätsvorgaben.

**Lösungsansatz:** Temperaturverlauf als Zeitreihe überwachen, Schwellwert-Alarm bei drohender
Fenster-Verletzung, KI-Agent bewertet Konsequenz und formuliert Handlungsempfehlung.

## 3. Kamerabasierte Rollgang-Überwachung

**Problem:** Bleche können auf dem Rollgang "ausschlagen" (seitlich von der Bahn abweichen) –
mit Schadenspotenzial im Millionenbereich bei Fehlfunktion nachgelagerter Anlagenteile.

**Lösungsansatz:** Kameragestützte Lagekontrolle des Blechs in Echtzeit, Abweichungserkennung,
automatisierter Stopp/Alarm vor Schadenseintritt. Guter Anwendungsfall für Computer-Vision-Anbindung
an das Multi-Agenten-System.

## 4. Dicken- und Oberflächenmessung

**Problem:** Qualitätssicherung erfordert präzise Dickenmessung (radiometrisch/Laser) sowie
Oberflächeninspektion mit bis zu 100.000 Messpunkten pro Blech.

**Lösungsansatz:** Sensordatenerfassung und -verarbeitung (Signalverarbeitung, keine genuine
KI-Aufgabe) mit nachgelagerter KI-gestützter Auswertung/Anomalieerkennung auf den Messdaten.

## 5. Live-Prozessvisualisierung (Werksstrecke Bramme → Blech)

**Problem/Kontext:** Auf einer ca. 400 m langen Produktionsstrecke (Brammenwaage → Ofen →
Walzgerüst → Kühlbett) laufen üblicherweise ca. 30 Produkte parallel. Jede Station quittiert
Prozessereignisse mit Zeitstempel (klassisches Muster: BWA, OE/OA, WALZ, KB).

**Lösungsansatz:** Event-getriebene Live-Visualisierung des Streckendurchlaufs (Sensortrigger →
Zeitstempel in Datenbank → Message-Queue → Visualisierung), inkl. Soll-Ist-Vergleich pro Station.
Eignet sich als anschauliche Demo-/Portfolio-Anwendung und lässt sich mit Anwendungsfall 1
(Umplanung bei Störung) zu einer durchgängigen Demo kombinieren.

## Technischer Kontext (Referenzarchitektur, generisch nachgebaut)

Enterprise-Applikationsserver-Stack (JBoss/WildFly, ActiveMQ, PostgreSQL, JPA/JMS/REST-Schnittstellen)
plus Qt-Fat-Client für Offline-/Sicherheitsanforderungen typischer Produktionsumgebungen
(keine Internetverbindung an Steuerrechnern), ergänzt um moderne Web-/Mobile-Visualisierung
(React, responsive Design) für zeitgemäße Nutzung.
