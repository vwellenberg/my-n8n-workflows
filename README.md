# my-n8n-workflows

Sammlung meiner [n8n](https://n8n.io/) Workflows zur automatisierten Nachrichtenanalyse, KI-gestützten Contentbewertung und Trading-relevanten Benachrichtigungen.

## Workflows

### Aivin-MAS

Multi-Agent-System, das über Telegram gesteuert wird. Verarbeitet verschiedene Datenquellen wie Aktienkurse (Alpha Vantage), Fitnessstudio-Pläne (ActivityFellbach), Google Calendar und Websuchen (SerpAPI). Verwaltet Google Tasks mit KI-generierten Inhalten.

### Analyze content

Zentraler Analyse-Workflow, der von anderen Workflows aufgerufen wird. Bewertet Inhalte per GPT nach Relevanz für AI/Tech-Themen und Aktienmarkt-Impact. Sendet gefilterte Benachrichtigungen via Telegram an relevante Empfänger.

### Analyze news (Tagesschau - Wirtschaft)

Überwacht minütlich den Tagesschau-Wirtschafts-RSS-Feed, lädt vollständige Artikel und übergibt sie an den Content-Analyzer.

### Analyze news (the-decoder)

Prüft stündlich den RSS-Feed von the-decoder.com auf AI/Tech-News und leitet relevante Artikel an den Content-Analyzer weiter.

### Claude-Analyzer: Gmail

Überwacht stündlich ungelesene Gmail-Nachrichten, analysiert sie per GPT auf Trading-relevante Erkenntnisse und benachrichtigt via Telegram, wenn relevante Marktinformationen gefunden werden.

### Error-Trigger

Globaler Error-Handler, der bei Workflow-Fehlern Benachrichtigungen via Telegram sendet.

### Watch Tagesschau-News

Überwacht minütlich den allgemeinen Tagesschau-RSS-Feed, lädt Artikel und leitet sie an den Analyzer weiter.

### Watch Trump posts

Überwacht minütlich Trumps Truth-Social-Feed, bereinigt Texte per GPT und analysiert Inhalte auf Trading-Relevanz.

## Tech-Stack

- **n8n** — Workflow-Automatisierung
- **OpenAI GPT** — Contentanalyse und Relevanzbewertung
- **Telegram** — Benachrichtigungen und Steuerung
- **RSS Feeds** — Tagesschau, the-decoder, Truth Social
- **APIs** — Alpha Vantage, SerpAPI, Gmail, Google Calendar/Tasks
