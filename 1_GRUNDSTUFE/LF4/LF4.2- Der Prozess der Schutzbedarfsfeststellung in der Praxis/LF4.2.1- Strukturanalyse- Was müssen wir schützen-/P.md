# 👀 Philipp

Als Mitglied im IT-Sicherheitsteam

möchte ich lernen, eine Strukturanalyse durchzuführen,

damit ich die Bestandsaufnahme für ein Sicherheitskonzept methodisch korrekt vorbereiten kann.

# Celebration Criteria

- Wir können erklären, was ein "Informationsverbund" im Sinne des BSI ist.
- Wir können die verschiedenen Zielobjekt-Typen (z.B. Geschäftsprozesse, Anwendungen, IT-Systeme, Netze, Räume, Personen) benennen.
- Wir können für einen gegebenen Arbeitsplatz oder eine Abteilung die relevanten Zielobjekte identifizieren und auflisten.
- Wir können die Abhängigkeiten zwischen den Zielobjekten beschreiben (z.B. "Anwendung X läuft auf IT-System Y").

# Wissens-Briefing

Bevor man den Schutzbedarf feststellen kann, muss man wissen, **was** genau geschützt werden soll. Diesen Prozess der Erfassung nennt man Strukturanalyse.

- **Informationsverbund:** Die Gesamtheit aller IT-Systeme, Netze, Räume, Personen und Prozesse, die zur Erfüllung einer bestimmten Aufgabe (z.B. der Arbeit in einer Abteilung) notwendig sind. Der Geltungsbereich der Analyse muss zu Beginn klar definiert werden (z.B. "der Arbeitsplatz des Grafikdesigners").
- **Zielobjekte:** Die einzelnen Bausteine eines Informationsverbunds, die geschützt werden müssen. Das BSI unterteilt diese in verschiedene Typen:
  - **Geschäftsprozesse & Anwendungen:** z.B. "Erstellung von Kundenentwürfen", "Adobe Photoshop", "Microsoft Teams".
  - **Informationen:** Die Daten, die verarbeitet werden, z.B. "Kundendaten", "Entwurfsdateien", "Rechnungen".
  - **IT-Systeme:** Die Hardware, auf der alles läuft, z.B. "Desktop-PC", "NAS-Speicher", "Smartphone".
  - **Netze & Kommunikationsverbindungen:** z.B. "LAN-Anschluss", "WLAN", "VPN-Verbindung zum Cloud-Speicher".
  - **Infrastruktur/Räume:** Die physische Umgebung, z.B. "Büroraum 2.04", "Serverraum".

Die Erfassung erfolgt typischerweise durch Interviews mit den verantwortlichen Mitarbeitern, Sichtung vorhandener Dokumentationen und Begehungen vor Ort. Das Ergebnis ist eine detaillierte Liste aller relevanten Zielobjekte und ihrer Abhängigkeiten.

**Beispiel für eine Abhängigkeit:** Die Anwendung "Adobe Photoshop" (Zielobjekt Anwendung) läuft auf dem "Desktop-PC" (Zielobjekt IT-System) und verarbeitet "Entwurfsdateien" (Zielobjekt Information).

# Aufgaben

1. **Zielobjekte identifizieren:** Nehmt das Szenario des Grafikdesigner-Arbeitsplatzes aus dem Lern-Epic. Erstellt in einem geteilten Dokument (z.B. einer Tabelle) eine Liste aller Zielobjekte, unterteilt nach den Kategorien (**Anwendungen & Prozesse, IT-Systeme, Räume, Kommunikationsverbindungen**). → https://www.bsi.bund.de/DE/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/IT-Grundschutz/Zertifizierte-Informationssicherheit/IT-Grundschutzschulung/Online-Kurs-IT-Grundschutz/Lektion_4_Schutzbedarfsfeststellung/Lektion_4_04/Lektion_4_04_node.html
  
  | Zielobjekt | Kategorie | prognostizierter Schutzbedarf |
  | --- | --- | --- |
  | Desktop-PC | IT-Systeme | Sehr hoch |
  | Bildbearbeitung (Adobe CC) | Anwendungen & Prozesse | Normal |
  | NAS-Server | IT-Systeme | Hoch |
  | Büroraum | Räume | Hoch |
  | WAN,LAN,WLAN | Kommunikationsverbindungen | Hoch |
  | Cloudzugang | Anwendungen & Prozesse | Sehr hoch |
  
