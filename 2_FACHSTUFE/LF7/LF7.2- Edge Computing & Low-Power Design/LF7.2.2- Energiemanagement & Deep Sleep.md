# LF7.2.2: Energiemanagement & Deep Sleep

## 👤 User Story

> Als Hardware-Entwickler\*in  
> möchte ich die verschiedenen Schlafmodi von Microcontrollern anwenden,  
> damit autonome, batteriebetriebene Sensoren über sehr lange Zeiträume wartungsfrei betrieben werden können.

## 🎉 Celebration Criteria (Lernziele)

- Ich kann den Begriff "Deep Sleep" im Kontext von Microcontrollern **erklären**. (K2)
- Ich **verstehe** den Unterschied zwischen zeitgesteuertem und ereignisgesteuertem Aufwachen (Interrupts). (K2)
- Ich kann den Energieverbrauch eines einfachen Sendezyklus **skizzieren** und **berechnen**. (K3)

## 🧠 Wissens-Briefing

- **Energie-Problem:** Ein ESP32 verbraucht bei aktiver WLAN-Verbindung ca. 160-240 mA. Eine normale Batterie (z.B. 2500 mAh) wäre so nach wenigen Stunden leer.
- **Deep Sleep (Tiefschlaf):** Der Hauptprozessor (CPU), RAM und Funkmodule (WLAN/Bluetooth) werden komplett stromlos geschaltet. Nur ein winziger Coprozessor (RTC - Real Time Clock) bleibt aktiv. Stromverbrauch sinkt auf ca. 10 µA (Mikroampere).
- **Wake-Up-Trigger (Aufweck-Methoden):**
  - _Timer:_ Der RTC-Coprozessor weckt das System nach einer festgelegten Zeit (z.B. alle 15 Minuten).
  - _External Interrupt:_ Ein physischer Reiz (z.B. ein Tastendruck, Bewegungssensor oder Reed-Kontakt an einer Tür) weckt das System sofort auf.

## 🚧 Typische Fallstricke & Impulsfragen

- **Boot-Zeit kostet Strom:** Das Aufwachen aus dem Deep Sleep gleicht einem kompletten Neustart. Das Herstellen der WLAN-Verbindung dauert oft mehrere Sekunden und frisst extrem viel Energie ("On-Time").
- **RAM-Verlust:** Im Deep Sleep gehen alle normalen Variablen im Arbeitsspeicher (RAM) verloren. Daten, die über den Schlaf hinaus benötigt werden, müssen im speziellen RTC-Memory gespeichert werden.

## 🛠️ Pflichtaufgaben (K2 & K3)

1. Beschreibe, welche Komponenten eines Microcontrollers (wie dem ESP32) während der Deep-Sleep-Phase deaktiviert werden und warum.
2. Erkläre den wesentlichen Unterschied für den Anwendungsfall, ob ein Sensor per Timer (z.B. alle 10 Minuten) oder per Hardware-Interrupt (z.B. beim Öffnen eines Fensters) geweckt wird.
3. Berechne theoretisch, wie lange eine 1000 mAh Batterie hält, wenn ein Sensor durchgehend 100 mA verbraucht, versus wenn er zu 99% der Zeit im Deep Sleep (0,01 mA) verweilt.
4. Skizziere ein Programm-Flussdiagramm für einen Sensor, der aufwacht, misst, sendet und wieder schlafen geht.
5. Wende Maßnahmen an, um die "On-Time" (die Zeit, in der das System voll aktiv ist) während eines Aufwach-Zyklus so gering wie möglich zu halten.

## 🔥 Freiwillige Zusatzaufgaben (K4 & K5)

1. Analysiere das Problem des "Memory Loss" beim Deep Sleep und erarbeite eine Lösung, wie ein Zähler (z.B. "Anzahl der Türöffnungen") über mehrere Schlafphasen hinweg erhalten bleiben kann.
2. Untersuche die Auswirkungen von schlechtem WLAN-Empfang auf die Batterielaufzeit eines Deep-Sleep-Sensors.
3. Beurteile, warum LoRaWAN für Deep-Sleep-Szenarien oft besser geeignet ist als eine herkömmliche WLAN-Anbindung.

## 🕸️ Web-Suchwortliste

| Thema / Seite | Suchbegriffe für die Google-/Plattform-Suche |
| --- | --- |
| **Elektronik-Praxis** | "ESP32 Deep Sleep Tutorial" |
| **Wikipedia** | "Hardware Interrupt Mikrocontroller" |
| **YouTube** | "IoT Battery Life Calculation" |