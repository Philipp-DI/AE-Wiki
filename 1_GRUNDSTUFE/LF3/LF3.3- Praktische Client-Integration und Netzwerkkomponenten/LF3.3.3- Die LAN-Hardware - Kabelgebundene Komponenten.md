# LF3.3.3- Die LAN-Hardware - Kabelgebundene Komponenten

Als **Netzwerktechniker**

möchte ich die verschiedenen kabelgebundenen Netzwerkkomponenten und Kabeltypen unterscheiden können,

damit ich das Netzwerk der "Innovate GmbH" korrekt aufbauen und bei Bedarf erweitern oder Fehler an der physischen Schicht finden kann.

# Celebration Criteria

- Wir können die Funktionsweise eines Hubs, einer Bridge und eines Switches vergleichen und erklären, warum der Switch sich durchgesetzt hat.
- Wir können die Rolle eines Gateways als Übergang zwischen zwei unterschiedlichen Netzwerken beschreiben.
- Wir können die verschiedenen Schirmungsarten von Twisted-Pair-Kabeln (z.B. U/UTP, F/UTP, S/FTP) erkennen und ihre Einsatzbereiche zuordnen.
- Wir können den Anwendungsbereich von Fibre Channel und SFP-Modulen zur Hochgeschwindigkeits-Anbindung von Servern und Switches erläutern.

# Wissens-Briefing

## Aktive Netzwerkkomponenten

- **Hub:** Veralteter "dummer" Verteiler. Leitet eingehende Datenpakete einfach an alle anderen Ports weiter. Führt zu Datenkollisionen und ineffizienter Netzwerkauslastung.
- **Bridge:** Verbindet zwei Netzwerksegmente. Lernt, welche Geräte sich in welchem Segment befinden, und leitet Daten nur bei Bedarf weiter.
- **Switch:** Moderner "intelligenter" Verteiler. Lernt die MAC-Adressen aller angeschlossenen Geräte und leitet Datenpakete gezielt nur an den Port des tatsächlichen Empfängers. Standard im heutigen LAN.
- **Router:** Verbindet unterschiedliche Netzwerke miteinander (z.B. das heimische LAN mit dem Internet). Arbeitet auf Basis von IP-Adressen, um den besten Weg für Datenpakete zu finden.
- **Gateway:** Ein Übergang zwischen zwei fundamental unterschiedlichen Netzen. Oft ist der Router auch das Standardgateway für die Clients in einem LAN.

## Hochgeschwindigkeitsverbindungen

- **SFP (Small Form-factor Pluggable):** Kompakte, modulare Einschübe (Transceiver) für Switches oder Server, die es ermöglichen, verschiedene Kabeltypen (z.B. Glasfaser, Kupfer) für schnelle Verbindungen (1 Gbit/s, 10 Gbit/s und mehr) flexibel zu nutzen.
- **Fibre Channel:** Ein spezielles Hochgeschwindigkeitsprotokoll, das primär zur Anbindung von Speichernetzwerken (SAN - Storage Area Network) verwendet wird.

# Aufgaben

1.  **Analyse & Identifikation:** Ihr packt die gelieferte Hardware für die "Innovate GmbH" aus. Darunter ist ein Gerät, das als "Router/Gateway" und eines, das als "Switch" bezeichnet ist. Erklärt anhand der Anschlüsse und Funktionen, welches Gerät welche Aufgabe im Netzwerk übernimmt.
2.  **Kabel-Zuordnung:** In der Materialkiste liegen verschiedene Patchkabel (U/UTP und S/FTP). Entscheidet, welches Kabel ihr für die Verbindung der PCs im normalen Büroumfeld und welches ihr eventuell für die Verbindung vom Switch zum Server in der Nähe einer möglichen Störquelle (z.B. Klimaanlage) verwenden würdet. Begründet eure Wahl.
3.  **Recherche & Planung:** Der Geschäftsführer überlegt, einen leistungsfähigen zentralen Server anzuschaffen. Recherchiert, was ein "10G SFP+ Port" an einem Switch bedeutet. Skizziert, wie man den Server über ein SFP+ Modul und ein passendes Kabel (Glasfaser oder DAC-Kupferkabel) für maximale Performance mit dem Switch verbinden würde.

# Quellen & Vertiefung

- **IT-Handbuch**
    - **Kap. 5.9 "Netzwerkhardware" (S. 301-308)**
    - **relevante Abschnitte aus Kap. 5.3 "Übertragungsmedien" und Kap. 6.3 "Speichersysteme".**
- Vertiefung (Wikipedia): [Switch (Netzwerktechnik)](https://de.wikipedia.org/wiki/Switch_%28Netzwerktechnik%29)
- Vertiefung (Wikipedia): [Gateway (Informatik)](https://de.wikipedia.org/wiki/Gateway_%28Informatik%29)