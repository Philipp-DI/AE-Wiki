# Mohammed

Als IT-Administrator möchte ich einen systematischen Prozess für das Patch-Management verstehen, damit ich die IT-Systeme des Unternehmens (mobil, desktop, server) zeitnah gegen bekannte Schwachstellen absichern kann.

# Celebration Criteria

- Wir können den Lebenszyklus einer Sicherheitslücke von der Entdeckung über die CVE-Nummer bis zum Patch erklären.
- Wir können die Wichtigkeit eines etablierten und schnellen Patch-Management-Prozesses für die IT-Sicherheit begründen.
- Wir können den Unterschied zwischen einem sicherheitskritischen Patch und einem reinen Funktionsupdate erläutern.
- Wir können anhand eines realen Beispiels (z.B. WannaCry/EternalBlue) die katastrophalen Folgen fehlender Updates erläutern.

# Wissens-Briefing

Eine der häufigsten Ursachen für erfolgreiche Cyberangriffe sind **nicht gepatchte Schwachstellen** in Software und Betriebssystemen. Patch-Management ist daher keine lästige Pflicht, sondern ein fundamentaler Sicherheitsprozess.

- **Schwachstelle (Vulnerability):** Ein Fehler in einer Software, der von einem Angreifer ausgenutzt werden kann.
- **CVE (Common Vulnerabilities and Exposures):** Sobald eine Schwachstelle bekannt und bestätigt ist, erhält sie eine eindeutige CVE-Nummer (z.B. `CVE-2017-0144` für die "EternalBlue"-Lücke), was die weltweite Kommunikation darüber erleichtert.
- **Patch:** Ein vom Hersteller bereitgestelltes Software-Update, das eine oder mehrere Sicherheitslücken schließt.
- **Zero-Day-Lücke:** Eine Schwachstelle, die Angreifern bereits bekannt ist und aktiv ausgenutzt wird, für die es aber vom Hersteller noch keinen Patch gibt. Hier zählt jede Sekunde.

Ein **Patch-Management-Prozess** sorgt dafür, dass Patches kontrolliert und zeitnah ausgerollt werden:

1. **Identifizieren:** Überwachen, welche neuen Patches für die im Unternehmen eingesetzte Software verfügbar sind.
2. **Bewerten:** Wie kritisch ist der Patch? Muss er sofort oder beim nächsten regulären Wartungsfenster installiert werden?
3. **Testen:** Wird der Patch in einer Testumgebung eingespielt, um sicherzustellen, dass er keine anderen wichtigen Programme stört.
4. **Ausrollen (Deployment):** Der Patch wird auf den produktiven Systemen installiert.
5. **Verifizieren:** Es wird überprüft, ob die Installation erfolgreich war und die Lücke geschlossen ist.

**Beispiel WannaCry (2017):** Diese Ransomware nutzte die "EternalBlue"-Schwachstelle in Windows aus. Microsoft hatte bereits zwei Monate zuvor einen Patch veröffentlicht. Hunderttausende Systeme weltweit, die nicht gepatcht waren, wurden innerhalb kürzester Zeit infiziert.

# Aufgaben

1. **CVE-Recherche:** Recherchiert die CVE-Datenbank (z.B. bei MITRE oder NIST). Sucht nach einer kürzlich veröffentlichten, kritischen Schwachstelle für eine bekannte Software (z.B. Windows, Chrome oder ein Adobe-Produkt). Fasst zusammen, was die Lücke ermöglicht und wie hoch ihr Schweregrad (CVSS-Score) ist

**_Eine kürzlich veröffentlichte, kritische Schwachstelle:_**

- **Schwachstelle:** CVE‑2025‑10200 – betroffen: **Google Chrome** (Desktop-Versionen vor 140.0.7339.127)
- **Beschreibung:** Ein _Use-After-Free_\-Fehler (CWE-416) im „ServiceWorker“-Modul erlaubt einem entfernten Angreifer über eine speziell gefertigte HTML-Seite, Heap-Korruption zu verursachen. Damit könnten Codeausführung, Datenmanipulation oder Systemübernahme möglich sein.
- **Schweregrad:** Der Base-CVSS v3.1 Score ist **8,8 (High)** nach Analysequelle.
- **Hinweis:** Auch wenn als „High“ klassifiziert, wird im Herstellerkontext als „Critical“ geführt.

**2\. Prozess-Visualisierung:** Erstellt eine einfache Grafik oder ein Flussdiagramm, das die fünf Phasen des Patch-Management-Prozesses darstellt.

**_Die fünf Phasen des Patch-Managements_**

https://www.canva.com/design/DAG3okUU3B4/OyUaNy0y537AjE7qLo2alA/edit?utm_content=DAG3okUU3B4&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton

![](files/019cee46-abc0-7400-82d8-682ca0786c74/image.png)

3. **Szenario-Diskussion:** Die "KreativKopf GmbH" hat Windows-PCs, macOS-Laptops, Android- und iOS-Smartphones sowie Linux-Server in der Cloud. Diskutiert die unterschiedlichen Herausforderungen beim Patch-Management für diese vier Systemwelten.

**_Die unterschiedlichen Herausforderungen im Patch-Management :_**

- **Windows-PCs**: Große Vielfalt an Hardware & Software, oft viele Drittanbieter-Programme. Patches (z. B. Microsoft Patch Tuesday) regelmäßig verfügbar, aber große Infrastruktur kann Deployment verzögern. Kompatibilität mit Legacy-Anwendungen kann Probleme machen.
- **macOS-Laptops**: Weniger Fragmentierung im Betriebssystem-Ökosystem, aber ggf. spezielle Mac-Apps oder Firmensoftware mit Einschränkungen. Verwaltung über MDM oder JAMF erforderlich; Nutzerakzeptanz (z. B. Neustarts) kann Hemmnis sein.
- **Android-Smartphones & iOS-Smartphones**: Mobile Geräte haben eigenen Update-Rhythmus; iOS ist tendenziell homogener, Android stark fragmentiert (Hersteller, Versionen). Nutzer-Interaktion nötig (Installieren, Neustart) und Geräte außerhalb des Firmennetzes schwerer zu kontrollieren.
- **Linux-Server in der Cloud**: Hier gilt Patchen mit hoher Priorität (oft kritische Dienste). Herausforderungen sind jedoch: Hochverfügbarkeit (Downtime vermeiden), Abhängigkeiten (Container, Bibliotheken), unterschiedliche Distributionen. Zudem Cloud-Umgebung kann Rollout über mehrere Regionen/Instanzen erforderlich machen.

3. **Argumentation:** Bereitet eine kurze Argumentation (3-4 Sätze) für die Geschäftsführung der "KreativKopf GmbH" vor, die erklärt, warum das Testen von Patches vor dem Ausrollen trotz des Zeitverlusts absolut notwendig ist.

**_Das Testen von Patches vor dem Rollout kostet zwar Zeit und Ressourcen, ist aber unverzichtbar: Ungeprüfte Updates können Systemausfälle, Kompatibilitätsprobleme oder neue Sicherheitslücken verursachen. Ein strukturierter Testlauf schützt langfristig die Stabilität und Sicherheit unserer IT_**_._

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.5 "Der Weg zum Sicherheitskonzept", Abschnitt "Sicherheitsmaßnahmen umsetzen" (implizit, S. 1004 ff.).
- **Online-Ressource:** [BSI - Baustein ORP.4 Patch- und Änderungsmanagement](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Grundschutz/DE/IT-GS-Kompendium/bausteine/ORP/ORP_4_Patch_und_Aenderungsmanagement.html)
- **Datenbank:** [CVE Details](https://www.cvedetails.com/)