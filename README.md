# Beschwerden automatisch beantworten (Entwürfe)

Erweiterung meines Projekts "Kundennachrichten sortieren": Claude ordnet
Kundennachrichten ein (Lob, Beschwerde, Frage, Sonstiges) und erstellt für
Beschwerden einen höflichen Antwortentwurf.

## Was es macht
- Liest Nachrichten aus `eingang.csv`
- Ordnet jede Nachricht einer Kategorie zu
- Erstellt nur für Beschwerden einen Antwortentwurf
- Speichert alles in `ausgang.csv`

## Technik
Python, Pandas, Anthropic API, Google Colab

## So nutzt du es
1. Notebook in Google Colab öffnen (Button: "Open in Colab")
2. Eigenen API-Key als Secret `ANTHROPIC_API_KEY` in Colab speichern
3. Zelle ausführen

## Wichtig
Die Antworten sind **Entwürfe**. Ein Mensch prüft sie, bevor etwas an Kunden
geht. Die Regeln im Prompt verhindern konkrete Versprechen (Fristen, Erstattungen),
trotzdem kann ein Sprachmodell Fehler machen und nicht jedes Mal gleich antworten.

## Was ich dabei gelernt habe
System-Prompts mit klaren Regeln, zeilenweise Verarbeitung mit Pandas (`apply`),
Prompts nachschärfen anhand der Ergebnisse.

## Hinweis
Der API-Key liegt als Secret in Colab und steht nicht im Code.
