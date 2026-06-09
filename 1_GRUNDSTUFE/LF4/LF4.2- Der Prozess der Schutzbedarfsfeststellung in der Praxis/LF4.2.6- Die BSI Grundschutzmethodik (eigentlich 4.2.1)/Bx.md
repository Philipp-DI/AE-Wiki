# BruddaJayx

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
  Ich habe APP.1.2 Webbrowser benutzt, da ich kein APP.3.2 Webbrowser gefunden habe.
  
  | Basis-Anforderungen | Standard-Anforderungen | Hoch-Anforderungen |
  | --- | --- | --- |
  | 6 (A1-A6) | 3 (A7,A8 und A13) | 4 (A9-A12) |
  | Anforderung 4 entfällt | Anforderung 5 entfällt |     |
  
2. **Anforderung analysieren:** Lest euch im selben Baustein die Standard-Anforderung `APP.1.2.A1 Verwendung von grundlegenden Sicherheitsmechanismen` durch. Fasst in eigenen Worten zusammen, was diese Anforderung verlangt und warum sie wichtig ist.  
  **Was verlangt sie?**
  
  - Browser soll grundlegende Sicherheitsfunktionen nutzen (z. B. Sandbox, Schutz vor schädlichen Webseiten).
  - Diese Funktionen sollen immer aktiv sein, nicht abgeschaltet werden.
  
  **Warum wichtig?**
  - Browser ist oft Ziel von Angriffen.
  - Schutzmechanismen verhindern, dass Angriffe das ganze System treffen.
  - Sichert Daten und sorgt für sichere Nutzung.
3. **Anwendung im Szenario:** Welche Bausteine aus dem Kompendium wären für die Analyse des Grafikdesigner-Arbeitsplatzes der "KreativKopf GmbH" (Desktop-PC mit Windows 11, Adobe CC, NAS, Cloud-Anbindung) relevant? Listet mindestens fünf passende Bausteine auf.  
  <br/>\*\*Arbeitsplatz des Grafikdesigners;\*\*Der Designer nutzt Windows 11, Adobe CC, NAS und Cloud.  
  Diese Bausteine sind dafür wichtig:
  1. **SYS.2.1 Client-System** → Sicherheit für den PC ==—> SYS2.2.3 Clients Windows 10/11 konkretisiert im Szenario==
  2. **APP.1.2 Webbrowser** → Schutz beim Surfen
  3. **APP.6 Allgemeine Software** → Adobe & andere Programme
  4. **OPS.1.1.3 Patch-Management** → Updates richtig machen
  5. **OPS.1.1.4 Schutz vor Schadsoftware** → Virenschutz

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.2 "Standards und Normen", Abschnitt "IT-Grundschutz des BSI" (S. 973-976).
- **Online-Ressource:** [BSI - IT-Grundschutz-Kompendium](https://www.bsi.bund.de/DE/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/IT-Grundschutz/IT-Grundschutz-Kompendium/it-grundschutz-kompendium_node.html)