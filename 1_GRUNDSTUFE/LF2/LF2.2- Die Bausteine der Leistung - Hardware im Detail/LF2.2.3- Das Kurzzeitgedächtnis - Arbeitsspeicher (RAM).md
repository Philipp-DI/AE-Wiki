# LF2.2.3- Das Kurzzeitgedächtnis - Arbeitsspeicher (RAM)

**Als** sorgfältiger Systemtechniker

**möchte ich** die verschiedenen Arten, Bauformen und Generationen von Arbeitsspeicher kennen,

**um** RAM-Probleme zu diagnostizieren und passende Aufrüstungen für Server, Desktops, Laptops und Grafikkarten empfehlen zu können.

# Celebration Criteria

- Wir können die grundlegende Funktion von **RAM (Random Access Memory)** als flüchtigen Arbeitsspeicher erklären.
- Wir können die RAM-Typen für **Desktops (UDIMM/CUDIMM)**, **Laptops (SO-DIMM)** und **Server (RDIMM)** unterscheiden.
- Wir können die Besonderheiten von Spezialspeichern wie **GDDR** für Grafikkarten und **LPDDR** für mobile Geräte erläutern.

# Wissens-Briefing

## Was ist Arbeitsspeicher?

Der **Arbeitsspeicher (RAM)** ist das ultraschnelle, aber **flüchtige** Kurzzeitgedächtnis eines Computers. Alle Programme und Daten, an denen die CPU aktiv arbeitet, müssen in den RAM geladen werden. "Flüchtig" bedeutet, dass alle Inhalte verloren gehen, sobald der Strom abgeschaltet wird. Seine hohe Geschwindigkeit ist entscheidend für die Performance des gesamten Systems. Die Zuggriffszeit auf Daten im RAM wird in Nanosekunden (ns) gemessen und als **Latenz** bezeichnet – je niedriger, desto besser.

## Bauformen und Entwicklung

- **SIMM (Single In-Line Memory Module):** Eine veraltete Bauform (ca. 80er/90er Jahre) mit einem 32-Bit-Datenbus.
- **DIMM (Dual In-Line Memory Module):** Der moderne Standard mit einem breiteren Datenbus (mind. 64-Bit). Die konkrete Ausführung variiert je nach Einsatzzweck.
- **GDDR (Graphics Double Data Rate):** Ein hochspezialisierter RAM-Typ, der für die extrem hohen Bandbreitenanforderungen von **Grafikkarten (GPUs)** optimiert ist. Er wird direkt auf die Grafikkartenplatine gelötet.

## Vergleich der DIMM-Bauformen

| Abkürzung | Name | Merkmale | Typische Einsatzzwecke |
| --- | --- | --- | --- |
| **UDIMM** | Unbuffered DIMM | Der Speichercontroller greift direkt auf die Speicherchips zu. Kein Puffer vorhanden. Standard bis DDR4 und frühes DDR5. | Desktop-PCs, Workstations, kleine Server. |
| **CUDIMM** | Clocked Unbuffered DIMM | Eine Weiterentwicklung für DDR5. Ein "Clock Driver"-Chip auf dem Modul stabilisiert das Taktsignal, was höhere Geschwindigkeiten ermöglicht. | Zukünftige High-Speed DDR5-Systeme im Desktop-Bereich. |
| **SO-DIMM** | Small Outline DIMM | Eine kleinere, kompaktere Bauform des UDIMM. | Laptops, Mini-PCs, All-in-One-Geräte. |
| **RDIMM** | Registered DIMM | Ein Register-Chip dient als Puffer zwischen Controller und Speicherchips; stabilisiert Signale für große Speichermengen. | Server, anspruchsvolle Workstations. |

## Vergleich der Arbeitsspeicher-Spezifikationen (nach höchster JEDEC-Spezifikation)

| Technologie | JEDEC Spezifikation | Max. Übertragungsrate | Typ. Latenz (CAS) | Spannung | Einsatzzeitraum | Desktop | Laptop | Server | Smart-phone | Grafik-karte |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **DDR** (hist.) | DDR-400 | 3.200 MB/s | CL 2.5 | 2.5 V | ca. 2000-2005 | ✅   | ✅   | ✅   |     |     |
| **DDR2** (hist.) | DDR2-800 | 6.400 MB/s | CL 5 | 1.8 V | ca. 2003-2010 | ✅   | ✅   | ✅   |     |     |
| **DDR3** (hist.) | DDR3-1600 | 12.800 MB/s | CL 11 | 1.5 V | ca. 2007-2015 | ✅   | ✅   | ✅   |     |     |
| **DDR4** (aktuell) | DDR4-3200 | 25.600 MB/s | CL 22 | 1.2 V | ca. 2014-heute | ✅   | ✅   | ✅   |     |     |
| **DDR5** (aktuell) | DDR5-6400 | 51.200 MB/s | CL 40 | 1.1 V | ca. 2021-heute | ✅   | ✅   | ✅   |     |     |
| **DDR6** (Zukunft) | DDR6-8800 (geplant) | \> 70.400 MB/s | \>CL40 | < 1.1 V | ab ca. 2026 | ✅   | ✅   | ✅   |     |     |
| **LPDDR4** (aktuell) | LPDDR4-4266 | 34.100 MB/s | \-  | < 1.1 V | ca. 2014-heute |     | ✅   |     | ✅   |     |
| **LPDDR5** (aktuell) | LPDDR5-6400 | 51.200 MB/s | \-  | < 1.1 V | ca. 2020-heute |     | ✅   |     | ✅   |     |
| **GDDR5** (hist.) | GDDR5 | ~ 300.000 MB/s | \-  | 1.5 V | ca. 2008-2018 |     |     |     |     | ✅   |
| **GDDR6** (aktuell) | GDDR6 | \> 700.000 MB/s | \-  | 1.25 V - 1.35 V | ca. 2018-heute |     |     |     |     | ✅   |

# Aufgaben

1.  Sucht Bilder von einem Standard-DDR5-UDIMM, einem SO-DIMM und einem DDR5-RDIMM mit ECC. Achtet auf die Anzahl und Anordnung der Speicherchips.
2.  Öffnet den Task-Manager (Strg+Shift+ESC) auf einem PC, geht zum Reiter "Leistung" und klickt auf "Arbeitsspeicher". Notiert die angezeigte Gesamtmenge, die Geschwindigkeit (in MHz) und den Typ (z.B. DDR4).
3.  Begründet, warum man in einem Unternehmens-Server RDIMMs anstatt UDIMMs verwendet und warum man den RAM eines Smartphones nicht aufrüsten kann.

# Quellen & Vertiefung

- **Rheinwerk IT-Handbuch:** Kapitel 4.1.3 "Arbeitsspeicher", Seiten 206 ff.
- **Wikipedia:** [Arbeitsspeicher](https://de.wikipedia.org/wiki/Arbeitsspeicher), [DDR-SDRAM](https://de.wikipedia.org/wiki/DDR-SDRAM)