# LF7.2.1: Edge Computing Architektur

## 👤 User Story

> Als System-Architekt\*in  
> möchte ich das Konzept der lokalen Datenverarbeitung (Edge Computing) verstehen,  
> damit ich Latenzzeiten und Netzwerkabhängigkeiten in cyber-physischen Systemen minimieren kann.

## 🎉 Celebration Criteria (Lernziele)

- Ich kann den Unterschied zwischen Cloud Computing und Edge Computing **benennen**. (K1)
- Ich **verstehe**, wie lokale Gateways Sensordaten filtern und aggregieren. (K2)
- Ich kann ein Szenario **skizzieren**, in dem Edge Computing zwingend erforderlich ist. (K3)

## 🧠 Wissens-Briefing

- **Edge Computing:** Daten werden nicht mehr roh an zentrale Server (Cloud) gesendet, sondern direkt an der "Kante" (Edge) des Netzwerks verarbeitet – z.B. auf dem Sensor selbst oder einem lokalen Gateway (wie einem Raspberry Pi).
- **Vorteile:** \* _Latenz:_ Millisekunden-Reaktionen, da der Weg ins Internet entfällt (wichtig bei Notabschaltungen).
  - _Bandbreite:_ Es werden nur noch aggregierte Daten oder Alarme gesendet ("Temperatur zu hoch" anstatt 1.000 Messwerte pro Sekunde).
  - _Autarkie:_ Die Anlage funktioniert auch bei einem Ausfall der Internetverbindung weiter.
- **Gateways:** Dienen als Brücke zwischen den lokalen (dummen) Sensoren und dem Internet. Sie übersetzen oft Protokolle (z.B. Bluetooth zu MQTT via WLAN).

## 🚧 Typische Fallstricke & Impulsfragen

- **Die Kostenfalle:** Edge Computing verlagert die Rechenleistung nach unten. 50 leistungsstarke Edge-Gateways sind in der Anschaffung und Wartung oft teurer als ein zentraler Cloud-Server.
- **Sicherheit:** Ein lokales Gateway in einer Werkhalle ist physisch leichter anzugreifen als ein hochgesichertes Rechenzentrum in Frankfurt.

## 🛠️ Pflichtaufgaben (K2 & K3)

1. Erläutere die Hauptunterschiede zwischen Edge Computing und Cloud Computing anhand der Faktoren "Latenz" und "Bandbreite".
2. Vergleiche die Ausfallsicherheit eines Cloud-basierten Systems mit der eines Edge-basierten Systems bei einem Ausfall des externen Internet-Providers (ISP).
3. Skizziere einen Datenfluss, bei dem ein Edge-Gateway aus 100 Roh-Messwerten pro Minute nur einen einzigen Durchschnittswert berechnet und weiterleitet.
4. Bestimme, welche Arten von Daten zwingend lokal verarbeitet werden müssen und welche unbedenklich in eine Cloud ausgelagert werden können.
5. Konstruiere ein lokales Regelwerk (Wenn-Dann-Logik) für einen Microcontroller, das ohne Internetverbindung einen Aktor auslöst.

## 🎉 Freiwillige Zusatzaufgaben (K4 & K5)

1. Analysiere die potenziellen Sicherheitsrisiken, die entstehen, wenn Daten dezentral auf vielen Edge-Gateways statt in einem zentralen Rechenzentrum gespeichert werden.
2. Beurteile, inwiefern Edge Computing bei der Einhaltung strenger Datenschutzrichtlinien (DSGVO) vorteilhaft gegenüber Cloud-Lösungen sein kann.
3. Entwickle eine Strategie, wie dezentrale Edge-Geräte (z.B. 100 Gateways) ohne physischen Zugriff zentral mit Firmware-Updates versorgt werden können.

## 🕸️ Web-Suchwortliste

| Thema / Seite | Suchbegriffe für die Google-/Plattform-Suche |
| --- | --- |
| **Studyflix** | "Edge Computing vs Cloud Computing" |
| **Elektronik-Kompendium** | "IoT Gateway Funktion" |
| **Wikipedia** | "Nebelrechnen / Fog Computing" |