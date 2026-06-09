# 3️⃣LF3.4- Netzwerksicherheit und -verfügbarkeit gewährleisten

Als angehender Fachinformatiker

möchte ich die grundlegenden Konzepte der Datensicherheit, Verfügbarkeit und des energieeffizienten Betriebs von Netzwerken verstehen,

damit ich für die "Innovate GmbH" ein robustes und sicheres Netzwerk konzipieren und grundlegende Schutzmaßnahmen empfehlen kann.

# Celebration Criteria

- Wir können die drei Schutzziele der Informationssicherheit (Vertraulichkeit, Integrität, Verfügbarkeit) erklären und auf das Netzwerk der "Innovate GmbH" anwenden.
- Wir können das Prinzip von RAID (insb. RAID 1 und RAID 5) zur Erhöhung der Datenverfügbarkeit auf einem Server erläutern.
- Wir können eine grundlegende Backup-Strategie (z.B. die 3-2-1-Regel) beschreiben und deren Wichtigkeit begründen.
- Wir können die Funktion einer Firewall erklären und typische Sicherheitsrisiken in einem kleinen Netzwerk (z.B. schwache Passwörter, ungesichertes WLAN) benennen.
- Wir können die Bedeutung einer unterbrechungsfreien Stromversorgung (USV) für kritische Netzwerkkomponenten erläutern.

**Szenario:** Das Netzwerk der "Innovate GmbH" läuft stabil. Die Geschäftsführung ist sehr zufrieden, macht sich nun aber Gedanken über die Sicherheit der zentral gespeicherten, geschäftskritischen Daten. Was passiert bei einem Festplattendefekt des Servers? Was bei einem Stromausfall? Wie kann verhindert werden, dass Unbefugte auf das Netzwerk zugreifen? Ihr sollt ein grundlegendes Sicherheits- und Verfügbarkeitskonzept erstellen.

# Abschlussaufgabe

## IT-Sicherheits- und Notfallkonzept (Basisschutz) für die "Innovate GmbH"

Das Netzwerk läuft, aber die Geschäftsführung macht sich Sorgen um die Sicherheit der Unternehmensdaten und die Ausfallsicherheit. Erstellt ein Basisschutzkonzept, das die wichtigsten Risiken für ein kleines Unternehmen adressiert und konkrete, umsetzbare Maßnahmen zur Verbesserung der IT-Sicherheit und Verfügbarkeit vorschlägt.

## Anforderungen an den Inhalt

1.  **Risikoanalyse und Schutzziele:**
    - Definiert die drei Schutzziele Vertraulichkeit, Integrität und Verfügbarkeit.
    - Beschreibt für jedes Schutzziel ein konkretes Bedrohungsszenario für die "Innovate GmbH" (z.B. Verfügbarkeit -> Server-Festplatte fällt aus; Vertraulichkeit -> Unbefugter im Gäste-WLAN greift auf Firmendaten zu).
2.  **Maßnahmenkatalog zur Erhöhung der Verfügbarkeit:**
    - **Hardware-Redundanz:** Empfehlt den Einsatz eines NAS-Servers mit einem konkreten RAID-Level (z.B. RAID 1 oder 5). Begründet, warum dieses RAID-Level geeignet ist und was es leistet.
    - **Datensicherungskonzept:** Entwickelt eine vollständige 3-2-1-Backup-Strategie. Definiert genau:
        - **WAS** wird gesichert (z.B. zentrale Dateifreigabe)?
        - **WIE** wird gesichert (z.B. wöchentliches Voll-Backup, tägliches inkrementelles Backup)?
        - **WOHIN** wird gesichert (Medium 1: NAS, Medium 2: externe USB-Festplatte, Medium 3: Cloud-Speicher)?
        - **WANN** wird gesichert (genauer Zeitplan)?
    - **Stromausfallvorsorge:** Dimensioniert eine USV für den Netzwerkschrank. Recherchiert die Leistungsaufnahme von Switch und geplantem NAS, wählt ein passendes USV-Modell und berechnet die ungefähre Überbrückungszeit. Begründet die Notwendigkeit dieser Anschaffung.
3.  **Maßnahmenkatalog zur Erhöhung der Sicherheit:**
    - **Firewall-** und **Router-Härtung:** Erstellt eine "Hardening Checklist" mit mindestens 5 Punkten, die bei der Konfiguration des Internet-Routers umgesetzt werden müssen.
    - **WLAN-Sicherheitsrichtlinie:** Definiert eine klare Richtlinie für das Mitarbeiter- und Gäste-WLAN.
4.  **Kosten-Nutzen-Aspekt (Green IT):** Schreibt einen kurzen Absatz, der erklärt, wie die Wahl energieeffizienter Server-Hardware (Green IT) nicht nur die Umwelt schont, sondern auch die Betriebskosten (Strom) senkt und somit direkt zum Unternehmenserfolg beiträgt.

## Präsentation

Fasst euer Konzept in einer Management-Präsentation zusammen. Fokussiert euch auf die Risiken und eure vorgeschlagenen Lösungen. Ziel ist es, die Geschäftsführung von der Notwendigkeit der Investitionen in Sicherheit und Verfügbarkeit zu überzeugen.