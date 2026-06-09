# LF3.2.2- Die Regeln der Kommunikation - Schichtenmodelle und Adressen

Als **Junior IT-Consultant**

möchte ich die logische Struktur der Netzwerkkommunikation anhand von Schichtenmodellen und die verschiedenen Adresstypen verstehen,

damit ich nachvollziehen kann, wie Datenpakete ihren Weg vom Absender zum richtigen Empfänger finden.

# Celebration Criteria

- Wir können die 7 Schichten des OSI-Referenzmodells benennen und dem 4-schichtigen TCP/IP-Modell gegenüberstellen.
- Wir können den Zweck und das Format einer MAC-Adresse (physikalische Adresse) erklären.
- Wir können den Aufbau einer IPv4-Adresse und die Funktion der Subnetzmaske zur Trennung von Netz- und Hostanteil erläutern.
- Wir können den grundlegenden Unterschied zwischen IPv4 und dem Nachfolger IPv6 beschreiben.

# Wissens-Briefing

Schichtenmodelle: Teilen die komplexe Netzwerkkommunikation in hierarchische Schichten auf. Jede Schicht hat eine bestimmte Aufgabe und nutzt die Dienste der Schicht unter ihr.  
<br/>OSI-Referenzmodell: Ein theoretisches, 7-schichtiges Modell, das als Referenz dient.  
<br/>TCP/IP-Referenzmodell: Das vier-schichtige, praxisrelevante Modell des Internets.  
<br/>Gegenüberstellung der Modelle und Protokolle:  
<br/>| OSI-Schicht | Nr. | TCP/IP-Schicht | Beispielprotokolle / -geräte |  
| Anwendung (Application) | 7 | \\multirow{3}{\*}{Anwendung} | HTTP, FTP, SMTP, DNS, DHCP |  
| Darstellung (Presentation) | 6 | | SSL/TLS, JPEG, ASCII |  
| Sitzung (Session) | 5 | | NetBIOS, Sockets |  
| Transport (Transport) | 4 | Transport | TCP, UDP |  
| Vermittlung (Network) | 3 | Internet | IP, ICMP, Router |  
| Sicherung (Data Link) | 2 | \\multirow{2}{\*}{Netzzugang} | Ethernet (MAC), Switches, Bridges |  
| Bitübertragung (Physical) | 1 | | Kabel, Stecker, Hubs, Repeater |

## Adressarten

- **MAC-Adresse (Media-Access-Control-Adresse):** Eine weltweit eindeutige, 48-Bit lange Hardware-Adresse einer Netzwerkschnittstelle. Sie wird für die Zustellung von Daten im **lokalen Netzwerksegment** (z.B. von PC zu Switch) verwendet. Schreibweise: Hexadezimal, z.B. `00:80:41:AE:FD:7E`.
- **IP-Adresse (Internet-Protocol-Adresse):** Eine logische Adresse, die einem Gerät in einem Netzwerk zugewiesen wird. Sie ist für die **netzwerkübergreifende** Adressierung und das Routing im Internet notwendig.

## IPv4-Adressierung

- **Aufbau:** Eine 32-Bit-Adresse, dargestellt als vier Dezimalzahlen (Oktette) von 0-255, getrennt durch Punkte (z.B. `192.168.1.10`).
- **Private IP-Adressen:** Bereiche, die in lokalen Netzen frei verwendet werden können und im Internet nicht geroutet werden (z.B. `192.168.0.0` bis `192.168.255.255`).
- **Subnetzmaske:** Eine 32-Bit-Maske (z.B. `255.255.255.0`), die eine IP-Adresse in einen **Netzanteil** und einen **Hostanteil** trennt. Alle Geräte im selben Subnetz müssen den gleichen Netzanteil haben, um direkt miteinander kommunizieren zu können.

## IPv6-Adressierung

- **Zweck:** Wurde aufgrund der Knappheit von IPv4-Adressen eingeführt.
- **Aufbau:** Eine 128-Bit-Adresse, dargestellt in acht Blöcken mit hexadezimalen Zahlen, getrennt durch Doppelpunkte (z.B. `2001:0db8:85a3:08d3:1319:8a2e:0370:7344`). Bietet einen quasi unerschöpflichen Adressraum.

# Aufgaben

1.  **Praktische Analyse (Windows & Linux):**
    - Öffnet erneut die Kommandozeile.
    - **Windows:** Gebt `ipconfig` /all ein.
    - **Ubuntu:** Gebt `ip addr` und `ip route` ein.
    - Identifiziert folgende Informationen und tragt sie in eine gemeinsame Tabelle ein: Physische Adresse (MAC), IPv4-Adresse, Subnetzmaske, Standardgateway. Diskutiert, welche Adresse für die Kommunikation im lokalen LAN und welche für die Kommunikation ins Internet (zum Gateway) verwendet wird.
2.  **Rechenübung:** Gegeben ist die IP-Adresse `192.168.10.50` mit der Subnetzmaske `255.255.255.0`. Ermittelt gemeinsam den Netzanteil und den Hostanteil der Adresse. Wie lautet die Netzwerkadresse? Wie viele Hosts kann es in diesem Netzwerk maximal geben? Nutzt zur Überprüfung einen Online-Subnetzrechner. (**Subnet Calculator**)
3.  **Recherche** & **Diskussion:** Recherchiert, warum die Umstellung von IPv4 auf IPv6 so langsam voranschreitet, obwohl die IPv4-Adressen seit Jahren erschöpft sind. Sammelt die Gründe (z.B. Kosten, Komplexität, NAT als "Krücke") und diskutiert sie in der Gruppe.

# Quellen & Vertiefung

- **IT-Handbuch**
    - **Kap. 5.2 "Netzwerkprotokolle" (S. 197-200)**
    - **Kap. 5.5.2 "MAC-Adresse" (S. 250-251)**
    - **Kap. 5.7 "IP-Adressierung" (S. 270-292).**
- Westermann Tabellenbuch
    - S. 578-580 "Kommunikationsmodelle"
    - S. 588 "MAC-Adresse"
    - S. 596-607 "IP-Adressierung".
- Vertiefung (Wikipedia): [IPv4](https://de.wikipedia.org/wiki/IPv4)
- Vertiefung (Heise Netze): [Online-Subnetz-Rechner](https://www.heise.de/netze/tools/netzwerkrechner/)
- Vertiefung (Wikipedia): OSI-Modell