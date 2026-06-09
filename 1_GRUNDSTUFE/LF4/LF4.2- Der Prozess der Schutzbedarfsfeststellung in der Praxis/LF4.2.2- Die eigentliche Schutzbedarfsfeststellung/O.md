# 🐝 Olena

Als Mitglied im IT-Sicherheitsteam

möchte ich lernen, eine Strukturanalyse durchzuführen,

damit ich die Bestandsaufnahme für ein Sicherheitskonzept methodisch korrekt vorbereiten kann.

# Celebration Criteria

- Wir können erklären, was ein "Informationsverbund" im Sinne des BSI ist.  
  <br/>**Informationsverbund:** Die Gesamtheit aller IT-Systeme, Netze, Räume, Personen und Prozesse, die zur Erfüllung einer bestimmten Aufgabe (z.B. der Arbeit in einer Abteilung) notwendig sind. Der Geltungsbereich der Analyse muss zu Beginn klar definiert werden (z.B. "der Arbeitsplatz des Grafikdesigners").
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

1. **Zielobjekte identifizieren:** Nehmt das Szenario des Grafikdesigner-Arbeitsplatzes aus dem Lern-Epic. Erstellt in einem geteilten Dokument (z.B. einer Tabelle) eine Liste aller Zielobjekte, unterteilt nach den Kategorien (Anwendungen, Informationen, IT-Systeme, etc.).
  1. Die "KreativKopf GmbH" hat nach eurer ersten Präsentation beschlossen, eine systematische **Schutzbedarfsanalyse** durchzuführen. Als Pilotprojekt soll der typische **Arbeitsplatz eines Grafikdesigners** analysiert werden. Dieser Arbeitsplatz besteht aus einem **leistungsstarken Desktop-PC (Windows 11) mit zwei Monitoren**, spezieller **Grafiksoftware (z.B. Adobe Creative Cloud)**, einem **lokalen NAS** für schnelle Zwischenspeicherung von großen Projektdateien und einer **Verbindung zum zentralen Cloud-Speicher** des Unternehmens, wo die finalen **Kundendaten** liegen. Der Designer arbeitet sowohl an öffentlichen Werbekampagnen als auch an **vertraulichen Entwürfen** für **noch nicht veröffentlichte Produkte**.  
    
    <div class="joplin-table-wrapper"><table style="width: 325px"><tbody><tr><th colspan="1" rowspan="1" colwidth="179"><p data-id="npjazopciggb">Zielobjekt</p></th><th colspan="1" rowspan="1" colwidth="146"><p data-id="zzryjawkehnu">Type</p></th></tr><tr><td colspan="1" rowspan="1" colwidth="179"><ul><li><p data-id="ivuoouyevjgd">Windows 11</p></li><li><p data-id="mdxnooiuizfl">Adobe Creative Cloud</p></li><li><p data-id="cvmvosqdiswl">Verbindung zum Cloud-Speicher</p></li><li><p data-id="loysarefejxo">Zwischenspeicherung</p></li><li><p data-id="jakdkyzvzook">Datenaustausch</p></li></ul></td><td colspan="1" rowspan="1" colwidth="146"><p data-id="hlpvrgdbfgbg">Geschäftsprozesse &amp; Anwendungen</p></td></tr><tr><td colspan="1" rowspan="1" colwidth="179"><p data-id="ybqdslscyday">Grafikdesigner</p></td><td colspan="1" rowspan="1" colwidth="146"><p data-id="kaseqxktytld">Personen</p></td></tr><tr><td colspan="1" rowspan="1" colwidth="179"><ul><li><p data-id="asymtfiqgyqm">Kundendaten</p></li><li><p data-id="ppghkhipxvgh">Vertrauliche Entwürfe</p></li><li><p data-id="lkgdtcfefodh">Noch nicht veröffentlichte Produkte</p></li></ul></td><td colspan="1" rowspan="1" colwidth="146"><p data-id="tqphsithcyrv">Informationen</p></td></tr><tr><td colspan="1" rowspan="1" colwidth="179"><ul><li><p data-id="vlnnmnqzumoh">lokalen NAS</p></li><li><p data-id="keuzehloziyp">Desktop-PC</p></li><li><p data-id="nawnjbpvvnnm">zwei Monitoren</p></li></ul></td><td colspan="1" rowspan="1" colwidth="146"><p data-id="oegtsjfynblw">IT-Systeme</p></td></tr><tr><td colspan="1" rowspan="1" colwidth="179"><ul><li><p data-id="xsloxyiimrxj">LAN</p></li><li><p data-id="urknjsymbzsz">WLAN</p></li></ul></td><td colspan="1" rowspan="1" colwidth="146"><p data-id="dppoycsrteto">Netze &amp; Kommunikationsverbindungen</p></td></tr><tr><td colspan="1" rowspan="1" colwidth="179"><p data-id="efcunqigtgcz">Büroraum (<strong>Arbeitsplatz eines Grafikdesigners</strong>)</p></td><td colspan="1" rowspan="1" colwidth="146"><p data-id="npbebntztyan">Infrastruktur/Räume</p></td></tr></tbody></table></div>
    
    **IT-Grundschutz-Kompendium Edition 2023**
    
    |     |     |     |
    | --- | --- | --- |
    | **Zielobjekt** | **BSI-Kategorie (Typ)** | **Anmerkung (Zweck des Bausteins)** |
    | **Windows 11** | IT-Systeme | Das Betriebssystem ist der Hauptbestandteil des Clients. |
    | **Adobe Creative Cloud** | Anwendungen | Allgemeiner Baustein für Anwendungssoftware auf dem Client. |
    | **lokalen NAS** | IT-Systeme | Baustein für das Speichern von Daten in Netzwerkspeichern. |
    | **zwei Monitoren** | Infrastrukturen | Physischer Schutz und Zugangskontrolle zum Arbeitsplatz. |
    | **LAN** | Kommunikationsverbindungen | Absicherung des kabelgebundenen lokalen Netzwerks. |
    | **WLAN** | Kommunikationsverbindungen | Absicherung des drahtlosen Netzwerks, falls genutzt. |
    | **Büroraum** | Infrastrukturen | Physischer Schutz des Raumes, in dem die IT steht. |
    | **Grafikdesigner** | Personen | Regelungen für Personal und Personalwechsel. |
    | **Kundendaten** | Informationen & Werte | **ISMS.1** legt den Schutz fest; **CON.2** behandelt Datenschutzanforderungen (DSGVO). |
    | **Vertrauliche Entwürfe** | Informationen & Werte | **ISMS.1** legt den Schutz fest; **CON.1** behandelt ggf. kryptografische Konzepte. |
    | **Noch nicht veröffentlichte Produkte** | Informationen & Werte | Definition und Klassifizierung der Schutzziele (Vertraulichkeit, Integrität, Verfügbarkeit). |
    | **Verbindung zum Cloud-Speicher** | Kommunikationsverbindungen | Baustein zur sicheren Nutzung von Cloud-Diensten. |
    | **Zwischenspeicherung** | Organisatorische Vorgaben | Sicherstellung der Datensicherung für Backups des NAS/PCs. |
    | **Datenaustausch** | Organisatorische Vorgaben | Sichere Regeln für den Austausch von Informationen (intern/extern). |
    
      
    
