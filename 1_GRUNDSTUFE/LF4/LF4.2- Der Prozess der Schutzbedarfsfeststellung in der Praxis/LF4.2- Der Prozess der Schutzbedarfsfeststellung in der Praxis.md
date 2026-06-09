# LF4.2- Der Prozess der Schutzbedarfsfeststellung in der Praxis

Als Umschüler zum Fachinformatiker

möchte ich den Prozess der Schutzbedarfsfeststellung nach dem BSI IT-Grundschutz praktisch anwenden können,

damit ich den Schutzbedarf für konkrete IT-Systeme und Informationen systematisch ermitteln und dokumentieren kann.

# Celebration Criteria

- Wir können die Prozessschritte der Schutzbedarfsfeststellung nach BSI-Standard 200-2 (Strukturanalyse, Schutzbedarfsfeststellung, Modellierung) in der richtigen Reihenfolge erklären.
- Wir können für einen definierten Anwendungsbereich (z.B. einen Arbeitsplatz) die relevanten Zielobjekte (Anwendungen, IT-Systeme, Räume, Informationen) identifizieren.
- Wir können den Schutzbedarf für ein Zielobjekt hinsichtlich Vertraulichkeit, Integrität und Verfügbarkeit in den Kategorien "normal", "hoch" und "sehr hoch" begründen und festlegen.
- Wir können das Maximumprinzip bei der Vererbung von Schutzbedarfen erklären und anwenden (z.B. von der Anwendung auf das IT-System).
- Wir können die Ergebnisse einer Schutzbedarfsfeststellung übersichtlich und nachvollziehbar dokumentieren.

![](files/019cee3c-140e-745b-9ec0-a1d552201dfe/image.png)

# Fiktives Szenario

Die "KreativKopf GmbH" hat nach eurer ersten Präsentation beschlossen, eine systematische **Schutzbedarfsanalyse** durchzuführen. Als Pilotprojekt soll der typische **Arbeitsplatz eines Grafikdesigners** analysiert werden. Dieser Arbeitsplatz besteht aus einem leistungsstarken **Desktop-PC (Windows 11)** mit **zwei Monitoren**, spezieller **Grafiksoftware (z.B. Adobe Creative Cloud)**, einem **lokalen NAS** für **schnelle Zwischenspeicherung** von großen Projektdateien und einer **Verbindung zum zentralen Cloud-Speicher** des Unternehmens, **wo die finalen Kundendaten liegen**. Der Designer arbeitet sowohl an öffentlichen Werbekampagnen als auch an **vertraulichen Entwürfen** für noch nicht veröffentlichte Produkte.

# Gesamtaufgabe

Führt als Lerngruppe eine vollständige Schutzbedarfsfeststellung für den beschriebenen Arbeitsplatz des Grafikdesigners bei der "KreativKopf GmbH" durch. Geht dabei wie folgt vor:

