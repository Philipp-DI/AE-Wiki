# LF7.3.2: Betriebssicherheit & OTA-Updates

## 👤 User Story

> Als System-Integrator\*in  
> möchte ich Mechanismen zur Ausfallsicherheit und Software-Aktualisierung implementieren,  
> damit das cyber-physische System über Jahre hinweg stabil und wartbar bleibt.

## 🎉 Celebration Criteria (Lernziele)

- Ich kann die Funktion eines Hardware-Watchdog-Timers **erklären**. (K2)
- Ich **verstehe** den Prozess eines "Over-the-Air" (OTA) Updates. (K2)
- Ich kann Fallback-Routinen für den Ausfall von Netzwerkverbindungen **entwerfen**. (K3)

## 🧠 Wissens-Briefing

- **Watchdog-Timer (WDT):** Eine Hardware-Komponente im Microcontroller, die wie ein "Totmannschalter" funktioniert. Die Software muss den Timer regelmäßig zurücksetzen ("füttern"). Stürzt die Software ab, läuft der Timer ab und löst einen harten Hardware-Reset aus.
- **Over-the-Air (OTA) Updates:** Die Möglichkeit, eine neue Firmware per WLAN/Mobilfunk auf den Microcontroller zu spielen, ohne ihn physisch per USB an einen PC anzuschließen.
- **A/B-Partitioning (Sicheres OTA):** Der Speicher des Microcontrollers wird geteilt. Das neue Update wird in Partition B geladen, während das System aus Partition A läuft. Nach dem Download wird auf B umgeschaltet. Ist das Update fehlerhaft, fällt das System automatisch auf A zurück.
- **Fallback-Strategien:** "Fail-Safe"-Zustände definieren. Was macht der Aktor (z.B. ein Heizungsventil), wenn der Controller 10 Minuten lang keine WLAN-Verbindung zum Server hat? (z.B. Sicherheitsabschaltung).

## 🚧 Typische Fallstricke & Impulsfragen

- **"Bricking":** Wenn während eines normalen Updates (ohne A/B-Partitionen) der Strom ausfällt, ist der Microcontroller defekt ("gebrickt") und muss oft händisch vor Ort geflasht werden.
- **Watchdog-Ignoranz:** Wenn der Watchdog-Timer fälschlicherweise in einem Hintergrund-Thread gefüttert wird, der von der abgestürzten Hauptschleife unabhängig ist, verfehlt er seinen Zweck.

## 🛠️ Pflichtaufgaben (K2 & K3)

1. Erläutere die exakte Funktionsweise eines Hardware-Watchdogs zur Verhinderung von dauerhaften Systemhängern.
2. Skizziere den Ablauf eines OTA-Updates unter Verwendung des A/B-Partitioning-Konzepts.
3. Konstruiere eine "Fail-Safe"-Logik (Wenn-Dann-Szenario) für einen IoT-gesteuerten Rollladen bei einem plötzlichen Ausfall der lokalen Internetverbindung.
4. Vergleiche den Wartungsaufwand eines Sensornetzwerks (100 Geräte) mit OTA-Fähigkeit gegenüber einem System ohne OTA-Fähigkeit über einen Zeitraum von 5 Jahren.
5. Bestimme, unter welchen Umständen ein automatischer Neustart durch einen Watchdog ein zugrundeliegendes Software-Problem verschleiern könnte.

## 🔥 Freiwillige Zusatzaufgaben (K4 & K5)

1. Analysiere das Risiko von Man-in-the-Middle-Angriffen während eines OTA-Updates und erarbeite kryptografische Gegenmaßnahmen (Firmware-Signierung).
2. Beurteile die Vor- und Nachteile eines Flotten-Management-Systems, das Firmware-Updates in Wellen (Canary Deployments) ausrollt.
3. Entwickle ein Architektur-Konzept für "Hardware-Redundanz" bei einem lebenserhaltenden CPS-System (z.B. medizinische Kühlung), falls der primäre Controller physisch zerstört wird.

## 🕸️ Web-Suchwortliste

| Thema / Seite | Suchbegriffe für die Google-/Plattform-Suche |
| --- | --- |
| **Elektronik-Praxis** | "Microcontroller Watchdog Timer Funktion" |
| **Wikipedia** | "Over-the-air update" |
| **IT-Wissen** | "Fail-Safe Zustand Systemarchitektur" |