# LF7.1.3: Das Publish/Subscribe Muster mit MQTT

## 👤 User Story

> Als Protokoll-Analyst\*in  
> möchte ich das Publish/Subscribe-Konzept von MQTT verstehen,  
> damit ich entkoppelte, skalierbare und robuste Nachrichtenarchitekturen für Sensornetzwerke aufbauen kann.

## 🎉 Celebration Criteria (Lernziele)

- Ich kann den Unterschied zwischen einer Client/Server-Architektur und dem Publish/Subscribe-Muster **erklären**. (K2)
- Ich **verstehe** die Rolle und Verantwortung des MQTT-Brokers. (K2)
- Ich kann eine logische Topic-Struktur für die Datenübermittlung **aufbauen**. (K3)

## 🧠 Wissens-Briefing

- **MQTT (Message Queuing Telemetry Transport):** Der De-facto-Standard für IoT-Nachrichten. Leichtgewichtig, basiert auf TCP/IP.
- **Publish / Subscribe:** Geräte kommunizieren niemals direkt miteinander.
  - Ein Gerät _veröffentlicht_ (publish) Daten zu einem bestimmten Thema (Topic).
  - Andere Geräte _abonnieren_ (subscribe) dieses Thema.
- **Der Broker:** Der zentrale Server in der Mitte. Er empfängt alle Nachrichten und verteilt sie sofort an alle Abonnenten weiter.
- **Topics (Themen-Baum):** Werden hierarchisch aufgebaut wie Dateipfade, z.B. `fabrik/halle1/sensor/temperatur`.
- **Quality of Service (QoS):** Definiert die Zustellsicherheit.
  - _QoS 0:_ "Fire and forget" (Nachricht kann verloren gehen).
  - _QoS 1:_ "At least once" (Zustellung garantiert, kann aber doppelt ankommen).
  - _QoS 2:_ "Exactly once" (Garantierte einmalige Zustellung, höchster Overhead).

## 🚧 Typische Fallstricke & Impulsfragen

- **Der Flaschenhals:** Das Pub/Sub-Muster entkoppelt die Geräte wunderbar, aber der Broker wird zum absoluten Single Point of Failure. Fällt er aus, steht die gesamte Kommunikation still.
- **Wildcard-Chaos:** Wer zu großzügig mit Topic-Wildcards (z.B. `#` in MQTT) arbeitet, abonniert versehentlich tausende Nachrichten und überlastet kleine Microcontroller.

## 🛠️ Pflichtaufgaben (K2 & K3)

1. Vergleiche das Publish/Subscribe-Prinzip von MQTT mit der klassischen Request/Response-Architektur von HTTP.
2. Erläutere die exakte Aufgabe des Brokers in einem MQTT-Netzwerk.
3. Skizziere einen logischen MQTT-Topic-Baum für ein Gebäude mit drei Stockwerken, in dem jeweils Temperatur und Luftfeuchtigkeit gemessen werden.
4. Unterscheide die Quality of Service (QoS) Level 0, 1 und 2 hinsichtlich ihrer Netzwerkauslastung und Zuverlässigkeit.
5. Bestimme, welches QoS-Level für das Senden eines unwichtigen Temperaturwerts im Gegensatz zur Übermittlung eines kritischen Maschinen-Nothalts verwendet werden sollte.

## 🔥 Freiwillige Zusatzaufgaben (K4 & K5)

1. Analysiere das MQTT-Feature "Last Will and Testament (LWT)" und beurteile seinen Nutzen für die Überwachung von Sensor-Ausfällen in Echtzeit.
2. Beurteile die Sicherheitsrisiken, die entstehen, wenn ein MQTT-Broker ohne TLS-Verschlüsselung und ohne Authentifizierung im öffentlichen Internet betrieben wird.
3. Entwickle ein Konzept für "High Availability" (Hochverfügbarkeit), um den Broker als Single Point of Failure abzusichern (z.B. Broker-Clustering).

## 🕸️ Web-Suchwortliste

| Thema / Seite | Suchbegriffe für die Google-/Plattform-Suche |
| --- | --- |
| **Studyflix** | "MQTT Publish Subscribe Erklärung" |
| **Heise / IT-Wissen** | "MQTT QoS Level Unterschiede" |
| **Wikipedia** | "Message Broker Architektur" |