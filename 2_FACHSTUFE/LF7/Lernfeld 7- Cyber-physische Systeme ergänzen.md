# Lernfeld 7: Cyber-physische Systeme ergänzen

## 📜 Überblick & Relevanz

Cyber-physische Systeme (CPS) verbinden die physische Welt (Maschinen, Anlagen, Umwelt) über Netzwerke mit der digitalen Welt. In diesem Lernfeld durchdringen wir das Internet of Things (IoT). Wir analysieren bestehende Sensor-Aktor-Netzwerke, planen intelligente Datenvorverarbeitung (Edge Computing), entwerfen energieeffiziente Übertragungswege (Low-Power) und sichern die Kommunikation industrieller Protokolle ab. Das primäre Ziel ist es, ein System technologisch ausfallsicher zu gestalten und durch neue Sensoren auf Hardware-Ebene (I2C/SPI) zu erweitern.

## **🏆 Kernkompetenzen (Groblernziele)**

- Die Architektur und Komponenten cyber-physischer Systeme verstehen und logisch strukturieren.
- Kommunikationsmodelle und IoT-Protokolle (MQTT, LoRaWAN, etc.) bewerten und passgenau auswählen.
- Konzepte für Edge Computing und Low-Power-Design in Hardware-nahen Netzwerken anwenden.
- IoT-Systeme hinsichtlich Betriebs- und Datensicherheit (TLS/SSL, OTA-Updates) analysieren und härten.
- Die physische Anbindung neuer Hardware-Komponenten über lokale Bussysteme (I2C, SPI) planen und integrieren.

## 🎭 Die 3 Wahl-Szenarien (Der Kontext)

Euer Team entscheidet sich zu Beginn für **eines** dieser drei fiktiven Unternehmen. Ihr werdet dieses Unternehmen durch alle Epics dieses Lernfelds begleiten.

### Szenario A: OceanWatch NGO (Umwelt & Forschung)

Die Umwelt-NGO überwacht die Wasserqualität in Küstengebieten. Um auf chemische Verunreinigungen in Echtzeit reagieren zu können, soll ein Netzwerk aus autarken Sensor-Bojen aufgebaut werden. Fokus: Aggressive Salzwasser-Bedingungen, fehlende Stromversorgung, sichere Daten.

### Szenario B: Tischlerei Holz&Herz (Handwerk & Smart Factory)

Die traditionsreiche Tischlerei kämpft mit hohen Energiekosten durch alte, zentral gesteuerte Absauganlagen. Die Werkstatt soll intelligent werden: Maschinen sollen per IoT kommunizieren und die Absaugung dezentral steuern. Fokus: Hohe Ausfallsicherheit, Edge Computing, Latenz.

### Szenario C: Kühlkette Direkt (Logistik & Transport)

Das Logistik-Startup transportiert lebenswichtige Medikamente. Die Einhaltung der Temperatur ist kritisch. Das bestehende System (Auslesen per USB nach der Fahrt) soll durch Live-Alarmierung ersetzt werden. Fokus: Mobile Netzwerke, extreme Datensicherheit (Verschlüsselung auf Rastplätzen).

## 🗺️ Unsere Lernreise (Epics)

### LF7.1: Architektur & IoT-Kommunikation

Wir zerlegen cyber-physische Systeme in ihre Bausteine (Sensoren, Aktoren, Controller) und planen das Nervensystem (z.B. per MQTT oder LoRaWAN) für den reibungslosen Datenaustausch vom Endgerät bis zum Server.

### LF7.2: Edge Computing & Low-Power Design

Wir optimieren das System: Daten werden nicht mehr blind in die Cloud geschickt, sondern direkt an der Maschine (Edge) vorverarbeitet. Gleichzeitig zwingen wir autarke Sensoren in den Tiefschlaf (Deep Sleep) und reduzieren Payloads, um Batterien zu schonen.

### LF7.3: Sicherheit, Wartung & Systemintegration

Wir härten die Kommunikation gegen Angreifer (TLS/SSL), etablieren ausfallsichere Update-Mechanismen (OTA) und binden abschließend neue Sensorik über physikalische Bussysteme (I2C/SPI) in unsere Architektur ein.