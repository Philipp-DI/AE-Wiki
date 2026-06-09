# LF7.2.3: Payload-Optimierung & Latenz

## 👤 User Story

> Als Protokoll-Spezialist\*in  
> möchte ich die Größe der übertragenen Datenpakete (Payload) minimieren,  
> um die Sendezeit, den Energieverbrauch und die Netzwerklast meines IoT-Systems zu reduzieren.

## 🎉 Celebration Criteria (Lernziele)

- Ich kann den Unterschied zwischen Payload und Protokoll-Overhead **erklären**. (K2)
- Ich **verstehe**, warum textbasierte Formate (wie JSON) für extreme Low-Power-Anwendungen ineffizient sind. (K2)
- Ich kann große Datensätze in binäre oder hexadezimale Strukturen **umwandeln**. (K3)

## 🧠 Wissens-Briefing

- **Payload vs. Overhead:** Der _Payload_ ist die eigentliche Nutzinformation (z.B. "22.5" für Temperatur). Der _Overhead_ sind die Metadaten des Protokolls (TCP-Header, MQTT-Topic, Routing-Infos).
- **JSON (JavaScript Object Notation):** Sehr gut lesbar für Menschen (`{"sensor": "Temp1", "wert": 22.5}`). Kostet aber viele Bytes durch Klammern, Anführungszeichen und Leerzeichen.
- **Binäre/Hexadezimale Formate:** Werden oft in LPWAN-Netzen (wie LoRaWAN) genutzt. Statt "22.5" wird der Wert in reine Bits umgewandelt (z.B. `0x165` als Hex-Wert). Spart massiv Sendezeit und damit Batterie.
- **Time-on-Air (Sendezeit):** Je mehr Bytes gesendet werden, desto länger muss das Funkmodul aktiv sein. Lange Sendezeit = hoher Stromverbrauch.

## 🚧 Typische Fallstricke & Impulsfragen

- **Zu feine Datenstrukturen:** Wenn jedes Sensor-Attribut ein eigenes MQTT-Topic bekommt (z.B. `haus/raum/sensor/temp` und `haus/raum/sensor/feuchte`), steigt der Protokoll-Overhead enorm.
- **Verlust an Lesbarkeit:** Binäre Daten können beim Debugging ohne einen passenden Decoder auf der Server-Seite nicht mehr einfach von Menschen gelesen werden.

## 🛠️ Pflichtaufgaben (K2 & K3)

1. Identifiziere in einer typischen Netzwerk-Nachricht, welche Teile zur Nutzinformation (Payload) und welche zum Protokoll-Overhead gehören.
2. Vergleiche die Speichereffizienz von lesbarem Text (JSON) mit rohen binären/hexadezimalen Daten anhand eines Beispiels.
3. Wandle einen einfachen Temperatur- und Feuchtigkeits-Datensatz, der in JSON vorliegt, in eine möglichst kurze, stringente Zeichenkette um.
4. Skizziere, wie sich die "Time-on-Air" (aktive Sendezeit) verändert, wenn man den Payload von 100 Bytes auf 10 Bytes reduziert.
5. Bestimme die Konsequenzen, die sich für das Backend (Cloud/Server) ergeben, wenn Sensoren keine strukturierten JSON-Daten, sondern unformatierte Hex-Strings senden.

## 🔥 Freiwillige Zusatzaufgaben (K4 & K5)

1. Analysiere einen MQTT-Topic-Tree (z.B. `fabrik/halle1/maschine3/sensor/temperatur`) hinsichtlich seines Overheads und erarbeite eine deutlich effizientere Alternative.
2. Untersuche Konzepte der "Daten-Kompression" direkt auf dem Microcontroller, bevor die Daten gefunkt werden.
3. Beurteile das Risiko von Paketverlusten (Packet Loss) in Abhängigkeit zur Größe des übertragenen Payloads bei schwachen Funknetzen.

## 🕸️ Web-Suchwortliste

| Thema / Seite | Suchbegriffe für die Google-/Plattform-Suche |
| --- | --- |
| **IT-Wissen** | "Netzwerk Payload Overhead Unterschied" |
| **YouTube** | "LoRaWAN Payload Decoder" |
| **Wikipedia** | "Hexadezimalsystem Datenübertragung" |