# LF7.1.2: IoT-Übertragungstechnologien im Vergleich

## 👤 User Story

> Als Netzwerk-Planer\*in  
> möchte ich verschiedene IoT-Kommunikationsstandards vergleichen,  
> damit ich für spezifische Distanz- und Energieanforderungen die physikalisch passende Funk- oder Kabeltechnologie auswählen kann.

## 🎉 Celebration Criteria (Lernziele)

- Ich kann den Begriff "LPWAN" (Low Power Wide Area Network) **erklären**. (K2)
- Ich **verstehe** den physikalischen Zusammenhang zwischen Übertragungsreichweite, Bandbreite und Energieverbrauch. (K2)
- Ich kann gängige Protokolle nach ihrem optimalen Einsatzbereich **klassifizieren**. (K3)

## 🧠 Wissens-Briefing

- **Das IoT-Dreieck:** Reichweite, Bandbreite und Energieeffizienz können physikalisch nicht gleichzeitig maximiert werden. Man muss Kompromisse schließen.
- **WLAN / Wi-Fi:** Hohe Bandbreite, mittlere Reichweite (lokal), sehr hoher Energieverbrauch. Ungeeignet für Batterien.
- **Bluetooth / Zigbee:** Mittlere bis hohe Bandbreite, sehr kurze Reichweite (PAN/LAN), geringer Energieverbrauch. Ideal für Smart Home.
- **LoRaWAN (LPWAN):** Extreme Reichweite (bis zu 15 km), extrem geringer Energieverbrauch (Batterien halten Jahre), aber extrem geringe Bandbreite (wenige Bytes pro Stunde).
- **Industrie-Busse (KNX, Profinet):** Meist kabelgebunden. Bieten extrem hohe Zuverlässigkeit, garantierte Echtzeit-Latenzen und sind unabhängig von Funk-Störungen.

## 🚧 Typische Fallstricke & Impulsfragen

- **Bandbreiten-Illusion:** LoRaWAN ist fantastisch für Temperaturwerte. Wer jedoch versucht, Video-Streams oder schnelle Live-Maschinensteuerungen über LoRaWAN zu realisieren, scheitert an der Physik.
- **Lizenzbänder:** WLAN und Bluetooth nutzen freie ISM-Bänder (2,4 GHz), die oft völlig überlastet sind. Mobilfunk-IoT (NB-IoT) nutzt lizenzierte Bänder, kostet aber Provider-Gebühren.

## 🛠️ Pflichtaufgaben (K2 & K3)

1. Erläutere das Spannungsfeld zwischen Reichweite, Bandbreite und Energieverbrauch bei der Auswahl einer Funktechnologie.
2. Vergleiche die typischen Einsatzgebiete von Bluetooth Low Energy (BLE) mit denen von LoRaWAN.
3. Ordne die Technologien WLAN, Zigbee und NB-IoT (Narrowband IoT) in ein Koordinatensystem aus "Energiebedarf" und "Reichweite" ein.
4. Skizziere die technischen und wirtschaftlichen Unterschiede zwischen der Nutzung eines unlizenzierten Funkbandes (z.B. 868 MHz) und eines lizenzierten Mobilfunkbandes.
5. Bestimme die Vorteile, die klassische kabelgebundene Feldbusse (wie KNX) gegenüber modernen Funkstandards in einer Produktionshalle mit vielen Störquellen bieten.

## 🔥 Freiwillige Zusatzaufgaben (K4 & K5)

1. Analysiere das Problem der Signalabschirmung (Dämpfung) in Gebäuden mit starker Stahlbeton-Struktur und erarbeite technologische Gegenmaßnahmen.
2. Beurteile das Risiko von "Kollisionen" in unlizenzierten LPWAN-Netzen, wenn hunderte Geräte gleichzeitig auf derselben Frequenz senden wollen.
3. Entwickle eine Entscheidungsmatrix zur Auswahl der passenden Netzwerktechnologie anhand der Kriterien "Latenzkritikalität", "Datenvolumen" und "Stromnetz-Verfügbarkeit".

## 🕸️ Web-Suchwortliste

| Thema / Seite | Suchbegriffe für die Google-/Plattform-Suche |
| --- | --- |
| **YouTube** | "LoRaWAN vs NB-IoT Architektur" |
| **Elektronik-Kompendium** | "LPWAN Technologien Übersicht" |
| **IT-Wissen** | "ISM Band Störungen IoT" |