2. **Abhängigkeiten visualisieren:** Erstellt eine einfache Mindmap oder ein Diagramm (z.B. mit Miro oder draw.io), das die Abhängigkeiten zwischen den von euch identifizierten Zielobjekten darstellt. Welche Anwendung läuft auf welcher Hardware? Welche Informationen werden von welcher Anwendung verarbeitet?  
  <br/>Der **Grafikdesigner** nutzt den **Desktop-PC**.Auf dem PC läuft das **Windows 11 (OS)**, das wiederum die **Adobe Creative Cloud** und den **Webbrowser** ausführt.Die **Adobe Creative Cloud** verarbeitet die **Vertraulichen Entwürfe**, **Kampagnendaten** und **Unveröffentlichte Produkte**.Diese Daten werden lokal auf dem **NAS** (Zwischenspeicherung) oder über den **Webbrowser**/das **Netzwerk (LAN/WLAN)** zum **Cloud-Speicher** (Finale Daten) übertragen.Der Schutz des **Desktop-PC** hängt somit direkt vom **Windows 11 OS** ab, und der Schutz der **Kundendaten** hängt von der Sicherheit des **Webbrowsers** und der **Cloud-Verbindung** ab.  
  
3. **Interview vorbereiten:** Simuliert die Vorbereitung eines Interviews mit dem Grafikdesigner. Erstellt einen kurzen Fragebogen mit 5-7 Fragen, die ihr ihm stellen würdet, um alle relevanten Informationen für die Strukturanalyse zu erhalten.  
  <br/>— Welche **spezifischen Programme** (neben Adobe CC) nutzen Sie täglich? Und **welchen Browser** verwenden Sie, um auf den Cloud-Speicher zuzugreifen?  
  <br/>— Bitte beschreiben Sie den genauen **Prozess des Speicherns** (z.B. von der lokalen Zwischenspeicherung auf dem NAS bis zur finalen Ablage in der Cloud). **Wie lange** bleiben die Dateien auf dem lokalen NAS?  
  <br/>— **Wie lange** können Sie maximal nicht arbeiten, falls Ihr **Desktop-PC ausfällt** oder die **Verbindung zur Cloud unterbrochen** wird, bevor ein großer Schaden (finanziell/Reputation) eintritt?  
  <br/>— Wer hat neben Ihnen **physischen** Zugriff auf den Büroraum, und wer hat **administrativen** Zugriff auf Ihren PC oder das  
  <br/>— Benötigen Sie **Fernzugriff** auf Ihren PC oder die Dateien auf dem NAS? Wenn ja, welche Methode nutzen Sie dafür (z.B. VPN, Remote Desktop)?  
  <br/>— Wie stellen Sie sicher, dass Ihre **Grafiksoftware** (z.B. Adobe) und Ihr **Windows-Betriebssystem** immer auf dem neuesten Stand sind (Manuell, automatisch, durch die IT)?  
  <br/><br/>
4. **Eigener Arbeitsplatz:** Führt eine vereinfachte Strukturanalyse eures eigenen (Lern-)Arbeitsplatzes durch. Listet die wichtigsten Anwendungen, IT-Systeme und Informationen auf, mit denen ihr täglich arbeitet.  
  <br/>\[Internet\]  
  ↓  
  \[Router (Magenta WLAN-490E)\]  
  ↓  
  \[PC / Laptop\] ─→ \[Cloud-Speicher\]  
  │  
  ├─ Anwendungen: Office, Teams, Browser  
  └─ Daten: Lernunterlagen, Passwörter

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.5 "Der Weg zum Sicherheitskonzept", Abschnitt "Strukturanalyse" (S. 996-997).
- **Online-Ressource:** [BSI-Standard 200-2: IT-Grundschutz-Vorgehensweise (PDF)](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Grundschutz/BSI-Standards/BSI-Standard_200-2.pdf%3F__blob%3DpublicationFile), Kapitel 4.2 "Strukturanalyse".

4.2 Aufbau der Informationssicherheitsorganisation  
7.4 Strukturanalyse .