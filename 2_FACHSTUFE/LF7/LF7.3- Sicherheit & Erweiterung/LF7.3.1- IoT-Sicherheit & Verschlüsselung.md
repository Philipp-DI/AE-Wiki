# LF7.3.1: IoT-Sicherheit & Verschlüsselung

## 👤 User Story

> Als IoT-Sicherheitsspezialist\*in  
> möchte ich die Angriffsvektoren in Sensornetzwerken verstehen,  
> damit ich Verschlüsselungsprotokolle anwenden und die Vertraulichkeit sowie Integrität der Maschinendaten garantieren kann.

## 🎉 Celebration Criteria (Lernziele)

- Ich kann die Schutzziele der Informationssicherheit (CIA-Triade) auf ein IoT-System **übertragen**. (K2)
- Ich **verstehe** den Unterschied zwischen unverschlüsselter und verschlüsselter Übertragung bei industriellen Protokollen. (K2)
- Ich kann die Integration von TLS/SSL-Zertifikaten in einem Kommunikationsfluss **skizzieren**. (K3)

## 🧠 Wissens-Briefing

- **Schutzziele (CIA-Triade):** \* _Confidentiality (Vertraulichkeit):_ Daten dürfen nicht mitgelesen werden (Verschlüsselung).
  - _Integrity (Integrität):_ Daten dürfen auf dem Transportweg nicht manipuliert werden.
  - _Availability (Verfügbarkeit):_ Das System muss erreichbar bleiben (Schutz vor DDoS).
- **Klartext-Problem:** Viele IoT-Protokolle (wie MQTT auf Port 1883) senden Daten und Passwörter standardmäßig im Klartext. Jeder im Netzwerk (z.B. mit Wireshark) kann mitlesen.
- **TLS/SSL (Transport Layer Security):** Der Standard zur Verschlüsselung von Netzwerktraffic (z.B. MQTTS nutzt Port 8883).
- **Zertifikate:** Werden genutzt, um die Identität des Brokers/Servers kryptografisch zu beweisen. Der Sensor (Client) prüft das Zertifikat, bevor er Daten sendet, um Man-in-the-Middle-Angriffe (MitM) zu verhindern.
- **Hardware-Einschränkungen:** Kryptografie kostet viel Rechenleistung. Sehr kleine, batteriebetriebene Sensoren haben oft Schwierigkeiten, komplexe TLS-Handshakes durchzuführen (Lightweight Cryptography wird hier erforscht).

## 🚧 Typische Fallstricke & Impulsfragen

- **Default-Passwörter:** Das größte IoT-Risiko ist nicht eine geknackte Verschlüsselung, sondern Sensoren, die massenhaft mit dem Passwort "admin" ausgeliefert und ins Netz gehängt werden (Mirai-Botnetz).
- **Zertifikats-Ablauf:** Zertifikate haben ein Ablaufdatum. Wenn ein Sensor-Zertifikat nach 3 Jahren abläuft und kein Update-Mechanismus existiert, verweigert der Sensor dauerhaft den Dienst.

## 🛠️ Pflichtaufgaben (K2 & K3)

1. Erläutere, wie eine fehlende Daten-Integrität in einem cyber-physischen System (z.B. bei einem Temperatur-Sensor für einen Hochofen) zu physischen Schäden führen kann.
2. Skizziere den grundlegenden Ablauf eines TLS-Handshakes zwischen einem IoT-Sensor und einem MQTT-Broker.
3. Vergleiche die Kommunikation über MQTT (Port 1883) mit MQTTS (Port 8883) hinsichtlich des Schutzes gegen "Man-in-the-Middle"-Angriffe.
4. Identifiziere drei typische Einfallstore (Angriffsvektoren) in einem lokalen Smart-Home-Netzwerk, das ans Internet angeschlossen ist.
5. Bestimme die Konsequenzen für das Energiemanagement (Batterielaufzeit) eines Sensors, wenn für jede Nachricht ein vollständiger TLS-Verbindungsaufbau erzwungen wird.

## 🔥 Freiwillige Zusatzaufgaben (K4 & K5)

1. Analysiere das Konzept der "Lightweight Cryptography" (z.B. nach NIST-Standard) und ihre Bedeutung für extrem ressourcenbeschränkte Microcontroller.
2. Beurteile die Sicherheitsarchitektur eines Systems, das zwar End-to-End-Verschlüsselung nutzt, aber physisch ungeschützte Sensoren an öffentlichen Orten einsetzt.
3. Entwickle eine Strategie für das "Certificate Rotation" (den automatisierten Austausch ablaufender Zertifikate) für hunderte autarke IoT-Geräte im Feld.

## 🕸️ Web-Suchwortliste

| Thema / Seite | Suchbegriffe für die Google-/Plattform-Suche |
| --- | --- |
| **Elektronik-Kompendium** | "IoT Security CIA Triade" |
| **Studyflix** | "TLS Handshake einfach erklärt" |
| **Wikipedia** | "Mirai Botnetz IoT" |