# Businessplan-1.0.0-rc

Bereich: B-Wissen
Schutzklasse: intern
Soll-Knoten: A-Gründung
Status: Review

# Businessplan – Neural Automatix

**Erstelldatum (fix):** 20.05.2026 (Ursprung V1)

**Letzte Aktualisierung:** 19.09.2026 (Europe/Berlin)

**Version:** 1.0.0-rc (Release Candidate – erstes vorzeigereifes Release; final "Stable" nach Prüfung)

**Status:** Review

**KI-Referenz:** BUSINESSPLAN-CURRENT

Update-Historie (Evolution)

| Zeitpunkt (TZ) | Version | Änderung |
| --- | --- | --- |
| 20.05.2026 | V1 | Erstfassung |
| 25.05.2026 | V2 | Positionierung, USP, Zielgruppen, Leistungsportfolio geschärft |
| 10.07.2026, 09:51 (Europe/Berlin) | 1.0.0-rc | Marktkapitel mit belegten Zahlen (Nachfrage-Story); Digital Twin als DTO mit Reifegrad; Master-Architektur auf Prinzip verdichtet; erstmals vorzeigereif/förderfähig |
| 10.07.2026, 11:16 (Europe/Berlin) | 1.0.0-rc | Fünfte Säule "Industrielle Anbindung & Systemintegration" ergänzt; Voice-Agent-Startangebot; Qualifikationsteil mit belegtem Dillinger-Werdegang (HTW Saar, Leitsystem Walzwerk); USP um Industrie-Nähe geschärft |
| 10.07.2026, 11:16 (Europe/Berlin) | 1.0.0-rc | Enterprise-/Application-Server-Kompetenz (EJB, JBoss→WildFly) in fünfte Säule und Qualifikation integriert; DTO-Vision mit Stahlwerk-Prozessabbildung als Vorläufer verknüpft |
| 10.07.2026, 11:30 (Europe/Berlin) | 1.0.0-rc | Portfolio von 5 auf 3 fokussierte Säulen verdichtet (Industrie/Enterprise · KI-Dev · Enablement); EJB-Lehrtätigkeit HTW Saar und 9 Jahre Rufbereitschaft/Qualitätsdisziplin ergänzt; industrielles Referenz-Umfeld als Demo-Use-Case |
| 10.07.2026, 11:45 (Europe/Berlin) | 1.0.0-rc | Firmenname von "Neural [KI.de](http://KI.de)" auf "Neural Automatix" geändert (durchgängig Englisch, international, besser schützbar); Domain [neuralautomatix.ai](http://neuralautomatix.ai) |
| 19.09.2026 (Europe/Berlin) | 1.0.0-rc | Überarbeitung nach Cowork-Review: Positionierung explizit auf Industrie-Fokus geschärft (Säule 1 als strategischer Kern statt nur Kompetenztiefe); Marktbelege M11–M13 (Malt-Nachfragewachstum, Bitkom-Fachkräftelücke, VDMA-Industrie-4.0-Engpass) in den Fließtext übernommen; Luxemburg/Benelux-Marktpriorität (M14–M18) neu ergänzt; Geplanter Business-Start von 01.09.2026 auf 01.12.2026 (Annahme) aktualisiert, konsistent mit Förderpfad-Reihenfolge in Kapitel 4/4a |

Standard: siehe Dokumentations-Styleguide (Global) und Schreib-/Qualitätsrichtlinie G7 (gutachterreife Sprache, Belegpflicht). Marktzahlen mit Quelle/Definition/Jahr; technische Detailtabellen ausgelagert in die AI-Driven-Software-Development-Wissensbasis.

## Executive Summary

ID: BP-SUMMARY-0001

Alexander Kiefer gründet ein spezialisiertes Einzelunternehmen für KI-gestützte Softwareentwicklung, Prozessautomatisierung und digitale Arbeitsabläufe. Das Angebot richtet sich in der Startphase vorrangig an kleine und mittlere Unternehmen, Bildungs- und Weiterbildungseinrichtungen sowie wissensintensive Dienstleister, die Prozesse digitalisieren und KI praktisch einsetzen möchten, ohne eigene KI-Abteilung oder Enterprise-Budget aufzubauen.

Das Unternehmen adressiert ein belegbares Problem: Zahlreiche Organisationen erkennen den Nutzen von KI, scheitern aber an unklaren Prozessen, fehlendem Wissen, rechtlicher Unsicherheit und fehlender Umsetzungskapazität. Genau diese Lücke bedient das Angebot, indem es unklare Anforderungen in nachvollziehbare, lauffähige und dokumentierte Lösungen übersetzt.

Der Kundennutzen liegt in messbarer Entlastung: weniger manuelle Arbeit, kürzere Durchlaufzeiten, transparentere Abläufe, bessere Entscheidungsgrundlagen, nachvollziehbare und rechtskonforme KI-Nutzung sowie interne Befähigung der Mitarbeitenden.

## Alleinstellungsmerkmal

ID: BP-USP-0001

Kurzform: 15 Jahre Enterprise-Softwareentwicklung, verbunden mit moderner Multi-Agenten-KI, für Organisationen, die Digitalisierung wollen, aber kein Enterprise-Budget haben.

Prüffähige Erweiterung: Das Angebot übersetzt unklare Digitalisierungs- und KI-Ideen in lauffähige, dokumentierte Software- und Automatisierungslösungen. Die Stärke liegt in der seltenen Kombination aus langjähriger Softwareentwicklung, didaktischer Vermittlung, Prozessdenken und praktischer KI-Orchestrierung. Kunden erhalten keine abstrakte KI-Beratung, sondern Analyse, Prototyp, Umsetzung, Übergabe, Dokumentation und Befähigung aus einer Hand.

Diese Kombination ist der eigentliche Differenzierer: Nicht KI-Kompetenz allein (die zunehmend verbreitet ist), sondern die Verbindung aus IT-Umsetzung, KI-Orchestrierung und didaktischer Befähigung, die in dieser Bündelung am Markt selten ist.

Ein besonderes Alleinstellungsmerkmal ist die **Industrie- und Produktionsnähe**: Durch über acht Jahre Entwicklung eines produktionskritischen Leitsystems in der Stahlindustrie besteht praktische Erfahrung mit der Integration von IT-Systemen in industrielle Automatisierungsumgebungen – einschließlich Datenaustausch mit speicherprogrammierbaren Steuerungen (SPS/S7). Damit adressiert das Angebot ein Kundensegment (produzierendes Gewerbe, Fertigung), das reine KI-Berater ohne Zugang zur Maschinen- und Automatisierungsebene nicht bedienen können.

## Start-Zielgruppen

ID: BP-ZIELGRUPPEN-0001

Entsprechend dem Industrie-Fokus (siehe Leistungsportfolio) steht Segment 1 strategisch an erster Stelle; Segmente 2–4 sind komplementäre, schneller anlaufende Zielgruppen:

1. **Produzierendes Gewerbe / Fertigungsbetriebe** mit bestehender Automatisierungs- und Steuerungsinfrastruktur (SPS/S7), bei denen KI-Nutzen an die Anbindung der Maschinen-/Systemebene gebunden ist – strategischer Kernfokus (Säule 1), priorisiert im Zielgebiet Luxemburg/Benelux.
2. KMU mit wiederkehrenden Verwaltungs-, Dokumenten- oder Kommunikationsprozessen.
3. Bildungs- und Weiterbildungseinrichtungen mit Bedarf an KI-Schulung, Lernsystemen oder digitalen Lehr-/Arbeitsprozessen.
4. Wissensintensive Dienstleister mit hohem Dokumentations-, Angebots-, Recherche- oder Kundenkommunikationsaufwand.

## Markt und Wettbewerb

ID: BP-MARKT-0001

Die tragende Marktlogik lautet: **Der Bedarf ist vorhanden, das Wissen fehlt.** Die Nachfrage nach praxisnaher KI-Umsetzung im Mittelstand ist belegt, ebenso die Umsetzungslücke, die das Angebot schließt.

**KI-Nutzung im Mittelstand – belegte Ausgangslage.** Nach der amtlichen IKT-Erhebung nutzten 2024 rund 20 % der Unternehmen ab 10 Beschäftigten KI, jedoch mit deutlichem Größengefälle: kleine Unternehmen (10–49 Beschäftigte) nur 17 %, mittlere (50–249) 28 %, große (ab 250) 48 % (Destatis, PM Nr. 444, 25.11.2024). Neuere Erhebungen zeigen einen steigenden Trend: Bitkom meldet für 2025 einen Einsatz von 36 % (Unternehmen ab 20 Beschäftigte; Bitkom KI-Studie 2025); ifo weist für 2026 eine KI-Software-Nutzung von 54,4 % aus (Handelsblatt/dpa zu ifo/ZEW, 06.06.2026).

Hinweis zur Zahleninterpretation: Die Spanne von 20 % (Destatis 2024) bis 54,4 % (ifo 2026) erklärt sich durch unterschiedliche Definitionen (enger KI-Begriff vs. inklusive generativer KI), Erhebungsjahre und Stichproben. Für die Bewertung ist weniger der absolute Nutzungsgrad entscheidend als das konsistente Muster: KMU liegen deutlich hinter Großunternehmen, und der Aufholbedarf ist strukturell.

**Die Umsetzungslücke als Geschäftsgrundlage.** Die amtliche Erhebung nennt als häufigste Gründe gegen KI-Nutzung: fehlendes Wissen (71 %), rechtliche Unsicherheit (58 %), Datenschutzbedenken (53 %) und mangelnde Datenqualität (45 %) (Destatis, 25.11.2024). Das ist die zentrale Marktbegründung: Der Engpass ist nicht mangelndes Interesse, sondern fehlendes Know-how und Umsetzungssicherheit – genau die Leistung, die das Angebot erbringt. Bitkom bestätigt die interne Kapazitätslücke: Nur 5 % der Unternehmen stellen gezielt KI-Fachkräfte ein, 43 % bieten keine KI-Schulungen (Bitkom KI-Studie 2025). Wer intern weder Personal noch Schulung aufbaut, muss extern zukaufen.

**Fachkräftemangel als Zukauf-Treiber.** Der IT-Fachkräftemangel verschärft die Zukauf-Notwendigkeit: 2025 waren rund 109.000 IT-Stellen unbesetzt, die durchschnittliche Vakanzzeit lag bei 7,7 Monaten (Bitkom, IT-Fachkräfte 2025). KI-bezogene Kompetenz ist dabei besonders gefragt und höher vergütet (Median-Jahresgehalt Data Scientist 67.000 € gegenüber 54.500 € für Softwareentwickler; Stepstone, 15.02.2024). Für KMU bedeutet das: Eigenaufbau ist teuer, langwierig und im Wettbewerb um Fachkräfte oft aussichtslos – externe, projektbezogene Umsetzung ist die realistische Alternative.

**Marktvolumen und Investitionsklima.** Das KI-Marktvolumen in Deutschland wuchs auf über 10 Mrd. € (2025; Bitkom/IDC). Gleichzeitig sind die Digitalisierungsausgaben im Mittelstand zuletzt rückläufig (2023: 31,9 Mrd. €, 2024: 23,8 Mrd. €; KfW-Digitalisierungsbericht Mittelstand 2024) – ein Signal, dass viele KMU zwar Bedarf sehen, aber bei der Umsetzung zögern. Das stützt die These der Umsetzungslücke: Nachfrage und tatsächliche Umsetzung klaffen auseinander. (Ein isoliertes Marktvolumen speziell für "KI-Dienstleistungen für KMU" liegt als eigene Kennzahl nicht vor; die Einordnung erfolgt daher näherungsweise über KI-Gesamtmarkt und Mittelstands-Digitalisierungsausgaben.)

**Nachfrage wächst schneller als das Angebot an Fachkräften.** Auf europäischen Freelance-Plattformen stiegen KI-Projektanfragen 2023–2024 um 230 %, während das Angebot an KI-Freelancern nur um 31 % zunahm (Deutschland: +67 % Nachfrage; Malt AI Report 2024). Die Bitkom-KI-Studie 2026 bestätigt den beschleunigten Trend: 41 % der deutschen Unternehmen setzen inzwischen aktiv KI ein (Vorjahr 17–20 %), weitere 48 % planen den Einstieg – bei einer gleichzeitigen DACH-weiten Lücke von rund 149.000 KI-Fachkräften. Für das industrielle Zielsegment (Säule 1) kommt ein eigener, noch engerer Engpass hinzu: Laut VDMA/produktion.de (2026) melden rund 80 % der Maschinenbauunternehmen einen Fachkräfteengpass speziell bei Industrie-4.0-/SPS-Integration, mit einem Gehaltsdelta von 75.000–100.000 € (SPS+IT-Integration) gegenüber 55.000–70.000 € (reines SPS) pro Jahr. Diese drei Belege zusammen begründen die Marktlogik über die generische KMU-KI-Nachfrage hinaus: Gerade die Kombination aus industrieller Systemintegration und KI-Automatisierung ist ein besonders knappes, überdurchschnittlich vergütetes Feld.

**Geografische Priorität: Luxemburg/Benelux vor Deutschland.** Der Standort Überherrn (Saarland) liegt näher an Luxemburg-Stadt und weiten Teilen von Belgien/Luxemburg/Niederlande als an vielen deutschen Wirtschaftszentren (400-km-Radius-Argument). Luxemburg (33,6 % KI-Nutzungsquote bei Unternehmen ≥10 MA, 2025), Belgien (34,5 %) und die Niederlande (33,2 %) liegen jeweils deutlich über dem EU-Durchschnitt von 20,0 % – der priorisierte Zielmarkt ist also nicht nachfrageschwächer als Deutschland, sondern eher adoptionsfreudiger, und ein Luxemburger Landesförderprogramm übernimmt laut Anbieterangaben bis zu 70 % der Projektkosten für KMU (gedeckelt auf ca. 17.500 €), was die Akquiseschwelle für Kunden senkt. Eine Proxy-Recherche identifiziert im Zielgebiet mehrere aktive Anbieter für generische KI-Beratung/-Automatisierung (u. a. 20More, ObsidianCorps, Lux AI Automation, n3tz), aber keinen mit erkennbarem Fokus auf industrielle Systemintegration (SPS/S7, OT-Ebene) – exakt die Nische von Säule 1. Details, Quellen und Einschränkungen der Luxemburg/Benelux-Zahlen stehen im Evidence Pack (Kapitel 5, Abschnitt 5.1.3, M14–M18).

**Wettbewerb und Abgrenzung.** Der Wettbewerb besteht aus IT-Freelancern, Webagenturen, Automatisierungstools, SaaS-Lösungen, internen Mitarbeitenden und reiner KI-Beratung. Die Abgrenzung liegt nicht im Begriff KI, sondern in der umsetzungsnahen Verbindung von Prozessanalyse, Softwareentwicklung, KI-Orchestrierung, Dokumentation und Schulung – aus einer Hand. Reine Beratung liefert kein lauffähiges Ergebnis; reine Entwicklung liefert keine Befähigung; das Angebot verbindet beides. Im priorisierten Zielgebiet Luxemburg/Benelux verschärft sich diese Abgrenzung zusätzlich zugunsten des Industrie-Fokus (siehe oben): Generische KI-Beratung ist dort bereits mehrfach besetzt, industrielle Systemintegration nicht.

Offen (vor finaler Einreichung zu ergänzen): konkrete freelancermap-Projekt-/Stundensatzdaten, regionale KMU-/IHK-Daten (Saarland und Luxemburg) und 2–3 anonymisierte Beispiel-Use-Cases aus Zielkundensicht.

## Leistungsportfolio

ID: BP-PORTFOLIO-0001

Die Positionierung ist ein **Industrie-Fokus**: Strategischer Kern und Türöffner ist die industrielle Systemintegration (Säule 1) – nicht generische KI-Beratung. Säule 2 und 3 sind komplementäre Umsetzungs- und Befähigungsangebote, die dasselbe Kompetenzprofil auf breitere KMU-Zielgruppen (auch außerhalb der Industrie) anwenden und so zusätzliche, schneller anlaufende Umsatzströme neben dem längeren Vertriebszyklus industrieller Projekte liefern. Die Reihenfolge der Säulen spiegelt diese Priorität wider, nicht nur die Kompetenztiefe.

**Säule 1 – Industrielle Systemintegration & Enterprise-Anbindung (strategischer Kern).** Das Angebot positioniert sich primär über diese Säule, weil sie im priorisierten Zielgebiet Luxemburg/Benelux (siehe Markt-Kapitel) eine belegte Marktlücke besetzt, die reine KI-Berater ohne Zugang zur Maschinen- und Systemebene nicht bedienen können, und weil dort laut VDMA-Daten ein besonders knappes, überdurchschnittlich vergütetes Fachkräftefeld vorliegt (siehe BP-MARKT-0001). Fachliche Basis: rund zehn Jahre Erfahrung in der Stahlindustrie. Anbindung von Software- und KI-Lösungen an industrielle und Enterprise-Landschaften: Datenaustausch mit Automatisierungs- und Steuerungssystemen (SPS/S7) über mehrere Hierarchieebenen, asynchrone Kommunikation zwischen Steuer- und Leitsystemen (Message-oriented Middleware), Enterprise-Application-Server für dauerhafte Langzeit-Prozessabbildung ohne Systemabschaltung, Datenbankanbindung und Prozesslogik (Enterprise JavaBeans), Standardschnittstellen zu externen Abteilungen (z. B. Produktionsplanung) über Webservices und REST sowie Anbindung von Hardware/Mikrocontrollern (Raspberry Pi, Calliope, Lego Mindstorms) über Bluetooth, USB oder WLAN. Industrielle Prozessautomatisierung und Enterprise-Systeme (ERP) gehören zusammen, weil beide in produktionskritischen Umgebungen mit vielen Akteuren, hoher Datenbanklast und Langzeitprozessen sinnvoll sind.

**Säule 2 – KI-gestützte Softwareentwicklung & Automatisierung (komplementärer Marktzugang, breiteres KMU-Segment).** Individuelle, KI-getriebene Softwarelösungen über den gesamten Entwicklungsprozess – von Anforderungsanalyse über Architektur und Implementierung bis Auslieferung, Dokumentation und Übergabe. Dient als schneller anlaufender Umsatzkanal neben dem längeren Vertriebszyklus industrieller Projekte und als Einstiegspunkt für Kunden außerhalb des Industrie-Fokus. Umfasst Prozessberatung (Discovery Sprint / KI-Prozess-Check als Einstiegsprodukt), Automatisierung von Verwaltungs-, Dokumenten- und Kommunikationsprozessen, datenschutzkonforme lokale RAG-/Wissenssysteme sowie optionale Wartung/Weiterentwicklung (Retainer). Startangebote: Mail-Agent Starter, Ops-Automation Starter, Vision-Extraction Starter, Social-Content Starter und Voice-Agent Starter (automatisierte Telefonie mit Kennzeichnung der KI-Interaktion).

**Säule 3 – KI-Enablement & Didaktik (Befähigung, komplementär).** Schulungen, interne Befähigung und didaktisch saubere Wissensvermittlung, damit KI nicht nur eingeführt, sondern verstanden und kontrolliert genutzt wird – auch als Begleitangebot zu Säule-1-Projekten (z. B. Schulung der Instandhaltungs-/Produktionsteams im Umgang mit neu integrierten KI-gestützten Systemen). Umfasst Mitarbeiterschulung, Wissensmanagement (interner Wissens-Chatbot, Meeting-/FAQ-Aufbereitung) und EdTech-Anwendungen mit Fokus auf nachvollziehbare Lern- und Übungslogik. Kernbotschaft: KI unterstützt Menschen, sie ersetzt sie nicht.

Alle KI-generierten Inhalte und KI-Interaktionen werden gemäß Transparenzpflicht gekennzeichnet (siehe BP-COMPLIANCE-0001).

Akquise-/Einstiegskanäle: [freelancermap.de](http://freelancermap.de) (Pro-Account) als primärer Kanal für Projektakquise und Pipeline-Aufbau; Hochschulen/IHK/Bildungsträger als Zweitkanal (Dozententätigkeit; tendenziell niedrigere Honorare, genaue Werte über IHK-Beratung).

## Technisches Grundkonzept (verdichtet)

ID: BP-ARCHITEKTUR-0001

Allen Leistungsbausteinen liegt ein Architekturprinzip zugrunde: KI wird nicht als "ein Modell macht alles" umgesetzt, sondern als stabile Systemarchitektur mit austauschbaren Modellkomponenten. Der Kundennutzen ist dreifach: planbare Qualität durch passende Modellwahl, kontrollierte Kosten durch Routing und Caching sowie Datenschutz-/Compliance-Fähigkeit durch lokale bzw. Offline-Optionen.

Das Prinzip: Modelle sind austauschbare Werkzeuge, nicht der Kern. Lokale Modelle übernehmen Vorverarbeitung, Routing und kostengünstige Massenaufgaben; leistungsstarke Cloud-Modelle die anspruchsvolle Kernintelligenz; Retrieval-/Suchsysteme die Faktenaktualität. Für datenschutzsensible Kunden können Prozesse vollständig lokal betrieben werden.

Die technische Detailausarbeitung (konkrete Modellzuordnung, Hardware-/Infrastrukturlogik, Orchestrierungsmuster) ist bewusst in die technische Wissensbasis ausgelagert und nicht Teil dieses Businessplans, da modellspezifische Angaben schnell veralten. Für den Businessplan zählt das stabile Prinzip, nicht die tagesaktuelle Modellwahl.

## Vision: Digital Twin of an Organization (DTO)

ID: BP-VISION-0001

Das langfristige Zielbild ist ein "Digital Twin of an Organization" (DTO): ein dynamisches Softwaremodell des eigenen Unternehmens, in dem Kernprozesse durch KI-Agenten abgebildet und vollständig protokolliert werden. Der Begriff ist etabliert (Gartner, seit 2017) und beschreibt ein Modell, das reales organisatorisches Verhalten abbildet – nicht nur Soll-Abläufe.

Strategischer Wert: Das eigene Unternehmen dient als Proof of Concept. Die am eigenen Betrieb erprobten, automatisierten Prozesse belegen gegenüber Kunden, dass das Konzept trägt, und können als Referenz und Live-Demo vorgeführt werden.

Das Grundprinzip ist für den Gründer keine Theorie: Eine echtzeitnahe digitale Abbildung real laufender Produktionsprozesse – das, was heute als Digital Twin bezeichnet wird – wurde in der Sache bereits in der Stahlindustrie umgesetzt (logistische Prozessabbildung der Warmzone, siehe BP-GRUENDER-0001). Die DTO-Vision überträgt dieses in der Industrie bewährte Prinzip auf die eigene Unternehmensorganisation und auf Kundenprozesse.

Als Referenz- und Demonstrationsgrundlage kann ein industrielles Systemumfeld nachgebildet werden (Datenbank, Application Server, Message-oriented Middleware, angebundene Steuerungssysteme). Damit lässt sich die Integrationskompetenz konkret vorführen, ohne Kundendaten zu benötigen – ein eigener, belastbarer Referenz-Use-Case (siehe Use-Case-Übersicht & Referenzprojekte).

Realistische Einordnung (bewusst als Entwicklungspfad, nicht als erreichter Zustand): Auf der gängigen fünfstufigen Reifegradskala für digitale Zwillinge (von einmaliger Nachbildung über statische und dynamische bis zu interaktiven und autonomen Zwillingen) entspricht der aktuelle Stand mit strukturiertem Event-Logging den unteren Stufen. Das DTO ist damit ein ambitioniertes, schrittweise erreichbares Zielbild – der Wert für Kunden entsteht bereits auf den frühen Stufen (transparente, protokollierte, teilautomatisierte Prozesse), nicht erst bei voller Autonomie.

## Gründerperson und Qualifikation

ID: BP-GRUENDER-0001

Alexander Kiefer verbindet langjährige technische Entwicklungserfahrung, industrielle Prozessnähe, didaktische Vermittlungskompetenz und praktische KI-Anwendung. Diese Kombination ist für das Vorhaben besonders relevant, weil Zielkunden nicht nur Code benötigen, sondern Orientierung, verständliche Entscheidungsgrundlagen, saubere Dokumentation und sichere Umsetzung.

**Akademische Ausbildung.** [M.Sc](http://M.Sc). Kommunikationsinformatik (HTW Saar, Saarbrücken, 2008–2010), vorausgehend [B.Sc](http://B.Sc). Kommunikationsinformatik (HTW Saar, 2004–2008). Der Studiengang ist ausgeprägt hardware- und nachrichtentechnisch orientiert (u. a. Elektro-, Nachrichten- und Digitaltechnik) und bildet die fachliche Grundlage für die industrielle Anbindungskompetenz.

**Industrielle Kernerfahrung (Stahlindustrie).** Der Einstieg in die Industrie erfolgte bereits während des Masterstudiums (2009–2010) als Masterand bei Dillinger (europäischer Marktführer für Grobbleche, vollintegriertes Hüttenwerk) mit dort verfasster Masterarbeit; anschließende Übernahme. Von 2010 bis 2019 Entwicklung von Leitsystem-Software nach Spezifikation und Anforderung für das Walzwerk im 24/7-Betrieb. Dazu gehörte ein logistisches System, das die Prozesse der Warmzone digitalisiert, dokumentiert, überwacht und annähernd echtzeitnah als digitale Abbildung der real laufenden Produktionsprozesse darstellt – Datenmodell und Visualisierung wurden selbst entwickelt (Steuerstand-GUI mit Qt). Übergeordnete Leitsysteme (z. B. Ofenführungsrechner zur Regelung der Stoßöfen) waren Teil dieser Landschaft. Kern der Tätigkeit: Umsetzung von Prozessanforderungen in enger Abstimmung mit den Fachbereichen, Integration in eine heterogene Systemlandschaft mit Datenaustausch zur Automatisierungs-/Steuerungsebene (SPS/S7) über mehrere Hierarchieebenen, Betriebssicherheit unter Produktionsdruck (IT-Rufbereitschaft, Fehleranalyse, Hotfixes).

**Enterprise-Systeme & Application-Server (belegt).** Abbildung der Prozesslogik und Datenbankanbindung mit Enterprise JavaBeans (EJB); Anbindung der Backend-Systeme über den JBoss Application Server; asynchrone Kommunikation zwischen Qt-basierten Steuersystemen und dem Application Server über Message-oriented Middleware; Standardschnittstellen (SOAP-Webservices) zu externen Abteilungen wie der Produktionsplanung. Administration mehrerer Evolutionsstufen des Application Servers (von JBoss 4.7 GA über die 5er-Reihe bis WildFly) im industriellen 24/7-Umfeld mit leistungsstarker Datenbank. Diese Enterprise-Kompetenz ist zusätzlich durch eine mehrjährige Lehrtätigkeit zu Enterprise JavaBeans (Nebenfach-Vorlesungen an der HTW Saar) fundiert belegt. Die Fähigkeit, IT-Lösungen produktionskritisch in bestehende Anlagen-, Enterprise- und Systemlandschaften zu integrieren und dauerhaft zu betreiben, ist damit sowohl praktisch als auch lehrend nachgewiesen.

**Qualitäts- und Betriebsdisziplin (Industrie).** Rund neun Jahre IT-Rufbereitschaft im Produktionsumfeld: Störungsanalyse in komplexen Industriesystemen unter Produktionsdruck, auf Basis umfangreicher Logdaten. Ein produktives Industrieumfeld verzeiht keine Fehler – daraus resultiert eine ausgeprägte, belastbare Disziplin bei Softwarequalität, Testing und Release. Diese Erfahrung ist unmittelbar auf die geforderte Zuverlässigkeit KI-gestützter Produktivsysteme übertragbar.

**Weitere Entwicklungspraxis.** Modernisierung von Legacy-Anwendungen und 3-Tier-Architekturen, REST-/API-Entwicklung (Java/Java EE, .NET/C#, Node.js), Datenbank- und Datenmodellierung (PostgreSQL/SQL), Standardschnittstellen (u. a. SOAP-Webservices) – u. a. bei HTW Saar, GQF und Prego Services.

**Didaktisch-kommunikativ.** Lehramt Informatik (Quereinstieg, Saarland, 2025–2026): Unterricht planen, durchführen, evaluieren; verständliche Vermittlung komplexer Inhalte, Schulungs- und Lernmaterialien.

**Vorgehen und Qualität.** Scrum-Praxis seit 2011 (Certified Scrum Developer, Certified Scrum Product Owner), Code Reviews, Test-/Release-Disziplin.

**Unternehmerisch-kaufmännisch.** Projektsteuerung, Preislogik, Liquiditätskontrolle, Buchhaltung, Steuerberatung, IHK-/Gründungsberatung.

**Laufende KI-Qualifikation.** Zertifizierungen im Bereich Multi-Agentic Coding / KI-Implementierung (u. a. bei Everlast AI, einem AZAV-zertifizierten, staatlich zugelassenen Bildungsträger).

Alle Angaben sind durch Lebenslauf und Arbeitszeugnisse belegbar.

## Regulatorik als Geschäftsfeld (AI Act)

ID: BP-COMPLIANCE-0001

Der EU AI Act ist für das Vorhaben kein Hindernis, sondern ein Geschäftsfeld. Ab dem 02.08.2026 gelten die Transparenzpflichten (Art. 50): KI-Interaktionen und KI-generierte Inhalte sind zu kennzeichnen. Kunden müssen diese Anforderungen erfüllen – das Angebot unterstützt sie dabei als Teil der Umsetzungsleistung.

Das eigene Angebot erfüllt die Transparenzpflicht von Beginn an (Kennzeichnung KI-generierter Inhalte und Avatare). Strengere Hochrisiko-Pflichten (u. a. im Personalbereich) sind nach aktuellem Stand voraussichtlich auf Ende 2027 verschoben, aber noch nicht rechtskräftig; das Vorhaben bleibt vorsorglich auf den 02.08.2026 vorbereitet. Parallel gilt die DSGVO. (Kein Rechtsrat; maßgeblich sind die amtlichen Fassungen und Leitlinien.)

## Einreichungsstatus

ID: BP-STATUS-0001

Diese Version (1.0.0-rc) ist erstmals vorzeigereif und förderorientiert aufbereitet. Vor finaler Freigabe (Status Stable) sind zu ergänzen: konkrete Finanzzahlen und Kapitalbedarf (siehe Finanzplan-Szenarien Kapitel 3a, inkl. 12-Monats-Grobgerüst), freelancermap-Projekt-/Stundensatzdaten, 2–3 anonymisierte Beispiel-Use-Cases sowie der Status der Gründungsfinanzierung (Bürgergeld/Einstiegsgeld, siehe Kapitel 4a). Nach Einarbeitung und Prüfung wird der Status auf Stable / Version 1.0.0 gesetzt.

**Geplanter Business-Start (aktualisiert 19.09.2026):** frühestens **01.12.2026** (Gewerbeanmeldung und Tätigkeitsaufnahme), vorbehaltlich des Jobcenter-Bescheids nach dem Termin am 23.09.2026 (siehe Kapitel 4a, KAP4A-STARTDATUM-0001). Der frühere Planwert „01.09.2026" aus der Vorversion ist überholt, da er vor Klärung des Förderpfads (SGB II/Jobcenter statt SGB III/Gründungszuschuss, siehe Kapitel 4 und 4a) und vor der kritischen Antragsreihenfolge lag. Das neue Datum ist eine Annahme und nach dem Jobcenter-Termin zu bestätigen.