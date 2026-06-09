# LF7.2: Edge Computing & Low-Power Design

## 👥 Epic User Story

> Als IoT-Entwickler-Team  
> möchten wir eine lokale Vorverarbeitungslogik (Edge) und ein strenges Energiemanagement für unser cyber-physisches System entwerfen,  
> damit das System auch bei Netzwerkausfällen autark reagieren kann und batteriebetriebene Sensoren über Monate wartungsfrei arbeiten.

## 🎉 Celebration Criteria (Kernkompetenzen)

- Wir können ein Edge-Computing-Konzept für unser gewähltes Szenario **entwickeln**, das die Cloud-Abhängigkeit und Latenz signifikant reduziert. (K5)
- Wir können die Batterielaufzeit unserer autonomen Sensorknoten durch die Orchestrierung von Deep-Sleep-Phasen und Interrupts **bewerten** und **optimieren**. (K6)
- Wir können ein hocheffizientes Datenformat (Payload) für die Übertragung **entwerfen**, um die Sendezeit und den Energieverbrauch zu minimieren. (K5)

## 🧩 Ganzheitliche Aufgabe

**Titel:** Das Autarkie- und Effizienz-Konzept **Schätzung:** 8 SP

Übertragt das erlernte Wissen zu Edge Computing, Deep Sleep und Datenreduktion auf euer zu Beginn gewähltes Szenario (OceanWatch NGO, Tischlerei Holz&Herz oder Kühlkette Direkt). Erstellt ein Konzept, das euer System so autark und energieeffizient wie möglich macht. Teilt euch in folgende Rollen auf:

- **Edge-Architekt\*in:** Welche spezifischen Berechnungen oder Schwellenwert-Prüfungen müssen zwingend lokal auf dem Gateway/Microcontroller stattfinden, bevor Daten gesendet werden?
- **Energie-Manager\*in:** Wie sieht der genaue Lebenszyklus eines batteriebetriebenen Sensors aus (Wann schläft er, was weckt ihn auf, wie lange ist er wach)?
- **Payload-Optimierer\*in:** Wie muss die Datenstruktur (z.B. von JSON zu Hexadezimal/Binär) für eine einzelne Übertragung komprimiert werden, um Sendezeit zu sparen?
- **Latenz-Prüfer\*in:** Welche kritischen Prozesse im Szenario dürfen auf keinen Fall auf eine Antwort aus dem Internet warten und wie stellt die Edge-Logik dies sicher?
- **Ressourcen-Analyst\*in:** Welchen Einfluss haben die gewählten Edge-Berechnungen auf die benötigte Hardware-Leistung (RAM/CPU) des lokalen Gateways?

## 📦 Ergebnisartefakt

Ein "Efficiency & Edge Design Document", das Flussdiagramme für die Datenvorverarbeitung am Edge-Gateway enthält, die Sleep-Zyklen der Sensoren dokumentiert und das optimierte Payload-Format (vorher/nachher Vergleich) aufzeigt.