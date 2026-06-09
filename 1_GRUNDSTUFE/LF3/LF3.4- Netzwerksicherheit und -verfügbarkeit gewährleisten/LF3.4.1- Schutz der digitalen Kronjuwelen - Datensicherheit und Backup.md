# LF3.4.1- Schutz der digitalen Kronjuwelen - Datensicherheit und Backup

Als **Junior-Systemadministrator**

möchte ich die Konzepte RAID und Backup-Strategien verstehen,

damit ich der "Innovate GmbH" effektive Maßnahmen zum Schutz vor Datenverlust durch Hardware-Ausfälle empfehlen kann.

# Celebration Criteria

- Wir können den Unterschied zwischen Redundanz (RAID) und Backup erklären.
- Wir können die Funktionsweise von RAID 1 (Spiegelung) und RAID 5 (Parität) skizzieren.
- Wir können die 3-2-1-Backup-Regel erläutern.
- Wir können zwischen einem Voll-Backup, einem differenziellen und einem inkrementellen Backup unterscheiden.

# Wissens-Briefing

- **Redundanz vs. Backup:**
    - **Redundanz:** Dient der Erhöhung der **Verfügbarkeit** durch doppelt vorhandene Komponenten. **RAID ist Redundanz, kein Backup!** Es schützt vor dem Ausfall einer Festplatte, aber nicht vor Datenverlust durch Löschen, Viren oder Katastrophen.
    - **Backup (Datensicherung):** Erstellt eine Kopie der Daten auf einem separaten Medium, um diese im Notfall **wiederherstellen** zu können.
- **RAID (Redundant Array of Independent Disks):**
    - **RAID 1 (Mirroring/Spiegelung):** Mind. 2 Festplatten. Alle Daten werden auf beide Platten identisch geschrieben. Fällt eine aus, sind die Daten auf der zweiten noch vorhanden.
    - **RAID 5 (Parität):** Mind. 3 Festplatten. Die Daten werden verteilt geschrieben, zusätzlich wird eine Paritätsinformation berechnet und ebenfalls verteilt. Fällt eine Platte aus, können ihre Daten aus den restlichen Daten und der Parität wiederhergestellt werden.
- **Backup-Strategie:**
    - **3-2-1-Regel:** Halte **3** Kopien deiner Daten auf **2** unterschiedlichen Medientypen, davon **1** Kopie außer Haus (Off-Site).
- **Backup-Arten:**
    - **Voll-Backup:** Sichert alle ausgewählten Daten.
    - **Inkrementelles Backup:** Sichert nur die Daten, die sich seit dem _letzten_ Backup (egal welcher Art) geändert haben.
    - **Differentielles Backup:** Sichert nur die Daten, die sich seit dem _letzten Voll-Backup_ geändert haben.

# Aufgaben

1.  **Konzeptaufgabe:** Entwerft eine konkrete 3-2-1-Backup-Strategie für die zentralen Daten der "Innovate GmbH". Definiert die Medien (z.B. NAS-Server im Büro, externe Festplatte, Cloud-Speicher) und einen Zeitplan (z.B. wöchentliches Voll-Backup, tägliches inkrementelles Backup).
2.  **Visualisierung:** Erstellt in der Gruppe eine einfache Grafik oder ein kurzes Erklärvideo (z.B. mit einem Online-Tool), das den Unterschied zwischen RAID 1 und einem Backup visualisiert. Ziel ist es, der Geschäftsführung zu zeigen, warum beides wichtig ist.
3.  **Recherche & Vergleich:** Recherchiert die Vor- und Nachteile von inkrementellen und differenziellen Backups in Bezug auf Speicherplatz, Backup-Dauer und Wiederherstellungszeit. Erstellt eine Entscheidungstabelle, die bei der Auswahl hilft.

# Quellen & Vertiefung:

- **IT-Handbuch**
    - **Kap. 6.3.2 "RAID-Systeme" (S. 334-339)**
    - **Kap. 7.5 "Datensicherung" (S. 386-391)**
- Vertiefung (Wikipedia): [RAID](https://de.wikipedia.org/wiki/RAID)
- Vertiefung (Wikipedia): [Datensicherung](https://de.wikipedia.org/wiki/Datensicherung)