# LF7.1: Architektur & IoT-Kommunikation

## 👥 Epic User Story

> Als IoT-Architektur-Team  
> möchten wir die logische und physische Kommunikationsstruktur für unser cyber-physisches System entwerfen,  
> damit alle Sensordaten ausfallsicher, energieeffizient und skalierbar verarbeitet werden können.

## 🎉 Celebration Criteria (Kernkompetenzen)

- Wir können die Systemarchitektur vom Endgerät (Edge) bis zur zentralen Verarbeitung (Cloud/Server) als logischen und physischen Netzwerkplan **visualisieren**. (K4)
- Wir können das passende Kommunikationsprotokoll basierend auf den Parametern Reichweite, Latenz und Energiebedarf für unser spezifisches Szenario **evaluieren** und fundiert **auswählen**. (K5)
- Wir können die Ausfallsicherheit (Single Points of Failure) unseres Architekturentwurfs kritisch **beurteilen** und Optimierungen **vorschlagen**. (K6)

## 🧩 Ganzheitliche Aufgabe

**Titel:** Das Architektur-Board **Schätzung:** 8 SP

Übertragt das Wissen aus den vorangegangenen Lern-Stories auf euer zu Beginn gewähltes Szenario (OceanWatch NGO, Tischlerei Holz&Herz oder Kühlkette Direkt). Erstellt einen ersten umfassenden Architekturentwurf für dieses Unternehmen. Teilt euch in folgende Rollen auf:

- **Hardware-Scout:** Welche spezifischen Sensoren und Aktoren sind für die physischen Umgebungsvariablen in diesem Szenario zwingend erforderlich und wie müssen diese lokal angebunden werden?
- **Protokoll-Architekt\*in:** Welches IoT-Funk- oder Kabel-Protokoll löst den Spannungsbogen zwischen der im Szenario geforderten Reichweite und dem verfügbaren Energiebudget am effektivsten?
- **Topologie-Zeichner\*in:** Wie sieht der vollständige visuelle Pfad eines Datenpakets von der Erfassung am Sensor über Gateways bis zur finalen Datenbank aus?
- **Datenfluss-Designer\*in:** Wie müssen die Nachrichteninhalte (z.B. der MQTT-Topic-Tree) logisch strukturiert sein, um später problemlos auf hunderte neue Sensoren skaliert werden zu können?
- **Risiko-Analyst\*in:** An welchen kritischen Netzwerkknoten bricht die Kommunikation bei einem Teilausfall im Szenario zusammen und wie lassen sich diese Risiken abmildern?

## 📦 Ergebnisartefakt

Ein präsentierbarer, digitaler oder analoger Netzwerkplan (Topologie) inklusive einer technischen Dokumentation. Diese Dokumentation enthält die Begründung für die Protokollwahl, die logische Datenstruktur und eine initiale Risikoanalyse.