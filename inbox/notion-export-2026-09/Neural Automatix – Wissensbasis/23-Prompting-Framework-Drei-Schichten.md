# 23-Prompting-Framework-Drei-Schichten

Bereich: B-Wissen
Schutzklasse: vertraulich
Soll-Knoten: F-Wissen
Status: Draft

Block ID: KB-PROMPT-0030

Kategorie: Prompt Library

Hierarchieebene: Root (#)

Beschreibung: Verbindliches Drei-Schichten-Modell fürs Prompting (Allgemein × Domäne × Modell) inkl. Kombinationsregel und Domänen für Text und Bild/Video.

Für KI relevant: Yes

Übergeordnete Seite: KB-PROMPT-0020

Verknüpfte Seiten: KB-PROMPT-0020, KB-AIAG-0019, KB-REF-0026

Letzte Änderung um: 07.07.2026 15:32

<aside>

💡

**Überblick**

Dieses Regelwerk definiert, wie Prompts aus drei entkoppelten Schichten zusammengesetzt werden: **Allgemein** (universelle Best Practices) × **Domäne** (aufgabenspezifisch, z. B. Software, Text, Bild/Video) × **Modell** (herstellerspezifisch, austauschbar). Die bestehende Prompt Library (KB-PROMPT-0020) ist dabei die erste Domäne (Software/SDLC) und wird nicht ersetzt, sondern eingeordnet.

</aside>

## 🎯 Ziel

ID: PROMPT_FRAMEWORK_GOAL

- Wiederholbar hochwertige Prompts durch klare Trennung von allgemeingültigen, domänenspezifischen und modellspezifischen Anteilen.
- Die volatilste Schicht (Modell) ist austauschbar, ohne allgemeine Regeln oder Domänenlogik anzufassen — analog zum „Rolle-nicht-Modell"-Prinzip.
- Reduktion von Prompt Drift und Halluzinationsrisiko über alle Domänen hinweg.

## 📥 Input

ID: PROMPT_FRAMEWORK_INPUT

- Aufgabenstellung + Domäne (Software / Text / Bild/Video / …)
- Zielmodell bzw. Modellklasse (z. B. Reasoning-Cloud-Modell, lokales Coder-Modell)
- Kontext/Constraints (Scope, Security, Compliance, Stil, Format)
- Bestehende Prompt-Templates der jeweiligen Domäne

## 📤 Output

ID: PROMPT_FRAMEWORK_OUTPUT

- Zusammengesetzter, einsatzfertiger Prompt (Allgemein + Domäne + Modell)
- Nachvollziehbare Herkunft je Prompt-Bestandteil (welche Schicht/ID)
- Optional: Varianten je Modellklasse

## 🧠 Methoden und Vorgehen

ID: PROMPT_FRAMEWORK_METHODS

<aside>

📌

**Die drei Schichten (Definition)**

- **Schicht 1 – Allgemein (PROMPT_LAYER_GENERAL):** universelle Best Practices, modell- und domänenunabhängig. Stabilste Schicht.
- **Schicht 2 – Domäne (PROMPT_LAYER_DOMAIN):** aufgabenspezifische Muster. Instanzen: Software (KB-PROMPT-0020), Text (PROMPT_DOMAIN_TEXT), Bild/Video (PROMPT_DOMAIN_VISUAL). Mittlere Stabilität.
- **Schicht 3 – Modell (PROMPT_LAYER_MODEL):** herstellerspezifische Eigenheiten/Guidance (z. B. Anthropic/Claude, OpenAI/GPT). Volatilste Schicht, bewusst zuletzt und austauschbar.

</aside>

<aside>

✅

**Kombinationsregel (Reihenfolge verbindlich)**

Ein einsatzfertiger Prompt entsteht durch Zusammensetzen in dieser Reihenfolge:

1. Allgemeine Basis (Schicht 1) setzen.
2. Domänen-Template (Schicht 2) auflegen — konkretisiert Aufgabe, Output-Format, Checks.
3. Modell-Anpassung (Schicht 3) ergänzen — nur was das konkrete Modell braucht.

Regel: Schicht 3 darf Schicht 1/2 nur ergänzen, nie deren Kernaussagen überschreiben. Wird die Domäne oder das Modell gewechselt, bleiben die jeweils anderen Schichten unverändert.

</aside>

### Schicht 1 – Allgemeine Best Practices

ID: PROMPT_LAYER_GENERAL

- **Rolle/Persona** klar benennen (z. B. „Du bist Requirements-Analyst").
- **Kontext** explizit liefern (Input-Links/Auszüge), keine impliziten Annahmen.
- **Aufgabe** eindeutig und schrittweise formulieren.
- **Constraints** setzen (Scope/Security/„no invention rule" — keine neuen Features/Fakten erfinden).
- **Output-Format** vorgeben (Tabellen/Listen/Überschriften), keine Textwände.
- **Checks** verlangen (Qualitätskriterien, offene Risiken, Annahmen).

Dies ist die explizit gemachte Fassung des bereits in KB-PROMPT-0020 genutzten Prompt-Standards (Kontext/Aufgabe/Constraints/Output/Checks).

### Schicht 2 – Domänen

ID: PROMPT_LAYER_DOMAIN

- **Software/SDLC:** bestehende Prompt Library KB-PROMPT-0020 (Analyse, Architektur, Implementierung, Testing, Review, Doku). Wird hier nur referenziert.
- **Text:** siehe PROMPT_DOMAIN_TEXT.
- **Bild/Video:** siehe PROMPT_DOMAIN_VISUAL.

Regel: Neue Domänen folgen demselben Prompt-Standard aus Schicht 1 und bekommen eine eigene ID `PROMPT_DOMAIN_<NAME>`.

### Schicht 3 – Modelle

ID: PROMPT_LAYER_MODEL

- Modell-Anpassungen werden **klassenbasiert** gepflegt (z. B. „Reasoning-Cloud-Modell", „lokales Coder-Modell"), nicht an einen Produktnamen gekettet.
- Konkrete Hersteller-Guidance (Anthropic zu Claude, OpenAI zu GPT) wird als austauschbarer Zusatz je Klasse hinterlegt und regelmäßig gegen den aktuellen Stand geprüft.
- Da diese Schicht am schnellsten altert, enthält sie einen Prüf-/Aktualisierungsvermerk.

### Domäne Text (Prompt-Set)

ID: PROMPT_DOMAIN_TEXT

<aside>

📌

**Metadaten (Prompt Standard)** — identisch zu KB-PROMPT-0020: Kontext, Aufgabe, Constraints, Output-Format, Checks.

</aside>

**Template Text 1 – Marketing-/Werbetext**

```
Du bist erfahrener Werbetexter.
Kontext:
- Produkt/Angebot:
- Zielgruppe/Persona:
- Tonalität/Marke:
Aufgabe:
- Erstelle 3 Textvarianten (kurz/mittel/lang) für [Kanal].
Constraints:
- Keine unbelegten Versprechen; Fakten nur aus Kontext.
- KI-Kennzeichnung berücksichtigen, wenn veröffentlicht (Transparenzpflicht).
Output:
- Tabelle: Variante | Text | Länge | Einsatzkanal
Checks:
- Passt Tonalität zur Marke? Belege für alle Aussagen vorhanden?
```

**Template Text 2 – Strukturierte Zusammenfassung**

```
Du bist Fachredakteur.
Kontext:
- Quelltext/Dokument:
Aufgabe:
- Fasse in [N] Kernpunkten zusammen, ohne Inhalte hinzuzuerfinden.
Constraints:
- Nur Aussagen aus der Quelle; Unsicherheiten kennzeichnen.
Output:
- Bulletliste + 1 Satz Kernaussage
Checks:
- Ist jede Aussage in der Quelle belegt?
```

### Domäne Bild/Video (Prompt-Set)

ID: PROMPT_DOMAIN_VISUAL

<aside>

📌

**Metadaten (Prompt Standard)** — identisch zu KB-PROMPT-0020: Kontext, Aufgabe, Constraints, Output-Format, Checks. Zusätzlich bei visuellen Prompts: Struktur/Komposition zuerst, Details/Stil danach.

</aside>

**Template Bild 1 – Struktur-zuerst-Bildprompt**

```
Rolle: Bild-Prompt-Designer.
Kontext:
- Motiv/Szene:
- Zweck (z. B. Flyer, Web-Header):
Aufgabe:
- Baue den Prompt in Schichten: (1) Komposition/Layout, (2) Hauptobjekte,
  (3) Stil/Farbe/Licht, (4) technische Parameter.
Constraints:
- Keine geschützten Marken/Charaktere; keine realen Personen ohne Freigabe.
Output:
- Fertiger Bildprompt + kurze Begründung je Schicht
Checks:
- Ist die Komposition eindeutig? Sind Stilangaben konsistent?
```

**Template Video 1 – Shot-/Sequenzplan**

```
Rolle: Video-Prompt-Designer.
Kontext:
- Botschaft/Story:
- Dauer/Format:
Aufgabe:
- Zerlege in Shots: pro Shot Bildinhalt, Kamera, Bewegung, Dauer.
Constraints:
- Konsistente Figuren/Stil über Shots; Übergänge benennen.
Output:
- Tabelle: Shot | Inhalt | Kamera/Bewegung | Dauer
Checks:
- Ergibt die Shotfolge eine klare Sequenz? Stil durchgehend konsistent?
```

## 🧠 KI-Agent Aufgaben

ID: PROMPT_FRAMEWORK_AI_TASKS

- Beim Prompt-Bau die drei Schichten in korrekter Reihenfolge zusammensetzen und Herkunft je Bestandteil (Schicht/ID) ausweisen.
- Prüfen, ob Schicht 3 (Modell) Schicht 1/2 nur ergänzt und nichts Kernhaftes überschreibt.
- Vorschläge machen (keine Freigaben): finaler Prompt-Einsatz erfolgt nach menschlichem Review (siehe KB-AIAG-0019).

## ✅ Qualitätskriterien

ID: PROMPT_FRAMEWORK_QUALITY

- Jeder zusammengesetzte Prompt lässt sich in Allgemein/Domäne/Modell zerlegen.
- Domänen-Templates folgen dem Prompt-Standard (Kontext/Aufgabe/Constraints/Output/Checks).
- Modell-Schicht ist klassenbasiert und trägt einen Aktualisierungsvermerk.
- Keine „no invention"-Verstöße (keine erfundenen Fakten/Features).

## 🔎 Review Checkliste

ID: PROMPT_FRAMEWORK_REVIEW

- Sind alle drei Schichten sauber getrennt und einzeln austauschbar?
- Ist die Domäne korrekt gewählt und referenziert (Software → KB-PROMPT-0020)?
- Ist die Modell-Schicht aktuell (Datum des letzten Abgleichs geprüft)?
- Enthält der Prompt Checks/Qualitätskriterien?

## 🔗 Referenzen

ID: PROMPT_FRAMEWORK_REFERENCES

- [16 Prompt Library](16%20Prompt%20Library.md) (KB-PROMPT-0020, Domäne Software)
- [15 AI Agent Instructions](15%20AI%20Agent%20Instructions.md) (KB-AIAG-0019, Human-in-the-Loop)
- [19 AI Reference Index](19%20AI%20Reference%20Index.md) (KB-REF-0026, ID-Lookup)