1. **Strukturanalyse:** Identifiziert und listet alle relevanten Zielobjekte auf, die zu diesem Arbeitsplatz gehören (z.B. Informationen, Anwendungen, IT-Systeme, Kommunikationsverbindungen, Räume).
2. **Schutzbedarfsfeststellung:** Bestimmt für jedes Zielobjekt den Schutzbedarf (normal, hoch, sehr hoch) für die Grundwerte Vertraulichkeit, Integrität und Verfügbarkeit. Begründet eure Einstufung schriftlich, insbesondere unter Anwendung des Maximumprinzips.
3. **Dokumentation:** Fasst eure Ergebnisse in einem **übersichtlichen Dokument** zusammen, das Tabellen nach dem [**Vorbild des BSI**](https://www.bsi.bund.de/DE/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/IT-Grundschutz/Zertifizierte-Informationssicherheit/IT-Grundschutzschulung/Online-Kurs-IT-Grundschutz/Lektion_4_Schutzbedarfsfeststellung/Lektion_4_04/Lektion_4_04_node.html) enthält. Erstellt eine Abschlusspräsentation, in der ihr der Geschäftsführung eure Ergebnisse und die Begründungen für die wichtigsten Einstufungen (insbesondere "hoch" oder "sehr hoch") vorstellt und erste Empfehlungen für **mind. 3 notwendige Schutzmaßnahmen** ableitet.
  
  #### Dokument:
  
  https://www.canva.com/design/DAG3ueIhv9g/baOWSlf2JhnaqEOfKdQIgQ/edit?utm_content=DAG3ueIhv9g&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton

| Zielobjekt | Schutzbedarf Vertraulichkeit | Begründung | Schutzbedarf Integrität | Begründung | Schutzbedarf Verfügbarkeit | Begründung |
| --- | --- | --- | --- | --- | --- | --- |
| **Desktop-PC** | Hoch | Enthält sensible Projektdateien und Zugang zu Anwendungen. Wenn jemand unbefugtes Zugang erhält wird die Vertraulichkeit maßgeblich verletzt. | Hoch | Alle Daten und Software müssen korrekt sein und funktionieren. Wenn sich hier Fehler einschleichen, kann dies in der Kette schlimme Folgen haben. | Normal | Ausfall blockiert sämtliche Arbeit, aber im schlimmsten Fall verliert man ein wenig Arbeitszeit. |
| **Grafiksoftware (Adobe CC)** | Hoch | Verarbeitung vertraulicher Kundendaten in Bildbearbeitung und Entwürfe. Bedeutet, dass Dokumente, die sich in der Bearbeitung finden einen hohen Schutzbedarf haben. | Hoch | Die Anwendungen selbst enthalten keine Daten oder Informationen. Im Falle der Nutzung der Cloud besteht für den Schutz ein hoher Bedarf. | Hoch | Verzögerung der Arbeitsprozesse bei Projekten wenn es zu einem Ausfall kommt. |
| **lokales NAS** | Hoch | Zwischengespeicherte Dateien können vertraulich sein. | Hoch | Daten müssen fehlerfrei gespeichert werden | Normal | Daten müssen für Arbeitsfluss verfügbar sein. |
| **Büroraum** | Hoch | Unbefugte sollten keinen Zugang haben, da sonst sensible Daten mitgelesen oder gestohlen werden könnten. | Normal | Die Integrität des Raumes ist absolut zweitrangig und hat keine Priorität. Nur durch abstrakte Fälle kann hierdurch ein Schaden entstehen. | Normal | Verzögerung der Arbeitsprozesse **_vor Ort_** bei Projekten wenn es zu einem Ausfall kommt. |
| **WAN, LAN, WLAN** **(Kommunikationsverbindungen)** | Hoch | Zugang zur Cloud-Anwendung benötigt sichere Internet-Verbindung. | Hoch | Datenübertragung muss fehlerfrei sein. | Hoch | Netzverbindung notwendig für Zugriff auf Cloud und NAS. |
| **Cloudzugang/ Cloud-Speicher** | Sehr hoch | Zugangsdaten müssen vertraulich behandelt werden! Enthält finale Kundendaten und vertrauliche Projekte. | Sehr hoch | Zugangsdaten und Kundendaten müssen unverändert und korrekt sein. Manipulation und/oder vollständiges Löschen könnte die Existenz des Unternehmens bedrohen. | Hoch | Ausfall verhindert Zugriff auf zentrale Daten/Kundendaten/Entwürfe. |

## Artefakt:

https://www.canva.com/design/DAG3ueIhv9g/baOWSlf2JhnaqEOfKdQIgQ/edit?utm_content=DAG3ueIhv9g&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton

- [ ] ==Auf welche Schutzziele zahlen eure Vorschläge jeweils ein?==
- [ ] ==SÜ1-3 im KMU-Szenario? Was wäre an dieser Stelle realisitischer?==