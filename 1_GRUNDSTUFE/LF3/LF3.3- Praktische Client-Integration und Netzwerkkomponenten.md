# 3️⃣LF3.3- Praktische Client-Integration und Netzwerkkomponenten

Als angehender Fachinformatiker

möchte ich Clients selbstständig in ein Netzwerk integrieren, die Funktionsweise der verschiedenen Netzwerkkomponenten verstehen und grundlegende Netzwerkfunktionen testen,

damit ich für die "Innovate GmbH" die Arbeitsplätze betriebsbereit machen und das Netzwerk erweitern kann.

# Celebration Criteria

- Wir können einen Windows- und einen Ubuntu-Client manuell mit einer statischen IP-Adresse sowie automatisch per DHCP konfigurieren.
- Wir können die grundlegenden Kommandozeilen-Tools (`ping`, `ipconfig`/`ip addr`, `tracert`/`traceroute`, `nslookup`/`dig`) anwenden, um die Netzwerkkonnektivität zu überprüfen und Fehler einzugrenzen.
- Wir können die Funktionen und Unterschiede der wichtigsten kabelgebundenen Netzwerkkomponenten (Hub, Switch, Bridge, Gateway) und Kabeltypen (SFTP, UFTP, Fibre Channel) erklären.
- Wir können die Funktionen und Unterschiede der wichtigsten WLAN-Komponenten (Router, Access Point, Repeater, Mesh-System) erklären.
- Wir können einen systematischen Prozess zur Fehlersuche bei Netzwerkproblemen eines Clients beschreiben.

**Szenario:** Die passive Verkabelung bei der "Innovate GmbH" ist abgeschlossen und der Internetanschluss ist aktiv. Eure Aufgabe ist es nun, die gelieferten Komponenten korrekt zu identifizieren und zu verbinden, die fünf Computer der Mitarbeiter zu konfigurieren und sicherzustellen, dass jeder Arbeitsplatz Zugriff auf das lokale Netzwerk und das Internet hat. Die Geschäftsführung fragt außerdem an, wie das WLAN für Gäste und mobile Geräte optimal aufgespannt werden kann.

# Abschlussaufgabe

## Inbetriebnahme- und Abnahmeprotokoll inkl. Erweiterungskonzept

Die Installation ist erfolgt. Euer Team ist nun für die "Inbetriebnahme" (das zum Leben Erwecken) und die offizielle "Abnahme" des Netzwerks verantwortlich. Erstellt ein umfassendes Protokoll, das diesen Prozess dokumentiert. Zusätzlich sollt ihr auf eine neue Anforderung der Geschäftsführung reagieren und ein Erweiterungskonzept für WLAN und einen zukünftigen zweiten Standort erstellen.

## Anforderungen an den Inhalt

### Teil A: Inbetriebnahme-Protokoll

- **Hardware-Verifikation:** Dokumentiert die verbauten aktiven Komponenten (Router, Switch) mit Modell und Seriennummer und bestätigt den korrekten Anschluss (Patchung vom Patchpanel zum Switch) (Wissen aus **LF3.3.3**).
- **Client-Konfiguration:** Erstellt eine Tabelle, in der für jeden der 5 Arbeitsplatz-PCs (gemischt Windows/Linux) die erfolgte IP-Konfiguration (ob statisch oder per DHCP bezogen) mit den finalen Werten (IP, Subnetzmaske, Gateway, DNS) dokumentiert wird (Wissen aus **LF3.3.1**).
- **Funktionstest & Abnahme:** Entwickelt ein Testprotokoll. Führt für jeden Client eine standardisierte Testreihe durch und hakt die Ergebnisse ab (OK/Fehler). Die Testreihe muss umfassen:
    - `ping` auf das Gateway
    - `ping` auf einen anderen Client im LAN
    - `ping` auf eine externe IP (z.B. `8.8.8.8`)
    - `nslookup` auf eine externe Domain (z.B. `www.rheinwerk-verlag.de`)
    - `tracert` zu einer externen Domain
    - Erfolgreicher Aufruf einer Webseite im Browser. Dokumentiert einen (simulierten) Fehler bei einem Client und beschreibt die Schritte eurer systematischen Fehlersuche zur Behebung (Wissen aus **LF3.3.2**).

### Teil B: Erweiterungskonzept

- **WLAN-Planung:** Die Geschäftsführung wünscht sich nun flächendeckendes WLAN für Mitarbeiter-Laptops und ein sicheres Gäste-WLAN. Erstellt ein Konzept, das eine begründete Empfehlung für eine technologische Lösung (z.B. Mesh-System vs. mehrere Access Points) enthält. Skizziert die geplanten Standorte der WLAN-Komponenten auf dem Büro-Grundriss und beschreibt die wichtigsten Konfigurationsparameter (SSIDs, Verschlüsselung, Gäste-Netz-Isolation) (Wissen aus **LF3.3.4**).
- **Vorbereitung für Skalierung:** Gebt einen kurzen, strategischen Ausblick, wie ein zukünftiger zweiter Standort angebunden werden könnte. Erklärt der Geschäftsführung in einfachen Worten den Unterschied zwischen einer traditionellen Standleitung und einer modernen SD-WAN-Lösung und warum letztere für ein agiles Startup vorteilhaft sein könnte (Wissen aus **LF3.3.5**).

## Präsentation

Stellt eure Ergebnisse in einer 15-minütigen "Projekt-Abnahme"-Sitzung vor. Übergebt das Protokoll und präsentiert das Erweiterungskonzept.  
<br/><br/>