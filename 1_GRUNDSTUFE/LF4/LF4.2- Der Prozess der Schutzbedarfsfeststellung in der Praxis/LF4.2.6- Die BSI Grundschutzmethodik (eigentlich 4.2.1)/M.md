# Mohammed

Als angehender IT-Sicherheitsbeauftragter möchte ich die Struktur und die Komponenten des BSI IT-Grundschutzes verstehen, damit ich systematisch Sicherheitsanforderungen für mein Unternehmen finden und anwenden kann.

# Celebration Criteria

- Wir können den Zweck des BSI IT-Grundschutzes und seine Beziehung zur internationalen Norm ISO 27001 erklären.
- Wir können die Hauptkomponenten des IT-Grundschutzes (BSI-Standards, IT-Grundschutz-Kompendium) benennen.
- Wir können die Struktur eines "Bausteins" aus dem Kompendium (Gefährdungen, Anforderungen) beschreiben.
- Wir können in den Bausteinen gezielt nach Sicherheitsanforderungen für ein konkretes Zielobjekt (z.B. einen Webserver) suchen.

# Wissens-Briefing

Der **BSI IT-Grundschutz** ist eine vom Bundesamt für Sicherheit in der Informationstechnik (BSI) entwickelte, praxiserprobte Methodik zum Aufbau eines Informationssicherheits-Managementsystems (ISMS). Er bietet eine konkrete Anleitung, um ein angemessenes Sicherheitsniveau zu erreichen und ist kompatibel zur internationalen Norm **ISO 27001**.

Die zentralen Bestandteile sind:

- **BSI-Standards:** Sie beschreiben die Vorgehensweise.
  - **BSI 200-1:** Allgemeine Anforderungen an ein ISMS.
  - **BSI 200-2:** Die IT-Grundschutz-Vorgehensweise (Strukturanalyse, Schutzbedarf, Modellierung - die wir in diesem Epic praktisch anwenden).
  - **BSI 200-3:** Risikomanagement.
- **IT-Grundschutz-Kompendium:** Dies ist das Herzstück und quasi ein riesiger Katalog von Best Practices. Es ist in **Bausteine** gegliedert, die typische Komponenten einer IT-Landschaft repräsentieren (z.B. `SYS.1.2 Windows Server`, `APP.3.2 Webbrowser`, `ORP.4 Patch- und Änderungsmanagement`).

Jeder **Baustein** enthält:

1. Eine Beschreibung des Themas.
2. Eine Liste typischer **elementarer Gefährdungen**.
3. Eine Liste konkreter **Sicherheitsanforderungen**, die umgesetzt werden müssen. Diese sind unterteilt in:
  - **Basis-Anforderungen (B):** Absolut grundlegend, müssen immer erfüllt sein.
  - **Standard-Anforderungen (S):** Sollten bei normalem Schutzbedarf umgesetzt werden.
  - **Anforderungen für hohen Schutzbedarf (H):** Notwendig bei hohem oder sehr hohem Schutzbedarf.

# Aufgaben

1. **Struktur verstehen:** Navigiert auf der Webseite des BSI zum IT-Grundschutz-Kompendium. Wählt den Baustein `APP.3.2 Webbrowser` aus. Identifiziert die Anzahl der Basis-, Standard- und Hoch-Anforderungen.
2. **Anforderung analysieren:** Lest euch im selben Baustein die Standard-Anforderung `APP.3.2.S5: Zeitnahe Aktualisierung eines Webbrowsers` durch. Fasst in eigenen Worten zusammen, was diese Anforderung verlangt und warum sie wichtig ist.

### **Was die Anforderung verlangt**

- Webbrowser auf allen Arbeitsplätzen sollen **regelmäßig aktualisiert** werden.
- Sicherheitsupdates und Patches müssen **zeitnah installiert** werden, sobald sie vom Hersteller verfügbar sind.
- Ziel ist, dass bekannte Schwachstellen **nicht offenbleiben** und von Angreifern ausgenutzt werden können.
- Im Unternehmen kann dies **automatisiert** erfolgen oder durch einen definierten Prozess für manuelles Patchen.

### **Warum diese Anforderung wichtig ist**

- **Browser sind häufige Angriffsziele:**  
  Hacker nutzen Sicherheitslücken in veralteten Browsern, um Schadcode auszuführen oder Daten zu stehlen.
- **Schutz vor Exploits:**  
  Je schneller Updates eingespielt werden, desto kleiner ist das Risiko, dass bekannte Schwachstellen ausgenutzt werden.
- **System- und Datensicherheit:**  
  Durch zeitnahe Updates bleibt der Arbeitsplatz sicher und die IT-Infrastruktur stabil.
  
  3. **Anwendung im Szenario:** Welche Bausteine aus dem Kompendium wären für die Analyse des Grafikdesigner-Arbeitsplatzes der "KreativKopf GmbH" (Desktop-PC mit Windows 11, Adobe CC, NAS, Cloud-Anbindung) relevant? Listet mindestens fünf passende Bausteine auf.
  
  **_Für den Arbeitsplatz eines Grafikdesigners bei der KreativKopf GmbH (Desktop-PC mit Windows 11, Adobe CC, NAS, Cloud-Anbindung) sind aus dem IT-Grundschutz-Kompendium mehrere Bausteine relevant. Hier sind mindestens fünf passende Bausteine mit kurzer Begründung:_**
  
  ### **1\. SYS.2.2.3 – Clients unter Windows**
  
  - Bezieht sich auf Windows-Desktop-PCs.
  - Beschreibt Sicherheitsmaßnahmen für Client-Rechner, Betriebssystem und Benutzerkonten.
  
  ### **2\. APP.1.2 – Webbrowser**
  
  - Browser werden am Arbeitsplatz für Recherche, Cloud-Zugriff oder Uploads genutzt.
  - Schutz vor Exploits und regelmäßige Updates sind hier gefordert.
  
  ### **3\. APP.6 – Allgemeine Software**
  
  - Bezieht sich auf Anwendungen wie **Adobe CC**.
  - Regelt Installation, Updates, Lizenzkontrolle und sichere Konfiguration von Software.
  
  ### **4\. INF.7 – Büroarbeitsplatz**
  
  - Beinhaltet Peripheriegeräte, Netzwerkzugang, NAS-Anbindung und Arbeitsplatzorganisation.
  - Wichtig für sichere Integration aller Geräte am Arbeitsplatz.
  
  ### **5\. OPS.1.1.3 – Patch- und Änderungsmanagement**
  
  - Regelt die Verwaltung von Software-Updates und Patches für Betriebssystem, Anwendungen und Tools.
  - Stellt sicher, dass Sicherheitslücken schnell geschlossen werden.
  
  ---
  
  #### **Optional weitere relevante Bausteine:**
  
  - **OPS.2.2 – Cloud-Nutzung** → Schutz von Cloud-Diensten, Datenzugriff und Authentifizierung.
  - **SYS.1.1 – Allgemeiner Server** → wenn NAS oder lokale Server genutzt werden.
  - **NET.3.2 – Firewall** → Netzwerk-Schutz und Trennung von internen und externen Zugängen.

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.2 "Standards und Normen", Abschnitt "IT-Grundschutz des BSI" (S. 973-976).
- **Online-Ressource:** [BSI - IT-Grundschutz-Kompendium](https://www.bsi.bund.de/DE/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/IT-Grundschutz/IT-Grundschutz-Kompendium/it-grundschutz-kompendium_node.html)