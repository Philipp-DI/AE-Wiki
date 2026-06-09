# LF4.3.4- Die unsichtbare Gefahr- Supply-Chain-Angriffe

Als Softwareentwickler

möchte ich die Mechanismen von Supply-Chain-Angriffen verstehen,

damit ich bei der Auswahl von externen Bibliotheken und Diensten die Risiken bewerten und sichere Entwicklungspraktiken anwenden kann.

# Celebration Criteria

- Wir können das Konzept eines Supply-Chain-Angriffs erklären.
- Wir können die Angriffe auf die Software-Lieferkette (z.B. kompromittierte Bibliothek) von Angriffen auf Dienstleister (z.B. kompromittierter IT-Dienstleister) unterscheiden.
- Wir können anhand eines realen Beispiels (SolarWinds oder Log4j) die immense Tragweite eines solchen Angriffs erläutern.
- Wir können den Zweck eines "Software Bill of Materials" (SBOM) als Abwehrmaßnahme erklären.

# Wissens-Briefing

Bei einem **Supply-Chain-Angriff** greift der Angreifer nicht sein eigentliches Ziel direkt an, sondern ein schwächeres Glied in dessen Lieferkette. Das Ziel ist es, das Vertrauensverhältnis zwischen dem Ziel und seinem Lieferanten auszunutzen, um so unbemerkt in die Systeme des Ziels zu gelangen.

**Zwei Haupttypen:**

1. **Angriff auf die Software-Lieferkette:** Der Angreifer schleust bösartigen Code in eine weit verbreitete Software-Komponente (z.B. eine Open-Source-Bibliothek) ein. Alle Entwickler, die diese kompromittierte Komponente in ihre eigene Software einbauen, verteilen unwissentlich die Schadsoftware an ihre eigenen Kunden.
  - **Beispiel Log4j (2021):** Eine extrem weit verbreitete Java-Bibliothek hatte eine kritische Sicherheitslücke, die es Angreifern erlaubte, aus der Ferne Code auf Servern auszuführen.
2. **Angriff auf Dienstleister:** Der Angreifer kompromittiert einen IT-Dienstleister (z.B. ein Systemhaus, einen Managed Service Provider), der Zugriff auf die Netzwerke vieler seiner Kunden hat. Über diesen vertrauenswürdigen Kanal kann der Angreifer dann in die Systeme der Kunden eindringen.
  - **Beispiel SolarWinds (2020):** Angreifer haben die Build-Umgebung der Firma SolarWinds kompromittiert und eine Backdoor in deren weit verbreitete Netzwerk-Management-Software "Orion" eingeschleust. Über ein reguläres Software-Update wurde diese Backdoor an tausende hochrangige Kunden (u.a. US-Ministerien) verteilt.

**Abwehrmaßnahmen:** Eine wichtige Maßnahme ist der **Software Bill of Materials (SBOM)**. Das ist eine "Stückliste" aller Software-Komponenten, aus denen eine Anwendung besteht. Im Falle einer neuer Schwachstelle wie bei Log4j kann ein Unternehmen so sofort prüfen, welche seiner Systeme betroffen sind.

# Aufgaben

1. **Recherche:** Wählt in der Gruppe eines der beiden Beispiele (SolarWinds oder Log4j). Recherchiert den Ablauf des Angriffs und erstellt eine einfache Visualisierung (z.B. eine Zeitachse oder ein Ablaufdiagramm), die den Weg des Angreifers von der Kompromittierung des Lieferanten bis zum Endziel zeigt.
2. **Diskussion:** Warum sind Supply-Chain-Angriffe so gefährlich und schwer zu erkennen? Brainstormt Gründe.
3. **SBOM in der Praxis:** Stellt euch vor, ihr nutzt eine Webanwendung, die aus 20 verschiedenen Open-Source-Komponenten besteht. Eine Warnung über eine kritische Lücke in Komponente "X" wird veröffentlicht. Beschreibt, wie euch ein vorhandener SBOM bei der Reaktion auf diesen Vorfall helfen würde.

# Quellen und Vertiefung

- **Online-Ressource:** [BSI - Cyber-Sicherheitslagebild zur Software-Lieferkette (2022)](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Lageberichte/Lagebild_Software_Lieferkette.pdf%3F__blob%3DpublicationFile)
- **Online-Ressource:** [Heise.de - Dossier zur Log4Shell-Sicherheitslücke](https://www.google.com/search?q=https://www.heise.de/thema/Log4Shell)