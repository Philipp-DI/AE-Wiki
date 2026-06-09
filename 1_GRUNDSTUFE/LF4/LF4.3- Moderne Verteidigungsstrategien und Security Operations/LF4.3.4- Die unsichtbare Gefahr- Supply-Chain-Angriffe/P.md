# Philipp

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
  Log4j ist eine extrem weit verbreitete Code-Bib, die für das Erstellen von Log-Dateien gedacht war bzw. ist. Hier ist durch eine unbewusste Sicherheitslücke ein riesiges und weitreichendes Problem entstanden. Durch diese Lücke war es sogar möglich von überall per Fremdzugriff Befehle auf fremden Servern auszuführen. Hierzu der Ablauf des Vorfalls aus meinem Gem und überprüft anhand der Quellen:
  
  |     |     |     |
  | --- | --- | --- |
  | **Datum** | **Ereignis** | **Bedeutung** |
  | **2013** | Einführung des **JNDI**\-Features | Die Schwachstelle wurde unbewusst in den Code eingebaut. |
  | **24\. Nov 2021** | Private Meldung | Ein Sicherheitsforscher von Alibaba meldet die Lücke heimlich an Apache. |
  | **01\. Dez 2021** | Erste Ausnutzungen | Hacker beginnen (noch unbemerkt), die Lücke im kleinen Stil zu nutzen. |
  | **09\. Dez 2021** | **Öffentliche Bekanntgabe** | Die Lücke wird unter **CVE-2021-44228** bekannt. PoC-Code erscheint auf GitHub. |
  | **10\. Dez 2021** | Warnstufe Rot | Das BSI ruft die höchste Warnstufe aus. Die IT-Welt gerät in Panik. |
  | **14\. Dez 2021** | Zweite Lücke | Der erste Patch (2.15.0) war unvollständig (**CVE-2021-45046**). Ein neuer Patch (2.16.0) folgt. |
  | **18\. Dez 2021** | Dritte Lücke | Eine DoS-Schwachstelle (**CVE-2021-45105**) wird entdeckt. Patch 2.17.0 erscheint. |
  | **28\. Dez 2021** | Vierte Lücke | Eine weitere Schwachstelle (**CVE-2021-44832**) führt zur Version 2.17.1. |
  | **Januar 2022** | Entspannung | Die meisten großen Dienste sind gepatcht; das BSI senkt die Warnstufe. |
  
2. **Diskussion:** Warum sind Supply-Chain-Angriffe so gefährlich und schwer zu erkennen? Brainstormt Gründe.  
  Angriffe bzw. Kompromittierungen bleiben zunächst verborgen, da man nicht das direkte bzw. erste Ziel ist und man auf Basis eines Vertrauensverhältnisses diesen Angriff ermöglicht. Man erkennt die potenzielle Gefahr erst dann, wenn es zu spät ist; sofern man sie überhaupt entdeckt. In der Theorie kann die Gefahr bereits seit langem bestehen, sie wurde bloß noch nicht ausgenutzt.  
  Der Umweg des Angriffs erschwert natürlich auch das Verfolgen und Beheben.
3. **SBOM in der Praxis:** Stellt euch vor, ihr nutzt eine Webanwendung, die aus 20 verschiedenen Open-Source-Komponenten besteht. Eine Warnung über eine kritische Lücke in Komponente "X" wird veröffentlicht. Beschreibt, wie euch ein vorhandener SBOM bei der Reaktion auf diesen Vorfall helfen würde.  
  Wenn eine SBOM-Liste geführt wird, kann einfach in ihr nach der kompromittierten Software gesucht werden und ein möglicher Vorfall entdeckt werden.

# Quellen und Vertiefung

- **Online-Ressource:** [BSI - Cyber-Sicherheitslagebild zur Software-Lieferkette (2022)](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Lageberichte/Lagebild_Software_Lieferkette.pdf%3F__blob%3DpublicationFile)
- **Online-Ressource:** [Heise.de - Dossier zur Log4Shell-Sicherheitslücke](https://www.google.com/search?q=https://www.heise.de/thema/Log4Shell)