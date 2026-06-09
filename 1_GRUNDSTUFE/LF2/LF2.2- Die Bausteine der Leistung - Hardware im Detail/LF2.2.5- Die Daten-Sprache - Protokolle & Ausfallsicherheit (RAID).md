# LF2.2.5- Die Daten-Sprache - Protokolle & Ausfallsicherheit (RAID)

Als **System-Analyst**

möchte ich **die Entwicklung von Speicherprotokollen und die Prinzipien von RAID verstehen**,

um **kompatible, leistungsfähige und ausfallsichere Speicherlösungen für Server und Workstations zu konzipieren**.

# Celebration Criteria

- Wir können die Protokolle **SATA**, **SAS** und **NVMe** anhand ihrer Leistung und ihres Einsatzgebietes unterscheiden.
- Wir können den Zweck von **RAID** erklären und **Hardware-RAID** von **Software-RAID** abgrenzen.
- Wir können die gängigen **RAID-Level (0, 1, 5, 10)** anhand ihrer Eigenschaften (Performance, Redundanz, Kosten) vergleichen und einem Anwendungsfall zuordnen.

# Wissens-Briefing

## Was ist RAID?

**RAID (Redundant Array of Independent Disks)** ist eine Technik, die mehrere physische Festplatten zu einem einzigen logischen Laufwerk zusammenschließt. Die Ziele sind, je nach Konfiguration, die **Leistung zu steigern**, die **Ausfallsicherheit (Redundanz) zu erhöhen** oder beides zu kombinieren.

- **Hardware-RAID:** Ein dedizierter RAID-Controller (als Steckkarte oder auf dem Mainboard) verwaltet den Verbund. Die CPU wird nicht belastet, was zu höherer Performance führt. Dies ist der Standard in Servern.
- **Software-RAID:** Das Betriebssystem übernimmt die Verwaltung des RAIDs. Es ist kostengünstiger, da keine spezielle Hardware benötigt wird, belastet aber die CPU.

## Vergleich der Festspeicher-Protokolle

| Protokoll | Typ | Aktuelle Version | Max. Durchsatz | Typische Einsatzzwecke |
| --- | --- | --- | --- | --- |
| IDE (hist.) | parallel | Ultra DMA 6 | 133 MB/s | HDDs und optische Laufwerke in Desktop-PCs und günstigen Servern. |
| SCSI (hist.) | parallel | Ultra-320 | 320 MB/s | HDDs in professionellen Servern. |
| SATA | seriell | SATA 3.x | 600 MB/s | HDDs und SSDs in Desktop-PCs, Laptops, günstigen Servern/NAS. |
| SAS | seriell | SAS-4 | 2.400 MB/s | HDDs und SSDs in professionellen Servern und Storage-Systemen |
| NVMe | seriell | NVMe 2.0 (PCIe 5.0) | 14.000 MB/s | Hochleistungs-SSDs in modernen Desktops, Laptops und Servern. |

## Überblick der gängigsten RAID-Level

| RAID-Level | Min. Drives | Beschreibung | Ziel | Ausfallsicherheit |
| --- | --- | --- | --- | --- |
| RAID 0 | 2   | **Striping**: Daten werden auf alle Laufwerke verteilt geschrieben | Maximale Geschwindigkeit | **Keine** (fällt ein Laufwerk aus, sind alle Daten verloren) |
| RAID 1 | 1   | **Morroring**: Alle Daten werden auf jedes Laufwerk identisch geschrieben | Maximale Redundanz | **Sehr hoch** (fällt ein Laufwerk aus, läuft das System weiter) |
| RAID 5 | 3   | **Striping mit Parität**: Daten werden verteilt, zusätzlich werden Paritätsinformationen auf allen Platten gespeichert. | Gute Balance aus Performance, Redundanz und nutzbarer Kapazität. | **Gut** (eine Platte darf ausfallen). |
| RAID 10 (1+0) | 4   | **Kombination:** Mehrere gespiegelte Paare (RAID 1) werden zu einem schnellen Verbund zusammengefasst (RAID 0). | Sehr hohe Performance **und** sehr hohe Redundanz. | **hoch** (mind. eine Platte pro Spiegel darf ausfallen). |

# Aufgaben

1.  Erklärt den Leistungsunterschied zwischen einer SATA-SSD und einer NVMe-SSD.
2.  Ein Kunde benötigt einen kleinen Server für seine Firmendaten. Er schwankt zwischen RAID 1 und RAID 5 mit jeweils drei Festplatten. Erstellt eine Entscheidungshilfe, die die Vor- und Nachteile beider Lösungen (nutzbare Kapazität, Schreibgeschwindigkeit, Sicherheit) für seinen Anwendungsfall gegenüberstellt.
3.  Konfiguriert in eurem Windows 11 Laptop mit dem Tool "Speicherplätze" ("Storage Spaces") ein Software-RAID 1 (Spiegelung) mit zwei virtuellen Festplatten. Dokumentiert die Schritte.

# Quellen & Vertiefung

- **Rheinwerk IT-Handbuch:** Kapitel 4.1.5 "Massenspeicher", Seiten 239 ff. (RAID).
- **Wikipedia:** [RAID](https://de.wikipedia.org/wiki/RAID), [Serial ATA](https://de.wikipedia.org/wiki/Serial_ATA), [NVM Express](https://de.wikipedia.org/wiki/NVM_Express)