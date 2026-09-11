# Unternehmensgründung 2026

Repository für Businessplan, Finanzplan, Geschäftsmodell und alle direkt
gründungsbezogenen Inhalte rund um Neural Automatix. Struktur folgt dem
gleichen dreistufigen Modell wie im Repo `knowledge-repository`
(inbox → unklassifiziert → knowledge).

## Struktur

- **inbox/** – Rohmaterial, ungeprüft. Hierher kommt zunächst der komplette
  Markdown-Export aus Notion (per Working Copy vom iPad gepusht).
  `lifecycle_status: inbox`, `indexing_allowed: false`, `review_required: true`.
- **unklassifiziert/** – Inhalte, die als zum Repo gehörig bestätigt sind,
  aber noch nicht nach dem Dokumenten-Styleguide strukturiert/gegliedert wurden.
  Entspricht `reviewed-unstructured/` im Wissens-Repo.
- **knowledge/** – Vollständig strukturiert, validiert, freigegeben.
  Erst danach Übernahme in die produktive RAG-Datenbank.

## Ablauf

1. Notion-Export landet 1:1 in `inbox/`.
2. Fachliche Prüfung: gehört der Inhalt wirklich hierher, oder in ein anderes
   Repo (ai-driven-development, knowledge-standards, neuralautomatix-strategy,
   avatar-agents-system, Digital-Twin-Thema, French-App)?
3. Bestätigte Inhalte wandern nach `unklassifiziert/`, werden dort nach dem
   Dokumenten-Styleguide (siehe knowledge-standards) neu gegliedert.
4. Fertige Kapitel wandern nach `knowledge/`.

## Aktueller Stand (Stand: 11.09.2026)

Business-Plan-Stand ist seit den Kapiteln 00 sowie 1–9 (Notion, Mai–Juli 2026)
unverändert und noch nicht abgeschlossen. Ziel: bis zum Fallmanagement-Termin
(23.09.2026) ein abgerundetes, abgeschlossenes Konzept inkl. erster
Implementierungsstände (Multi-Agent-Fortschritt).
