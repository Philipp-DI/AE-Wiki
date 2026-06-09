# 🐝 Olena

Als angehender IT-Sicherheitsbeauftragter

möchte ich die Struktur und die Komponenten des BSI IT-Grundschutzes verstehen,

damit ich systematisch Sicherheitsanforderungen für mein Unternehmen finden und anwenden kann.

# Celebration Criteria

- Wir können den Zweck des BSI IT-Grundschutzes und seine Beziehung zur internationalen Norm ISO 27001 erklären.  
  <br/>Der IT-Grundschutz ist somit ein **"Wie"**\-Leitfaden für Informationssicherheit, der klare Anweisungen zur Implementierung gibt.
  
  |     |     |     |
  | --- | --- | --- |
  | **Standard** | **Fokus (Die Frage)** | **Art der Vorgabe** |
  | **ISO 27001** | **WAS** muss getan werden, um ein ISMS zu führen? | Stellt **Anforderungen** an das Managementsystem (ISMS). |
  | **BSI IT-Grundschutz** | **WIE** setze ich diese Anforderungen praktisch um? | Liefert **Lösungen und Maßnahmen** zur Erfüllung dieser Anforderungen. |
  
  **Komplementarität und Zertifizierung:**
  
  1. **Erfüllung der Anforderungen:** Der IT-Grundschutz wurde explizit so konzipiert, dass eine vollständige und korrekte Umsetzung der BSI-Standards **200-1, 200-2 und 200-3** automatisch die **Anforderungen der ISO 27001 erfüllt**.
  2. **Vereinfachte Umsetzung:** Anstatt die Maßnahmen aus dem abstrakten ISO-Anhang A (Kontrollen) selbst zu entwickeln, bietet das BSI mit dem **IT-Grundschutz-Kompendium** einen **vorgefertigten, detaillierten Maßnahmenkatalog** an.
  3. **Zertifizierung:** Eine Organisation kann ein **ISO 27001-Zertifikat auf Basis des IT-Grundschutzes** erlangen. Dieses Zertifikat bescheinigt die Konformität mit der ISO 27001, wobei die Einhaltung der BSI-Standards als Nachweis für die Umsetzung der Kontrollen dient.
  
  Kurz gesagt: Der **BSI IT-Grundschutz** ist in Deutschland der wichtigste und detaillierteste Weg, um **ISO 27001-Konformität** zu erreichen.
- Wir können die Hauptkomponenten des IT-Grundschutzes (BSI-Standards, IT-Grundschutz-Kompendium) benennen.  
  
- Wir können die Struktur eines "Bausteins" aus dem Kompendium (Gefährdungen, Anforderungen) beschreiben.  
  <br/>Jeder Baustein enthält- Thema  
  \- Elementare Gefährdungen- Eine Liste Sicherheitsanforderungen  
  \- Basis immer  
  \- Standard bei normalem Schutzbedarf  
  \- Hohe bei hohem oder sehr hohem Schutzbedarf
- Wir können in den Bausteinen gezielt nach Sicherheitsanforderungen für ein konkretes Zielobjekt (z.B. einen Webserver) suchen.

# Wissens-Briefing

Der **BSI IT-Grundschutz** ist eine vom Bundesamt für Sicherheit in der Informationstechnik (BSI) entwickelte, praxiserprobte Methodik zum Aufbau eines Informationssicherheits-Managementsystems (ISMS). Er bietet eine konkrete Anleitung, um ein angemessenes Sicherheitsniveau zu erreichen und ist kompatibel zur internationalen Norm **ISO 27001**.

Die zentralen Bestandteile sind:

- **BSI-Standards:** Sie beschreiben die Vorgehensweise.
  - **BSI 200-1:** Allgemeine Anforderungen an ein ISMS.
  - **BSI 200-2:** Die IT-Grundschutz-Vorgehensweise (Strukturanalyse, Schutzbedarf, Modellierung - die wir in diesem Epic praktisch anwenden).
  - **BSI 200-3:** Risikomanagement.
- **IT-Grundschutz-Kompendium:** Dies ist das Herzstück und quasi ein riesiger Katalog von Best Practices. Es ist in **Bausteine** gegliedert, die typische Komponenten einer IT-Landschaft repräsentieren (z.B. `SYS.1.2 Windows Server`, `APP.1.2 Webbrowser`, `ORP.4 Patch- und Änderungsmanagement`).

Jeder **Baustein** enthält:

