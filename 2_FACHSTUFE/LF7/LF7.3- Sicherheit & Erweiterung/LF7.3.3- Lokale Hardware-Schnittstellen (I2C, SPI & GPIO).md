# LF7.3.3: Lokale Hardware-Schnittstellen (I2C, SPI & GPIO)

## 👤 User Story

> Als Hardware-Integrator\*in  
> möchte ich die lokalen Kommunikationsbusse und Schnittstellen verstehen,  
> damit ich neue Sensoren und Aktoren physisch korrekt in bestehende cyber-physische Systeme einbinden kann.

## 🎉 Celebration Criteria (Lernziele)

- Ich kann den Unterschied zwischen digitalen und analogen GPIO-Signalen **erklären**. (K2)
- Ich **verstehe** die Topologie und Funktionsweise des I2C-Bussystems. (K2)
- Ich kann **entscheiden**, für welchen Sensor-Typ (z.B. Kamera vs. Temperatur) SPI oder I2C besser geeignet ist. (K3)

## 🧠 Wissens-Briefing

- **GPIO (General Purpose Input/Output):** Einzelne, programmierbare Pins an einem Microcontroller. Können "HIGH" (z.B. 3.3V) oder "LOW" (0V) sein, um simple Aktoren (LEDs, Relais) zu schalten oder digitale Signale auszulesen.
- **ADC (Analog-to-Digital Converter):** Erlaubt es, stufenlose analoge Spannungen (z.B. von einem Potentiometer oder einem Lichtsensor) an einem GPIO-Pin einzulesen und in digitale Zahlenwerte umzuwandeln.
- **I2C (Inter-Integrated Circuit):** Ein serieller Datenbus, der nur zwei Leitungen benötigt: SDA (Daten) und SCL (Takt).
  - _Topologie:_ Bus-Struktur. Dutzende Geräte können parallel an dieselben zwei Leitungen angeschlossen werden.
  - _Identifikation:_ Jedes Gerät hat eine feste Hardware-Adresse (z.B. `0x3C`).
  - _Einsatz:_ Langsamere Sensoren (Temperatur, Luftdruck, kleine OLED-Displays).
- **SPI (Serial Peripheral Interface):** Benötigt meist 4 Leitungen (MISO, MOSI, SCK, CS).
  - _Topologie:_ Stern-ähnlich. Die Datenleitungen werden geteilt, aber jedes Gerät braucht eine eigene "Chip Select" (CS) Leitung vom Master.
  - _Einsatz:_ Sehr hohe Geschwindigkeiten (SD-Karten, Kameras, große Farbdisplays).

## 🚧 Typische Fallstricke & Impulsfragen

- **Adresskonflikte:** Wenn man zwei baugleiche Temperatur-Sensoren mit der festen I2C-Adresse `0x27` an denselben I2C-Bus anschließt, kollidieren sie. Der Microcontroller weiß nicht, welcher Sensor gerade antwortet.
- **Kabellängen:** I2C und SPI sind "On-Board"-Busse (für Entfernungen von wenigen Zentimetern gedacht). Wer versucht, einen I2C-Sensor über ein 5 Meter langes Kabel quer durch die Werkhalle zu verbinden, scheitert an Signalstörungen und Kapazitäten.

## 🛠️ Pflichtaufgaben (K2 & K3)

1. Erläutere den grundlegenden Unterschied bei der Signalverarbeitung zwischen einem digitalen (GPIO) und einem analogen (ADC) Eingang.
2. Skizziere die Verdrahtung (SDA, SCL, VCC, GND) eines Microcontrollers (Master) mit drei unterschiedlichen I2C-Sensoren (Slaves).
3. Vergleiche die Vor- und Nachteile von I2C gegenüber SPI in Bezug auf den Verkabelungsaufwand und die Übertragungsgeschwindigkeit.
4. Ordne folgende Bauteile dem passenden Schnittstellen-Typ (GPIO, I2C oder SPI) zu: Eine einfache LED-Warnlampe, ein komplexer Umweltsensor (Temperatur/Feuchtigkeit/Druck), ein hochauflösendes Kamera-Modul.
5. Skizziere eine Lösung für das Problem, dass zwei identische I2C-Sensoren mit der gleichen Hardware-Adresse an einen Controller angeschlossen werden müssen (Stichwort: I2C-Multiplexer).

## 🔥 Freiwillige Zusatzaufgaben (K4 & K5)

1. Analysiere das physikalische Problem der Kapazität bei langen Kabelverbindungen auf einem I2C-Bus und beurteile den Einsatz von "Pull-Up-Widerständen" als Gegenmaßnahme.
2. Entwickle ein Architektur-Konzept zur Überbrückung von Entfernungen: Wie bindet man einen SPI-Sensor, der 20 Meter vom Haupt-Controller entfernt ist, mithilfe von lokalen Edge-Knoten an das Netzwerk an?
3. Beurteile das Risiko von Spannungsinkompatibilitäten (z.B. 5V-Sensor an 3.3V-Microcontroller) und bestimme die Notwendigkeit von "Logic Level Convertern".

## 🕸️ Web-Suchwortliste

| Thema / Seite | Suchbegriffe für die Google-/Plattform-Suche |
| --- | --- |
| **Elektronik-Kompendium** | "I2C Bus Funktionsweise" |
| **Mikrocontroller.net** | "SPI Schnittstelle Erklärung MISO MOSI" |
| **Studyflix** | "Analog Digital Wandler ADC" |