2. **Abhängigkeiten visualisieren:** Erstellt eine einfache Mindmap oder ein Diagramm (z.B. mit Miro oder [draw.io](http://draw.io)), das die Abhängigkeiten zwischen den von euch identifizierten Zielobjekten darstellt. Welche Anwendung läuft auf welcher Hardware? Welche Informationen werden von welcher Anwendung verarbeitet?![diagram.drawio.svg](files/019cee46-8dd7-7492-9c65-e88adbbce72e/diagram.drawio.svg)  
  <br/>
3. **Interview vorbereiten:** Simuliert die Vorbereitung eines Interviews mit dem Grafikdesigner. Erstellt einen kurzen Fragebogen mit 5-7 Fragen, die ihr ihm stellen würdet, um alle relevanten Informationen für die Strukturanalyse zu erhalten.

| Nr. | Frage | Ziel der Frage |
| --- | --- | --- |

|     |     |     |
| --- | --- | --- |
| **1 Arbeitsabläufe** | Welche Hauptaufgaben führen Sie an Ihrem Arbeitsplatz täglich durch? | Definition der Geschäftsprozesse |

|     |     |     |
| --- | --- | --- |
| **2 Verwendete Anwendungen** | Mit welchen Programmen oder Anwendungen arbeiten Sie regelmäßig? | Erfassung der Anwendungen |

|     |     |     |
| --- | --- | --- |
| **3 Daten und Dateien** | Wo speichern Sie Ihre Arbeitsdateien und Kundendaten ab? | Ermittlung der Speicherorte / IT-Systeme |

|     |     |     |
| --- | --- | --- |
| **4 Zugriff von Zuhause oder Unterwegs** | Greifen Sie auch von unterwegs oder von zu Hause auf Ihre Daten zu? | Feststellung von Netzen / Verbindungen |

|     |     |     |
| --- | --- | --- |
| **5 Sensibilität der Daten** | Welche Daten sind aus Ihrer Sicht besonders sensibel oder kritisch? | Einschätzung des Schutzbedarfs |

|     |     |     |
| --- | --- | --- |
| **6 Hardware und IT-Systeme** | Wie wichtig ist es für Ihre Arbeit, dass Ihr PC oder das NAS jederzeit verfügbar ist? | Bewertung der Verfügbarkeitsanforderung |

|     |     |     |
| --- | --- | --- |
| **7 Probleme und Risiken** | Welche Sicherheitsmaßnahmen kennen oder nutzen Sie bereits (z. B. Passwörter, VPN, Verschlüsselung)? | Erfassung organisatorischer Maßnahmen |

4. **Eigener Arbeitsplatz:** Führt eine vereinfachte Strukturanalyse eures eigenen (Lern-)Arbeitsplatzes Zuhause durch. Listet die wichtigsten Anwendungen, IT-Systeme und Informationen auf, mit denen ihr täglich arbeitet auf.+++ columnContainer +++  
  +++ column xs:12 md:6 lg:6 +++
  
  ### Netzplan
  
  ![diagram.drawio.svg](files/019cee46-8de5-753b-a372-fc80234d17e9/diagram.drawio.svg)  
  +++ end:column ++++++ column xs:12 md:6 lg:6 +++
  
  ### Anwendungen
  
  | Bezeichnung & Beschreibung | Benutzer/Verantwortlicher |
  | --- | --- |
  | **Docmost** - Wiki-artige online- bzw. browserbasierte Anwendung zu Darstellung und Bearbeitung der Lerninhalte. | Alle Lernenden und Mitarbeiter/ Dualis GmbH |
  | **Openproject** - Browserbasiertes Management-Tool zur Arbeitsstrukturierung der Projekt- und Lernarbeit. | Alle Lernenden und Mitarbeiter/ Dualis GmbH |
  | **Canva** - Browserbasiertes Präsentationstool zur Erstellung von Dokumenten und mehr. | Team Grundwerk/ Team Grundwerk |
  
  ### IT-Systeme
  
  | Bezeichnung & Beschreibung | Standort | Benutzer/Verantwortlicher |
  | --- | --- | --- |
  | **Laptop** - Hauptgerät zur Bearbeitung der Lerninhalte | Dynamisch | Philipp/ Philipp |
  | **Router inkl. Firewall** - Gateway zum WAN (Internet) | Zuhause | Philipp/ Philipp |
  | +++ end:column +++ |     |     |
  | +++ end:columnContainer +++ |     |     |
  

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.5 "Der Weg zum Sicherheitskonzept", Abschnitt "Strukturanalyse"
- **Online-Ressource:** [BSI-Standard 200-2: IT-Grundschutz-Vorgehensweise (PDF)](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Grundschutz/BSI-Standards/BSI-Standard_200-2.pdf%3F__blob%3DpublicationFile), Kapitel 4.2 "Strukturanalyse".