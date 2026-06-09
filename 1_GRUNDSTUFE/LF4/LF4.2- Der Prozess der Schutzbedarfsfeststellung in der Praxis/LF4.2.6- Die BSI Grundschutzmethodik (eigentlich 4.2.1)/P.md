# Philipp

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
  
  | Anforderung | Anzahl |
  | --- | --- |
  | Basis (B) | 5   |
  | Standard (s) | 1   |
  | Hoch (H) | 4   |
  
2. **Anforderung analysieren:** Lest euch im selben Baustein die Standard-Anforderung `APP.1.2.A1 Verwendung von grundlegenden Sicherheitsmechanismen` durch. Fasst in eigenen Worten zusammen, was diese Anforderung verlangt und warum sie wichtig ist.Der Webbrowser muss **gut isoliert** sein.
  - **Jeder Tab ein eigener Raum (Sandboxing):** Jede Webseite (jeder Tab) und jedes Add-on (Plug-in) muss in einem eigenen, abgeschlossenen "Raum" laufen. So kann eine bösartige Webseite nicht aus ihrem "Raum" ausbrechen und andere Tabs (z. B. dein Online-Banking) oder den Computer angreifen.
  - **SOP & CSP:**
    - Eine Webseite darf nicht einfach Daten von einer anderen, fremden Webseite klauen (**Same-Origin-Policy**).
    - Der Browser muss kontrollieren, welche Inhalte eine Webseite laden darf, um Angriffe zu blockieren (**Content Security Policy**).
  - **Subresource Integrity:** Wenn eine Webseite Code von einer anderen Quelle lädt, muss der Browser prüfen können, ob dieser Code unterwegs manipuliert (z. B. mit einem Virus infiziert) wurde.
3. **Anwendung im Szenario:** Welche Bausteine aus dem Kompendium wären für die Analyse des Grafikdesigner-Arbeitsplatzes der "KreativKopf GmbH" (Desktop-PC mit Windows 11, Adobe CC, NAS, Cloud-Anbindung) relevant? Listet mindestens fünf passende Bausteine auf.
4. ORP.3 Sensibilisierung und Schulung zur Informationssicherheit
5. APP.1.1 Office-Produkte
6. APP.3.3 Fileserver
7. SYS.2.2 Windows-Clients
8. SYS.1.8 Speicherlösungen

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.2 "Standards und Normen", Abschnitt "IT-Grundschutz des BSI" (S. 973-976).
- **Online-Ressource:** [BSI - IT-Grundschutz-Kompendium](https://www.bsi.bund.de/DE/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/IT-Grundschutz/IT-Grundschutz-Kompendium/it-grundschutz-kompendium_node.html)