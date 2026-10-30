<h1 align="center">Maximilian Schneider</h1>

<p align="center">
  <strong>Applied AI Engineer · KI für Einkauf, Supply Chain und Mittelstand</strong><br>
  Python · lokale LLMs · strukturierte Ausgaben · Prozessautomatisierung
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/maximilian-schneider-4a6952309">LinkedIn</a> ·
  <a href="https://github.com/MaxXSammy?tab=repositories">Projekte</a>
</p>

<br>

Ich baue KI-Systeme, die in echten Geschäftsprozessen funktionieren müssen, nicht nur in der Demo.

Mein Hintergrund liegt im strategischen Einkauf und im Produktmanagement. Deshalb beginne ich nicht beim Modell, sondern beim Prozess: Wo geht Zeit verloren, wo entstehen Fehler, und was muss ein System leisten, damit man ihm vertrauen kann?

**Aktuell:** Weiterbildung zum AI Engineer & KI-Manager (DEKRA/TÜV-zertifiziert, bis 02/2027). Offen für Remote-Rollen in AI Engineering, AI Automation und KI-Transformation.

<br>

## Projekte

### [procurement-rag-agent](https://github.com/MaxXSammy/procurement-rag-agent) · [▶ Live-Demo](https://procurement-rag-agent.streamlit.app/)

KI-gestützte Lieferantenauswahl. Der Agent durchsucht Angebote, Selbstauskünfte und Verträge, extrahiert strukturierte Lieferantenprofile und bewertet sie nach frei einstellbaren Kriterien. Ein Dashboard zeigt der Geschäftsleitung Einsparpotenzial, Zeitersparnis und die gemessene Zuverlässigkeit des Systems.

- RAG mit Quellenangabe und Agent mit Tool Calling: Er entscheidet selbst zwischen Dokumentsuche, Ranking und Lieferantenprofil
- Belegprüfung: Jede extrahierte Zahl muss im Quelldokument stehen, sonst wird sie verworfen
- Evaluation gegen Gold-Daten mit Regel-Basislinie als Vergleich, damit der Nutzen des LLM messbar ist

<sub>Python · Ollama · RAG · Tool Calling · Pydantic · scikit-learn · Streamlit · pytest</sub>

### [n8n-supplier-mail-triage](https://github.com/MaxXSammy/n8n-supplier-mail-triage)

Self-hosted n8n-Workflow, der Lieferanten-Mails automatisch einordnet. Ein lokales LLM erkennt Angebot, Reklamation, Lieferverzug oder Rechnung und extrahiert die Daten. Danach landet die Mail als Ticket beim zuständigen Team. Unsichere und verdächtige Fälle gehen an einen Menschen.

- Validierung im Code statt Vertrauen in die Konfidenz: Belegprüfung, Pflichtfelder, Betrugsschutz bei geänderten Bankdaten, Erkennung von Prompt-Injection
- Human-in-the-loop mit Review-Queue und Formular, Error-Workflow, Retry und Duplikaterkennung
- Messung gegen Gold-Daten und zwölf Angriffstests: 0 Mails falsch automatisch geroutet

<sub>n8n · Ollama · PostgreSQL · Docker · JSON-Schema · JavaScript · Python</sub>

### [site-report-bot](https://github.com/MaxXSammy/site-report-bot)

Baustellendokumentation per Messenger. Handwerker schicken Fotos und Sprachnachrichten, und der Bot erstellt daraus einen strukturierten PDF-Bericht. Alles läuft lokal, ohne Cloud-KI.

- Halluzinationskontrolle im Code: Jeder Name und jede Zahl im Bericht wird gegen die Originalnotizen geprüft
- Kanalunabhängiger Kern mit austauschbarem LLM-Provider: Telegram ist aktiv, WhatsApp vorbereitet
- Pydantic-Schema, Dependency Injection, 27 Tests ohne echtes Modell

<sub>Python · Ollama (qwen2.5-vl) · faster-whisper · Pydantic · FastAPI · pytest</sub>

### [lieferanten-angebotsvergleich](https://github.com/MaxXSammy/lieferanten-angebotsvergleich)

Lieferantenangebote in mehreren Währungen vergleichbar machen und nach gewichteten Kriterien bewerten, mit KI-gestützter Kaufempfehlung. Die Grundlage dafür ist meine Praxis im strategischen Einkauf.

- Robuster CSV-Import, der typische Formatfehler automatisch repariert
- Live-Wechselkurse der EZB mit Fallback und gewichtetes Mehrkriterien-Scoring
- Streamlit-Oberfläche mit einstellbaren Gewichten

<sub>Python · pandas · Streamlit · OpenAI API · REST</sub>

<br>

## Arbeitsweise

| | |
|---|---|
| **Lokal zuerst** | Sensible Unternehmensdaten verlassen das Haus nicht, und Ollama-Modelle laufen auf eigener Hardware. |
| **Prüfen statt vertrauen** | LLM-Ausgaben werden validiert, sowohl durch Schemas als auch durch deterministische Checks. |
| **Ehrlich dokumentiert** | Jedes Projekt nennt seine bekannten Grenzen. |
| **Austauschbar gebaut** | Modelle und Kanäle lassen sich wechseln, ohne die Kernlogik anzufassen. |

<br>

## Stack

**Sprache & Daten:** Python, pandas, Pydantic<br>
**KI:** Ollama, OpenAI API, RAG, Tool Calling, faster-whisper, Structured Output, Evaluation<br>
**Apps & Automatisierung:** FastAPI, Streamlit, n8n, REST APIs<br>
**Qualität:** pytest, Ruff, Git
