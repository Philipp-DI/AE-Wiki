# Mohammed

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

> 1. **Recherche:** Wählt in der Gruppe eines der beiden Beispiele (SolarWinds oder Log4j). Recherchiert den Ablauf des Angriffs und erstellt eine einfache Visualisierung (z.B. eine Zeitachse oder ein Ablaufdiagramm), die den Weg des Angreifers von der Kompromittierung des Lieferanten bis zum Endziel zeigt.

:::success
![](files/019cee46-bfa2-75ca-ab6b-9c5627ba0781/Orange_Yellow_and_Purple_Modern_Business_Marketing_Process_Infographic_Presentation.png)
:::

> 2. **Diskussion:** Warum sind Supply-Chain-Angriffe so gefährlich und schwer zu erkennen? Brainstormt Gründe.

:::success
**Warum Supply-Chain-Angriffe der Albtraum jedes IT-Leiters sind?:**

- **Das Vertrauens-Paradoxon:** Wir sind darauf trainiert, Updates von bekannten Herstellern zu vertrauen. Wenn der vertrauenswürdige Kanal selbst kompromittiert ist, versagen unsere normalen Warnsysteme.
- **Die Nadel im Heuhaufen:** Moderner Code besteht aus Millionen Zeilen. Ein paar Zeilen bösartiger Code fallen darin kaum auf, besonders wenn sie gut versteckt sind.
- **Enorme Reichweite:** Mit nur einem erfolgreichen Hack bei einem Lieferanten (oder einer Bibliothek wie Log4j) erreicht ein Angreifer mit einem Schlag tausende Ziele gleichzeitig. Das ist extrem effizient für Hacker.
:::

> 3. **SBOM in der Praxis:** Stellt euch vor, ihr nutzt eine Webanwendung, die aus 20 verschiedenen Open-Source-Komponenten besteht. Eine Warnung über eine kritische Lücke in Komponente "X" wird veröffentlicht. Beschreibt, wie euch ein vorhandener SBOM bei der Reaktion auf diesen Vorfall helfen würde.

:::success
**KreativKopf GmbH** nutzt eine Webanwendung. Plötzlich ploppt die Warnung auf: _"Kritische Sicherheitslücke in Komponente X gefunden!"_

### Ohne SBOM (Das Chaos):

Die IT-Abteilung müsste panisch alle Entwickler anrufen oder hunderte Code-Dateien manuell durchsuchen: "Nutzen wir Komponente X irgendwo? In welcher Version? In welcher App?" Das kann Tage oder Wochen dauern – Zeit, in der die Hacker schon längst im System sein könnten.

### Mit SBOM (Die schnelle Lösung):

Ein **SBOM (Software Bill of Materials)** ist wie die **Zutatenliste auf einer Pizzapackung**. Wenn man weiß, dass man gegen Erdnüsse allergisch ist, schaut man einfach auf die Liste.

1. **Abgleich:** Die IT öffnet die SBOM-Datei (oft ein einfaches digitales Dokument).
2. **Suche:** Ein kurzer Suchbefehl nach **"Komponente X".**
3. **Ergebnis:** Innerhalb von Sekunden wissen wir: "Ja, wir nutzen sie in **App A** und **App B** in der betroffenen Version 1.2."
4. **Reaktion:** Wir können gezielt nur diese beiden Apps abschalten oder patchen, während alles andere sicher weiterläuft.
:::

# Quellen und Vertiefung

- **Online-Ressource:** [BSI - Cyber-Sicherheitslagebild zur Software-Lieferkette (2022)](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Lageberichte/Lagebild_Software_Lieferkette.pdf%3F__blob%3DpublicationFile)
- **Online-Ressource:** [Heise.de - Dossier zur Log4Shell-Sicherheitslücke](https://www.google.com/search?q=https://www.heise.de/thema/Log4Shell)