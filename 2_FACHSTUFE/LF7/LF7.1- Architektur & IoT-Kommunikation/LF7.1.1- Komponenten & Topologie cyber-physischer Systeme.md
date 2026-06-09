# LF7.1.1: Komponenten & Topologie cyber-physischer Systeme

## 👤 User Story

> Als System-Integrator\*in  
> möchte ich die physischen und logischen Grundbausteine eines cyber-physischen Systems (CPS) unterscheiden,  
> damit ich den Aufbau von Hardware-Netzwerken systematisch planen kann.

## 🎉 Celebration Criteria (Lernziele)

- Ich kann den Unterschied zwischen Sensoren und Aktoren **benennen**. (K1)
- Ich **verstehe** die Rolle eines Gateways als Brücke zwischen lokalen Geräten und dem globalen Netzwerk. (K2)
- Ich kann den grundlegenden Datenfluss von der physischen Erfassung bis zur IT-Ebene **skizzieren**. (K3)

## 🧠 Wissens-Briefing

- **Cyber-physische Systeme (CPS):** Verbinden die physische Welt (Mechanik/Elektronik) mit der digitalen Welt (IT-Netzwerke, Software). Sie sind die Basis des Internet of Things (IoT).
- **Sensor vs. Aktor:** \* _Sensoren:_ Erfassen physische Umgebungsdaten (Temperatur, Druck, Helligkeit) und wandeln sie in elektrische Signale um.
  - _Aktoren:_ Empfangen digitale Befehle und wandeln diese in mechanische Arbeit oder physische Reaktionen um (Motoren, Ventile, LEDs, Heizungen).
- **Controller/Microcontroller:** Das lokale "Gehirn" (z.B. ein ESP32 oder Arduino), das Sensordaten ausliest und Aktoren steuert.
- **Gateways:** Knotenpunkte, die lokale, teils inkompatible Netzwerke (z.B. Bluetooth-Sensoren) mit weitreichenden IP-Netzwerken (Internet/WLAN) verbinden und Protokolle übersetzen.

## 🚧 Typische Fallstricke & Impulsfragen

- **Verwechslungsgefahr:** Ein Sensor misst nur den Zustand. Er kann niemals aktiv eine Maschine abschalten – der Controller muss den Messwert auswerten und den Befehl an einen Aktor senden.
- **Topologie-Irrtum:** Nicht jeder Sensor muss direkt mit dem Internet verbunden sein. Oft sammeln Gateways die Daten von Dutzenden "dummen" Sensoren per Funk und leiten sie gebündelt weiter.

## 🛠️ Pflichtaufgaben (K2 & K3)

1. Erläutere die grundlegenden Unterschiede zwischen einem Sensor und einem Aktor anhand ihrer Funktion im Datenkreislauf.
2. Skizziere einen logischen Datenfluss von der reinen Datenerfassung an der Maschine bis zur Auslösung einer physischen Reaktion.
3. Erkläre die Notwendigkeit eines IoT-Gateways in einem Netzwerk, das aus reinen Bluetooth-Sensoren besteht, aber über das Internet überwacht werden soll.
4. Vergleiche eine Stern-Topologie mit einer Mesh-Topologie hinsichtlich der Kommunikation zwischen einzelnen Sensorknoten.
5. Bestimme die Voraussetzungen, unter denen ein Microcontroller gleichzeitig die Rolle eines Endgeräts und die eines Gateways übernehmen kann.

## 🔥 Freiwillige Zusatzaufgaben (K4 & K5)

1. Analysiere die Ausfallsicherheit einer reinen Cloud-Architektur im Vergleich zu einer Architektur, in der lokale Controller Notfall-Routinen für Aktoren beinhalten.
2. Beurteile die Auswirkungen auf das Netzwerk, wenn dumme Sensoren durch "Smart Sensors" ersetzt werden, die bereits Vorverarbeitungen (z.B. Durchschnittswerte) durchführen.
3. Entwickle ein Konzept zur physischen Absicherung von IoT-Gateways in öffentlich zugänglichen, rauen Industrieumgebungen.

## 🕸️ Web-Suchwortliste

| Thema / Seite | Suchbegriffe für die Google-/Plattform-Suche |
| --- | --- |
| **Wikipedia** | "Cyber-physisches System Definition" |
| **Studyflix** | "Aktorik Sensorik Unterschied" |
| **Elektronik-Kompendium** | "IoT Gateway Funktion" |