# LF2.2.1- Das Gehirn des Computers - CPU-Architekturen

**Als** angehender Hardware-Spezialist

**möchte ich** die grundlegenden CPU-Architekturen und deren Anwendungsbereiche verstehen,

**um** für verschiedene Gerätetypen wie Server, PCs, Smartphones oder IoT-Geräte den passenden Prozessor-Typ bewerten zu können.

# Celebration Criteria (Lernziele)

- Wir können die dominanten Architekturen für die Bereiche **Server/Desktop (x86)**, **Mobil (ARM)** und **IoT/Embedded (ARM, MIPS, RISC-V)** zuordnen.
- Wir können die grundlegenden Konzepte von **CISC** und **RISC** an einem einfachen Beispiel erklären.
- Wir können erläutern, warum unterschiedliche Einsatzbereiche unterschiedliche Anforderungen an einen Prozessor stellen.

# Wissens-Briefing

## Grundlegende Design-Philosophien

- **CISC (Complex Instruction Set Computer):** Ein Prozessor-Design, das darauf abzielt, Aufgaben in so wenigen Befehlen wie möglich abzuschließen. Dafür besitzt die CPU einen großen Satz an sehr mächtigen, aber komplexen Befehlen, die intern in viele kleine Schritte zerlegt werden. **Analogie:** Ein einzelner Befehl "Backe eine Pizza" startet einen komplexen, mehrstufigen Prozess.
- **RISC (Reduced Instruction Set Computer):** Ein Prozessor-Design, das auf einen kleinen, hochoptimierten Satz von einfachen Befehlen setzt. Jeder Befehl ist sehr schnell und in einem Taktzyklus ausführbar. Komplexe Aufgaben werden vom Compiler in viele dieser einfachen Befehle zerlegt. **Analogie:** Die Aufgabe "Backe eine Pizza" wird in viele simple Befehle zerlegt: "Nimm Teig", "Rolle Teig aus", "Belege Teig" etc.

## Vergleich der CPU-Architekturen

| Architektur | CISC/RISC | Wesentliche Merkmale | Vorteile ✅ | Nachteile ❌ | Hersteller & Modelle |
| --- | --- | --- | --- | --- | --- |
| **x86-64** | CISC | Dominante Architektur; hohe Abwärtskompatibilität; komplexe Befehle. | Riesige Softwarebasis, hohe Single-Core-Leistung. | Hohe Komplexität und Leistungsaufnahme, thermische Herausforderungen. | **Intel**: Core (Desktop), Xeon (Server); **AMD**: Ryzen (Desktop), Epyc (Server) |
| **ARM** | RISC | Fokus auf Energieeffizienz; Lizenzmodell (Hersteller designen eigene Chips). | Sehr geringer Stromverbrauch, gute Leistung pro Watt, hohe Skalierbarkeit. | Geringere maximale Single-Core-Leistung als x86, Software muss oft angepasst werden. | **Qualcomm**: Snapdragon (Mobil); **Apple**: A-Series (Mobil), M-Series (Laptop); **Ampere**: Altra (Server) |
| **MIPS** | RISC | Klassische, "reine" RISC-Architektur; war früher einflussreich. | Einfaches, elegantes Design, energieeffizient. | Hat an Marktanteilen verloren, kleinere Software-Unterstützung als ARM/x86. | Broadcom/MediaTek: SoCs in Routern (z.B. AVM Fritz!Box); Microchip: PIC32 (Mikrocontroller) |
| **Power** | RISC | Fokus auf hohe Parallelität und Multithreading (SMT). | Sehr hohe Rechenleistung für spezialisierte, parallele Workloads. | Sehr teuer, Nischenmarkt, hoher Stromverbrauch. | IBM: **POWER10** (High-End-Server); NXP: PowerQUICC (Netzwerkprozessoren) |
| **SPARC** (historisch) | RISC | Offener Standard, für hohe Zuverlässigkeit und Skalierbarkeit konzipiert. | Robustheit, war führend im Server-Bereich. | Weitgehend vom Markt verdrängt, kaum noch Neuentwicklungen. | Oracle/Sun Microsystems: **SPARC T**\-Series (ältere Server) |
| **RISC-V** | RISC | Moderner, offener und lizenzkostenfreier Standard (ISA). | Extrem flexibel, anpassbar, keine Lizenzgebühren, hohe Sicherheit möglich. | Junges Ökosystem, noch begrenzte Verfügbarkeit von High-End-Implementierungen. | **SiFive**: Performance Series (SoCs); Espressif: ESP32-C3 (IoT-Mikrocontroller) |

# Aufgaben zur Zielerreichung

1.  Recherchiert die Prozessoren in eurem eigenen Smartphone, eurem PC und eurem WLAN-Router zu Hause. Notiert, welche Architektur (x86, ARM, MIPS) jeweils wahrscheinlich zum Einsatz kommt.
2.  Erklärt den Unterschied zwischen CISC und RISC mit einer Analogie aus dem Alltag.
3.  Erstellt eine Tabelle mit den Spalten "Einsatzbereich", "Wichtigste Anforderung" und "Typische Architektur" für die Bereiche Server, Desktop-PC, Smartphone und IoT-Sensor.

# Quellen & Vertiefung

- **Rheinwerk IT-Handbuch:** Kapitel 4.1.2 "Prozessoren", Seiten 183 ff.
- **Wikipedia:** [Prozessorarchitektur](https://de.wikipedia.org/wiki/Prozessorarchitektur), [CISC-Prozessor](https://www.google.com/search?q=https://de.wikipedia.org/wiki/CISC-Prozessor), [RISC-Prozessor](https://www.google.com/search?q=https://de.wikipedia.org/wiki/RISC-Prozessor)