1. Eine Beschreibung des Themas.
2. Eine Liste typischer **elementarer Gefährdungen**.
3. Eine Liste konkreter **Sicherheitsanforderungen**, die umgesetzt werden müssen. Diese sind unterteilt in:
  - **Basis-Anforderungen (B):** Absolut grundlegend, müssen immer erfüllt sein.
  - **Standard-Anforderungen (S):** Sollten bei normalem Schutzbedarf umgesetzt werden.
  - **Anforderungen für hohen Schutzbedarf (H):** Notwendig bei hohem oder sehr hohem Schutzbedarf.

# Aufgaben

1. **Struktur verstehen:** Navigiert auf der Webseite des BSI zum IT-Grundschutz-Kompendium. Wählt den Baustein `APP.1.2 Webbrowser` aus. Identifiziert die Anzahl der Basis-, Standard- und Hoch-Anforderungen.  
  <br/>https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Grundschutz/IT-GS-Kompendium_Einzel_PDFs_2023/06_APP_Anwendungen/APP_1_2_Webbrowser_Edition_2023.pdf?__blob=publicationFile&v=3  
  <br/>APP.1.2.A1 Verwendung von grundlegenden Sicherheitsmechanismen (B)  
  APP.1.2.A2 Unterstützung sicherer Verschlüsselung der Kommunikation (B)  
  APP.1.2.A3 Verwendung von vertrauenswürdigen Zertifikaten (B)  
  APP.1.2.A6 Kennwortmanagement im Webbrowser (B)  
  APP.1.2.A13 Nutzung von DNS-over-HTTPS (B)  
  <br/>**APP.1.2.A7 Datensparsamkeit in Webbrowsern (S) \[Benutzende\]**  
  <br/>\__  
  APP.1.2.A9 Einsatz einer isolierten Webbrowser-Umgebung (H)  
  APP.1.2.A10 Verwendung des privaten Modus (H) \[Benutzende\]  
  APP.1.2.A11 Überprüfung auf schädliche Inhalte (H)  
  APP.1.2.A12 Zwei-Browser-Strategie (H)  
  
2. **Anforderung analysieren:** Lest euch im selben Baustein die Standard-Anforderung `APP.1.2.A1 Verwendung von grundlegenden Sicherheitsmechanismen` durch. Fasst in eigenen Worten zusammen, was diese Anforderung verlangt und warum sie wichtig ist.  
  <br/>Die Anforderung APP.1.2.A1 besagt, dass Ihr Webbrowser für die Arbeit im Unternehmen modern und geschützt sein MUSS, fähig, bösartige Prozesse zu isolieren und das Laden verdächtiger Inhalte zu verhindern.
3. **Anwendung im Szenario:** Welche Bausteine aus dem Kompendium wären für die Analyse des Grafikdesigner-Arbeitsplatzes der "KreativKopf GmbH" (Desktop-PC mit Windows 11, Adobe CC, NAS, Cloud-Anbindung) relevant? Listet mindestens fünf passende Bausteine auf.  
  <br/>Die "KreativKopf GmbH" hat nach eurer ersten Präsentation beschlossen, eine systematische **Schutzbedarfsanalyse** durchzuführen. Als Pilotprojekt soll der typische **Arbeitsplatz eines Grafikdesigners** analysiert werden. Dieser Arbeitsplatz besteht aus einem leistungsstarken **Desktop-PC (Windows 11)** mit **zwei Monitoren**, spezieller **Grafiksoftware (z.B. Adobe Creative Cloud)**, einem **lokalen NAS** für **schnelle Zwischenspeicherung** von großen Projektdateien und einer **Verbindung zum zentralen Cloud-Speicher** des Unternehmens, **wo die finalen Kundendaten liegen**. Der Designer arbeitet sowohl an öffentlichen  
  <br/>https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Grundschutz/IT-GS-Kompendium/IT_Grundschutz_Kompendium_Edition2023.pdf?__blob=publicationFile&v=4#download=1
  
  | Baustein |
  | --- |
  | NET.2.2 WLAN-Nutzung |
  | SYS.2.2.3 Clients unter Windows |
  | SYS.1.8 Speicherlösungen |
  | ORP.2 Personal |
  | OPS.2.2 Cloud-Nutzung |
  

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.2 "Standards und Normen", Abschnitt "IT-Grundschutz des BSI”
- **Online-Ressource:** [BSI - IT-Grundschutz-Kompendium](https://www.bsi.bund.de/DE/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/IT-Grundschutz/IT-Grundschutz-Kompendium/it-grundschutz-kompendium_node.html)