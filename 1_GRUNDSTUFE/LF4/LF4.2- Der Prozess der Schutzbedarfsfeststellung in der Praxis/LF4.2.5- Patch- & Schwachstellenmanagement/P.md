# Philipp

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

1. **CVE-Recherche:** Recherchiert die CVE-Datenbank (z.B. bei MITRE oder NIST). Sucht nach einer kürzlich veröffentlichten, kritischen Schwachstelle für eine bekannte Software (z.B. Windows, Chrome oder ein Adobe-Produkt). Fasst zusammen, was die Lücke ermöglicht und wie hoch ihr Schweregrad (CVSS-Score) ist. → https://www.cvedetails.com/cve/CVE-2025-24893/
  - Hier konnte auf **xwiki** über eine Anfrage an “**SolrSearch**” jeglicher Code ausgeführt/injected werden.
  - Alle drei Schutzziele **CIA** (Confidentiality, Integrity, Availablity) sind betroffen
  - **CVSS Base Score: 9.8**
2. **Prozess-Visualisierung:** Erstellt eine einfache Grafik oder ein Flussdiagramm, das die fünf Phasen des Patch-Management-Prozesses darstellt. → [**8 SCHRITTE**](https://www.rapid7.com/de/cybersecurity-grundlagen/patch-management/)![diagram.drawio.svg](files/019cee46-ad4d-74db-b803-2d45872f7dbf/diagram.drawio.svg)
3. **Szenario-Diskussion:** Die "KreativKopf GmbH" hat Windows-PCs, macOS-Laptops, Android- und iOS-Smartphones sowie Linux-Server in der Cloud. Diskutiert die unterschiedlichen Herausforderungen beim Patch-Management für diese vier Systemwelten.
  - Die Vielzahl an Betriebssystemen erschwert den Überblick über Updates. Sowie Betriebssysteme selber und auf ihnen laufende Software.Von Olena übernommen:
    
    | System / Plattform | Herausforderungen beim Patch-Management |
    | --- | --- |
    | **Windows-PCs** | Viele Versionen, regelmäßige Sicherheits- und Funktionsupdates, Gefahr von verpassten Updates bei Offline-Geräten. |
    | **macOS-Laptops** | Updates oft manuell nötig, weniger zentrale Tools als bei Windows, Geräte können außerhalb Unternehmensnetz arbeiten. |
    | **Android-Smartphones** | Unterschiedliche Hersteller und Versionen → Patches kommen ungleichmäßig, BYOD\*\*\*-Probleme (eigene Geräte von Mitarbeitern). |
    | **iOS-Smartphones** | Updates zentral über Apple, aber BYOD-Policy nötig, Kontrolle über Installation eingeschränkt. |
    | **Linux-Server (Cloud)** | Unterschiedliche Distributionen (Ubuntu, CentOS, etc.), automatisierte Updates möglich, aber Risiko von Downtime bei Produktionsservern, Testing nötig. |
    
4. **Argumentation:** Bereitet eine kurze Argumentation (3-4 Sätze) für die Geschäftsführung der "KreativKopf GmbH" vor, die erklärt, warum das Testen von Patches vor dem Ausrollen trotz des Zeitverlusts absolut notwendig ist.Das Testen ist essenziell, um unvorhergesehene Probleme möglichst zu vermeiden. Ohne einen Test gibt es keinerlei Garantie, dass sämtliche Systeme weiterhin funktionieren (Verfügbarkeit). Außerdem ist nicht jeder Patch ein “Upgrade” (Funktionsverlust, Bloatware).

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.5 "Der Weg zum Sicherheitskonzept", Abschnitt "Sicherheitsmaßnahmen umsetzen" (implizit, S. 1004 ff.).
- **Online-Ressource:** [BSI - Baustein ORP.4 Patch- und Änderungsmanagement](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Grundschutz/DE/IT-GS-Kompendium/bausteine/ORP/ORP_4_Patch_und_Aenderungsmanagement.html)
- **Datenbank:** [CVE Details](https://www.cvedetails.com/)