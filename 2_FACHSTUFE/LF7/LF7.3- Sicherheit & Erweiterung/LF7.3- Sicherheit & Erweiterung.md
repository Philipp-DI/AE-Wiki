# LF7.3: Sicherheit & Erweiterung

## 👥 Epic User Story

> Als IoT-Consulting-Team  
> möchten wir die Datensicherheit unseres Systems härten, neue Hardware-Schnittstellen planen und das technische Konzept überzeugend präsentieren,  
> damit die Geschäftsführung das Budget für die physische Umsetzung unserer cyber-physischen Architektur freigibt.

## 🎉 Celebration Criteria (Kenkompetenzen)

- Wir können die Kommunikationswege unseres Netzwerks gegen Manipulation und Abhören (z.B. durch TLS/SSL) absichern und Schwachstellen **bewerten**. (K5)
- Wir können ein Ausfall- und Update-Konzept (Over-the-Air) für die sichere Erweiterung der Systemkomponenten im laufenden Betrieb **entwerfen**. (K6)
- Wir können die physische Anbindung neuer Sensoren an bestehende Microcontroller über lokale Bussysteme (I2C, SPI) **planen**. (K4)
- Wir können die technischen und wirtschaftlichen Vorteile unserer Gesamtlösung als adressatengerechten Elevator Pitch nach dem AIDA-Modell **argumentieren**. (K5)

## 🧩 Ganzheitliche Aufgabe

**Titel:** Der Security- & Investitions-Pitch **Schätzung:** 8 SP

Härtet euren Architekturentwurf aus den vorherigen Epics gegen IT-Sicherheitsrisiken, plant die physische Erweiterung um einen neuen Sensor und bereitet die finale Präsentation für die Geschäftsführung eures gewählten Szenarios (NGO, Tischlerei oder Logistik) vor. Teilt euch in folgende Rollen auf:

- **Krypto-Architekt\*in:** An welchen Knotenpunkten (Sensor zu Gateway, Gateway zu Cloud) muss die Kommunikation zwingend verschlüsselt werden und wie wird das Zertifikatsmanagement gelöst?
- **Operations-Manager\*in:** Wie wird sichergestellt, dass hunderte im Feld verteilte Sensoren sicher mit neuen Firmware-Updates (OTA) versorgt werden können, ohne das System bei Fehlern lahmzulegen?
- **Hardware-Integrator\*in:** Über welches lokale Bussystem (I2C vs. SPI vs. GPIO) wird der neu geforderte Sensor physisch an das Edge-Gateway angebunden und warum?
- **AIDA-Strateg\*in:** Wie wird der Spannungsbogen des Elevator Pitches aufgebaut, um innerhalb der ersten 15 Sekunden die ungeteilte Aufmerksamkeit (Attention) der Geschäftsführung zu sichern?
- **Value-Übersetzer\*in & Einwand-Behandler\*in:** Wie werden die abstrakten technischen Features (Hardware-Bus, OTA, TLS) in messbare Business-Mehrwerte übersetzt und welche kritischen Rückfragen zum Budget wird das Management stellen?

## 📦 Ergebnisartefakt

Ein technischer "Security & Integration Annex" (inkl. Hardware-Schaltplanskizze) zur bestehenden Architektur sowie ein final durchgeführter, 3-minütiger "Elevator Pitch" (mündlich präsentiert), bei dem das gesamte Team die Lösung vor dem Plenum verteidigt.