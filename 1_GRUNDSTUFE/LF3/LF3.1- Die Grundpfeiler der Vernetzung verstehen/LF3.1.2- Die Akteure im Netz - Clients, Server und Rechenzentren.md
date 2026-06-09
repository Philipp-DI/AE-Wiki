# LF3.1.2- Die Akteure im Netz - Clients, Server und Rechenzentren

Als **Praktikant im IT-Support**

möchte ich die unterschiedlichen Rollen von Clients und Servern sowie die Bedeutung von Rechenzentren verstehen,

damit ich für die "Innovate GmbH" eine fundierte Empfehlung für die zukünftige Infrastruktur geben kann.

# Celebration Criteria

- Wir können verschiedene Client-Typen (z.B. Desktop-PC, Thin Client, Mobilgerät) und ihre typischen Einsatzszenarien beschreiben.
- Wir können mindestens drei gängige Serverdienste (z.B. File-Server, Print-Server, Web-Server) und ihre Funktion im Netzwerk erklären.
- Wir können den Unterschied zwischen einer On-Premises-Lösung und einem Cloud-Dienst aus einem Rechenzentrum erläutern.

# Wissens-Briefing

## Client-Typen

- **Fat/Thick Client:** Ein Standard-PC, der Rechenleistung und Datenspeicherung lokal durchführt. Hohe Autonomie, aber dezentrale Verwaltung.
- **Thin Client:** Ein reduziertes Endgerät, das hauptsächlich zur Ein- und Ausgabe für einen zentralen Terminalserver dient. Die Verarbeitung findet auf dem Server statt. Vorteile: Geringere Kosten, zentrale Administration.

## Serverdienste (Beispiele)

- **File-Server:** Stellt zentralen Speicherplatz für Dateien bereit (Netzlaufwerke).
- **Print-Server:** Verwaltet und verteilt Druckaufträge an Netzwerkdrucker.
- **Web-Server:** Liefert Webseiten an die Browser der Clients aus (z.B. für ein Intranet).
- **DHCP-Server:** Weist Clients automatisch eine IP-Adresse und Netzwerkkonfiguration zu.
- **DNS-Server:** Übersetzt Domainnamen (z.B. [www.google.de](http://www.google.de)) in IP-Adressen.

## Infrastruktur-Modelle

- **On-Premises ("Vor Ort"):** Das Unternehmen betreibt seine eigene Server-Infrastruktur im eigenen Gebäude. Bietet volle Kontrolle, erfordert aber hohe Investitions- und Wartungskosten.
- **Cloud Computing:** Server, Speicher oder Software werden als Dienst von einem externen Anbieter über das Internet gemietet. Man unterscheidet u.a.:
    - **IaaS (Infrastructure as a Service):** Miete von reiner IT-Infrastruktur (virtuelle Server, Speicher).
    - **PaaS (Platform as a Service):** Miete einer kompletten Entwicklungs- und Laufzeitumgebung.
    - **SaaS (Software as a Service):** Miete von fertigen Software-Anwendungen (z.B. Microsoft 365).

# Aufgaben

1.  **Diskussion & Entscheidung:** Diskutiert in der Gruppe die Vor- und Nachteile einer On-Premises-Lösung (z.B. ein kleiner NAS-Server im Büro) gegenüber einer Cloud-Lösung (z.B. Microsoft 365 / Google Workspace) für die zentrale Datenhaltung der "Innovate GmbH". Bereitet eine Empfehlung für die Geschäftsführung vor.

<table style="min-width: 75px"><tbody><tr><th colspan="1" rowspan="1"><p></p></th><th colspan="1" rowspan="1"><p>Vorteile / Pro</p></th><th colspan="1" rowspan="1"><p>Nachteile / Contra</p></th></tr><tr><td colspan="1" rowspan="1"><p><strong>On-Premise</strong></p></td><td colspan="1" rowspan="1"><ul><li><p>Volle Datenkontrolle</p></li><li><p>Keine Abhängigkeit von Cloud Anbieter</p></li><li><p>Hohe Geschwindigkeit im Lokalen Netzwerk</p></li><li><p>Einmalige Investition statt laufender Abokosten</p></li></ul></td><td colspan="1" rowspan="1"><ul><li><p>Einstiegskosten</p></li><li><p>Wartung erforderlich</p></li><li><p>Ausfallsicherheit</p></li><li><p>Erfordert neue Hardware</p></li></ul></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Cloud-Dienste</strong></p></td><td colspan="1" rowspan="1"><ul><li><p>Geringer Verwaltungsaufwand</p></li><li><p>Einfache Einrichtung</p></li><li><p>mobiles Arbeiten ebenfalls leicht einzurichten</p></li><li><p>Enthält u.U. zusätzliche Features</p></li></ul></td><td colspan="1" rowspan="1"><ul><li><p>Laufende Kosten</p></li><li><p>Sicherheitsrisiko (Daten-Leaks)</p></li><li><p>Abhängig von Anbieter</p></li><li><p>Datenschutz</p></li><li><p>Internet Abhängig</p></li></ul></td></tr></tbody></table>

2.  **Recherche & Präsentation:** Teilt die folgenden Serverdienste unter euch auf: File-Server, DHCP-Server, DNS-Server, Print-Server. Jedes Mitglied recherchiert die genaue Funktion "seines" Dienstes und erstellt eine einzelne Folie, die den Dienst einfach erklärt. Führt die Folien zu einer gemeinsamen Kurzpräsentation zusammen.  
    [Link zum Canva-Dokument](https://www.canva.com/design/DAG0FLfDBXk/o-h4ScJdh9VmAjOhXsgP0Q/edit?utm_content=DAG0FLfDBXk&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)  
    
3.  **Konzeptaufgabe:** Skizziert, welche Serverdienste die "Innovate GmbH" in der ersten Ausbaustufe mindestens benötigen würde, um Dateien zentral zu speichern, gemeinsam zu drucken und einen sicheren Internetzugang für alle zu gewährleisten.
    - Datenserver bzw. Fileserver
    - Printserver
    - DHCP-Server → statische Zuordnung für Print- und Fileserver; automatische Zuordnung für Büro-PC (Clients); dynamische Zuordnung für WLAN (Gästezugang, wechselnde Endgeräte, etc.)
    - [Skizze](https://affine.ideenschmiede.hamburg/workspace/4def35ef-4587-45fc-bfd4-73b2ac3b4e32/SddLNN9ZM-1OcNgfqxaxm?mode=edgeless&blockIds=eUn02WJGL_)

# Quellen & Vertiefung

- **IT-Handbuch, Kapitel 6 "Server" (insb. 6.1, 6.4, 6.5, 6.6, S. 327-364).**
- **Westermann Tabellenbuch, S. 626-628 "Server".**
- Vertiefung (Wikipedia): [Server (Informatik)](https://www.google.com/search?q=https://de.wikipedia.org/wiki/Server_%28Informatik%29)
- Vertiefung (IONOS): [Was ist Cloud Computing?](https://www.google.com/search?q=https://www.ionos.de/digitalguide/server/know-how/was-ist-cloud-computing/)